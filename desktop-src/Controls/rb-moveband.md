---
title: Mensagem de RB_MOVEBAND (commctrl. h)
description: Move uma banda de um índice para outro.
ms.assetid: bb5b45de-957e-46fb-b59a-18b55b69c395
keywords:
- Controles de RB_MOVEBAND de mensagens do Windows
topic_type:
- apiref
api_name:
- RB_MOVEBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146103c4c3d70fc0514729a00eac152c4847b85c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454688"
---
# <a name="rb_moveband-message"></a>\_Mensagem MOVEBAND RB

Move uma banda de um índice para outro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero da banda a ser movida.

</dd> <dt>

*lParam* 
</dt> <dd>

Índice de base zero da nova posição de banda.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornará zero se for bem-sucedido ou nenhum outro.

## <a name="remarks"></a>Comentários

Provavelmente, essa mensagem alterará o índice de outras bandas no controle rebar. Se uma banda for movida do índice 6 para o índice 0, todas as faixas entre o terão seu índice incrementado em um.

*lParam* nunca deve ser maior que o número de faixas menos um. O número de faixas pode ser obtido com a [**mensagem \_ GETBANDCOUNT RB**](rb-getbandcount.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





