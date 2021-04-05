---
title: Mensagem de BCM_SETIMAGELIST (commctrl. h)
description: Atribui uma lista de imagens a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetImageList do botão.
ms.assetid: 805d2d9b-3e8f-4323-abaf-0dd5765cd740
keywords:
- Controles de BCM_SETIMAGELIST de mensagens do Windows
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
ms.openlocfilehash: c9bdf29735958f3c40af544bca4b946458df8431
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009270"
---
# <a name="bcm_setimagelist-message"></a>Mensagem do BCM \_ SETimagelist

Atribui uma lista de imagens a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetImageList do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**botão \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que contém informações da lista de imagens.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

A lista de imagens referenciada no membro **himl** da estrutura de [**botão \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) deve conter uma única imagem a ser usada para todos os Estados ou imagens individuais para cada Estado. Os Estados a seguir são definidos em vssym32. h.

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

Observe que o PBS \_ STYLUSHOT é usado somente em computadores tablet.

Cada valor é um índice para a imagem apropriada na lista de imagens. Se apenas uma imagem estiver presente, ela será usada para todos os Estados. Se a lista de imagens contiver mais de uma imagem, cada índice corresponderá a um estado do botão. Se uma imagem não for fornecida para cada Estado, nada será desenhado para esses Estados sem imagens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





