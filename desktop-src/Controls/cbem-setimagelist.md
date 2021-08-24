---
title: CBEM_SETIMAGELIST mensagem (Commctrl.h)
description: Define uma lista de imagens para um controle ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- CBEM_SETIMAGELIST controles de Windows mensagem
topic_type:
- apiref
api_name:
- CBEM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd83336d27bf8e47900554a6f3c36d2d767e5e8ddd4b8680b50050d87da79bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119699256"
---
# <a name="cbem_setimagelist-message"></a>Mensagem CBEM \_ SETIMAGELIST

Define uma lista de imagens para um controle ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para a lista de imagens a ser definida para o controle .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o alça para a lista de imagens associada anteriormente ao controle ou retorna **NULL** se nenhuma lista de imagens foi definida anteriormente.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> A altura das imagens na lista de imagens pode alterar os requisitos de tamanho do controle ComboBoxEx. É recomendável que você reesize o controle depois de enviar essa mensagem para garantir que ele seja exibido corretamente.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





