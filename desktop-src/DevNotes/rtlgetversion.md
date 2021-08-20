---
description: Obtém informações de versão sobre o sistema operacional em execução no momento.
ms.assetid: F04F0981-A07D-4B38-9DE4-B8461EAFC19F
title: Função RtlGetVersion (Ntddk.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetVersion
api_type:
- DllExport
api_location:
- Ntdll.dll
- NtosKrnl.exe
ms.openlocfilehash: 7420b9dba03e3b136331f4463f476908882ca5564d0fc7ac563036c7acccb356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161678"
---
# <a name="rtlgetversion-function"></a>Função RtlGetVersion

Obtém informações de versão sobre o sistema operacional em execução no momento.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS RtlGetVersion(
  _Out_ PRTL_OSVERSIONINFOW lpVersionInformation
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lpVersionInformation* \[ out\]
</dt> <dd>

Ponteiro para uma estrutura [**\_ RTL OSVERSIONINFOW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfow) ou uma estrutura [**\_ RTL OSVERSIONINFOEXW**](/windows-hardware/drivers/ddi/wdm/ns-wdm-_osversioninfoexw) que contém as informações de versão sobre o sistema operacional em execução no momento. Um chamador especifica qual estrutura de entrada é usada definindo o **membro dwOSVersionInfoSize** da estrutura para o tamanho em bytes da estrutura usada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna STATUS \_ SUCCESS.

## <a name="remarks"></a>Comentários

**RtlGetVersion** é o equivalente da [**função GetVersionEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getversionexa) no SDK do Windows. Consulte o exemplo no SDK Windows que mostra como obter a versão do sistema.

Ao usar **RtlGetVersion** para determinar se uma versão específica do sistema operacional está em execução, um chamador deve verificar se há números de versão maiores ou iguais ao número de versão necessário. Isso garante que um teste de versão seja bem-sucedido para versões posteriores do Windows.

Como os recursos do sistema operacional podem ser adicionados em uma DLL redistribuível, verificar apenas os números de versão principal e secundária não é a maneira mais confiável de verificar a presença de um recurso específico do sistema. Um driver deve usar [**RtlVerifyVersionInfo**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlverifyversioninfo) para testar a presença de um recurso específico do sistema.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                     |
| Plataforma de destino<br/>          | <dl> <dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt> </dl>                  |
| Cabeçalho<br/>                   | <dl> <dt>Ntddk.h (incluir Ntddk.h)</dt> </dl>                                                     |
| Biblioteca<br/>                  | <dl> <dt>Ntdll.lib; </dt> <dt>NtosKrnl.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Ntdll.dll; </dt> <dt>NtosKrnl.exe</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**PsGetVersion**](/windows-hardware/drivers/ddi/wdm/nf-wdm-psgetversion)
</dt> </dl>

 

 
