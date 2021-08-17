---
description: Notifica um aplicativo quando o IME selecionado precisa da cadeia de caracteres convertida do aplicativo. O aplicativo recebe esse comando por meio da \_ mensagem de solicitação do IME do WM \_ com parâmetros definidos, conforme mostrado abaixo.
ms.assetid: 1a007bed-15e5-4400-9d2f-32e37e1765d2
title: IMR_DOCUMENTFEED código de notificação (IMM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbef4c83d35fa02e2c879d76b9520df6d01588c07cb725b13e66888e9dd27722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118948773"
---
# <a name="imr_documentfeed-notification-code"></a>Código de notificação do IMR \_ DOCUMENTFEED

Notifica um aplicativo quando o IME selecionado precisa da cadeia de caracteres convertida do aplicativo. O aplicativo recebe esse comando por meio da mensagem de [**\_ \_ solicitação do IME do WM**](wm-ime-request.md) com parâmetros definidos, conforme mostrado abaixo.


```C++
LRESULT IMR_DOCUMENTFEED
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*
</dt> <dd>

Defina como IMR \_ DOCUMENTFEED.

</dd> <dt>

<span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*
</dt> <dd>

O ponteiro para um buffer que contém a estrutura [**REconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring) .

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna a estrutura da cadeia de caracteres de reconversão atual. Se *lParam* for definido como **NULL**, o aplicativo retornará o tamanho necessário para que o buffer mantenha a estrutura. O comando retornará 0 se não tiver sucesso.

## <a name="remarks"></a>Comentários

O IME armazena em cache as cadeias de caracteres convertidas para maior precisão de conversão. Uma limitação de cache do IME é que ele perde a cadeia de caracteres convertida nas seguintes circunstâncias:

-   A posição do cursor para o aplicativo é movida por uma chave, por exemplo, uma tecla de cursor.
-   A posição do cursor para o aplicativo é movida pelo mouse.
-   Um novo documento é aberto.

Com o comando **IMR \_ DOCUMENTFEED** , o IME pode atualizar suas cadeias de caracteres em cache a qualquer momento. O uso desse comando melhora a precisão da conversão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Imm. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de métodos de entrada](input-method-manager.md)
</dt> <dt>

[Comandos do Gerenciador de métodos de entrada](input-method-manager-commands.md)
</dt> <dt>

[**Reconverterstring**](/windows/win32/api/imm/ns-imm-reconvertstring)
</dt> <dt>

[**\_solicitação do IME do WM \_**](wm-ime-request.md)
</dt> </dl>

 

 




