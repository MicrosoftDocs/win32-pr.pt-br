---
title: TB_SAVERESTORE mensagem (Commctrl.h)
description: Envie esta mensagem para iniciar a salvação ou a restauração de um estado da barra de ferramentas.
ms.assetid: 59f51d07-cd08-4d6f-9d19-614064ba6f20
keywords:
- TB_SAVERESTORE controles de Windows mensagem
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
ms.openlocfilehash: 94d04c16fda40bf66736431a684398eddf313529c669cc6db9ec49fbaad4f6f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168016"
---
# <a name="tb_saverestore-message"></a>Mensagem \_ SAVERESTORE de TB

Envie esta mensagem para iniciar a salvação ou a restauração de um estado da barra de ferramentas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Salvar ou restaurar sinalizador. Se esse parâmetro for **TRUE,** as informações são salvas. Se for **FALSE,** as informações são restauradas.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura TBSAVEPARAMS**](/windows/win32/api/commctrl/ns-commctrl-tbsaveparamsa) que especifica a chave do Registro, a subkey e o nome do valor para as informações de estado da barra de ferramentas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Para a versão 4.72 e anteriores, para usar essa mensagem para salvar ou restaurar uma barra de ferramentas, a janela pai do controle de barra de ferramentas deve implementar um manipulador para o código de notificação [ \_ TBN GETBUTTONINFO.](tbn-getbuttoninfo.md) A barra de ferramentas emite essa notificação para recuperar informações sobre cada botão conforme ele é restaurado.

A versão 5.80 inclui uma nova opção de salvar/restaurar. No início do processo e conforme cada botão é salvo ou restaurado, seu aplicativo receberá uma notificação [TBN \_ SAVE](tbn-save.md) ou [TBN \_ RESTORE.](tbn-restore.md) Para usar essa opção, você deve implementar manipuladores de notificação para fornecer ao Shell as informações de bitmap e estado necessárias para salvar ou restaurar com êxito o estado da barra de ferramentas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TB \_ SAVERESTOREW** (Unicode) e **TB \_ SAVERESTOREA** (ANSI)<br/>             |



 

 





