---
description: Uma função de retorno de chamada de notificação especificada com a função LdrRegisterDllNotification.
ms.assetid: 12202797-c80c-4fa3-9cc4-dcb1a9f01551
title: Função de retorno de chamada LdrDllNotification
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LdrDllNotification
- PLDR_DLL_NOTIFICATION_FUNCTION
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e29cd7b17c634250f56cbafcf86379449ac88199
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826117"
---
# <a name="ldrdllnotification-callback-function"></a>Função de retorno de chamada LdrDllNotification

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Uma função de retorno de chamada de notificação especificada com a função [**LdrRegisterDllNotification**](ldrregisterdllnotification.md) . O carregador chama essa função quando uma DLL é carregada pela primeira vez.

**AVISO:** Não é seguro que a função de retorno de chamada de notificação chame funções em qualquer DLL.

## <a name="syntax"></a>Sintaxe


```C++
VOID CALLBACK LdrDllNotification(
  _In_     ULONG                       NotificationReason,
  _In_     PCLDR_DLL_NOTIFICATION_DATA NotificationData,
  _In_opt_ PVOID                       Context
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*NotificationReason* \[ no\]
</dt> <dd>

O motivo pelo qual a função de retorno de chamada de notificação foi chamada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                        | Significado                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ Motivo da notificação de DLL \_ \_ \_ carregado**</dt> <dt>1</dt> </dl>       | A DLL foi carregada. O parâmetro *NotificationData* aponta para a estrutura de dados de notificação de uma **\_ dll LDR \_ carregada \_ \_** . <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ Motivo da notificação de DLL \_ \_ \_ descarregado**</dt> <dt>2</dt> </dl> | A DLL foi descarregada. O parâmetro *NotificationData* aponta para uma estrutura de **\_ \_ \_ \_ dados de notificação descarregada da DLL de LDR** . <br/> |



 

</dd> <dt>

*NotificationData* \[ no\]
</dt> <dd>

Um ponteiro para uma constante **de \_ \_ notificação de dll DDL de LDR** que contém dados de notificação. Essa União tem a seguinte definição:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

A estrutura de **\_ dados de notificação da dll LDR \_ carregada \_ \_** tem a seguinte definição:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

A estrutura de dados de notificação de a **dll de LDR \_ \_ descarregada \_ \_** tem a seguinte definição:

``` syntax
typedef struct _LDR_DLL_UNLOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_UNLOADED_NOTIFICATION_DATA, *PLDR_DLL_UNLOADED_NOTIFICATION_DATA;
```

</dd> <dt>

*Contexto* \[ do em, opcional\]
</dt> <dd>

Um ponteiro para dados de contexto para a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa função de retorno de chamada não retorna um valor.

## <a name="remarks"></a>Comentários

A função de retorno de chamada de notificação é chamada antes que a vinculação dinâmica ocorra.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




