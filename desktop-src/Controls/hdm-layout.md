---
title: HDM_LAYOUT mensagem (Commctrl.h)
description: Recupera informações usadas para definir o tamanho e a posição do controle de cabeça dentro do retângulo de destino da janela pai. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Layout do Header.
ms.assetid: 0763e483-f01d-4739-8c61-1c52d1aad0b4
keywords:
- HDM_LAYOUT controles Windows mensagem
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
ms.openlocfilehash: ff4194ad5aa1847aa977bac1269a7ab88d36a571824387e07264713726135f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435926"
---
# <a name="hdm_layout-message"></a>Mensagem DE LAYOUT do HDM \_

Recupera informações usadas para definir o tamanho e a posição do controle de cabeça dentro do retângulo de destino da janela pai. Você pode enviar essa mensagem explicitamente ou usar a [**\_ macro Layout do Header.**](/windows/desktop/api/Commctrl/nf-commctrl-header_layout)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura HDLAYOUT.**](/windows/win32/api/commctrl/ns-commctrl-hdlayout) O **membro prc** especifica as coordenadas de um retângulo e o membro **pwpos** recebe o tamanho e a posição do controle de cabeça dentro do retângulo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **TRUE se** for bem-sucedido ou FALSE **caso** contrário.

## <a name="remarks"></a>Comentários

O **membro pwpos** da estrutura *lParam* recebe valores de tamanho e posição apropriados para posicionar o controle na parte superior do retângulo especificado. O valor de altura é a soma das alturas das bordas horizontais do controle e a altura média dos caracteres na fonte atualmente selecionada no contexto do dispositivo do controle.

Para usar **o \_ LAYOUT do HDM** para definir o tamanho inicial e a posição de um controle de cabeça, de definido o estado de visibilidade inicial do controle para que ele seja ocultado. Depois de **enviar o LAYOUT \_ do HDM** para recuperar os valores de tamanho e posição, use a função [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) para definir o novo tamanho, a posição e o estado de visibilidade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

