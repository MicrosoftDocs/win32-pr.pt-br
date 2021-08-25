---
title: Mensagem de BCM_GETNOTELENGTH (commctrl. h)
description: Obtém o comprimento do texto da nota que pode ser exibido na descrição de um botão de link de comando. Envie essa mensagem explicitamente ou usando o botão \_ GetNoteLength macro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- controles de Windows de mensagem de BCM_GETNOTELENGTH
topic_type:
- apiref
api_name:
- BCM_GETNOTELENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 385cb5d7694818a0e0e03ab74bcc31b76d13f5d304c7415b1f70a0fd43e1b31b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921656"
---
# <a name="bcm_getnotelength-message"></a>\_Mensagem GETNOTELENGTH do BCM

Obtém o comprimento do texto da nota que pode ser exibido na descrição de um botão de link de comando. Envie essa mensagem explicitamente ou usando o [**botão \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna o comprimento do texto da nota em **WCHARs**, não incluindo nenhum **nulo** de término ou zero se não houver texto de nota.

## <a name="remarks"></a>Comentários

Começando com o comctl32 DLL versão 6, 1, os botões de link de comando podem ter uma observação. Para obter informações sobre versões de DLL, consulte [versões de controle comuns](common-control-versions.md).

A **mensagem \_ GETNOTELENGTH do BCM** funciona apenas com os estilos de botão [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[Estilos de botão](button-styles.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Tipos de botão](button-types-and-styles.md)
</dt> </dl>

 

 





