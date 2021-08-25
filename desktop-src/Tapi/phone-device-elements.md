---
description: Um dispositivo de telefone é um dispositivo que dá suporte à classe de dispositivo de telefone e que inclui ganchos, handsets, alto-falantes e headsets.
ms.assetid: c2660d77-0265-49d4-bd04-1cddd674b760
title: Telefone Elementos do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c882e7f9ebe279d0ee6622708f8b735b68f4c37a2f93dffe2a870271d556cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774166"
---
# <a name="phone-device-elements"></a>Telefone Elementos do dispositivo

Um dispositivo de telefone é um dispositivo que dá suporte à classe de dispositivo de telefone e que inclui alguns ou todos os seguintes elementos:

-   **Hookswitch/transducer:** isso é um meio para entrada e saída de áudio. Um dispositivo de telefone pode ter vários transdutores, que podem ser ativados e desativados (retirados ou colocados nohook) sob controle de usuário manual ou de aplicativo.

    A telefonia identifica três tipos de dispositivos hookswitch comuns a muitos conjuntos de telefone:

     **Conjunto de** mãos: a combinação tradicional de peças de boca e de ouvido que deve ser retirada manualmente de uma cabeça e mantida no ouvido do usuário.  
    **Speakerphone:** permite que o usuário conduza chamadas de mãos livres. O speakerphone pode ser interno ou externo ao dispositivo de telefone. A parte do locutor de um speakerphone permite vários ouvintes.  
    **Headset:** permite que o usuário conduza chamadas sem mãos.  
    

    Um hookswitch deve ser offhook para permitir que os dados de áudio sejam enviados para e/ou recebidos pelo transdutor correspondente.

-   Controle de Volume/Controle de Ganho/Mute: cada dispositivo hookswitch é o emparelhamento de um alto-falante e um componente de microfone. A API fornece controle de volume e muting de componentes do locutor e para obter controle ou muting de componentes de microfone.
-   [Ringer:](ring.md)um meio para alertar os usuários, geralmente por meio de um sino. Um dispositivo de telefone pode ser capaz de tocar em uma variedade de modos ou padrões.
-   [Exibir](display.md): um mecanismo para apresentar visualmente mensagens ao usuário. Uma exibição de telefone é caracterizada pelo número de linhas e colunas.
-   [Telefone botões](phone-buttons.md): uma matriz de botões. Sempre que o usuário pressiona um botão no conjunto de telefone, a API informa que o botão correspondente foi pressionado. Identificadores de lâmpada de botão identificam um botão e um par de lâmpadas. É claro que é possível ter pares de lâmpada de botão sem botão ou sem lâmpada. Identificadores de lâmpada de botão são valores inteiros que variam de 0 ao número máximo de lâmpadas de botão disponíveis no dispositivo de telefone, menos um. Cada botão pertence a uma classe de botão. As classes incluem botões de aparência de chamada, botões de recurso, botões de teclado e botões locais.
-   [Lâmpadas:](lamps.md)uma matriz de lâmpadas (como LEDs) individualmente controláveis da API. As lâmpadas podem ser acendidas em modos diferentes variando a frequência de ativas e desligadas. O identificador de lâmpada de botão identifica a lâmpada.
-   [Áreas de](data-areas.md)dados: áreas de memória no dispositivo de telefone em que o código de instrução ou os dados podem ser baixados para e/ou carregados. As informações baixadas afetariam o comportamento (ou, em outras palavras, programar) o dispositivo de telefone.

O TAPI permite que um aplicativo monitore e controle elementos do dispositivo de telefone. Os elementos mais úteis para um aplicativo são os dispositivos hookswitch. O conjunto de telefone pode atuar como um dispositivo de E/S de áudio (para o computador) com controle de volume, obter controle e mute, um toque (para alertar o usuário), áreas de dados (para programação do telefone) e, talvez, uma exibição, embora a exibição do computador seja mais capaz. O autor do aplicativo não é desencorajado de controlar diretamente ou usar lâmpadas de telefone ou botões de telefone, pois os recursos de lâmpada e botão podem variar muito entre conjuntos de telefone e os aplicativos podem se adaptar rapidamente a conjuntos de telefone específicos.

Não há nenhum conjunto principal garantido de serviços com suporte em todos os dispositivos de telefone, pois há para dispositivos de linha (os serviços básicos de telefonia). Portanto, antes que um aplicativo possa usar um dispositivo de telefone, o aplicativo deve primeiro determinar as funcionalidades exatas do dispositivo de telefone. A funcionalidade de telefonia varia de acordo com a configuração (cliente versus cliente/servidor), o hardware de telefone e o software do provedor de serviços. Os aplicativos não devem fazer suposições sobre quais funcionalidades de telefonia estão disponíveis. Um aplicativo determina os recursos de dispositivo de um dispositivo de telefone chamando a [**função phoneGetDevCaps.**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps) Os recursos do dispositivo de um telefone indicam quais desses elementos existem para cada dispositivo de telefone presente no sistema e quais são seus recursos. Embora fortemente orientada para conjuntos de telefones reais, essa abstração também pode fornecer uma implementação significativa (ou subconjunto) para outros dispositivos. Veja como exemplo um headset separado diretamente conectado e controlável do computador e operado como um dispositivo de telefone. As alterações de gancho podem ser disparadas pela detecção de energia de voz (offhook) ou um período de silêncio (onhook); pode ser emulado pela geração de um sinal audível no headset; uma exibição pode ser emulada por meio da conversão de texto em fala.

Um dispositivo de telefone não precisa ser realizado em hardware, mas pode ser emulado em software usando uma interface de comando gráfica controlada por mouse ou teclado e o sistema de som ou alto-falante do computador. Esse "telefone celular" pode ser um aplicativo que usa TAPI. Ele também pode ser um provedor de serviços, que pode ser listado como um dispositivo de telefone disponível para outros aplicativos por meio da API e, como tal, recebe um identificador de dispositivo de telefone.

Dependendo do ambiente e da configuração, os conjuntos de telefone podem ser dispositivos compartilhados entre o aplicativo e a opção. Algumas provisões secundárias são feitas na API em que a opção pode suspender temporariamente o controle da API de um dispositivo de telefone.

 

 



