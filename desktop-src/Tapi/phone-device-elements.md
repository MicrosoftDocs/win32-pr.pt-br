---
description: Um dispositivo de telefone é um dispositivo que dá suporte à classe de dispositivo de telefone e que inclui hookswitches, fones, viva-voz e headsets.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Elementos de dispositivo de telefone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc5744967dc738a65d7632dc1a1f6126bfbc9887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754730"
---
# <a name="phone-device-elements"></a>Elementos de dispositivo de telefone

Um dispositivo de telefone é um dispositivo que dá suporte à classe de dispositivo de telefone e que inclui alguns ou todos os elementos a seguir:

-   **Hookswitch/transdutor**: é um meio para entrada e saída de áudio. Um dispositivo de telefone pode ter vários transdutores, que podem ser ativados e desativados (tirados de offhook ou colocados no enhook) em um aplicativo ou controle de usuário manual.

    A telefonia identifica três tipos de dispositivos Hookswitch comuns a vários conjuntos de telefone:

     **Monofone**: a combinação tradicional de peças de boca e Ear que deve ser manualmente levantada de uma base e mantida em relação à ear do usuário.  
    **Viva-voz**: permite que o usuário realize chamadas sem intervenções. O viva-voz pode ser interno ou externo ao dispositivo de telefone. A parte do palestrante de um viva-voz permite vários ouvintes.  
    **Headset**: permite que o usuário realize chamadas sem intervenções.  
    

    Um Hookswitch deve ser offhook para permitir que os dados de áudio sejam enviados e/ou recebidos pelo transdutor correspondente.

-   Controle de volume/controle de lucro/mudo: cada dispositivo Hookswitch é o emparelhamento de um palestrante e um componente de microfone. A API fornece controle de volume e mudo dos componentes do alto-falante e para obter controle ou mudo dos componentes do microfone.
-   [Campainha](ring.md): um meio para alertar os usuários, geralmente por meio de um sino. Um dispositivo de telefone pode ser capaz de tocar em uma variedade de modos ou padrões.
-   [Display](display.md): um mecanismo para apresentar visualmente mensagens ao usuário. Uma exibição de telefone é caracterizada por seu número de linhas e colunas.
-   [Botões de telefone](phone-buttons.md): uma matriz de botões. Sempre que o usuário pressiona um botão no conjunto de telefone, a API relata que o botão correspondente foi pressionado. Identificadores de lâmpada de botão identificam um par de botão e de lâmpada. É claro que é possível ter pares de luzes de botão sem nenhum botão ou nenhuma lâmpada. Os identificadores de lâmpada de botão são valores inteiros que variam de 0 até o número máximo de lâmpadas de botão disponíveis no dispositivo de telefone, menos um. Cada botão pertence a uma classe de botão. As classes incluem botões de aparência de chamada, botões de recurso, botões de teclado e botões locais.
-   [Lâmpadas](lamps.md): uma matriz de lâmpadas (como LEDs) individualmente controláveis da API. As lâmpadas podem ser acesas em modos diferentes por meio da variação da frequência de ativar e desativar. O identificador de lâmpada do botão identifica a lâmpada.
-   [Áreas de dados](data-areas.md): áreas de memória no dispositivo de telefone em que o código de instrução ou os dados podem ser baixados e/ou carregados. As informações baixadas afetariam o comportamento (ou, em outras palavras, programa) o dispositivo de telefone.

A TAPI permite que um aplicativo monitore e controle elementos do dispositivo de telefone. Os elementos mais úteis para um aplicativo são os dispositivos Hookswitch. O conjunto de telefone pode atuar como um dispositivo de e/s de áudio (para o computador) com controle de volume, obter controle e mudo, um toque (para alertar o usuário), áreas de dados (para programar o telefone) e, talvez, uma exibição, embora a exibição do computador seja mais compatível. O gravador de aplicativos não é incentivado de controlar diretamente ou usar lâmpadas telefônicas ou botões de telefone, pois os recursos de lâmpada e botão podem variar muito entre conjuntos de telefone, e os aplicativos podem rapidamente se tornar personalizados para conjuntos de telefone específicos.

Não há nenhum conjunto principal de serviços garantidos com suporte de todos os dispositivos de telefone como há para dispositivos de linha (os serviços de telefonia básicos). Portanto, antes que um aplicativo possa usar um dispositivo de telefone, o aplicativo deve primeiro determinar os recursos exatos do dispositivo de telefone. A capacidade de telefonia varia de acordo com a configuração (cliente versus cliente/servidor), o hardware de telefone e o software do provedor de serviços. Os aplicativos não devem fazer suposições sobre quais recursos de telefonia estão disponíveis. Um aplicativo determina os recursos de um dispositivo telefônico chamando a função [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) . Os recursos de dispositivo de um telefone indicam quais desses elementos existem para cada dispositivo de telefone presente no sistema e quais são seus recursos. Embora seja altamente orientado para conjuntos de telefone da vida real, essa abstração pode fornecer uma implementação significativa (ou subconjunto) para outros dispositivos também. Veja um exemplo de um headset separado conectado diretamente e controlável do computador e operado como um dispositivo de telefone. As alterações Hookswitch podem ser disparadas pela detecção de energia de voz (offhook) ou um período de silêncio (onhook); o toque pode ser emulado pela geração de um sinal audível no headset; uma exibição pode ser emulada por meio da conversão de texto em fala.

Um dispositivo de telefone não precisa ser realizado em hardware, mas pode ser emulado no software usando uma interface de comando gráfica voltada para o mouse ou teclado e o sistema de fala ou de som do computador. Tal "telefone suave" pode ser um aplicativo que usa a TAPI. Ele também pode ser um provedor de serviços, que pode ser listado como um dispositivo de telefone disponível para outros aplicativos por meio da API e, como tal, é atribuído a um identificador de dispositivo de telefone.

Dependendo do ambiente e da configuração, os conjuntos de telefone podem ser dispositivos compartilhados entre o aplicativo e o comutador. Um provisionamento menor é feito na API em que a opção pode suspender temporariamente o controle da API de um dispositivo de telefone.

 

 



