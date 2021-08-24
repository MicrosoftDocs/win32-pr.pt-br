---
description: A interface IKsPin fornece um método para recuperar as mídias com suporte por um pin em um filtro de modo kernel. O IKsPin tem métodos adicionais além do mostrado aqui, mas não há suporte para DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interface IKsPin (Ksproxy.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 8855378544bcc2ea7357af220b5d80d32edde74a50c304e973c9821aa8e9a41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792326"
---
# <a name="ikspin-interface"></a>Interface IKsPin

A `IKsPin` interface fornece um método para recuperar as mídias com suporte por um pin em um filtro de modo kernel. `IKsPin`tem métodos adicionais além do mostrado aqui, mas não há suporte para DirectShow.

## <a name="members"></a>Membros

A interface **IKsPin** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **O IKsPin** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IKsPin** tem esses métodos.



| Método                                          | Descrição                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Recupera as mídias com suporte por um pino.<br/> |



 

## <a name="remarks"></a>Comentários

Você deve incluir Ks.h antes de Ksproxy.h.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Ksproxy.h</dt> </dl>    |
| Biblioteca<br/>                  | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
