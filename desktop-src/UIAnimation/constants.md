---
title: constantes (referência de animação de Windows)
description: documentação de referência para constantes e enumerações definidas pelo gerenciador de animação Windows.
ms.assetid: c590cf68-28ce-4d7d-949d-2683ece3c12d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23964a2936b3879d551bcde9c2c25c2d63465e1cb4afb07cee25a3ce74a2a57f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419113"
---
# <a name="constants-windows-animation-reference"></a>constantes (referência de animação de Windows)

documentação de referência para constantes e enumerações definidas pelo gerenciador de animação Windows.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                             | Descrição                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**dimensão de animação de interface do usuário \_ \_ \_ desconhecida**](ui-animation-dimension-unknown.md)<br/>                                            | Indica que a dimensão solicitada não pode ser recuperada.<br/>                                                                                                                                                                                                     |
| [**\_iteração de animação de IU \_ \_ nenhum**](-ui-animation-iteration-none.md)<br/>                                                 | Indica que esta é a entrada inicial em um determinado loop.<br/>                                                                                                                                                                                                     |
| [**\_quadro-chave da animação \_ KEYFRAME \_ início do storyboard \_**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))<br/>                           | Representa o quadro-chave implícito no início de cada Storyboard.<br/>                                                                                                                                                                                              |
| [**repetição de animação da interface do usuário \_ \_ \_ indefinidamente**](ui-animation-repeat-indefinitely.md)<br/>                                        | Indica que o intervalo entre dois quadros-chave em um storyboard deve repetir indefinidamente até que o método [**IUIAnimationStoryboard:: concluir**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) seja chamado.<br/>                                                            |
| [**repetição de animação da interface do usuário \_ \_ \_ indefinidamente \_ concluída \_ no \_ final**](ui-animation-repeat-indefinitely-conclude-at-end.md)<br/>     | Indica que o intervalo entre dois quadros-chave em um storyboard deve repetir indefinidamente até que o loop de Keyframe termine no quadro-chave final quando o método [**IUIAnimationStoryboard:: concluir**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) for chamado.<br/>   |
| [**repetição de animação da interface do usuário \_ \_ \_ indefinidamente \_ concluída \_ no \_ início**](ui-animation-repeat-indefinitely-conclude-at-start.md)<br/> | Indica que o intervalo entre dois quadros-chave em um storyboard deve repetir indefinidamente até que o loop de Keyframe termine no quadro-chave inicial quando o método [**IUIAnimationStoryboard:: concluir**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-conclude) for chamado.<br/> |
| [**segundos de animação da interface do usuário \_ \_ \_ eventualmente**](ui-animation-seconds-eventually.md)<br/>                                          | indica que Windows animação pode atrasar o início agendado de um storyboard para o máximo de tempo necessário para evitar conflitos de agendamento.<br/>                                                                                                                     |
| [**segundos de animação de IU \_ \_ \_ infinitas**](ui-animation-seconds-infinite.md)<br/>                                              | Indica que não há eventos agendados.<br/>                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Windows Referência de animação](windows-animation-reference.md)
</dt> </dl>

 

