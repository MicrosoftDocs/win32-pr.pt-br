---
title: Mensagem de TB_SETHOTIMAGELIST (commctrl. h)
description: Define a lista de imagens que o controle Toolbar usará para exibir botões quentes.
ms.assetid: 3c29cdde-bd57-4194-984f-220dbf963733
keywords:
- Controles de TB_SETHOTIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: f9a84c3420eaf64710ac1f8764db20d2cfc88b7b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918857"
---
# <a name="tb_sethotimagelist-message"></a>TB de \_ mensagem SETHOTIMAGELIST

Define a lista de imagens que o controle Toolbar usará para exibir botões quentes.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a lista de imagens que será definida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens usada anteriormente para exibir botões quentes ou **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.

## <a name="remarks"></a>Comentários

Um botão fica quente quando o cursor está sobre ele. Os controles da barra de ferramentas devem ter o estilo de [**\_ lista**](toolbar-control-and-button-styles.md) [**TBSTYLE \_ simples**](toolbar-control-and-button-styles.md) ou TBSTYLE para ter itens quentes.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





