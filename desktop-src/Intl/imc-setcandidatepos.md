---
description: Instrui uma janela do IME a definir a posição da janela candidatos. Para enviar esse comando, o aplicativo usa a mensagem WM \_ IME \_ CONTROL com as configurações de parâmetro mostradas abaixo.
ms.assetid: 7a2f9958-4a4e-462a-9737-e7796fd90216
title: IMC_SETCANDIDATEPOS comando (Imm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fbce21cac53eecf3ad5b99cc7dbe5cf5b52304ed25869a5c3f6ae729ac9d016
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120107266"
---
# <a name="imc_setcandidatepos-command"></a>Comando IMC \_ SETCANDIDATEPOS

Instrui uma janela do IME a definir a posição da janela candidatos. Para enviar esse comando, o aplicativo usa a mensagem [**WM \_ IME \_ CONTROL**](wm-ime-control.md) com as configurações de parâmetro mostradas abaixo.


```C++
LRESULT IMC_SETCANDIDATEPOS
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*Wparam*
</dt> <dd>

Definido como IMC \_ SETCANDIDATEPOS.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*Lparam*
</dt> <dd>

Ponteiro para uma [**estrutura CANDIDATEFORM**](/windows/win32/api/imm/ns-imm-candidateform) que contém a coordenada x e a coordenada y para a janela candidatos. O aplicativo deve definir o **membro dwIndex** dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna 0 se for bem-sucedido ou um valor diferente de zero, caso contrário.

## <a name="remarks"></a>Comentários

Esse comando destina-se a aplicativos que exibem caracteres de composição por conta própria, mas usam a janela IME para exibir candidatos.

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
</dt> <dt>

[**CONTROLE \_ WM IME \_**](wm-ime-control.md)
</dt> </dl>

 

 




