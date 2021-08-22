---
title: WM/WMContentID
description: O atributo WM/WMContentID contém um GUID que identifica o conteúdo.
ms.assetid: b46d02f4-04f5-430a-b3f7-0f80e03bed2c
keywords:
- Formato de mídia do Windows WM/WMContentID
topic_type:
- apiref
api_name:
- WM/WMContentID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef6b1b77bf0305fa0890ea7e85172d77d6e213864c1fc114136bc42e08a8507b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083860"
---
# <a name="wmwmcontentid"></a>WM/WMContentID

O **atributo WM/WMContentID** contém um GUID que identifica o conteúdo.

## <a name="global-constant"></a>Constante global

g \_ wszWMWMContentID

## <a name="data-type"></a>Tipo de Dados

**GUID DE \_ TIPO \_ WMT**

## <a name="remarks"></a>Comentários

O conteúdo é identificado por tecnologias Windows Media usando três valores: **WM/WMCollectionGroupID,** **WM/WMCollectionID** e **WM/WMContentID.** Esses valores identificam o conteúdo, a coleção à qual ele pertence e o grupo ao qual a coleção pertence. Todos esses três valores são preenchidos por Windows Media Player quando os metadados do conteúdo são recuperados. Você pode fazer com que seu aplicativo grave esses valores e use-os para identificar o conteúdo, mas não deve alterá-los se eles estão presentes.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Lista de Atributos**](attribute-list.md)
</dt> </dl>

 

 




