---
title: Mensagem de BCM_GETNOTELENGTH (commctrl. h)
description: Obtém o comprimento do texto da nota que pode ser exibido na descrição de um botão de link de comando. Envie essa mensagem explicitamente ou usando o botão \_ GetNoteLength macro.
ms.assetid: 62385485-b553-47e9-9f15-696cc4694752
keywords:
- Controles de BCM_GETNOTELENGTH de mensagens do Windows
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
ms.openlocfilehash: 1b33c5245778481033bd97326c3d66a40bf03210
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009271"
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

## <a name="return-value"></a>Retornar valor

Retorna o comprimento do texto da nota em **WCHARs**, não incluindo nenhum **nulo** de término ou zero se não houver texto de nota.

## <a name="remarks"></a>Comentários

Começando com o comctl32 DLL versão 6, 1, os botões de link de comando podem ter uma observação. Para obter informações sobre versões de DLL, consulte [versões de controle comuns](common-control-versions.md).

A **mensagem \_ GETNOTELENGTH do BCM** funciona apenas com os estilos de botão [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



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

 

 





