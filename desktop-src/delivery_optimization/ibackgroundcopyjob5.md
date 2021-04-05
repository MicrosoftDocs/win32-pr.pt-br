---
title: Interface IBackgroundCopyJob5 (Deliveryoptimization. h)
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
ms.openlocfilehash: e76898f7bbfe4d4dc34aec035b842e6671091630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086104"
---
# <a name="ibackgroundcopyjob5-interface"></a>Interface IBackgroundCopyJob5

Use essa interface para consultar ou definir vários comportamentos opcionais de um trabalho.

Para obter essa interface, chame o método **método ibackgroundcopyjob:: QueryInterface** usando `__uuidof(IBackgroundCopyJob5)` como o identificador de interface.

## <a name="members"></a>Membros

A interface **IBackgroundCopyJob5** herda de [**método ibackgroundcopyjob**](ibackgroundcopyjob-.md). **IBackgroundCopyJob5** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **IBackgroundCopyJob5** tem esses métodos.



| Método                                                 | Descrição                                                |
|:-------------------------------------------------------|:-----------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyjob5-getproperty.md) | Um método genérico para obter as propriedades DO trabalho.<br/> |
| [**SetProperty**](ibackgroundcopyjob5-setproperty.md) | Um método genérico para definir as propriedades DO trabalho.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1709\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Server, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 é definido como E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Método ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





