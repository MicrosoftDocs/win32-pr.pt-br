---
title: Mensagem de TB_GETIMAGELIST (commctrl. h)
description: Recupera a lista de imagens que um controle Toolbar usa para exibir botões em seu estado padrão. Um controle Toolbar usa essa lista de imagens para exibir botões quando eles não estão ativos ou desabilitados.
ms.assetid: 21edde99-019b-495c-a38b-4d686e124f8e
keywords:
- Controles de TB_GETIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a56b8b847bd212e703d3b512b255cf1693abf7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644343"
---
# <a name="tb_getimagelist-message"></a>Mensagem de TB \_ GETimagelist

Recupera a lista de imagens que um controle Toolbar usa para exibir botões em seu estado padrão. Um controle Toolbar usa essa lista de imagens para exibir botões quando eles não estão ativos ou desabilitados.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens, ou **NULL** se nenhuma lista de imagens for definida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





