---
title: BCM_SETIMAGELIST mensagem (Commctrl.h)
description: Atribui uma lista de imagens a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetImageList do botão.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- BCM_SETIMAGELIST controles de Windows mensagem
topic_type:
- apiref
api_name:
- BCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f5c88020bb139c358b17386b003bfb9de9cfcd4e769b9262ed90e23f3f95e75
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921556"
---
# <a name="bcm_setimagelist-message"></a>Mensagem BCM \_ SETIMAGELIST

Atribui uma lista de imagens a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ SetImageList do**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) botão.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**\_ BUTTON IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contém informações de lista de imagens.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, ela retornará **TRUE.** Caso contrário, **retornará FALSE.**

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6.0. Para obter mais informações sobre manifestos, consulte [Habilitando estilos visuais.](cookbook-overview.md)

 

A lista de imagens referenciada no membro **himl** da estrutura [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) deve conter uma única imagem a ser usada para todos os estados ou imagens individuais para cada estado. Os estados a seguir são definidos em vssym32.h.

``` syntax
enum PUSHBUTTONSTATES {
    PBS_NORMAL = 1,
    PBS_HOT = 2,
    PBS_PRESSED = 3,
    PBS_DISABLED = 4,
    PBS_DEFAULTED = 5,
    PBS_STYLUSHOT = 6,
};
```

Observe que PBS \_ STYLUSHOT é usado somente em computadores tablets.

Cada valor é um índice para a imagem apropriada na lista de imagens. Se apenas uma imagem estiver presente, ela será usada para todos os estados. Se a lista de imagens contiver mais de uma imagem, cada índice corresponderá a um estado do botão. Se uma imagem não for fornecida para cada estado, nada será desenhado para esses estados sem imagens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





