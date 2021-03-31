---
title: Mensagem de EM_SETIMEOPTIONS (RichEdit. h)
description: Define as opções do IME (editor de método de entrada).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- Controles de EM_SETIMEOPTIONS de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETIMEOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59be3148bd00abd998af200368f2ed77ad3ff911
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824527"
---
# <a name="em_setimeoptions-message"></a>\_Mensagem em SETIMEOPTIONS

Define as opções do IME (editor de método de entrada).

> [!Note]  
> Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Não há suporte para ele em nenhuma versão posterior.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um dos valores a seguir.



| Valor                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**conjunto de ECOOP \_**</dt> </dl> | Define as opções para as especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ ou**</dt> </dl>    | Combina as opções especificadas com as opções atuais.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ e**</dt> </dl> | Retém somente as opções atuais que também são especificadas por *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**\_XOR ECOOP**</dt> </dl> | Logicamente exclusivas ou as opções atuais com as especificadas por *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                 | Significado                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**CLOSESTATUSWINDOW do IMF \_**</dt> </dl> | Fecha a janela de status do IME quando o controle recebe o foco de entrada.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**FORCEACTIVE do IMF \_**</dt> </dl>                   | Ativa o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**FORCEDISABLE do IMF \_**</dt> </dl>                | Desabilita o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**FORCEENABLE do IMF \_**</dt> </dl>                   | Habilita o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**FORCEINACTIVE do IMF \_**</dt> </dl>             | Desativa o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**FORCENONE do IMF \_**</dt> </dl>                         | Desabilita a manipulação do IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**FORCEREMEMBER do IMF \_**</dt> </dl>             | Restaura o status anterior do IME quando o controle recebe o foco de entrada.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**MULTIPLEEDIT do IMF \_**</dt> </dl>                | Especifica que a cadeia de caracteres de composição não será cancelada ou determinada pelas alterações de foco. Isso permite que um aplicativo tenha cadeias de caracteres de composição separadas em cada controle de edição rico.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**VERTICAL do IMF \_**</dt> </dl>                            | Observação usada no rich edit 2,0 e posterior. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com sucesso, o valor de retorno será um valor diferente de zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**em \_ GETIMEOPTIONS**](em-getimeoptions.md)
</dt> </dl>

 

 





