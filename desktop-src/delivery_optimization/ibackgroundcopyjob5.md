---
title: Interface IBackgroundCopyJob5 (Deliveryoptimization.h)
description: Use essa interface para consultar ou definir vários comportamentos opcionais de um trabalho.
ms.assetid: C4706E10-40E6-489B-9772-59D581781038
keywords:
- Interface IBackgroundCopyJob5
- Interface IBackgroundCopyJob5, descrita
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 593f06f74dde7e6891417871cd16dc3730ef005fb90a0a1b6cf5377fda7ebcd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461966"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interface IBackgroundCopyJob5

Use essa interface para consultar ou definir vários comportamentos opcionais de um trabalho.

Para obter essa interface, chame o **método IBackgroundCopyJob::QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` como o identificador de interface.

## <a name="members"></a>Membros

A interface **IBackgroundCopyJob5** herda de [**IBackgroundCopyJob.**](ibackgroundcopyjob-.md) **IBackgroundCopyJob5** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyJob5** tem esses métodos.



| Método                                                 | Descrição                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**Getproperty**](ibackgroundcopyjob5-getproperty.md) | Um método genérico para obter propriedades de trabalho DO.<br/> |
| [**Setproperty**](ibackgroundcopyjob5-setproperty.md) | Um método genérico para definir propriedades de trabalho DO.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1709 somente para \[ aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 somente \[ aplicativos da área de trabalho\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>DeliveryOptimization.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc.lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





