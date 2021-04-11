---
title: Mensagem de HDM_LAYOUT (commctrl. h)
description: Recupera informações usadas para definir o tamanho e a posição do controle de cabeçalho dentro do retângulo de destino da janela pai. Você pode enviar essa mensagem explicitamente ou usar a macro de layout de cabeçalho \_ .
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- Controles de HDM_LAYOUT de mensagens do Windows
topic_type:
- apiref
api_name:
- HDM_LAYOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a70fc46dee52f52862136dbe583db9f6d7a0e13e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009398"
---
# <a name="hdm_layout-message"></a>\_Mensagem de layout HDM

Recupera informações usadas para definir o tamanho e a posição do controle de cabeçalho dentro do retângulo de destino da janela pai. Você pode enviar essa mensagem explicitamente ou usar a macro de [**\_ layout de cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**HDLAYOUT**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) . O membro **prc** especifica as coordenadas de um retângulo e o membro **pwpos** recebe o tamanho e a posição do controle de cabeçalho dentro do retângulo.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

O membro **pwpos** da estrutura *lParam* recebe valores de tamanho e posição apropriados para posicionar o controle ao longo da parte superior do retângulo especificado. O valor de altura é a soma das alturas das bordas horizontais do controle e a altura média de caracteres na fonte selecionada atualmente no contexto do dispositivo do controle.

Para usar **o \_ layout HDM** para definir o tamanho inicial e a posição de um controle de cabeçalho, defina o estado de visibilidade inicial do controle para que ele fique oculto. Depois de enviar o **\_ layout HDM** para recuperar os valores de tamanho e posição, use a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para definir o novo tamanho, a posição e o estado de visibilidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

