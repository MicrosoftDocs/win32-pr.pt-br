---
title: Mensagem de EM_SETCTFMODEBIAS (RichEdit. h)
description: Define o ajuste do modo TSF (estrutura de serviços de texto) para um controle de edição rico.
ms.assetid: 17e3aac8-2ba8-4c06-bfd6-e118cfb82529
keywords:
- controles de Windows de mensagem de EM_SETCTFMODEBIAS
topic_type:
- apiref
api_name:
- EM_SETCTFMODEBIAS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd6aa0f10b07092d9637d9e5a993848671ab6aa7e7eb610eca48c3df353c4a0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019504"
---
# <a name="em_setctfmodebias-message"></a>\_Mensagem em SETCTFMODEBIAS

Define o ajuste do modo TSF (estrutura de serviços de texto) para um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor de ajuste do modo. Isso pode ser um dos valores a seguir.



| Valor                                                                                                                                                                                                                     | Significado                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="CTFMODEBIAS_DEFAULT"></span><span id="ctfmodebias_default"></span><dl> <dt>**CTFMODEBIAS \_ padrão**</dt> </dl>                                           | Não há nenhuma diferença de modo.<br/>                             |
| <span id="CTFMODEBIAS_FILENAME"></span><span id="ctfmodebias_filename"></span><dl> <dt>**\_nome de arquivo CTFMODEBIAS**</dt> </dl>                                        | A tendência é de um nome de arquivo.<br/>                         |
| <span id="CTFMODEBIAS_NAME"></span><span id="ctfmodebias_name"></span><dl> <dt>**nome do CTFMODEBIAS \_**</dt> </dl>                                                    | A tendência é de um nome.<br/>                             |
| <span id="CTFMODEBIAS_READING"></span><span id="ctfmodebias_reading"></span><dl> <dt>**CTFMODEBIAS \_ leitura**</dt> </dl>                                           | A tendência é a leitura.<br/>                        |
| <span id="CTFMODEBIAS_DATETIME"></span><span id="ctfmodebias_datetime"></span><dl> <dt>**CTFMODEBIAS \_ DateTime**</dt> </dl>                                        | A tendência é de uma data ou hora.<br/>                     |
| <span id="CTFMODEBIAS_CONVERSATION"></span><span id="ctfmodebias_conversation"></span><dl> <dt>**conversa do CTFMODEBIAS \_**</dt> </dl>                            | A tendência é de uma conversa.<br/>                     |
| <span id="CTFMODEBIAS_NUMERIC"></span><span id="ctfmodebias_numeric"></span><dl> <dt>**CTFMODEBIAS \_ numeric**</dt> </dl>                                           | A tendência é de um número.<br/>                           |
| <span id="CTFMODEBIAS_HIRAGANA"></span><span id="ctfmodebias_hiragana"></span><dl> <dt>**CTFMODEBIAS \_ Hiragana**</dt> </dl>                                        | A tendência é a cadeias de caracteres hiragana.<br/>                   |
| <span id="CTFMODEBIAS_KATAKANA"></span><span id="ctfmodebias_katakana"></span><dl> <dt>**CTFMODEBIAS \_ katakana**</dt> </dl>                                        | A tendência é a cadeias de caracteres de katakana.<br/>                   |
| <span id="CTFMODEBIAS_HANGUL"></span><span id="ctfmodebias_hangul"></span><dl> <dt>**CTFMODEBIAS \_ Hangul**</dt> </dl>                                              | A tendência é de caracteres Hangul.<br/>                  |
| <span id="CTFMODEBIAS_HALFWIDTHKATAKANA"></span><span id="ctfmodebias_halfwidthkatakana"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHKATAKANA**</dt> </dl>             | A tendência é a cadeias de caracteres Katakana de meia largura.<br/>        |
| <span id="CTFMODEBIAS_FULLWIDTHALPHANUMERIC"></span><span id="ctfmodebias_fullwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ FULLWIDTHALPHANUMERIC**</dt> </dl> | A tendência é de caracteres alfanuméricos de largura total.<br/> |
| <span id="CTFMODEBIAS_HALFWIDTHALPHANUMERIC"></span><span id="ctfmodebias_halfwidthalphanumeric"></span><dl> <dt>**CTFMODEBIAS \_ HALFWIDTHALPHANUMERIC**</dt> </dl> | A tendência é a caracteres alfanuméricos de meia largura.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, o valor de retorno será o novo valor de tendência do modo TSF. Se não for bem-sucedida, o valor de retorno será o antigo valor de tendência do modo TSF.

## <a name="remarks"></a>Comentários

Quando um aplicativo de edição rica da Microsoft usa o TSF, ele pode selecionar a tendência do modo TSF. Essa mensagem define os critérios pelos quais uma opção alternativa aparece na parte superior da lista para seleção.

Para definir a tendência de modo para o IME (editor de método de entrada), use em [**\_ SETIMEMODEBIAS**](em-setimemodebias.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows XP somente com \[ aplicativos da área de trabalho do SP1\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**em \_ GETCTFMODEBIAS**](em-getctfmodebias.md)
</dt> <dt>

[**em \_ SETIMEMODEBIAS**](em-setimemodebias.md)
</dt> </dl>

 

 





