---
title: Método IMsRdpClient9 SyncSessionDisplaySettings
description: Sincroniza as configurações de exibição da sessão.
ms.assetid: cc2c497f-665a-458d-895b-21dd21977890
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SyncSessionDisplaySettings
- Método SyncSessionDisplaySettings Serviços de Área de Trabalho Remota, interface IMsRdpClient9
- Serviços de Área de Trabalho Remota de interface IMsRdpClient9, método SyncSessionDisplaySettings
- Método SyncSessionDisplaySettings Serviços de Área de Trabalho Remota, interface IMsRdpClient10
- Serviços de Área de Trabalho Remota de interface IMsRdpClient10, método SyncSessionDisplaySettings
topic_type:
- apiref
api_name:
- IMsRdpClient9.SyncSessionDisplaySettings
- IMsRdpClient10.SyncSessionDisplaySettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4429f966c00fb608416d541bec229defeca3e5b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918005"
---
# <a name="imsrdpclient9syncsessiondisplaysettings-method"></a>Método IMsRdpClient9:: SyncSessionDisplaySettings

Sincroniza as configurações de exibição da sessão.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SyncSessionDisplaySettings();
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

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

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> </dl>

 

 





