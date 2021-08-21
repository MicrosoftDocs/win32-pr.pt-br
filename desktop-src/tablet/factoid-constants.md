---
description: Define valores de cadeia de caracteres constantes usados para aumentar a precisão do reconhecimento fornecendo informações contextuais ao reconhecedor.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Constantes factoid (Msinkaut.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 239818f4306e1a774c1384a89a25b0785cad03d840a292b61d4f30f2473945c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045384"
---
# <a name="factoid-constants"></a>Constantes factoid

Define valores de cadeia de caracteres constantes usados para aumentar a precisão do reconhecimento fornecendo informações contextuais ao reconhecedor.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nome</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <dt><strong>FACTOID_NONE</strong></dt> </dl></td>
<td style="text-align: left;">Desabilita todos os outros factoids e dicionários.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <dt><strong>FACTOID_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">A configuração Padrão para factoids para idiomas do oeste inclui o dicionário do sistema, o dicionário de usuário, várias pontuações e o factoid Web e Number. A configuração Padrão para factoids para idiomas do Leste da Ásia inclui todos os caracteres com suporte pelo reconhecedor. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor usar apenas o dicionário do sistema.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <dt><strong>FACTOID_WORDLIST</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor usar uma lista de palavras definida programaticamente. A lista de palavras é definida pela propriedade <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>WordList</strong></a> de um <a href="inkrecognizercontext-class.md"><strong>objeto InkRecognizerContext.</strong></a> <br/>
<blockquote>
[!Note]<br />
Se uma cadeia de caracteres for adicionada a uma lista de palavras, suas versões em maiúsculas também serão adicionadas implicitamente. Por exemplo, adicionar &quot; hello &quot; adiciona implicitamente Hello e &quot; HELLO &quot; &quot; &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <dt><strong>FACTOID_EMAIL</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um endereço de email.<br/>
<blockquote>
[!Note]<br />
Um endereço de email totalmente qualificado, como &quot; someone@example.com &quot; , deve ser usado para esse factoid. Um alias de alias de alias, como &quot; alguém , não é &quot; reconhecido.
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <dt><strong>FACTOID_WEB</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um endereço Web.<br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <dt><strong>FACTOID_ONECHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um único caractere.<br/>
<blockquote>
[!Note]<br />
Esse factoid procura qualquer caractere ANSI isolado.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <dt><strong>FACTOID_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um número.<br/>
<blockquote>
[!Note]<br />
Os valores numéricos incluem separadores, decimais, ordinais e outros símbolos numéricos comumente usados.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <dt><strong>FACTOID_DIGIT</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um único dígito, de 0 a 9.<br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </dl></td>
<td style="text-align: left;">Fornece um contexto numérico simples para um reconhecedor.<br/>
<blockquote>
[!Note]<br />
Não há suporte para esse factoid nesta versão do SDK do Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <dt><strong>FACTOID_CURRENCY</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres que denotam um valor de moeda.<br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <dt><strong>FACTOID_POSTALCODE</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar códigos postais.<br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <dt><strong>FACTOID_PERCENT</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar por percentuais.<br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <dt><strong>FACTOID_DATE</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres que denotam uma data.<br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <dt><strong>FACTOID_TIME</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres que denotam uma hora.<br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <dt><strong>FACTOID_TELEPHONE</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres que denotam um número de telefone.<br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <dt><strong>FACTOID_FILENAME</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres que denotam um nome de arquivo.<br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <dt><strong>FACTOID_UPPERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um único caractere em letras maiúsculas: A a Z.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <dt><strong>FACTOID_LOWERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar um único caractere minúsculo: A a Z.<br/>
<blockquote>
[!Note]<br />
Não há suporte para esse factoid nesta versão do SDK do Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <dt><strong>FACTOID_PUNCCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres de pontuação.<br/>
<blockquote>
[!Note]<br />
Não há suporte para esse factoid nesta versão do SDK do Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres Kanji, Katakana e Hiragana comumente usados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres chinês simplificados comumente usados.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres chineses tradicionais comumente usados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <dt><strong>FACTOID_KOREANCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres coreanos comumente usados.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <dt><strong>FACTOID_HIRAGANA</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar apenas caracteres Hiragana.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <dt><strong>FACTOID_KATAKANA</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar apenas caracteres Katakana.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <dt><strong>FACTOID_KANJICOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres kanji comumente usados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <dt><strong>FACTOID_KANJIRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres Kanji raramente usados.<br/>
<blockquote>
[!Note]<br />
Não há suporte para esse factoid nesta versão do SDK do Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <dt><strong>FACTOID_BOPOMOFO</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres Bopomofo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <dt><strong>FACTOID_JAMO</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres Jamo de compatibilidade do Hangul.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <dt><strong>FACTOID_HANGULCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres Hangul comumente usados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <dt><strong>FACTOID_HANGULRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indica para um reconhecedor procurar caracteres Hangul raramente usados.<br/>
<blockquote>
[!Note]<br />
Não há suporte para esse factoid nesta versão do SDK do Tablet PC.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Comentários

No C++, você pode acessar essas constantes no arquivo de header Msinkaut.h, que está localizado no diretório : Arquivos de Programas Microsoft Tablet PC Platform SDK Include se você instalou o <systemdrive> SDK no local \\ \\ \\ padrão.

> [!Note]  
> Essas constantes são WCHARs, não BSTRs. Eles devem ser convertidos em BSTRs antes de usar como parâmetros para métodos de objeto. Para obter mais informações sobre o tipo de dados BSTR, consulte [Usando a biblioteca COM](using-the-com-library.md).

 

> [!Note]  
> Para reconhecedores de script latino, os factoids definidos nesta classe são fornecidos apenas para compatibilidade com backward. Para novos desenvolvimentos, você é incentivado a usar os valores definidos na [função SetInputScope.](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) Para obter detalhes, consulte [Usando o contexto para melhorar a precisão.](using-context-to-improve-accuracy.md)

 

Use esses identificadores para especificar qual factoid deve ser usado durante o reconhecimento.

As combinações de factoids a seguir têm suporte apenas para idiomas do oeste. Eles não têm definições separadas, mas são entradas literais de cadeia de caracteres aceitáveis para a propriedade [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) de objetos que usam factoids. Essas constantes de cadeia de caracteres factoid permitem que a entrada corresponder a qualquer um dos factoids na expressão.



| Combinação               | Definição                                                |
|---------------------------|-----------------------------------------------------------|
| "WEB \| WORDLIST"           | O factoid da Web ou a lista de palavras.                         |
| "EMAIL \| WORDLIST"         | O facto de email ou a lista de palavras.                       |
| " \| listas de palavras da Web de nome de arquivo \| " | O nome do arquivo ou o factor da Web ou a lista de palavras. |



 

Se você estiver usando o controle [InkEdit](inkedit-control-reference.md) , o factor poderá ser definido como uma propriedade do controle.

Se você estiver usando as APIs de plataforma do Tablet PC, poderá definir a propriedade [**factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) em um objeto [**InkRecognizerContext**](inkrecognizercontext-class.md) .

Como alternativa, você pode definir essa propriedade com a constante de cadeia de caracteres de factor real.

> [!Note]  
> Constantes de cadeia de caracteres de facto diferencia maiúsculas de minúsculas. Para obter mais informações sobre os factos e como usá-los, consulte usando o contexto para [melhorar a precisão](using-context-to-improve-accuracy.md). Para determinar se um factor está disponível em um idioma específico, consulte as [edições com suporte na versão 1](supported-factoids-from-version-1.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do XP Tablet PC Edition\]<br/>                                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Msinkaut. h (também requer Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Classe InkRecognizeContext de Propriedade do factor \[\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Classe PenInputPanel de Propriedade do factor \[\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Controle de Propriedade InkEdit do factor \[\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Usando o contexto para melhorar a precisão](using-context-to-improve-accuracy.md)
</dt> <dt>

[Factos com suporte da versão 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

