---
title: WM/WMCollectionGroupID
description: O atributo WM/WMCollectionGroupID contém um GUID que identifica o grupo de coleta.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Formato de mídia do Windows WM/WMCollectionGroupID
topic_type:
- apiref
api_name:
- WM/WMCollectionGroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12b9d89724751e778eb9545b6c743dbfbcf077b860a8d85c5ab9297680deb930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118698230"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

O **atributo WM/WMCollectionGroupID** contém um GUID que identifica o grupo de coleta.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo de Dados

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

O conteúdo é identificado por tecnologias Windows Media usando três valores: **WM/WMCollectionGroupID,** **WM/WMCollectionID** e **WM/WMContentID.** Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. Todos esses três valores são preenchidos por Windows Media Player quando os metadados do conteúdo são recuperados. Você pode fazer com que seu aplicativo grave esses valores e use-os para identificar o conteúdo, mas não deve alterá-los se eles estão presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




