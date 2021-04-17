---
description: As propriedades de resumo para pacotes de instalação, transformações e patches são descritos nas tabelas a seguir.
ms.assetid: b44b24b7-7fc4-4c3c-9d10-7e2f3c43cf36
title: Descrições de propriedades de resumo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41addb58571b6d18e1cccc4a34c3026f3d0544cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105782324"
---
# <a name="summary-property-descriptions"></a>Descrições de propriedades de resumo

As propriedades de resumo para pacotes de instalação, transformações e patches são descritos nas tabelas a seguir. Observe que o significado de uma determinada propriedade de resumo pode ser diferente dependendo se o banco de dados pertence a um pacote de instalação, transformação ou pacote de patch. Para obter mais informações sobre as IDs de propriedade, PIDs e tipos, consulte [Summary Information Stream Property Set](summary-information-stream-property-set.md).

## <a name="installation-packages"></a>Pacotes de instalação



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade Summary</th>
<th>Significado dessa propriedade em um banco de dados de instalação</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Título</strong></a></td>
<td>Uma descrição desse arquivo como um pacote de instalação. A descrição deve incluir o &quot; <a href="about-the-installer-database.md">banco de dados de instalação</a>de frase.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Assunto</strong></a></td>
<td>O nome do produto instalado por este pacote. Deve ser o mesmo nome que na propriedade <a href="productname.md"><strong>ProductName</strong></a> .</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>O nome do fabricante deste produto. Deve ser o mesmo nome da Propriedade do <a href="manufacturer.md"><strong>fabricante</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Palavras-chave</strong></a></td>
<td>Uma lista de palavras-chave que podem ser usadas por navegadores de arquivos para realizar pesquisas de palavra-chaves em um arquivo. As palavras-chave devem incluir o &quot; instalador &quot; , bem como palavras-chave específicas do produto.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Comentários</strong></a></td>
<td>Contém a frase: &quot; este banco de dados do instalador contém a lógica e os requisitos necessários para instalar <<em>nome do produto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modelo</strong></a> (obrigatório)</td>
<td>A plataforma e as linguagens compatíveis com este pacote de instalação. Consulte <a href="template-summary.md"><strong>modelo</strong></a> para obter a sintaxe.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Salvo pela última vez por</strong></a></td>
<td>Os desenvolvedores de ferramentas de edição de banco de dados podem usar essa propriedade durante o processo de desenvolvimento para acompanhar a última pessoa para modificar o banco de dados de instalação. Essa propriedade deve ser definida como NULL em um banco de dados de envio final. O instalador define essa propriedade como o valor da propriedade <a href="logonuser.md"><strong>LogonUser</strong></a> durante uma <a href="administrative-installation.md"><strong>instalação administrativa</strong></a>. O instalador nunca usa essa propriedade e um usuário nunca precisa modificá-la.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Número de revisão</strong></a> (obrigatório)</td>
<td>Contém o <a href="package-codes.md">código do pacote</a> do instalador.</td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Última Impressão</strong></a></td>
<td>Pode ser definido como a data e a hora durante uma <a href="administrative-installation.md">instalação administrativa</a> para registro quando a imagem administrativa foi criada.</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Criar data/hora</strong></a></td>
<td>A data e a hora em que este banco de dados do instalador foi criado.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Hora da última gravação/data</strong></a></td>
<td>A data e a hora atuais do sistema no momento em que o banco de dados do instalador foi salvo pela última vez. Inicialmente nulo.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Contagem de páginas</strong></a> (obrigatória)</td>
<td>Contém um valor usado para identificar a versão mínima do instalador exigida por este pacote de instalação. Por exemplo, se o pacote exigir, no mínimo, a versão 2,0 do instalador, essa propriedade deverá ser definida como um inteiro de 200.
<blockquote>
[!Note]<br />
O valor dessa propriedade deve ser 200 ou maior com <a href="64-bit-windows-installer-packages.md">pacotes de Windows Installer de 64 bits</a>.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Contagem de palavras</strong></a> (obrigatória)</td>
<td>O tipo da imagem do arquivo de origem. Armazenado no lugar da propriedade Count padrão. Essa propriedade é um campo de bits. Consulte o tópico <a href="word-count-summary.md"><strong>contagem de palavras</strong></a> para os valores.<br/> A partir do Windows Installer versão 4,0 no Windows Vista, essa propriedade inclui bits para especificar se são necessários privilégios elevados.<br/></td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Contagem de caracteres</strong></a></td>
<td>Nulo</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Criando aplicativo</strong></a></td>
<td>Contém o nome do software usado para criar este banco de dados de instalação.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Segurança</strong></a></td>
<td>O valor dessa propriedade deve ser 2-somente leitura recomendável.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Código</strong></a></td>
<td>O valor numérico da página de código ANSI usada para exibir as informações de resumo. Essa propriedade deve ser definida antes que quaisquer propriedades de cadeia de caracteres sejam definidas nas informações de resumo.</td>
</tr>
</tbody>
</table>



 

