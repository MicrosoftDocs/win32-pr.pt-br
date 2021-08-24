---
title: Estilos de dica de ferramenta (CommCtrl.h)
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
ms.openlocfilehash: 2dddd890f8bf3aad35d20ec2eabcbe34f89b3ef262fbe30586f9a0a893f85e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751016"
---
# <a name="tooltip-styles"></a>Estilos de dica de ferramenta

Esta seção lista os estilos de controle usados com controles de dica de ferramenta.



| Constante                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                                                                                       |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TTS_ALWAYSTIP"></span><span id="tts_alwaystip"></span><dl> <dt>**TTS \_ ALWAYSTIP**</dt> </dl>                | Indica que o controle de dica de ferramenta aparece quando o cursor está em uma ferramenta, mesmo se a janela do proprietário do controle de dica de ferramenta estiver inativa. Sem esse estilo, a dica de ferramenta aparece somente quando a janela do proprietário da ferramenta está ativa.<br/>                                                                                                                                  |
| <span id="TTS_BALLOON"></span><span id="tts_balloon"></span><dl> <dt>**BALÃO \_ DE TTS**</dt> </dl>                      | [Versão 5.80.](common-control-versions.md) Indica que o controle de dica de ferramenta tem a aparência de um "balão" de desenho animado, com cantos arredondados e um tronco apontando para o item. <br/>                                                                                                                                                                      |
| <span id="TTS_CLOSE"></span><span id="tts_close"></span><dl> <dt>**TTS \_ CLOSE**</dt> </dl>                            | Exibe um **botão Fechar** na dica de ferramenta. Válido somente quando a dica de ferramenta tiver o estilo TTS BALLOON e \_ um título; consulte [**TTM \_ SETTITLE**](ttm-settitle.md).<br/>                                                                                                                                                                                             |
| <span id="TTS_NOANIMATE"></span><span id="tts_noanimate"></span><dl> <dt>**TTS \_ NOANIMATE**</dt> </dl>                | [Versão 5.80.](common-control-versions.md) Desabilita a animação de dica de ferramenta deslizante Windows 98 e Windows 2000. Esse estilo é ignorado em sistemas anteriores.<br/>                                                                                                                                                                                      |
| <span id="TTS_NOFADE"></span><span id="tts_nofade"></span><dl> <dt>**TTS \_ NOFADE**</dt> </dl>                         | [Versão 5.80.](common-control-versions.md) Desabilita a animação de dica de ferramenta de esbotão. <br/>                                                                                                                                                                                                                                                                       |
| <span id="TTS_NOPREFIX"></span><span id="tts_noprefix"></span><dl> <dt>**TTS \_ NOPREFIX**</dt> </dl>                   | Impede que o sistema esvaia caracteres e ampersand de uma cadeia de caracteres ou finalização de uma cadeia de caracteres em um caractere de tabulação. Sem esse estilo, o sistema retira automaticamente caracteres e ampersand e encerra uma cadeia de caracteres no primeiro caractere de tabulação. Isso permite que um aplicativo use a mesma cadeia de caracteres que um item de menu e um texto em um controle de dica de ferramenta.<br/> |
| <span id="TTS_USEVISUALSTYLE"></span><span id="tts_usevisualstyle"></span><dl> <dt>**TTS \_ USEVISUALSTYLE**</dt> </dl> | Usa hiperlinks com temas. O tema definirá os estilos para todos os links na dica de ferramenta. Esse estilo sempre requer que TTF \_ PARSELINKS seja definido. <br/>                                                                                                                                                                                                          |



## <a name="remarks"></a>Comentários

Um controle de dica de ferramenta sempre tem os estilos de janela POPUP do WS e \_ DO WS EXWINDOW, independentemente de você especificá-los ao \_ \_ criar o controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>CommCtrl.h</dt> </dl> |



 

 





