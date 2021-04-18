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
ms.openlocfilehash: 1fee03b4a06d274b495070eb40833b270a795158
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370352"
---
# <a name="ldrunregisterdllnotification-function"></a>Função LdrUnregisterDllNotification

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Cancela a notificação de carregamento de DLL registrada anteriormente chamando a função [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) .

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NTAPI LdrUnregisterDllNotification(
  _In_ PVOID Cookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Cookie* \[ no\]
</dt> <dd>

Um ponteiro para o identificador de retorno de chamada recebido da chamadas [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) registradas para notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um **NTSTATUS** ou um código de erro.

Se a função for bem-sucedida, ela retornará o **status \_ êxito**.

Se a função de retorno de chamada não for encontrada, a função retornará a **dll de status \_ \_ não \_ encontrada**.

Os formulários e o significado dos códigos de erro **NTSTATUS** são listados no arquivo de cabeçalho Ntstatus. h disponível no WDK e são descritos na documentação do WDK.

## <a name="remarks"></a>Comentários

Esta função não tem nenhum arquivo de cabeçalho associado. A biblioteca de importação associada, ntdll. lib, está disponível no WDK. Você também pode usar as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinamicamente a Ntdll.dll.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> </dl>

 

 
