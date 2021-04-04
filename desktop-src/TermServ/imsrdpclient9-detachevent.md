---
title: Método IMsRdpClient9 detachEvent
description: Desanexa um evento.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método detachEvent
- método detachEvent Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método detachEvent
- método detachEvent Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método detachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085193"
---
# <a name="imsrdpclient9detachevent-method"></a>IMsRdpClient9: método etachEvent de:d

Desanexa um evento.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*eventoname* \[ no\]
</dt> <dd>

O nome do evento.

</dd> <dt>

*retorno de chamada* \[ no\]
</dt> <dd>

O retorno de chamada associado ao evento.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | CLSID \_ MsRdpClient9 é definido como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting é definido como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> IID \_ IMsRdpClient9 é definido como 28904001-04B6-436C-A55B-0AF1A0883DC9<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> </dl>

 

 





