---
title: WM/WMCollectionID
description: O atributo WM/WMCollectionID contém um GUID que identifica a coleção.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Formato de mídia do Windows WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ad7e22c6769d459dc3d99b964a2df8e4dc562c709a231163d05a1b6b0be911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928826"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

O **atributo WM/WMCollectionID** contém um GUID que identifica a coleção.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Tipo de Dados

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

O conteúdo é identificado por tecnologias Windows Media usando três valores: **WM/WMCollectionGroupID,** **WM/WMCollectionID** e **WM/WMContentID.** Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. Todos esses três valores são preenchidos por Windows Media Player quando os metadados do conteúdo são recuperados. Você pode fazer com que seu aplicativo grave esses valores e use-os para identificar o conteúdo, mas não deve alterá-los se eles estão presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




