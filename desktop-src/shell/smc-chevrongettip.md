---
description: Solicita o título e o texto de um InfoTip de divisa para o item especificado pela estrutura SMDATA que o acompanha.
ms.assetid: 7bce4079-994c-4eb0-ab86-9044701d85a1
title: Mensagem de SMC_CHEVRONGETTIP (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 118056627d19990648e81b69aa355f3df99ec286
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968056"
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

## <a name="return-value"></a>Retornar valor

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



 

 