## <a name="transforms"></a>Transformações



| Propriedade Summary                                              | Significado dessa propriedade em uma transformação                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Título**](title-summary.md)                                | Uma descrição desse arquivo como uma transformação. A descrição deve incluir a frase: "[transformar](database-transforms.md)".                                                                                                                                                                     |
| [**Assunto**](subject-summary.md)                            | O nome do produto instalado pelo pacote de instalação original. Deve ser o mesmo valor que a propriedade de [**Resumo do assunto**](subject-summary.md) no pacote de instalação original.                                                                                            |
| [**Autor**](author-summary.md)                              | O nome do fabricante desta transformação.                                                                                                                                                                                                                                                   |
| [**Palavras-chave**](keywords-summary.md)                          | Uma lista de palavras-chave que podem ser usadas por navegadores de arquivos para realizar pesquisas de palavra-chaves em um arquivo. As palavras-chave devem incluir "instalador", bem como palavras-chave específicas do produto.                                                                                                                             |
| [**Comentários**](comments-summary.md)                          | Contém a frase: "esta transformação contém a lógica e os dados necessários para instalar <*nome do produto*>".                                                                                                                                                                                     |
| [**Modelo**](template-summary.md) (obrigatório)               | As versões de plataforma e idioma compatíveis com essa transformação. Esse valor pode ser deixado em branco se não houver restrições. Apenas um idioma pode ser especificado para uma transformação. Para obter mais informações sobre a sintaxe, consulte [**Template**](template-summary.md).                                |
| [**Salvo pela última vez por**](last-saved-by-summary.md)                | A plataforma e as IDs de idioma que o banco de dados tem depois de ser transformado. A propriedade de [**Resumo do modelo**](template-summary.md) no novo banco de dados deve ser definida com os mesmos valores.                                                                                              |
| [**Número de revisão**](revision-number-summary.md) (obrigatório) | Uma lista dos GUIDs de código do produto e da versão dos produtos novos e originais e o GUID do código de atualização. A lista é separada por ponto e vírgula da seguinte maneira. *Original-produto-código original-versão do produto*; Novo produto de *código novo-produto-versão*; *Atualizar código*<br/>                       |
| [**Última Impressão**](last-printed-summary.md)                  | Nulo                                                                                                                                                                                                                                                                                              |
| [**Criar data/hora**](create-time-date-summary.md)          | A hora e a data em que a transformação foi criada.                                                                                                                                                                                                                                                 |
| [**Hora da última gravação/data**](last-saved-time-date-summary.md)  | A data e a hora atuais do sistema no momento em que a transformação foi salva. Inicialmente nulo.                                                                                                                                                                                                             |
| [**Contagem de páginas**](page-count-summary.md) (obrigatória)           | Um valor usado para indicar a versão mínima do instalador necessária para processar a transformação. O valor deve ser definido como o maior dos valores de propriedade de contagem de duas [**páginas**](page-count-summary.md) que pertencem aos bancos de dados usados para gerar a transformação.                                 |
| [**Contagem de palavras**](word-count-summary.md) (obrigatória)           | Nulo                                                                                                                                                                                                                                                                                              |
| [**Contagem de caracteres**](character-count-summary.md)            | Essa parte do fluxo de informações de resumo é dividida em palavras de 2 16 bits. A palavra superior contém [*sinalizadores de validação de transformação*](t-gly.md). A palavra inferior contém [*sinalizadores de condição de erro de transformação*](t-gly.md). |
| [**Criando aplicativo**](creating-application-summary.md)  | Contém o nome do software usado para criar essa transformação.                                                                                                                                                                                                                                  |
| [**Segurança**](security-summary.md)                          | O valor dessa propriedade deve ser de 4 impostos como somente leitura.                                                                                                                                                                                                                                      |
| [**Código**](codepage-summary.md)                          | O valor numérico da página de código ANSI usada para exibir as informações de resumo. Essa propriedade deve ser definida antes que as propriedades de cadeia de caracteres possam ser definidas nas informações de resumo.                                                                                                                    |



 

