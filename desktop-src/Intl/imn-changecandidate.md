---
description: Notifica o aplicativo quando um IME está prestes a alterar o conteúdo da janela candidata. O aplicativo recebe esse comando por meio da \_ mensagem de notificação do IME do WM \_ com configurações de parâmetro, conforme mostrado abaixo.
ms.assetid: 0a276f9c-cece-4fa6-b71a-ba0daad5ca05
title: IMN_CHANGECANDIDATE código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 197380c3cf6369e0dbfd7dbca76bb3b84334eb6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091666"
---
# <a name="imn_changecandidate-notification-code"></a>Código de notificação do IMN \_ CHANGECANDIDATE

Notifica o aplicativo quando um IME está prestes a alterar o conteúdo da janela candidata. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ notificação do IME do WM**](wm-ime-notify.md) com configurações de parâmetro, conforme mostrado abaixo.


```C++
IMN_CHANGECANDIDATE
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMN \_ CHANGECANDIDATE.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Sinalizador de lista de candidatos. Cada bit corresponde a uma lista de candidatos: bit 0 à primeira lista, bit 1 à segunda lista e assim por diante. Se um bit especificado for 1, a janela candidata correspondente estará prestes a ser alterada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Este comando não tem nenhum valor de retorno.

## <a name="remarks"></a>Comentários

Um aplicativo deve processar esse comando se ele exibir os candidatos em si.

A janela do IME altera a aparência da janela candidata ao processar esse comando. Um aplicativo pode obter informações sobre a janela do sistema com [**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta) e [**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>IMM. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**ImmGetCandidateList**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelista)
</dt> <dt>

[**ImmGetCandidateListCount**](/windows/desktop/api/Imm/nf-imm-immgetcandidatelistcounta)
</dt> <dt>

[**\_notificação do IME do WM \_**](wm-ime-notify.md)
</dt> </dl>

 

 




