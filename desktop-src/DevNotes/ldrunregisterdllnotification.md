---
description: Cancela a notificação de carregamento de DLL registrada anteriormente chamando a função LdrRegisterDllNotification.
ms.assetid: 18c3a027-e3cb-4083-afdc-00f416a70d8c
title: Função LdrUnregisterDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrUnregisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: c70a732f1e1d1dd71db8d89489066547ee5238e89cf992fca9f2b04759b4c9ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001296"
---
# <a name="ldrunregisterdllnotification-function"></a>Função LdrUnregisterDllNotification

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Cancela a notificação de carregamento de DLL registrada anteriormente chamando a [**função LdrRegisterDllNotification.**](ldrregisterdllnotification.md)

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cookie* \[ Em\]
</dt> <dd>

Um ponteiro para o identificador de retorno de chamada recebido da [**chamada LdrRegisterDllNotification**](ldrregisterdllnotification.md) registrada para notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um **código de erro ou NTSTATUS.**

Se a função for bem-sucedida, ela **retornará STATUS \_ SUCCESS.**

Se a função de retorno de chamada não for encontrada, a função **retornará STATUS \_ DLL \_ NOT \_ FOUND**.

Os formulários e a significância dos códigos de erro **NTSTATUS** são listados no arquivo de título Ntstatus.h disponível no WDK e são descritos na documentação do WDK.

## <a name="remarks"></a>Comentários

Essa função não tem nenhum arquivo de header associado. A biblioteca de importação associada, Ntdll.lib, está disponível no WDK. Você também pode usar as [**funções LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
