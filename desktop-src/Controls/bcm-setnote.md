---
title: Mensagem de BCM_SETNOTE (commctrl. h)
description: Define o texto da observação associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a \_ macro setnote do botão.
ms.assetid: c167072a-8207-4744-ac66-247141d726ab
keywords:
- Controles de BCM_SETNOTE de mensagens do Windows
topic_type:
- apiref
api_name:
- BCM_SETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f544a7fb9dd89346cc2aa9725d36122746a8f608
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918437"
---
# <a name="bcm_setnote-message"></a>Mensagem do BCM \_ SETnote

Define o texto da observação associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ setnote do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma cadeia de caracteres **WCHAR** terminada em nulo que contém a observação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Começando com o comctl32 DLL versão 6, 1, os botões de link de comando podem ter uma observação.

A mensagem de **\_ Observação do BCM** funciona apenas com os estilos de botão [**BS \_ COMMANDLINK**](button-styles.md) e [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

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

 

 





