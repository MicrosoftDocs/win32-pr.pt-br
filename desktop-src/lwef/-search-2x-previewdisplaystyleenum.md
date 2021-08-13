---
title: Enumeração PreviewDisplayStyle
description: Usado por IResultsViewer PreviewStyle para definir ou determinar o estilo de exibição que está sendo usado no momento.
ms.assetid: ccbbfe38-0719-41e0-9331-cc0c1be651eb
keywords:
- PreviewDisplayStyle enumeration Legacy Windows Environment Features
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
ms.openlocfilehash: bd98a439daeadfd2af6135c1519aea8f981f94394ac68efe142a64037e70a25f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753390"
---
# <a name="previewdisplaystyle-enumeration"></a>Enumeração PreviewDisplayStyle

> [!NOTE]
> Windows A Pesquisa de Área de Trabalho 2.x é uma tecnologia obsoleta que estava originalmente disponível como um complemento para Windows XP e Windows Server 2003. Em versões posteriores, use a [API Windows Search.](../search/-search-reference-entry-page.md) 

Usado por [**IResultsViewer::P reviewStyle**](-search-2x-iresultsviewer-previewstyle.md) para definir ou determinar o estilo de exibição que está sendo usado no momento.

## <a name="syntax"></a>Sintaxe


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

<span id="AutoPreview"></span><span id="autopreview"></span><span id="AUTOPREVIEW"></span>**Visualização Automática**
</dt> <dd>

Indica Visualização Automática.

</dd> <dt>

<span id="RightPreview"></span><span id="rightpreview"></span><span id="RIGHTPREVIEW"></span>**RightPreview**
</dt> <dd>

Indica RightPreview.

</dd> <dt>

<span id="BottomPreview"></span><span id="bottompreview"></span><span id="BOTTOMPREVIEW"></span>**BottomPreview**
</dt> <dd>

Indica BottomPreview.

</dd> <dt>

<span id="NoPreview"></span><span id="nopreview"></span><span id="NOPREVIEW"></span>**NoPreview**
</dt> <dd>

Indica NoPreview.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|----------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>WdsView.idl</dt> </dl> |



 

 





