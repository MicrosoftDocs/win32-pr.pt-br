---
title: Estilos de dica de ferramenta (CommCtrl. h)
description: Esta seção lista os estilos de controle usados com controles de dica de ferramenta.
ms.assetid: a6aeac71-6a69-4903-af78-0bfe1f83e632
topic_type:
- apiref
api_name:
- TTS_ALWAYSTIP
- TTS_BALLOON
- TTS_CLOSE
- TTS_NOANIMATE
- TTS_NOFADE
- TTS_NOPREFIX
- TTS_USEVISUALSTYLE
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8b89aed88caddceae815414b9f2b4d93a550c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752602"
---
# <a name="tooltip-styles"></a>Estilos de dica de ferramenta

Esta seção lista os estilos de controle usados com controles de dica de ferramenta.



| Constante                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**\_ALWAYSTIP TTS**</dt> </dl>                | Indica que o controle ToolTip aparece quando o cursor está em uma ferramenta, mesmo que a janela do proprietário do controle ToolTip esteja inativa. Sem esse estilo, a dica de ferramenta é exibida somente quando a janela do proprietário de ferramentas está ativa.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**balão de TTS \_**</dt> </dl>                      | [Versão 5,80](common-control-versions.md). Indica que o controle ToolTip tem a aparência de um "balão" animado com cantos arredondados e uma haste apontando para o item. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**fechamento de TTS \_**</dt> </dl>                            | Exibe um botão **fechar** na dica de ferramenta. Válido somente quando a dica de ferramenta tem o \_ estilo de balão TTS e um título; consulte [**\_ SetTitle TTM**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**noanime de TTS \_**</dt> </dl>                | [Versão 5,80](common-control-versions.md). Desabilita a animação deslizante da dica de ferramenta nos sistemas Windows 98 e Windows 2000. Esse estilo é ignorado em sistemas anteriores.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**nofade de TTS \_**</dt> </dl>                         | [Versão 5,80](common-control-versions.md). Desabilita a animação de dica de ferramenta de esmaecimento. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**NoPrefix de TTS \_**</dt> </dl>                   | Impede que o sistema retirasse caracteres de e comercial de uma cadeia de caracteres ou encerrando uma cadeia de caracteres em um caractere de tabulação. Sem esse estilo, o sistema retira automaticamente os caracteres de e comercial e encerra uma cadeia de caracteres no primeiro caractere de tabulação. Isso permite que um aplicativo use a mesma cadeia de caracteres como um item de menu e como texto em um controle ToolTip.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**\_USEVISUALSTYLE TTS**</dt> </dl> | Usa hiperlinks com tema. O tema definirá os estilos para todos os links na dica de ferramenta. Esse estilo sempre exige que o TTF \_ PARSELINKS seja definido. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

Um controle ToolTip sempre tem os \_ estilos de janela pop-up WS e WS \_ ex \_ TOOLWINDOW, independentemente de você especificá-los ao criar o controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





