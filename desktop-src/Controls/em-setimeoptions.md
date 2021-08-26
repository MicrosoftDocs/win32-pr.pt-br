---
title: EM_SETIMEOPTIONS mensagem (Richedit.h)
description: Define as opções do IME (Editor de Método de Entrada).
ms.assetid: 8a72ee1c-f6b8-44eb-b8df-57cd834db326
keywords:
- EM_SETIMEOPTIONS controles de Windows mensagem
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
ms.openlocfilehash: 83ffae9586c3ee05f951672f0927c4f10ad2115684643af8418062bb7724c7b1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048386"
---
# <a name="em_setimeoptions-message"></a>Mensagem EM \_ SETIMEOPTIONS

Define as opções do IME (Editor de Método de Entrada).

> [!Note]  
> Essa mensagem só tem suporte em versões de idioma asiático do Microsoft Rich Edit 1.0. Não há suporte para ele em nenhuma versão posterior.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um dos valores a seguir.



| Valor                                                                                                                                             | Significado                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="ECOOP_SET"></span><span id="ecoop_set"></span><dl> <dt>**ECOOP \_ SET**</dt> </dl> | Define as opções para as especificadas por *lParam*.<br/>                             |
| <span id="ECOOP_OR"></span><span id="ecoop_or"></span><dl> <dt>**ECOOP \_ OU**</dt> </dl>    | Combina as opções especificadas com as opções atuais.<br/>                     |
| <span id="ECOOP_AND"></span><span id="ecoop_and"></span><dl> <dt>**ECOOP \_ E**</dt> </dl> | Retém apenas as opções atuais que também são especificadas por *lParam*.<br/>      |
| <span id="ECOOP_XOR"></span><span id="ecoop_xor"></span><dl> <dt>**ECOOP \_ XOR**</dt> </dl> | OR logicamente exclusivo as opções atuais com as especificadas por *lParam.*<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Especifica um dos valores a seguir.



| Valor                                                                                                                                                                                 | Significado                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IMF_CLOSESTATUSWINDOW"></span><span id="imf_closestatuswindow"></span><dl> <dt>**IMF \_ CLOSESTATUSWINDOW**</dt> </dl> | Fecha a janela de status do IME quando o controle recebe o foco de entrada.<br/>                                                                                                               |
| <span id="IMF_FORCEACTIVE"></span><span id="imf_forceactive"></span><dl> <dt>**IMF \_ FORCEACTIVE**</dt> </dl>                   | Ativa o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                          |
| <span id="IMF_FORCEDISABLE"></span><span id="imf_forcedisable"></span><dl> <dt>**IMF \_ FORCEDISABLE**</dt> </dl>                | Desabilita o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                           |
| <span id="IMF_FORCEENABLE"></span><span id="imf_forceenable"></span><dl> <dt>**IMF \_ FORCEENABLE**</dt> </dl>                   | Habilita o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                            |
| <span id="IMF_FORCEINACTIVE"></span><span id="imf_forceinactive"></span><dl> <dt>**IMF \_ FORCEINACTIVE**</dt> </dl>             | Inativa o IME quando o controle recebe o foco de entrada.<br/>                                                                                                                        |
| <span id="IMF_FORCENONE"></span><span id="imf_forcenone"></span><dl> <dt>**IMF \_ FORCENONE**</dt> </dl>                         | Desabilita a manipulação do IME.<br/>                                                                                                                                                                |
| <span id="IMF_FORCEREMEMBER"></span><span id="imf_forceremember"></span><dl> <dt>**IMF \_ FORCEREMEMBER**</dt> </dl>             | Restaura o status do IME anterior quando o controle recebe o foco de entrada.<br/>                                                                                                           |
| <span id="IMF_MULTIPLEEDIT"></span><span id="imf_multipleedit"></span><dl> <dt>**MULTIPLEEDIT do IMF \_**</dt> </dl>                | Especifica que a cadeia de caracteres de composição não será cancelada nem determinada pelas alterações de foco. Isso permite que um aplicativo tenha cadeias de caracteres de composição separadas em cada controle de edição rico.<br/> |
| <span id="IMF_VERTICAL"></span><span id="imf_vertical"></span><dl> <dt>**IMF \_ VERTICAL**</dt> </dl>                            | Observação usada na Edição 2.0 e posteriores. <br/>                                                                                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a operação for bem-sucedida, o valor de retorno será um valor não zero.

Se a operação falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**EM \_ GETIMEOPTIONS**](em-getimeoptions.md)
</dt> </dl>

 

 





