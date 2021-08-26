---
title: Mensagem de LVM_SETINFOTIP (commctrl. h)
description: Define o texto da dica de ferramenta em resposta atrasada à notificação de GETINFOTIP de LVN \_ .
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- controles de Windows de mensagem de LVM_SETINFOTIP
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef739535e399550911adfbe86d7376d3efeb77cd797ba807b24ee682d1f3fe3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919896"
---
# <a name="lvm_setinfotip-message"></a>\_Mensagem SETINFOTIP LVM

Define o texto da dica de ferramenta em resposta atrasada à notificação de [ \_ GETINFOTIP de LVN](lvn-getinfotip.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Ponteiro para uma estrutura <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> que contém as informações a serem definidas.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se o texto da dica de ferramenta for definido com êxito ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A mensagem **LVM \_ SETINFOTIP** permite que um aplicativo Calcule Infotips em segundo plano executando as seguintes etapas:

1.  Em resposta à notificação [LVN \_ GETINFOTIP](lvn-getinfotip.md) , defina o membro **pszText** da estrutura [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) como uma cadeia de caracteres vazia e retorne 0.
2.  Em segundo plano, COMPUTE o InfoTip.
3.  Depois de computar o InfoTip, envie a mensagem **LVM \_ SETINFOTIP** , definindo o membro **pszText** da estrutura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) para o InfoTip e os membros **iItem** e **iSubItem** para o item e o subitem ao qual a InfoTip se aplica.

O texto passado para a **mensagem \_ SETINFOTIP do LVM** aparece apenas se o item e o subitem descritos pela estrutura [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) ainda estiverem em um estado que exija um InfoTip

> [!Note]  
> Para usar essa mensagem, você deve fornecer um manifesto especificando Comclt32.dll versão 6,0. Para obter mais informações sobre manifestos, consulte [habilitando estilos visuais](cookbook-overview.md).

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





