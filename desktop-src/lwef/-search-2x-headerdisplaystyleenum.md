---
title: Enumeração HeaderDisplayStyle
description: Usado por IResultsViewer HeaderStyle para definir ou retornar o estilo de cabeçalho atual.
ms.assetid: 13ae6317-d990-4ccf-83b3-275caf953611
keywords:
- Recursos do ambiente Windows herdado de enumeração HeaderDisplayStyle
topic_type:
- apiref
api_name:
- HeaderDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc65b17fa61b799fc9ab8ea7cc1b01380a5843c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761062"
---
# <a name="headerdisplaystyle-enumeration"></a>Enumeração HeaderDisplayStyle

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Usado por [**IResultsViewer:: HeaderStyle**](-search-2x-iresultsviewer-headerstyle.md) para definir ou retornar o estilo de cabeçalho atual.

## <a name="syntax"></a>Syntax


```C++
typedef enum HeaderDisplayStyleEnum { 
  FullHeader     = 0,
  CompactHeader  = 1,
  NoHeader       = 2
} HeaderDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="FullHeader"></span><span id="fullheader"></span><span id="FULLHEADER"></span>**FullHeader**
</dt> <dd>

Indica ou define o uso de cabeçalhos completos.

</dd> <dt>

<span id="CompactHeader"></span><span id="compactheader"></span><span id="COMPACTHEADER"></span>**CompactHeader**
</dt> <dd>

Indica ou define o uso de cabeçalhos de compactação.

</dd> <dt>

<span id="NoHeader"></span><span id="noheader"></span><span id="NOHEADER"></span>**Noheader**
</dt> <dd>

Indica ou define o uso de nenhum cabeçalho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





