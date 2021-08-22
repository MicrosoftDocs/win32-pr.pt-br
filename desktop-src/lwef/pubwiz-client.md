---
title: Design de Client-Side
description: O script em páginas HTML do lado do servidor se comunica com o cliente do assistente de ordenação de impressão online no qual ele está hospedado. Essa comunicação é realizada por meio de métodos e propriedades acessados pelo objeto Window. external.
ms.assetid: fa76ccee-0b94-41b5-8cc8-eb7e1818dbed
keywords:
- assistentes de publicação, design do lado do cliente
- janela. external, assistentes de publicação
- assistentes de publicação, janela. externa
- assistentes de publicação, considerações de design
- assistentes de publicação, assistente para ordenação de impressão online
- Assistente de ordenação de impressão online, design do lado do cliente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40aafc7a08820125df222c1c6d911b0d2b4d0a1fb625b7c62fc6d4be8bebd7c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665076"
---
# <a name="client-side-design"></a>Design de Client-Side

O script em páginas HTML do lado do servidor se comunica com o cliente do assistente de ordenação de impressão online no qual ele está hospedado. Essa comunicação é realizada por meio de métodos e propriedades acessados pelo objeto **Window. external** .

Os tópicos a seguir são abordados neste documento.

-   [Métodos e propriedades](#methods-and-properties)
-   [Considerações de criação](#design-considerations)
-   [Tópicos relacionados](#related-topics)

## <a name="methods-and-properties"></a>Métodos e propriedades

Os métodos e as propriedades a seguir estão disponíveis por meio do objeto **Window. external** .

-   [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback)
-   [**FinalNext**](/windows/desktop/shell/iwebwizardhost-finalnext)
-   [**Cancelar**](/windows/desktop/shell/iwebwizardhost-cancel)
-   [**PassportAuthenticate**](/windows/desktop/shell/inewwdevents-passportauthenticate)
-   [**Setheadertext**](/windows/desktop/shell/iwebwizardhost-setheadertext)
-   [**SetWizardButtons**](/windows/desktop/shell/iwebwizardhost-setwizardbuttons)
-   [**Legenda**](/previous-versions/windows/desktop/legacy/bb774352(v=vs.85))
-   [**Propriedade**](/windows/desktop/shell/iwebwizardhost-property)

O script da página do lado do servidor chama esses métodos para notificar o cliente sobre eventos durante o procedimento de publicação. Vejamos [**FinalBack**](/windows/desktop/shell/iwebwizardhost-finalback) como exemplo. Quando o assistente exibe a primeira página HTML do lado do servidor, ele faz isso com o conhecimento dos identificadores das páginas do assistente anteriores e das páginas HTML hospedadas a seguir. Neste ponto do nosso exemplo, o usuário, sentado nessa primeira página HTML, clica no botão **voltar** . O assistente envia uma notificação desse evento para o servidor. Ao receber essa mensagem, o script do lado do servidor refere-se a seu manipulador **onback** para esse evento, que, como esta é a primeira página HTML, chama o método **FinalBack** . Isso faz com que o assistente navegue até a página de assistente exibida antes de entrar na interface do usuário do lado do servidor.

Para obter uma discussão completa sobre esses métodos e propriedades, consulte a documentação para os objetos [**WebWizardHost**](/windows/desktop/shell/webwizardhost) e [**NewWDEvents**](/windows/desktop/shell/newwdevents) .

## <a name="design-considerations"></a>Considerações de criação

O HTML que compõe cada página do lado do servidor é exibido normalmente no painel do assistente. Ao criar essas páginas, tenha em mente que uma janela do assistente não pode ser redimensionada. As páginas devem, portanto, ser construídas e dimensionadas para que as barras de rolagem sejam evitadas sempre que possível para fornecer ao usuário navegação suave por meio do assistente.

Cada página HTML também deve fornecer um manipulador para eventos **OnDelete**, **OnNext** e **OnCancel** . O manipulador **OnNext** também manipulará o evento **Finish** . Uma página que não implementa uma função **onback** é considerada inválida e fará com que uma página de erro seja exibida.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**WebWizardHost**](/windows/desktop/shell/webwizardhost)
</dt> <dt>

[**NewWDEvents**](/windows/desktop/shell/newwdevents)
</dt> <dt>

[Design do lado do servidor](pubwiz-server.md)
</dt> </dl>

 

 