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
ms.openlocfilehash: 652007933669db4ed7977474858c7089ca0d577f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364904"
---
# <a name="wmwmcollectiongroupid"></a>WM/WMCollectionGroupID

O atributo **WM/WMCollectionGroupID** contém um GUID que identifica o grupo de coleta.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionGroupID

## <a name="data-type"></a>Tipo de Dados

**\_GUID do tipo WMT \_**

## <a name="remarks"></a>Comentários

O conteúdo é identificado pelas tecnologias de mídia do Windows usando três valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. Todos esses três valores são preenchidos pelo Windows Media Player quando os metadados para o conteúdo são recuperados. Você pode fazer com que seu aplicativo registre esses valores e usá-los para identificar conteúdo, mas você não deve alterá-los se estiverem presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




