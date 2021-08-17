---
title: Função DDCCIGetCapabilitiesStringLength
description: Obtém o comprimento de uma cadeia de caracteres de recursos para um monitor.
ms.assetid: 8a26d17b-1535-49c7-8cfb-48feb283a3c4
keywords:
- Configuração do monitor de função DDCCIGetCapabilitiesStringLength
topic_type:
- apiref
api_name:
- DDCCIGetCapabilitiesStringLength
api_location:
- gdi32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd30aeb1e71d88b649478d0ecd1c3052dbbe32372909882f73ae77db6e4dbc1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066606"
---
# <a name="ddccigetcapabilitiesstringlength-function"></a>Função DDCCIGetCapabilitiesStringLength

> [!IMPORTANT]
> Essa função é usada pela API de configuração do monitor para acessar a funcionalidade no driver de vídeo. Os aplicativos não devem chamar essa função.

 

Obtém o comprimento de uma cadeia de caracteres de recursos para um monitor.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS WINAPI DDCCIGetCapabilitiesStringLength(
  _In_  HANDLE hMonitor,
  _Out_ DWORD  *pdwLength
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HMONITOR* \[ no\]
</dt> <dd>

Um identificador para um monitor físico.

</dd> <dt>

*pdwLength* \[ fora\]
</dt> <dd>

Recebe o comprimento da cadeia de caracteres de recursos, em caracteres, incluindo o caractere nulo de terminação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se o método for bem-sucedido, ele retornará o **status \_ êxito**. Caso contrário, ele retorna um código de erro **NTSTATUS** .

## <a name="remarks"></a>Comentários

Os aplicativos devem chamar [**GetCapabilitiesStringLength**](/windows/desktop/api/LowLevelMonitorConfigurationAPI/nf-lowlevelmonitorconfigurationapi-getcapabilitiesstringlength) em vez de chamar essa função.

Esta função não tem biblioteca de importação associada. Para chamar essa função, você deve usar as funções [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Gdi32.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Gdi32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Monitorar funções de configuração](monitor-configuration-functions.md)
</dt> </dl>

 

