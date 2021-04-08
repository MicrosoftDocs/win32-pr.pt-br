---
title: Mensagem de EM_SETWORDWRAPMODE (RichEdit. h)
description: Define as opções de quebra automática de palavras e quebra de palavras para um controle de edição rico.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- Controles de EM_SETWORDWRAPMODE de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009481"
---
# <a name="em_setwordwrapmode-message"></a>\_Mensagem em SETwordwrapmode

Define as opções de quebra automática de palavras e quebra de palavras para um controle de edição rico.

> [!Note]  
> Esta mensagem tem suporte apenas em versões de idioma asiático do Microsoft Rich Edit 1,0. Não há suporte para ele em nenhuma versão posterior.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica um ou mais dos valores a seguir.



| Valor                                                                                                                                                         | Significado                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | Permite operações de quebra automática de palavras específicas do idioma, como kinsoku em Japonês. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ justificação**</dt> </dl> | Habilita as operações de separação de palavras em inglês em Japonês e chinês. Habilita a operação de quebra de palavras hangeul.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**estouro de WBF \_**</dt> </dl>    | Reconhece Pontuação de estouro. (Não tem suporte no momento.)<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ LEVEL1**</dt> </dl>          | Define a tabela de Pontuação de nível 1 como padrão.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF \_ LEVEL2**</dt> </dl>          | Define a tabela de Pontuação de nível 2 como o padrão.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ personalizado**</dt> </dl>          | Define a tabela de pontuação definida pelo aplicativo.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado; Ele deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem retorna as opções de quebra automática de texto e quebra de palavra atuais.

## <a name="remarks"></a>Comentários

Esta mensagem não deve ser enviada pelo procedimento de quebra de palavras definido pelo aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





