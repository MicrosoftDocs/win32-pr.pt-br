---
title: Mensagem de TCM_REMOVEIMAGE (commctrl. h)
description: Remove uma imagem da lista de imagens de um controle guia. Você pode enviar essa mensagem explicitamente ou usando a macro TabCtrl \_ RemoveImage.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Controles de TCM_REMOVEIMAGE de mensagens do Windows
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
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756022"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O controle guia atualiza o índice de imagem de cada guia, de modo que cada guia permanece associada à mesma imagem que antes. Se uma guia estiver usando a imagem que está sendo removida, a guia será definida como sem imagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





