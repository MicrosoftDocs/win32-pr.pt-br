---
description: Dispositivos de ponto de extremidade de áudio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Dispositivos de ponto de extremidade de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c14d21aa174e34f8cb4ddab520819446a0e0ec89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920569"
---
# <a name="audio-endpoint-devices"></a>Dispositivos de ponto de extremidade de áudio

O termo *dispositivo de ponto de extremidade* refere-se a um dispositivo de hardware que está em uma extremidade de um caminho de dados originado ou encerrado em um programa de aplicativo. Exemplos de dispositivos de ponto de extremidade de áudio são palestrantes, fones de ouvido, microfones e CD players. Os dados de áudio que se movem ao longo do caminho de dados podem atravessar vários componentes de software e hardware durante sua jornada entre o aplicativo e o dispositivo de ponto de extremidade. Embora esses componentes sejam essenciais para a operação do dispositivo de ponto de extremidade, eles tendem a ser invisíveis para os usuários. É mais provável que os usuários considerem em termos de dispositivos de ponto de extremidade que manipulam diretamente, e não em termos dos dispositivos em adaptadores de áudio que os dispositivos de ponto de extremidade conectam ou em termos dos componentes de software que processam os fluxos de áudio que fluem para e desses adaptadores.

Para evitar confusão com dispositivos de ponto de extremidade, esta documentação refere-se a um dispositivo em um adaptador de áudio como um *dispositivo de adaptador*.

O diagrama a seguir mostra como os dispositivos de ponto de extremidade de áudio são diferentes dos dispositivos de adaptador.

![exemplos de dispositivos de ponto de extremidade de áudio e dispositivos de adaptador](images/devices.jpg)

No diagrama anterior, veja a seguir exemplos de dispositivos de ponto de extremidade:

-   Speakers
-   Microfone
-   Dispositivo de entrada auxiliar

Veja a seguir exemplos de dispositivos de adaptador:

-   Dispositivo de saída Wave (contém o conversor digital para analógico)
-   Dispositivo de controles de saída (contém controles de volume e mudo)
-   Dispositivo de entrada Wave (contém o conversor analógico para digital)
-   Dispositivo de controles de entrada (contém controle de volume e multiplexador)

Normalmente, as interfaces de usuário de aplicativos de áudio referem-se a dispositivos de ponto de extremidade de áudio, e não a dispositivos de adaptador. O Windows Vista simplifica o design de aplicativos amigáveis, dando suporte direto à abstração de dispositivo de ponto de extremidade.

Alguns dispositivos de ponto de extremidade podem se conectar permanentemente a um dispositivo adaptador. Por exemplo, um computador pode conter dispositivos internos, como um CD player, um microfone ou alto-falantes integrados ao chassi do sistema. Normalmente, o usuário não remove fisicamente esses dispositivos de ponto de extremidade.

Outros dispositivos de ponto de extremidade podem se conectar a um adaptador de áudio por meio de tomadas de áudio. O usuário conecta e desconecta esses dispositivos externos. Por exemplo, um dispositivo de ponto de extremidade de áudio, como um microfone externo ou fone de ouvido, está em uma extremidade de um cabo cuja outra extremidade se conecta a uma tomada em um dispositivo de adaptador.

O adaptador se comunica com o processador do sistema por meio de um barramento do sistema (normalmente, PCI ou PCI Express) ou barramento externo (USB ou IEEE 1394) que dá suporte a Plug and Play (PnP). Durante a enumeração do dispositivo, o Gerenciador de Plug and Play identifica os dispositivos no adaptador de áudio e registra esses dispositivos para torná-los disponíveis para uso pelo sistema operacional e por aplicativos.

Ao contrário da conexão entre um adaptador e um barramento externo, como USB ou o barramento IEEE 1394, a conexão entre um dispositivo de ponto de extremidade e um dispositivo de adaptador não oferece suporte à detecção de dispositivo PnP. No entanto, alguns adaptadores de áudio oferecem suporte à *detecção de presença de Jack*: quando um plug-in é inserido ou removido de um conector, o hardware gera uma interrupção para notificar o driver do adaptador da alteração na configuração de hardware. O Gerenciador de pontos de extremidade do Windows Vista pode explorar essa capacidade de hardware para notificar aplicativos que os dispositivos de ponto de extremidade estão presentes a qualquer momento. Dessa forma, a operação do Endpoint Manager é análoga à do Gerenciador de Plug and Play, que controla os dispositivos de adaptador que estão presentes no sistema.

