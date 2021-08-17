---
title: RB_GETBANDINFO mensagem (Commctrl.h)
description: Recupera informações sobre uma faixa especificada em um controle de barra rebar.
ms.assetid: c2a76c91-7d44-4278-823d-bd263520e7a8
keywords:
- RB_GETBANDINFO controles de Windows mensagem
topic_type:
- apiref
api_name:
- RB_GETBANDINFO
- RB_GETBANDINFOA
- RB_GETBANDINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b0ae509699c23ad24b9b97451178f4711ab52176a9c15aeef757bab85c861c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118409437"
---
# <a name="rb_getbandinfo-message"></a>Mensagem GETBANDINFO do RB \_

Recupera informações sobre uma faixa especificada em um controle de barra rebar.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice baseado em zero da banda para a qual as informações serão recuperadas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) que receberá as informações de banda solicitadas. Antes de enviar essa mensagem, você deve definir o membro **cbSize** dessa estrutura para o tamanho da estrutura **REBARBANDINFO** e definir o membro **fMask** para os itens que você deseja recuperar. Além disso, você deve definir o membro **cch** da estrutura **REBARBANDINFO** para o tamanho do buffer **lpText** quando RBBIM \_ TEXT for especificado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará diferente de zero se for bem-sucedido ou zero caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **RB \_ GETBANDINFOW** (Unicode) e **RB \_ GETBANDINFOA** (ANSI)<br/>             |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RB \_ SETBANDINFO**](rb-setbandinfo.md)
</dt> </dl>

 

 





