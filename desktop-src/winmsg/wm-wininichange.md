---
description: Um aplicativo envia a mensagem do WM \_ WININICHANGE para todas as janelas de nível superior depois de fazer uma alteração no arquivo de WIN.INI. A função SystemParametersInfo envia essa mensagem depois que um aplicativo usa a função para alterar uma configuração em WIN.INI.
ms.assetid: 402f8d71-ad52-486d-be26-8b41a3f22045
title: Mensagem de WM_WININICHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79b8db6c4794a8c1a572f61028d32eaeaf578d0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920874"
---
# <a name="wm_wininichange-message"></a>Mensagem do WM \_ WININICHANGE

Um aplicativo envia a mensagem do **WM \_ WININICHANGE** para todas as janelas de nível superior depois de fazer uma alteração no arquivo de WIN.INI. A função [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) envia essa mensagem depois que um aplicativo usa a função para alterar uma configuração em WIN.INI.

> [!Note]  
> A mensagem do **WM \_ WININICHANGE** é fornecida apenas para compatibilidade com versões anteriores do sistema. Os aplicativos devem usar a mensagem [**\_ SETTINGCHANGE do WM**](wm-settingchange.md) .

 

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_WININICHANGE                 0x001A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres que contém o nome do parâmetro do sistema que foi alterado. Por exemplo, essa cadeia de caracteres pode ser o nome de uma chave do registro ou o nome de uma seção no arquivo de Win.ini. Esse parâmetro não é particularmente útil para determinar qual parâmetro do sistema foi alterado. Por exemplo, quando a cadeia de caracteres é um nome de registro, ela normalmente indica apenas o nó folha no registro, não o caminho inteiro. Além disso, alguns aplicativos enviam essa mensagem com *lParam* definido como **NULL**. Em geral, ao receber essa mensagem, você deve verificar e recarregar as configurações de parâmetro do sistema que são usadas pelo seu aplicativo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se você processar essa mensagem, retornará zero.

## <a name="remarks"></a>Comentários

Para enviar a mensagem do **WM \_ WININICHANGE** para todas as janelas de nível superior, use a função [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) com o parâmetro *HWND* definido como **\_ transmissão de HWND**.

Chamadas para funções que mudam WIN.INI podem ser mapeadas para o registro em vez disso. Esse mapeamento ocorre quando WIN.INI e a seção que está sendo alterada são especificados no registro na seguinte chave:

**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ IniFileMapping**

A alteração no local de armazenamento não tem nenhum efeito sobre o comportamento dessa mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)
</dt> </dl>

 

 
