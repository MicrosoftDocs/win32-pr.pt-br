---
title: Os conjuntos de propriedades DocumentSummaryInformation e UserDefined
description: Um conjunto de propriedades DocumentSummaryInformation e UserDefined é uma extensão para o conjunto de propriedades de informações resumidas. Os dois conjuntos de propriedades podem existir simultaneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Conjuntos de propriedades UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 411c6081ec098539baa2b26b6594d04216f5b455
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498688"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Os conjuntos de propriedades DocumentSummaryInformation e UserDefined

Um conjunto de propriedades **DocumentSummaryInformation** **e UserDefined** é uma extensão para [o conjunto de propriedades de informações resumidas](the-summary-information-property-set.md). Os dois conjuntos de propriedades podem existir simultaneamente.

O nome do fluxo que contém o conjunto de propriedades **DocumentSummaryInformation** é **" \\ 005DocumentSummaryInformation"**. O identificador de formato (FMTID) para o conjunto de propriedades **DocumentSummaryInformation** é **D5CDD502-2E9C-101B-9397-08002B2CF9AE**.

A declaração para esse valor está disponível nos arquivos de cabeçalho fornecidos como **FMTID \_ DocSummaryInformation**. Para obter mais informações, consulte [nomes em IStorage](names-in-istorage.md), [o resumo de propriedades de informações de resumido](the-summary-information-property-set.md), [**IPropertySetStorage:: criar**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) e [Formatar identificadores](format-identifiers.md).

Esse fluxo também tem uma seção separada para as propriedades definidas pelo usuário personalizado, como nos conjuntos de propriedades **DocumentSummaryInformation** **e UserDefined** . Esta seção aparece na interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) como um conjunto de propriedades separado, com o seguinte FMTID (disponível como **FMTID \_ userdefineproperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Esses dois conjuntos de propriedades são os únicos para os quais um único fluxo pode conter vários conjuntos de propriedades. O fato de que esses dois conjuntos de propriedades estão em um único fluxo afeta o comportamento da interface **IPropertySetStorage** . Para obter mais informações, consulte [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

A tabela a seguir lista as propriedades adicionadas ao conjunto **de propriedades** **DocumentSummaryInformation** e UserDefined. Como no conjunto de propriedades **SummaryInformation** , os nomes normalmente não são armazenados no conjunto de propriedades, mas são inferidos do identificador de propriedade.



| Nome da propriedade      | Identificador de propriedade     | Valor do identificador de propriedade | Tipo de variante                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Categoria           | **\_categoria PIDDSI**    | 0x00000002                | **a VT \_ LPSTR**                     |
| PresentationTarget | **PIDDSI \_ PRESFORMAT**  | 0x00000003                | **a VT \_ LPSTR**                     |
| Bytes              | **BYTECOUNT do PIDDSI \_**   | 0x00000004                | **\_I4 VT**                        |
| Linhas              | **PIDDSI \_ LINECOUNT**   | 0x00000005                | **\_I4 VT**                        |
| Parágrafos         | **PIDDSI \_ PARCOUNT**    | 0x00000006                | **\_I4 VT**                        |
| Slides             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **\_I4 VT**                        |
| Observações              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **\_I4 VT**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **\_I4 VT**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | 0x0000000A                | **\_I4 VT**                        |
| ScaleCrop          | **escala de PIDDSI \_**       | 0x0000000B                | **BOOL do VT \_**                      |
| HeadingPairs       | **PIDDSI \_ HEADINGPAIR** | 0x0000000C                | **VT \_** \| **\_ vetor VT** de variante |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_** \| **\_ LPSTR** de vetor VT   |
| Gerente            | **Gerenciador de PIDDSI \_**     | 0x0000000E                | **a VT \_ LPSTR**                     |
| Empresa            | **\_empresa PIDDSI**     | 0x0000000F                | **a VT \_ LPSTR**                     |
| LinksUpToDate      | **PIDDSI \_ LINKSDIRTY**  | 0x00000010                | **BOOL do VT \_**                      |



 

Essas propriedades têm os seguintes usos:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias
</dt> <dd>

Uma cadeia de texto digitada pelo usuário que indica a qual categoria o arquivo pertence (memorando, proposta e assim por diante). É útil para localizar arquivos do mesmo tipo.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Formato de destino para apresentação (35mm, impressora, vídeo e assim por diante).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes
</dt> <dd>

Quantidade de bytes.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Alinha
</dt> <dd>

Número de linhas.

</dd> <dt>

<span id="Paragraphs"></span><span id="paragraphs"></span><span id="PARAGRAPHS"></span>Parágrafos
</dt> <dd>

Número de parágrafos.

</dd> <dt>

<span id="Slides"></span><span id="slides"></span><span id="SLIDES"></span>Slides
</dt> <dd>

Número de slides.

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Registra
</dt> <dd>

Número de páginas que contêm anotações.

</dd> <dt>

<span id="HiddenSlides"></span><span id="hiddenslides"></span><span id="HIDDENSLIDES"></span>HiddenSlides
</dt> <dd>

Número de slides ocultos.

</dd> <dt>

<span id="MMClips"></span><span id="mmclips"></span><span id="MMCLIPS"></span>MMClips
</dt> <dd>

Número de clipes de som ou de vídeo.

</dd> <dt>

<span id="ScaleCrop"></span><span id="scalecrop"></span><span id="SCALECROP"></span>ScaleCrop
</dt> <dd>

Defina como true (-1) quando o dimensionamento da miniatura for desejado. Se não estiver definido, o corte será desejado.

</dd> <dt>

<span id="HeadingPairs"></span><span id="headingpairs"></span><span id="HEADINGPAIRS"></span>HeadingPairs
</dt> <dd>

Propriedade usada internamente indicando o agrupamento de diferentes partes do documento e o número de itens em cada grupo. Os títulos das partes do documento são armazenados na propriedade **TitlesofParts** . A propriedade **HeadingPairs** é armazenada como um vetor de variantes, em pares de repetição de **VT \_ LPSTR** (ou **VT \_ LPWSTR**) e valores de **\_ i4 VT** . O valor de ' **VT \_ LPSTR** ' representa um nome de título e o valor de **\_ i4 de VT** indica a contagem de partes de documento sob esse título.

</dd> <dt>

<span id="TitlesofParts"></span><span id="titlesofparts"></span><span id="TITLESOFPARTS"></span>TitlesofParts
</dt> <dd>

Nomes de partes do documento.

</dd> <dt>

<span id="Manager"></span><span id="manager"></span><span id="MANAGER"></span>Manager
</dt> <dd>

Gerente do projeto.

</dd> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>Corporativa
</dt> <dd>

Nome da empresa.

</dd> <dt>

<span id="LinksUpToDate"></span><span id="linksuptodate"></span><span id="LINKSUPTODATE"></span>LinksUpToDate
</dt> <dd>

Valor booliano para indicar se os links personalizados são dificultados por ruído excessivo, para todos os aplicativos.

> [!Note]  
> Conforme descrito em 12,3. Formato serializado para conjuntos de propriedades da especificação de design de OLE 2,0, os elementos de vetor nas propriedades **HeadingPairs** e **TitlesofParts** devem ser alinhados em limites de bit 32 dentro do conjunto de propriedades. No entanto, nos conjuntos de propriedades **DocumentSummaryInformation** **e UserDefined** , quando a página de código do conjunto de propriedades não é Unicode, esses elementos devem ser empacotados.

 

</dd> </dl>

O conjunto de propriedades **UserDefined** pode ser usado para manter qualquer propriedade. Normalmente, ele é usado para armazenar as propriedades nomeadas criadas por um usuário.

 

 




