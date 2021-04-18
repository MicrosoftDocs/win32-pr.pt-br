---
description: Coloca o serviço convidado em um estado iniciado.
ms.assetid: 1DC6A5B3-0F91-4AC1-99D5-0E8CF5ED35A2
title: 'Método Msvm_GuestService:: StartService'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestService.StartService
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1a87bc9933bd7b3a54bd59169b0099e34eb04c52
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758793"
---
# <a name="msvm_guestservicestartservice-method"></a>\_Método Msvm GuestService:: StartService

Coloca o serviço convidado em um estado iniciado.

## <a name="syntax"></a>Sintaxe


```C++
uint32 StartService();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.



| Código/valor de retorno                                                                                                                                             | Descrição         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl> | Êxito.<br/> |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>           |                     |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\\\\\Virtualização \\ v2 de raiz<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ GuestService**](msvm-guestservice.md)
</dt> </dl>

 

 




