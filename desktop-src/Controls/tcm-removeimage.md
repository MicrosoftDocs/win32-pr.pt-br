---
title: Mensagem de TCM_REMOVEIMAGE (commctrl. h)
description: Remove uma imagem da lista de imagens de um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- controles de Windows de mensagem de TCM_REMOVEIMAGE
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d2305386f948e1dc4522124708b31ca360203ba9723241c99262fcdb5d2b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104835"
---
# <a name="tcm_removeimage-message"></a>\_Mensagem REMOVEIMAGE de TCM

Remove uma imagem da lista de imagens de um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro [**TabCtrl \_ RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da imagem a ser removida.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O controle guia atualiza o índice de imagem de cada guia, de modo que cada guia permanece associada à mesma imagem que antes. Se uma guia estiver usando a imagem que está sendo removida, a guia será definida como sem imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





