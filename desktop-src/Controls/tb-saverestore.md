---
title: Mensagem de TB_SAVERESTORE (commctrl. h)
description: Envie esta mensagem para iniciar o salvamento ou a restauração de um estado da barra de ferramentas.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- Controles de TB_SAVERESTORE de mensagens do Windows
topic_type:
- apiref
api_name:
- TB_SAVERESTORE
- TB_SAVERESTOREA
- TB_SAVERESTOREW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e87e4ddbed87e81a88c8711c9931dcf95cf9e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824151"
---
# <a name="tb_saverestore-message"></a>TB de \_ mensagem SAVERESTORE

Envie esta mensagem para iniciar o salvamento ou a restauração de um estado da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Sinalizador de salvar ou restaurar. Se esse parâmetro for **true**, as informações serão salvas. Se for **false**, as informações serão restauradas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) que especifica a chave do registro, a subchave e o nome do valor das informações de estado da barra de ferramentas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Para a versão 4,72 e anterior, para usar essa mensagem para salvar ou restaurar uma barra de ferramentas, a janela pai do controle Toolbar deve implementar um manipulador para o código de notificação [tbn \_ GETBUTTONINFO](tbn-getbuttoninfo.md) . A barra de ferramentas emite essa notificação para recuperar informações sobre cada botão conforme ele é restaurado.

A versão 5,80 inclui uma nova opção salvar/restaurar. No início do processo e, como cada botão é salvo ou restaurado, seu aplicativo receberá uma notificação [tbn \_ Save](tbn-save.md) ou [tbn \_ Restore](tbn-restore.md) . Para usar essa opção, você deve implementar manipuladores de notificação para fornecer ao shell as informações de bitmap e estado necessárias para salvar ou restaurar com êxito o estado da barra de ferramentas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ SAVERESTOREW** (Unicode) e **TB \_ SAVERESTOREA** (ANSI)<br/>             |



 

 





