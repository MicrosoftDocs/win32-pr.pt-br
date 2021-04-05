---
title: Mensagem de TBM_SETLINESIZE (commctrl. h)
description: Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.
ms.assetid: 7fe3f9b8-2ddf-4460-882f-6be439f83daa
keywords:
- Controles de TBM_SETLINESIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- TBM_SETLINESIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec898ed09b20f15023ef04a399f5644df746e495
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918116"
---
# <a name="tbm_setlinesize-message"></a>TBM \_ SETlinhasize mensagem

Define o número de posições lógicas que o controle deslizante do TrackBar move em resposta à entrada do teclado das teclas de direção, como as chaves ou. As posições lógicas são os incrementos inteiros no intervalo de TrackBar de mínimo a máximo de posições do controle deslizante.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Novo tamanho da linha.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um valor de 32 bits que especifica o tamanho da linha anterior.

## <a name="remarks"></a>Comentários

A configuração padrão para o tamanho da linha é 1.

O TrackBar também envia uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) com os códigos de notificação da lista de TB \_ e TB \_ LINEDOWN para sua janela pai quando o usuário pressiona as teclas de direção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**TBM \_ GETlines**](tbm-getlinesize.md)
</dt> </dl>

 

 





