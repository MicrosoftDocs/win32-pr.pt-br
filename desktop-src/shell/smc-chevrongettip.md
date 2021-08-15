---
description: Solicita o título e o texto de um InfoTip de divisa para o item especificado pela estrutura SMDATA que o acompanha.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Mensagem de SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e64636994743d4b13a96fe75947fb515c4dbd3edcc94e6dee0fa85efb8bc9d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968235"
---
# <a name="smc_chevrongettip-message"></a>Mensagem do SMC \_ CHEVRONGETTIP

Solicita o título e o texto de um InfoTip de divisa para o item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.


```C++
SMC_CHEVRONGETTIP 
    wParam = (WPARAM) (LPWSTR) pwszTipTitle;
    lParam = (LPARAM) (LPWSTR) pwszTipText
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pwszTipTitle* 
</dt> <dd>

Um ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em **nulo** que contém o título de InfoTip. Essa cadeia de caracteres não deve ultrapassar o máximo de \_ caracteres de caminho, incluindo o caractere **nulo** de terminação.

</dd> <dt>

*pwszTipText* 
</dt> <dd>

Um ponteiro para um buffer que recebe uma cadeia de caracteres Unicode terminada em **nulo** que contém o texto de InfoTip. Essa cadeia de caracteres não deve ultrapassar o máximo de \_ caracteres de caminho, incluindo o caractere **nulo** de terminação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar S \_ OK.

## <a name="remarks"></a>Comentários

Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




