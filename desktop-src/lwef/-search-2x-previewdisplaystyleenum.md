---
title: Enumeração PreviewDisplayStyle
description: Usado pelo IResultsViewer PreviewStyle para definir ou determinar o estilo de exibição que está sendo usado no momento.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- Recursos do ambiente Windows herdado de enumeração PreviewDisplayStyle
topic_type:
- apiref
api_name:
- PreviewDisplayStyle
api_location:
- WdsView.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11902821ec9fdbbaa9ab8d3fda8971f42fc28c1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105772900"
---
# <a name="previewdisplaystyle-enumeration"></a>Enumeração PreviewDisplayStyle

> [!NOTE]
> O Windows Desktop Search 2. x é uma tecnologia obsoleta que originalmente estava disponível como um suplemento para o Windows XP e o Windows Server 2003. Em versões posteriores, use a [API de pesquisa do Windows](../search/-search-reference-entry-page.md) em vez disso. 

Usado por [**IResultsViewer::P reviewstyle**](-search-2x-iresultsviewer-previewstyle.md) para definir ou determinar o estilo de exibição que está sendo usado no momento.

## <a name="syntax"></a>Syntax


```C++
typedef enum PreviewDisplayStyleEnum { 
  AutoPreview    = 0,
  RightPreview   = 1,
  BottomPreview  = 2,
  NoPreview      = 3
} PreviewDisplayStyle;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Visualização prévia**
</dt> <dd>

Indica AutoVisualização.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**
</dt> <dd>

Indica RightPreview.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

Indica BottomPreview.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**Nopreview**
</dt> <dd>

Indica nopreview.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>WdsView. idl</dt> </dl> |



 

 





