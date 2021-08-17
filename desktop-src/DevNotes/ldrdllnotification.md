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
ms.openlocfilehash: e1e9bea21cd4e21ca7549ce34343b42c50b293471e69576d7c1164f92a371c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118004101"
---
# <a name="ldrdllnotification-callback-function"></a>Função de retorno de chamada LdrDllNotification

\[Essa função pode ser alterada ou removida do Windows sem aviso prévio.\]

Uma função de retorno de chamada de notificação especificada com a [**função LdrRegisterDllNotification.**](ldrregisterdllnotification.md) O carregador chama essa função quando uma DLL é carregada pela primeira vez.

**Aviso:** Não é seguro para a função de retorno de chamada de notificação chamar funções em qualquer DLL.

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

*NotificationReason* \[ Em\]
</dt> <dd>

O motivo pelo qual a função de retorno de chamada de notificação foi chamada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                                        | Significado                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LDR_DLL_NOTIFICATION_REASON_LOADED"></span><span id="ldr_dll_notification_reason_loaded"></span><dl> <dt>**LDR \_ MOTIVO DA NOTIFICAÇÃO DE DLL \_ \_ \_ CARREGADO**</dt> <dt>1</dt> </dl>       | A DLL foi carregada. O *parâmetro NotificationData* aponta para uma estrutura de DADOS DE NOTIFICAÇÃO CARREGADA **de \_ DLL \_ \_ \_ LDR.** <br/>     |
| <span id="LDR_DLL_NOTIFICATION_REASON_UNLOADED"></span><span id="ldr_dll_notification_reason_unloaded"></span><dl> <dt>**LDR \_ MOTIVO DA NOTIFICAÇÃO DE DLL \_ \_ \_ DESCARREGADO**</dt> <dt>2</dt> </dl> | A DLL foi descarregada. O *parâmetro NotificationData* aponta para uma estrutura de DADOS DE NOTIFICAÇÃO **\_ \_ DESCARREGADA \_ \_ de DLL LDR.** <br/> |



 

</dd> <dt>

*NotificationData* \[ Em\]
</dt> <dd>

Um ponteiro para uma união **constante de NOTIFICAÇÃO \_ de DLL \_ LDR** que contém dados de notificação. Essa união tem a seguinte definição:

``` syntax
typedef union _LDR_DLL_NOTIFICATION_DATA {
    LDR_DLL_LOADED_NOTIFICATION_DATA Loaded;
    LDR_DLL_UNLOADED_NOTIFICATION_DATA Unloaded;
} LDR_DLL_NOTIFICATION_DATA, *PLDR_DLL_NOTIFICATION_DATA;
```

A **estrutura de DADOS DE \_ NOTIFICAÇÃO CARREGADA de DLL \_ \_ \_ LDR** tem a seguinte definição:

``` syntax
typedef struct _LDR_DLL_LOADED_NOTIFICATION_DATA {
    ULONG Flags;                    //Reserved.
    PCUNICODE_STRING FullDllName;   //The full path name of the DLL module.
    PCUNICODE_STRING BaseDllName;   //The base file name of the DLL module.
    PVOID DllBase;                  //A pointer to the base address for the DLL in memory.
    ULONG SizeOfImage;              //The size of the DLL image, in bytes.
} LDR_DLL_LOADED_NOTIFICATION_DATA, *PLDR_DLL_LOADED_NOTIFICATION_DATA;
```

A **estrutura de DADOS DE \_ NOTIFICAÇÃO \_ DESCARREGADA \_ \_ da DLL LDR** tem a seguinte definição:

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

*Contexto* \[ in, opcional\]
</dt> <dd>

Um ponteiro para dados de contexto para a função de retorno de chamada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa função de retorno de chamada não retorna um valor.

## <a name="remarks"></a>Comentários

A função de retorno de chamada de notificação é chamada antes da vinculação dinâmica ocorrer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>       |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LdrRegisterDllNotification**](ldrregisterdllnotification.md)
</dt> <dt>

[**LdrUnregisterDllNotification**](ldrunregisterdllnotification.md)
</dt> </dl>

 

 




