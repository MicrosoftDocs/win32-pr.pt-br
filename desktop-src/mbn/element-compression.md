---
description: MBNProfileExt... \/ \/ Compactação (v4)
MS-HAID: WWAN\_profile\_v4.element\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Compactação
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4b2ad853-ecb3-46ef-8ce2-aa001bb070e6
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7782052ef467725a099929e8940262d1f08329431f68525b8c401f36a276ebcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745099"
---
# <a name="span-idwwan_profile_v4element_compressionspanmbnprofileextcompression-v4"></a><span id="WWAN_profile_v4.element_Compression"></span>MBNProfileExt... \/ \/ Compactação (v4)

Especifica se a compactação será usada no link de dados para transferência de dados e de título.

Para obter mais informações, consulte a documentação do elemento [**Compression**](./schema-compression-contexttype-element.md) v1.

## <a name="element-hierarchy"></a>Hierarquia de elementos

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a>Sintaxe

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Atributos e elementos

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Atributos

Nenhum.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Elementos filho

Nenhum.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Elementos pai

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Elemento pai</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="element-context.md">Contexto</a></td>
<td><p>Especifica os parâmetros necessários para estabelecer uma conexão de dados.</p></td>
</tr>
</tbody>
</table>

 

## <a name="requirements"></a>Requisitos

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Namespace</p></td>
<td><p>https://www.microsoft.com/networking/WWAN/profile/v4</p></td>
</tr>
</tbody>
</table>

 

 
