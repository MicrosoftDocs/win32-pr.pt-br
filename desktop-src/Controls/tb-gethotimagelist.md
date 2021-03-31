---
title: Mensagem de TB_GETHOTIMAGELIST (commctrl. h)
description: Recupera a lista de imagens que um controle Toolbar usa para exibir botões de atalho.
ms.assetid: 63054449-2768-459c-933c-781d31bdcc15
keywords:
- Controles de TB_GETHOTIMAGELIST de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_GETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e19c1f3989b0d749a9c663d00b5fb7b54d67fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085672"
---
# <a name="tb_gethotimagelist-message"></a>TB de \_ mensagem GETHOTIMAGELIST

Recupera a lista de imagens que um controle Toolbar usa para exibir botões de atalho.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens que o controle usa para exibir botões quentes ou **NULL** se nenhuma lista de imagens ativas estiver definida.

## <a name="remarks"></a>Comentários

Um botão fica quente quando o cursor está sobre ele. Os controles da barra de ferramentas devem ter o estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ simples**](toolbar-control-and-button-styles.md) ou TBSTYLE para ter itens quentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





