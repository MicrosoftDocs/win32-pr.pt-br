---
description: Os aplicativos podem usar Unicode para representar cadeias de caracteres em vários formulários.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Usando a normalização Unicode para representar cadeias de caracteres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837416"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Usando a normalização Unicode para representar cadeias de caracteres

Os aplicativos podem usar Unicode para representar cadeias de caracteres em vários formulários. À medida que a aceitação Unicode cresceu, especialmente pela Internet, a necessidade foi surgida para eliminar diferenças não essenciais em cadeias de caracteres Unicode. Várias representações para uma combinação de caracteres complicam o software, por exemplo, quando um servidor Web responde a uma solicitação de página ou um vinculador procura um identificador específico em uma biblioteca.

> [!Caution]  
> Diferentes cadeias de caracteres Unicode podem parecer visualmente idênticas, gerando preocupações de segurança. Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).

 

Em resposta a esse requisito, o consórcio Unicode definiu um processo chamado "normalização", que produz uma representação binária para qualquer uma das representações binárias equivalentes de um caractere. Depois de normalizado, duas cadeias de caracteres serão equivalentes se e somente se tiverem representações binárias idênticas. A normalização elimina algumas diferenças, mas preserva maiúsculas e minúsculas.

Para usar a normalização Unicode, um aplicativo pode chamar as funções [**normalizestring**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) e [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) para reorganização das cadeias de caracteres ACCCORDING para Unicode 4,0 TR \# 15. A normalização pode ajudar a melhorar a segurança, reduzindo representações de cadeias de caracteres alternativas que têm o mesmo significado linguístico. Lembre-se, no entanto, que a normalização não pode eliminar totalmente as representações alternativas.