## <a name="patch-packages"></a>Pacotes de patch



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade Summary</th>
<th>Significado dessa propriedade em um pacote de patch</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="title-summary.md"><strong>Título</strong></a></td>
<td>Uma descrição desse arquivo como um pacote de patch. A descrição deve incluir a frase: &quot; <a href="patch-packages.md">patch</a>.&quot;</td>
</tr>
<tr class="even">
<td><a href="subject-summary.md"><strong>Assunto</strong></a></td>
<td>Uma descrição do patch que inclui o nome do produto.</td>
</tr>
<tr class="odd">
<td><a href="author-summary.md"><strong>Autor</strong></a></td>
<td>O nome do fabricante do pacote de patch.</td>
</tr>
<tr class="even">
<td><a href="keywords-summary.md"><strong>Palavras-chave</strong></a></td>
<td>Uma lista delimitada por ponto e vírgula de fontes do patch.</td>
</tr>
<tr class="odd">
<td><a href="comments-summary.md"><strong>Comentários</strong></a></td>
<td>Contém a frase: &quot; esse patch contém a lógica e os dados necessários para instalar <<em>nome do produto</em> > .&quot;</td>
</tr>
<tr class="even">
<td><a href="template-summary.md"><strong>Modelo</strong></a> (obrigatório)</td>
<td>Uma lista delimitada por ponto e vírgula dos códigos de produto que podem aceitar esse patch.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-by-summary.md"><strong>Salvo pela última vez por</strong></a></td>
<td>Uma lista delimitada por ponto e vírgula de nomes de subarmazenamento de transformação na ordem em que são aplicadas por esse patch.</td>
</tr>
<tr class="even">
<td><a href="revision-number-summary.md"><strong>Número de revisão</strong></a> (obrigatório)</td>
<td>Contém o código de patch GUID para o patch. Isso pode ser seguido por uma lista de GUIDs de código de patch para patches que são removidos quando esse patch é aplicado. Os códigos de patch são concatenados sem delimitadores separando GUIDs na lista.
<blockquote>
[!Note]<br />
Se o pacote de patch contiver uma tabela <a href="msipatchsequence-table.md"><strong>MsiPatchSequence</strong></a> , o patch não removerá os patches listados após o GUID do patch atual.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="last-printed-summary.md"><strong>Última Impressão</strong></a></td>
<td>Nulo</td>
</tr>
<tr class="even">
<td><a href="create-time-date-summary.md"><strong>Criar data/hora</strong></a></td>
<td>A data e a hora em que o arquivo de patch foi criado.</td>
</tr>
<tr class="odd">
<td><a href="last-saved-time-date-summary.md"><strong>Hora da última gravação/data</strong></a></td>
<td>A data e a hora atuais do sistema no momento em que o pacote de patch foi salvo. Esse valor é inicialmente nulo.</td>
</tr>
<tr class="even">
<td><a href="page-count-summary.md"><strong>Contagem de páginas</strong></a> (obrigatória)</td>
<td>Nulo</td>
</tr>
<tr class="odd">
<td><a href="word-count-summary.md"><strong>Contagem de palavras</strong></a> (obrigatória)</td>
<td>Contém um valor que indica a versão de Windows Installer mínima necessária para instalar o patch. Um patch com um valor de contagem de palavras de 4 requer Windows Installer versão 3,0 ou superior para que o patch seja aplicado. Um valor de 3 indica que Windows Installer versão 2,0 ou superior é necessária. Um valor de 2 indica que Windows Installer versão 1,2 ou superior é necessária. O valor padrão é 1.</td>
</tr>
<tr class="even">
<td><a href="character-count-summary.md"><strong>Contagem de caracteres</strong></a></td>
<td>Nulo</td>
</tr>
<tr class="odd">
<td><a href="creating-application-summary.md"><strong>Criando aplicativo</strong></a></td>
<td>O nome do software usado para criar o patch.</td>
</tr>
<tr class="even">
<td><a href="security-summary.md"><strong>Segurança</strong></a></td>
<td>O valor dessa propriedade deve ser de 4 impostos como somente leitura.</td>
</tr>
<tr class="odd">
<td><a href="codepage-summary.md"><strong>Código</strong></a></td>
<td>O valor numérico da página de código ANSI usada para exibir as informações de resumo. Essa propriedade deve ser definida antes que quaisquer propriedades de cadeia de caracteres sejam definidas nas informações de resumo.</td>
</tr>
</tbody>
</table>



 

 

 




