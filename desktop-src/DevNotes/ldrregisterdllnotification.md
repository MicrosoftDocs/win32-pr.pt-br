---
description: Registra para notificação quando uma DLL é carregada pela primeira vez. Essa notificação ocorre antes que a vinculação dinâmica ocorra.
ms.assetid: c2757aa0-76fa-427a-a4f6-cb26e7f7d0d1
title: Função LdrRegisterDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrRegisterDllNotification
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: 82ec05a24f4cccc89cece666b18cb63412a78259
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010105"
---
# <a name="ldrregisterdllnotification-function"></a>Função LdrRegisterDllNotification

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Registra para notificação quando uma DLL é carregada pela primeira vez. Essa notificação ocorre antes que a vinculação dinâmica ocorra.

## <a name="syntax"></a>Sintaxe


```C++
NTSTATUS NTAPI LdrRegisterDllNotification(
  _In_     ULONG                          Flags,
  _In_     PLDR_DLL_NOTIFICATION_FUNCTION NotificationFunction,
  _In_opt_ PVOID                          Context,
  _Out_    PVOID                          *Cookie
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Flags* \[in\]
</dt> <dd>

Esse parâmetro deve ser zero.

</dd> <dt>

*NotificationFunction* \[ no\]
</dt> <dd>

Um ponteiro para uma função de retorno de chamada de notificação [*LdrDllNotification*](ldrdllnotification.md) para chamar quando a dll é carregada.

</dd> <dt>

*Contexto* \[ do em, opcional\]
</dt> <dd>

Um ponteiro para dados de contexto para a função de retorno de chamada.

</dd> <dt>

*Cookie* \[ fora\]
</dt> <dd>

Um ponteiro para uma variável para receber um identificador para a função de retorno de chamada. Esse identificador é usado para cancelar o registro da função de retorno de chamada de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a função for bem-sucedida, ela retornará o **status \_ êxito**.

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

[*LdrDllNotification*](ldrdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 
