# Tvořím Web od A do Z: Podklady pro 11. lekci

## Sémantické značky

Sám sice přesně nevím, co _[sémantika](https://cs.wikipedia.org/wiki/S%C3%A9mantika)_ je, jsem přeci jen vyučený číšník a neúspěšný herec :) , ale snažím se používat značky s významem. Při psaní strukury HTML dokumentu se ptám, co je to za část stránky, co představuje? Bude to běžný text, poznámka pod čarou, seznam, článek, navigace atd.? A podle toho volím značku. Pouze tehdy, kdy se žádná nehodí, použiju neutrální `div` (blokový), nebo `span` (řádkový). Naopak, pokud potřebuji do HTML přidat prvek, abych mohl dosáhnout kýženého stylu, například potřebuji vytvořit flexboxový kontejner, přidám `div`.

Pro začátek se držte doporučení z [Marksheet.io](https://marksheet.io) (mimochodem výborný zdroj pro začátky s HTML/CSS: stručný a přehledný a v angličtině):

> Máte na výběr asi stovku HTML elementů. To je _dost_. Dá to fušku procházet celý jejich seznam, abyste vybraly tu správnou značku. Takže si to nekomplikujte a nemarněte čas výběrem vhodné značky pro ten který kousek stránky. Pro začátek po stačí, když si osvojíte tyto značky (a postupně se seznámíte s dalšími):

<table>
    <tbody>
        <tr>
            <th>Structure</th>
            <th>Text</th>
            <th>Inline</th>
        </tr>
        <tr>
            <td>
                <code>header</code><br>
                <code>h1</code><br>
                <code>h2</code><br>
                <code>h3</code><br>
                <code>nav</code><br>
                <code>footer</code><br>
                <code>article</code><br>
                <code>section</code>
            </td>
            <td>
                <code>p</code><br>
                <code>ul</code><br>
                <code>ol</code><br>
                <code>li</code><br>
                <code>blockquote</code>
            </td>
            <td>
                <code>a</code><br>
                <code>strong</code><br>
                <code>em</code><br>
                <code>q</code><br>
                <code>abbr</code><br>
                <code>small</code>
            </td>
        </tr>
    </tbody>
  </table>

- [Sémantika v HTML](https://marksheet.io/html-semantics.html)
- [Sémantika řádkových prvků](https://marksheet.io/html-inline-semantics.html)

## HTML entity

Všechny myšlené znaky (písmena, číslice, klikyháky, emotikony) se dají v HTML vyjádřit kódem, tzv. entitou. Například `š` lze zapsat jako `&scaron;`. S tím, že HTML entita vždy začíná `&` a končí `;`. Mezi nimi je buď pojmenovaná entita, jako v příkladě výše, nebo číselný kód. Pozor, na velikosti písmen záleží (`&scaron;` = š, `&Scaron;` = Š).

Dnes, když je kódování UTF-8 plně rozšířeno, ztrácejí entity na významu. Většinu písmen a symbolů stačí zapsat prostým znakem. Z entit nám pak zůstává nejčastěji nezalomitelná (pevná mezera) `&nbsp;` (Non-Breaking SPace). Tu bychom například v českých textech měli používat vždy za jednopísmennými předložkami: <q>v&nbsp;řece</q>. Nebo mezi číslem a jednotkou: <q>80&nbsp;kg</q>.

**Pozor, entitou vždy zapisujeme, tzv. escapujeme řídicí znaky (které mají v&nbsp;HTML zvláštní význam):**

- `&gt;` = `>`
- `&lt;` = `<`
- `&amp;` = `&`

**Entitu musíme například použít, když chceme vypsat &lt; ve smyslu _větší než_. Nepoužití entity mate prohlížeč, který vidí začátek otevírací značky.**

Nově se entity vracejí na scénu v podobě populárních emoji, např. `&#128567;` = 😷

- [Přehled HTML entit](https://www.w3schools.com/html/html_entities.asp)
- [Jiný přehled týchž HTML entit](https://www.toptal.com/designers/htmlarrows/symbols/)
