---
title: Os conjuntos de propriedades DocumentSummaryInformation e UserDefined
description: Um conjunto de propriedades DocumentSummaryInformation e UserDefined é uma extensão para o conjunto de propriedades Informações resumidas. Ambos os conjuntos de propriedades podem existir simultaneamente.
ms.assetid: c6d4e2bc-f7f6-429d-aa91-432d833c69d1
keywords:
- DocumentSummaryInformation
- Conjuntos de propriedades UserDefined
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d76c679fd8b4059e821598bed37d68735c45f914e4685e43a1c514b832e199e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886832"
---
# <a name="the-documentsummaryinformation-and-userdefined-property-sets"></a>Os conjuntos de propriedades DocumentSummaryInformation e UserDefined

Um **conjunto de propriedades DocumentSummaryInformation** e **UserDefined** é uma extensão para o conjunto de [propriedades Informações resumidas](the-summary-information-property-set.md). Ambos os conjuntos de propriedades podem existir simultaneamente.

O nome do fluxo que contém o conjunto de propriedades **DocumentSummaryInformation** **é " \\ 005DocumentSummaryInformation".** O FMTID (identificador de formato) do conjunto de propriedades **DocumentSummaryInformation** é **D5CDD502-2E9C-101B-9397-08002B2CF9AE.**

A declaração para esse valor está disponível nos arquivos de título fornecidos como **FMTID \_ DocSummaryInformation**. Para obter mais informações, consulte [Names in IStorage](names-in-istorage.md), [The Summary Information Property Set](the-summary-information-property-set.md), [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) and [Format Identifiers](format-identifiers.md).

Esse fluxo também tem uma seção separada para as propriedades definidas pelo usuário personalizado como nos conjuntos de propriedades **DocumentSummaryInformation** e **UserDefined.** Esta seção aparece na interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) como um conjunto de propriedades separado, com o seguinte FMTID (disponível como **FmTID \_ UserDefinedProperties**): **D5CDD505-2E9C-101B-9397-08002B2CF9AE**.

Esses dois conjuntos de propriedades são os únicos para os quais um único fluxo pode conter vários conjuntos de propriedades. O fato de que esses dois conjuntos de propriedades estão em um único fluxo afeta o comportamento da interface **IPropertySetStorage.** Para obter mais informações, [**consulte IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

A tabela a seguir lista as propriedades adicionadas ao conjunto de propriedades **DocumentSummaryInformation** e **UserDefined.** Assim como no conjunto de propriedades **SummaryInformation,** os nomes normalmente não são armazenados no conjunto de propriedades, mas são inferidos do identificador de propriedade.



| Nome da propriedade      | Identificador de propriedade     | Valor do identificador de propriedade | Tipo VARIANT                      |
|--------------------|-------------------------|---------------------------|-----------------------------------|
| Categoria           | **CATEGORIA PIDDSI \_**    | 0x00000002                | **VT \_ LPSTR**                     |
| PresentationTarget | **PRÉ-FORMATO PIDDSI \_**  | 0x00000003                | **VT \_ LPSTR**                     |
| Bytes              | **PIDDSI \_ BYTECOUNT**   | 0x00000004                | **VT \_ I4**                        |
| Linhas              | **PIDDSI \_ LINECOUNT**   | 0x00000005                | **VT \_ I4**                        |
| Parágrafos         | **PIDDSI \_ PARCOUNT**    | 0x00000006                | **VT \_ I4**                        |
| Slides             | **PIDDSI \_ SLIDECOUNT**  | 0x00000007                | **VT \_ I4**                        |
| Observações              | **PIDDSI \_ NOTECOUNT**   | 0x00000008                | **VT \_ I4**                        |
| HiddenSlides       | **PIDDSI \_ HIDDENCOUNT** | 0x00000009                | **VT \_ I4**                        |
| MMClips            | **PIDDSI \_ MMCLIPCOUNT** | 0x0000000A                | **VT \_ I4**                        |
| ScaleCrop          | **ESCALA PIDDSI \_**       | 0x0000000B                | **BOOL da VT \_**                      |
| HeadingPairs       | **TÍTULO PIDDSIPAIR \_** | 0x0000000C                | **VT \_ VARIANT** \| **VT \_ VECTOR** |
| TitlesofParts      | **PIDDSI \_ DOCPARTS**    | 0x0000000D                | **VT \_ VECTOR** \| **VT \_ LPSTR**   |
| Gerente            | **PIDDSI \_ MANAGER**     | 0x0000000E                | **VT \_ LPSTR**                     |
| Empresa            | **PIDDSI \_ COMPANY**     | 0x0000000F                | **VT \_ LPSTR**                     |
| LinksUpToDate      | **LINKS DO PIDDSIDIRTY \_**  | 0x00000010                | **BOOL da VT \_**                      |



 

Essas propriedades têm os seguintes usos:

<dl> <dt>

<span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria
</dt> <dd>

Uma cadeia de caracteres de texto digitada pelo usuário que indica a qual categoria o arquivo pertence (memorando, proposta e assim por diante). É útil para localizar arquivos do mesmo tipo.

</dd> <dt>

<span id="PresentationTarget"></span><span id="presentationtarget"></span><span id="PRESENTATIONTARGET"></span>PresentationTarget
</dt> <dd>

Formato de destino para apresentação (35mm, impressora, vídeo e assim por diante).

</dd> <dt>

<span id="Bytes"></span><span id="bytes"></span><span id="BYTES"></span>Bytes
</dt> <dd>

Quantidade de bytes.

</dd> <dt>

<span id="Lines"></span><span id="lines"></span><span id="LINES"></span>Linhas
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

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>Notas
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

 

 




