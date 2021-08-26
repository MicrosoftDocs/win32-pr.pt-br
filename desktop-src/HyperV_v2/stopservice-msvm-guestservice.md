---
description: Interrompe o serviço convidado.
ms.assetid: 67FFA46C-0B61-4845-A617-BA10F4D42CBC
title: 'Método Msvm_GuestService:: StopService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StopService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f67234a09ad150f2f039a57b321797e03444c75defe2e83cfd06b60de320a664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050386"
---
# <a name="msvm_guestservicestopservice-method"></a>\_Método Msvm GuestService:: StopService

Interrompe o serviço convidado.

## <a name="syntax"></a>Sintaxe


```C++
uint32 StopService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                                             | Descrição         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl> | Êxito.<br/> |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




