---
description: Instrui uma janela do IME para obter a posição da janela candidata. Para enviar esse comando, o aplicativo usa a \_ mensagem de controle IME do WM \_ com as configurações de parâmetro mostradas abaixo.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: Comando IMC_GETCANDIDATEPOS (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bcb5cd143bf45f9bdb37be4cbe3078a483f53db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749813"
---
# <a name="imc_getcandidatepos-command"></a>\_Comando GETCANDIDATEPOS do IMC

Instrui uma janela do IME para obter a posição da janela candidata. Para enviar esse comando, o aplicativo usa a mensagem de [**\_ \_ controle IME do WM**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMC \_ GETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

Ponteiro para uma estrutura [**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contém a posição da janela candidata.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.

## <a name="remarks"></a>Comentários

Como o IME pode ajustar a posição de uma janela candidata, um aplicativo usa esse comando para obter a posição real para decidir se a janela deve ser reposicionada. A posição recuperada está em coordenadas de janela em relação à janela que tem o foco de entrada atual.

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

[**CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




