---
title: Mensagem de BCM_GETIDEALSIZE (commctrl. h)
description: Obtém o tamanho do botão que melhor se adapta a seu texto e imagem, se uma lista de imagens estiver presente. Você pode enviar essa mensagem explicitamente ou usar o botão \_ GetIdealSize macro.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Controles de BCM_GETIDEALSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756240"
---
# <a name="bcm_getidealsize-message"></a>\_Mensagem GETIDEALSIZE do BCM

Obtém o tamanho do botão que melhor se adapta a seu texto e imagem, se uma lista de imagens estiver presente. Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura de [**tamanho**](/previous-versions//dd145106(v=vs.85)) que recebe o tamanho desejado do botão, incluindo a lista de texto e imagem, se presente. O aplicativo de chamada é responsável por alocar essa estrutura. Defina os membros **CX** e **CY** como zero para que a altura e a largura ideais sejam retornadas na estrutura de **tamanho** . Para especificar uma largura de botão, defina o membro **CX** para a largura de botão desejada. O sistema calculará a altura ideal para essa largura e a retornará no membro **CY** .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, retornará **true**. Caso contrário, retornará **false**.

## <a name="remarks"></a>Comentários

> [!Note]  
> Se nenhuma largura de botão especial for desejada, você deverá definir ambos os membros de [**tamanho**](/previous-versions//dd145106(v=vs.85)) como zero para calcular e retornar a altura e a largura ideais. Se o valor do membro **CX** for maior que zero, esse valor será considerado a largura do botão desejado e a altura ideal para essa largura será calculada e retornada no membro **CY** .

 

Essa mensagem é mais aplicável a supressãos. Quando enviado a um botão de pressão, a mensagem recupera o retângulo delimitador necessário para exibir o texto do Button. Além disso, se o botão de pressão tiver uma lista de imagens, o retângulo delimitador também será dimensionado para incluir a imagem do botão.

Quando enviado a um botão de qualquer outro tipo, o tamanho do retângulo da janela do controle é recuperado.

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