Para obter uma descrição detalhada dos padrões Unicode para normalização, consulte [Unicode padrão do anexo \# 15: formulários de normalização Unicode](https://www.unicode.org/reports/tr15) (UAX \# 15).

> [!Caution]  
> Como a normalização pode alterar a forma de uma cadeia de caracteres, mecanismos de segurança ou algoritmos de validação de caracteres normalmente devem ser implementados após a normalização. Para obter mais informações, consulte [Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Fornecer várias representações da mesma cadeia de caracteres

Em muitos casos, o Unicode permite várias representações do que é, lingüísticamente, a mesma cadeia de caracteres. Por exemplo:

-   A maiúscula A com trema (trem) pode ser representada como um único ponto de código Unicode "Ä" (U + 00C4) ou a combinação de maiúscula A e combinação de caracteres de trema ("A" + "̈", ou seja, U + 0041 U + 0308). As considerações semelhantes se aplicam a muitos outros caracteres com marcas de sinais diacríticos.
-   A própria capital pode ser representada da maneira usual (letra latina maiúscula A, U + 0041) ou por letra minúscula latina maiúscula A (U + FF21). As considerações semelhantes se aplicam às outras letras latinas simples (maiúsculas e minúsculas) e aos caracteres Katakana usados na escrita de japonês.
-   A cadeia de caracteres "fi" pode ser representada pelos caracteres "f" e "i" (U + 0066 U + 0069) ou pela ligadura "fi" (U + FB01). Considerações semelhantes se aplicam a muitas outras combinações de caracteres para os quais o Unicode define ligaturas.

## <a name="use-the-four-defined-normalization-forms"></a>Usar os quatro formulários de normalização definidos

Seus aplicativos podem executar a normalização Unicode usando vários algoritmos, chamados de "formas de normalização", que obedecem a diferentes regras. O consórcio Unicode definiu quatro formas de normalização: NFC (forma C), NFD (forma D), NFKC (Form KC) e NFKD (Form KD). Cada formulário elimina algumas diferenças, mas preserva maiúsculas e minúsculas. O Win32 e o .NET Framework dão suporte a todos os quatro formulários de normalização.

O [**\_ formulário**](/windows/desktop/api/Winnls/ne-winnls-norm_form) normal de tipo de enumeração NLS dá suporte aos quatro formulários de normalização Unicode padrão. Os formulários C e D fornecem formulários canônicos para cadeias de caracteres. As formas não canônicas KC e KD fornecem compatibilidade adicional e podem revelar determinadas equivalências semânticas que não são aparentes nos formulários C e D. No entanto, eles fazem isso às custas de uma certa perda de informações e geralmente não devem ser usados como uma forma canônica de armazenar cadeias de caracteres.

Das duas formas canônicas, o formulário C é um formulário "composto" e o formulário D é um formulário "decomposto". Por exemplo, o formulário C usa o único ponto de código Unicode "Ä" (U + 00C4), enquanto o formato D usa ("A" + "̈", que é U + 0041 U + 0308). Elas são processadas de forma idêntica, pois "̈" (U + 0308) é um caractere de combinação. O formulário D pode usar qualquer número de pontos de código para representar um único ponto de código usado pelo formulário C.

Se duas cadeias de caracteres forem idênticas nas formas C ou D, elas serão idênticas no outro formulário. Além disso, quando renderizado corretamente, eles são exibidos de forma indistinguíveis uns dos outros e da cadeia de caracteres não normalizada original.

Depois de normalizadas, as cadeias de caracteres não podem ser retornadas consistentemente para sua representação original. Por exemplo, se uma cadeia de caracteres com uma mistura de representações de caracteres compostas e decompostas for convertida em uma forma normalizada, não haverá nenhuma maneira de desnormalizar a cadeia de caracteres mista original. Portanto, se um aplicativo exigir a representação original da cadeia de caracteres, ele deverá armazenar essa representação explicitamente. No entanto, a conversão entre os dois formulários canônicos é reversível. Uma cadeia de caracteres no formato C pode ser convertida para o formulário D e, em seguida, de volta para o formulário C, e o resultado é idêntico ao formato original da cadeia C.

Os formulários KC e KD são semelhantes aos formulários C e D, respectivamente, mas essas "formas de compatibilidade" têm mapeamentos adicionais de caracteres compatíveis para a forma básica de cada caractere. Esses mapeamentos podem causar a perda de variações de caracteres secundárias. Eles combinam determinados caracteres que são visualmente distintos. Por exemplo, eles combinam caracteres de largura inteira e de meia largura com o mesmo significado semântico, ou formas diferentes da mesma letra árabe, ou a Ligadura "fi" (U + FB01) e o par de caracteres "fi" (U + 0066 U + 0069). Eles também combinam alguns caracteres que às vezes podem ter um significado semântico diferente, como um dígito escrito como um sobrescrito, como subscrito ou colocado em um círculo. Devido a essa perda de informações, os formulários KC e KD geralmente não devem ser usados como formas canônicas de cadeias de caracteres, mas são úteis para determinados aplicativos.

O formulário KC é um formulário composto e o formulário KD é um formulário decomposto. O aplicativo pode voltar entre os formulários KC e KD, mas não há uma maneira consistente de ir de forma KC ou KD de volta para a cadeia de caracteres original, mesmo que a cadeia de caracteres original esteja no formato C ou D.

O Windows, os aplicativos da Microsoft e o .NET Framework geralmente geram caracteres na forma C usando métodos de entrada normais. Para a maioria dos fins no Windows, o formulário C é o formulário preferido. Por exemplo, os caracteres no formato C são produzidos pela entrada de teclado do Windows. No entanto, os caracteres importados da Web e de outras plataformas podem introduzir outros formulários de normalização no fluxo de dados.

Os exemplos a seguir são desenhados a partir de UAX \# 15 e ilustram as diferenças entre os quatro formulários de normalização.



<table>
<thead>
<tr class="header">
<th>Original</th>
<th>Formulário D</th>
<th>Formulário C</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">O ffi_ligature (U + FB03) não é decomposto, pois tem um mapeamento de compatibilidade, não um mapeamento canônico. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä \ uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">O NUMERAL Romano IV (U + 2163) não é decomposto. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + dez</td>
<td>ga</td>
<td rowspan="5">Diferentes equivalentes de compatibilidade de um único caractere japonês não resultam na mesma cadeia de caracteres no formato C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + dez</td>
<td>Ka + dez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka + dez</td>
<td>hw_ka + dez</td>
<td>hw_ka + dez</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>kaks</td>
<td>As sílabas Hangul são mantidas sob normalização.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Original</th>
<th>Formulário KD</th>
<th>Formulário KC</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">O ffi_ligature (U + FB03) é decomposto no formato KC, mas não no formato C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">As cadeias de caracteres resultantes aqui são idênticas no formato KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + dez</td>
<td>ga</td>
<td rowspan="5">Diferentes equivalentes de compatibilidade de um único caractere japonês resultam na mesma cadeia de caracteres no formato KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + dez</td>
<td>Ka + dez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>Ka + dez</td>
<td>ga</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + dez</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + dez</td>
<td>Ka + dez</td>
<td>ga</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>kaks</td>
<td>As sílabas Hangul são mantidas sob normalização. Em versões anteriores do Unicode, caracteres Jamo como KS <sub>f</sub> tinham mapeamentos de compatibilidade para k <sub>f</sub> + s <sub>f</sub>. Esses mapeamentos foram removidos em 2.1.9 Unicode para garantir que as sílabas Hangul sejam mantidas.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> As duas tabelas acima têm direitos autorais de © 1998-2006 Unicode, Inc. Todos os direitos reservados.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Usar formulários compostos para glifos únicos

Muitas sequências de caracteres que correspondem a um único glifo não têm formulários compostos. Mesmo quando normalizado pela forma C, um único glifo Visual ou elemento de texto lógico pode ser composto por vários pontos de código Unicode. Por exemplo, vários caracteres usados na escrita de lituano têm diacríticos duplos, pois têm apenas formulários decompostos. Um exemplo é minúscula U com Macron e til ("ū̃", U + 016B U + 0303, em que o primeiro ponto de código é um U minúsculo com Macron e o segundo é um acento agudo combinável).

## <a name="example"></a>Exemplo

Um exemplo relevante pode ser encontrado em [NLS: exemplo de normalização Unicode](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o suporte ao idioma nacional](using-national-language-support.md)
</dt> <dt>

[Considerações sobre segurança: recursos internacionais](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**Normalizestring**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




