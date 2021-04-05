---
title: Mensagem de CBEM_SETIMAGELIST (commctrl. h)
description: Define uma lista de imagens para um controle ComboBoxEx.
ms.assetid: a4a8ed61-a532-4cf8-8291-c157ab0e7f31
keywords:
- Controles de CBEM_SETIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: 33816abe36e2d1e1593e6365061a500d072c155b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919090"
---
# <a name="cbem_setimagelist-message"></a>\_Mensagem CBEM SETimagelist

Define uma lista de imagens para um controle ComboBoxEx.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para a lista de imagens a ser definido para o controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o identificador para a lista de imagens associada anteriormente ao controle ou retorna **NULL** se nenhuma lista de imagens tiver sido definida anteriormente.

## <a name="remarks"></a>Comentários

> [!IMPORTANT]
> A altura das imagens na sua lista de imagens pode alterar os requisitos de tamanho do controle ComboBoxEx. É recomendável que você redimensione o controle depois de enviar essa mensagem para garantir que ela seja exibida corretamente.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