No Windows Vista, o sistema de áudio controla os dispositivos de ponto de extremidade e os dispositivos de adaptador. O Gerenciador de pontos de extremidade registra dispositivos de ponto de extremidade e o Gerenciador de Plug and Play registra os dispositivos de adaptador. O registro de dispositivos de ponto de extremidade torna mais fácil para aplicativos amigáveis permitir que os usuários façam referência aos dispositivos de ponto de extremidade que os usuários manipulam diretamente em vez de se referir a dispositivos de adaptador que podem estar ocultos dentro do chassi do computador. Os dispositivos de ponto de extremidade que são relatados pelo sistema operacional controlam com fidelidade as alterações dinâmicas na configuração de hardware de áudio que tem detecção de presença de sensor. Enquanto um dispositivo de ponto de extremidade permanece conectado, o sistema enumera esse dispositivo. Quando o usuário desconectar um dispositivo de ponto de extremidade, o sistema deixará de enumerar.

Em versões anteriores do Windows, incluindo Windows 98, Windows me, Windows 2000 e Windows XP, o sistema apresenta explicitamente apenas dispositivos PnP a aplicativos. Portanto, os aplicativos devem inferir a existência de dispositivos de ponto de extremidade. Um sistema operacional que não tem suporte explícito para dispositivos de ponto de extremidade força os aplicativos cliente a realizarem mais do trabalho em si. Por exemplo, um aplicativo de captura de áudio deve executar as seguintes etapas para habilitar a captura de um microfone externo:

1.  Enumere todos os dispositivos de captura de áudio (estes são dispositivos de adaptador) que foram previamente registrados pelo Gerenciador de PnP.
2.  Depois de selecionar um dispositivo de captura, abra um fluxo de captura no dispositivo chamando a função **waveInOpen** ou usando a API do **DirectSoundCapture** ou do DirectShow.
3.  Chame a função mixerOpen e use as outras funções do **mixerXxx** para procurar por uma \_ linha de microfone src de componente do mixer \_ \_ que corresponda ao dispositivo de captura aberto na etapa 2. Essa é uma estimativa reinstruída.
4.  Desbloqueie o caminho de dados do microfone. Se o caminho de dados incluir um nó sem áudio, o cliente deverá desabilitar o mudo do sinal do microfone. Se o dispositivo de captura contiver um multiplexador para seleção entre várias entradas, o cliente deverá selecionar a entrada do microfone.

Esse processo é propenso a erros, pois o software que executa essas operações poderá falhar se encontrar uma configuração de hardware que seus designers não preveem ou para as quais ele não foi testado.

No Windows Vista, que dá suporte a dispositivos de ponto de extremidade, o processo de conexão ao mesmo dispositivo de ponto de extremidade é muito mais simples:

1.  Selecione um microfone de uma coleção de dispositivos de ponto de extremidade.
2.  Ative uma interface de captura de áudio nesse microfone.

O sistema operacional faz todo o trabalho necessário para identificar e habilitar o dispositivo de ponto de extremidade. Por exemplo, se o caminho de dados do microfone incluir um multiplexador, o sistema selecionará automaticamente a entrada do microfone para o multiplexador.

O comportamento do subsistema de áudio é mais confiável e determinístico se os aplicativos, em vez de implementar seus próprios algoritmos de identificação de ponto de extremidade, podem relegador a tarefa de identificar dispositivos de ponto de extremidade para o sistema operacional. Os fornecedores de software não precisam mais verificar se seus algoritmos de identificação de ponto de extremidade funcionam corretamente com todos os dispositivos e configurações de hardware de áudio disponíveis – eles podem simplesmente contar com o sistema operacional para identificação de ponto de extremidade. Da mesma forma, os fornecedores de hardware não precisam mais verificar se cada aplicativo cliente relevante pode rapidamente identificar qualquer dispositivo de ponto de extremidade que esteja conectado ao adaptador de áudio — eles precisam apenas verificar se o sistema operacional pode identificar um dispositivo de ponto de extremidade conectado ao adaptador de áudio.

Os tópicos a seguir fornecem informações adicionais sobre dispositivos de ponto de extremidade de áudio:

-   [Sobre a API do MMDevice](mmdevice-api.md)
-   [Enumerando dispositivos de áudio](enumerating-audio-devices.md)
-   [Cadeias de ID do ponto de extremidade](endpoint-id-strings.md)
-   [Propriedades do Dispositivo](device-properties.md)
-   [Eventos de dispositivo](device-events.md)
-   [Funções de dispositivo](device-roles.md)
-   [Formatos de dispositivo](device-formats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



