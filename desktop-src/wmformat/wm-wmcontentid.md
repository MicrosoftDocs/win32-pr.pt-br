---
title: WM/WMContentID
description: O atributo WM/WMContentID contém um GUID que identifica o conteúdo.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato de mídia do Windows do WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ef250e2e2e797ce5ba3c4492c2a3f8b71d30eb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364903"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

O atributo **WM/WMContentID** contém um GUID que identifica o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMContentID

## <a name="data-type"></a>Tipo de Dados

**\_GUID do tipo WMT \_**

## <a name="remarks"></a>Comentários

O conteúdo é identificado pelas tecnologias de mídia do Windows usando três valores: **WM/WMCollectionGroupID**, **WM/WMCollectionID** e **WM/WMContentID**. Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. Todos esses três valores são preenchidos pelo Windows Media Player quando os metadados para o conteúdo são recuperados. Você pode fazer com que seu aplicativo registre esses valores e usá-los para identificar conteúdo, mas você não deve alterá-los se estiverem presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




