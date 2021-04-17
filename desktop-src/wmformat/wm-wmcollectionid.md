---
title: WM/WMCollectionID
description: O atributo WM/WMCollectionID contém um GUID que identifica a coleção.
ms.assetid: 088fe2d7-e2d9-42a3-8deb-1d7948ff7df9
keywords:
- Formato de mídia do Windows do WM/WMCollectionID
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d2ffe9ca827b19b4ce403b2e2929dea64ae684
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364905"
---
# <a name="wmwmcollectionid"></a>WM/WMCollectionID

O atributo **WM/WMCollectionID** contém um GUID que identifica a coleção.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMCollectionID

## <a name="data-type"></a>Tipo de Dados

**\_GUID do tipo WMT \_**

## <a name="remarks"></a>Comentários

O conteúdo é identificado pelas tecnologias de mídia do Windows usando três valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. Todos esses três valores são preenchidos pelo Windows Media Player quando os metadados para o conteúdo são recuperados. Você pode fazer com que seu aplicativo registre esses valores e usá-los para identificar conteúdo, mas você não deve alterá-los se estiverem presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




