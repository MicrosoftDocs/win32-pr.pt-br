---
title: TB_SETHOTIMAGELIST mensagem (Commctrl.h)
description: Define a lista de imagens que o controle da barra de ferramentas usará para exibir botões de acesso.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- TB_SETHOTIMAGELIST controles Windows mensagem
topic_type:
- apiref
api_name:
- TB_SETHOTIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12d07c66add48fa8022f7b8505bee377be184af3ed8195251b3a92b46d0ff58c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119318846"
---
# <a name="tb_sethotimagelist-message"></a>Mensagem \_ TBTBOTIMAGELIST

Define a lista de imagens que o controle da barra de ferramentas usará para exibir botões de acesso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a lista de imagens que será definida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens usada anteriormente para exibir botões a quente ou **NULL** se nenhuma lista de imagens foi definida anteriormente.

## <a name="remarks"></a>Comentários

Um botão fica quente quando o cursor está sobre ele. Os controles da barra de ferramentas devem ter o [**estilo TBSTYLE \_ FLAT**](toolbar-control-and-button-styles.md) ou [**TBSTYLE \_ LIST**](toolbar-control-and-button-styles.md) para ter itens ativos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





