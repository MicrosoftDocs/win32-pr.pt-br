---
title: WM/WMCollectionGroupID
description: O atributo WM/WMCollectionGroupID contém um GUID que identifica o grupo de coleta.
ms.assetid: 5cfa1747-ce3b-4e8d-bcce-84fb719123e8
keywords:
- Formato de mídia do Windows do WM/WMCollectionGroupID
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

O atributo **WM/WMCollectionGroupID** contém um GUID que identifica o grupo de coleta.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo de Dados

**\_GUID do tipo WMT \_**

## <a name="remarks"></a>Comentários

o conteúdo é identificado por Windows tecnologias de mídia usando três valores: **wm/WMCollectionGroupID**, **wm/WMCollectionID** e **wm/WMContentID**. Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. todos esses três valores são populados por Windows Media Player quando os metadados para o conteúdo são recuperados. Você pode fazer com que seu aplicativo registre esses valores e usá-los para identificar conteúdo, mas você não deve alterá-los se estiverem presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




