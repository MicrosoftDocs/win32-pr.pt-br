---
description: Instrui uma janela do IME a obter a posição da janela candidata. Para enviar esse comando, o aplicativo usa a mensagem WM \_ IME \_ CONTROL com as configurações de parâmetro mostradas abaixo.
ms.assetid: e582dbc2-8081-424c-a972-1a182a477293
title: IMC_GETCANDIDATEPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e155a08c9d95fa2ac9f865d80b18d51120d19b28489bcad418eb4323dda39c3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107316"
---
# <a name="imc_getcandidatepos-command"></a>Comando \_ GETCANDIDATEPOS do IMC

Instrui uma janela do IME a obter a posição da janela candidata. Para enviar esse comando, o aplicativo usa a mensagem [**WM \_ IME \_ CONTROL**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_GETCANDIDATEPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Definido como IMC \_ GETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ponteiro para uma [**estrutura CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contém a posição da janela candidata.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.

## <a name="remarks"></a>Comentários

Como o IME pode ajustar a posição de uma janela candidata, um aplicativo usa esse comando para obter a posição real para decidir se deve reposicionar a janela. A posição recuperada está em coordenadas de janela em relação à janela que tem o foco de entrada atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Métodos de Entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de Métodos de Entrada](input-method-manager-commands.md)
</dt> <dt>

[**Candidateform**](/windows/win32/api/imm/ns-imm-candidateform)
</dt> </dl>

 

 




