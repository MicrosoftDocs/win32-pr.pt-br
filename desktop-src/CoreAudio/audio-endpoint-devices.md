---
description: Dispositivos de ponto de extremidade de áudio
ms.assetid: 773714fb-3b00-4f03-988f-05c5835f87cf
title: Dispositivos de ponto de extremidade de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11145227ff4f6cf4eb7dd11342e28b3a8260aac95c41b32faed6b2d6bd414dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407322"
---
# <a name="audio-endpoint-devices"></a>Dispositivos de ponto de extremidade de áudio

O termo *dispositivo de ponto de* extremidade refere-se a um dispositivo de hardware que está em uma extremidade de um caminho de dados originado ou encerrado em um programa de aplicativo. Exemplos de dispositivos de ponto de extremidade de áudio são alto-falantes, fones de ouvido, microfones e players de CD. Os dados de áudio que se movem ao longo do caminho de dados podem percorrer vários componentes de software e hardware durante seu percurso entre o aplicativo e o dispositivo de ponto de extremidade. Embora esses componentes sejam essenciais para a operação do dispositivo de ponto de extremidade, eles tendem a ser invisíveis para os usuários. Os usuários têm mais probabilidade de pensar em termos de dispositivos de ponto de extremidade que manipulam diretamente em vez de em termos dos dispositivos em adaptadores de áudio que os dispositivos de ponto de extremidade conectam ou em termos dos componentes de software que processam os fluxos de áudio que fluem de e para esses adaptadores.

Para evitar confusão com dispositivos de ponto de extremidade, esta documentação refere-se a um dispositivo em um adaptador de áudio como um *dispositivo de adaptador*.

O diagrama a seguir mostra como os dispositivos de ponto de extremidade de áudio diferem dos dispositivos de adaptador.

![exemplos de dispositivos de ponto de extremidade de áudio e dispositivos de adaptador](images/devices.jpg)

No diagrama anterior, veja a seguir exemplos de dispositivos de ponto de extremidade:

-   Speakers
-   Microfone
-   Dispositivo de entrada auxiliar

Veja a seguir exemplos de dispositivos de adaptador:

-   Dispositivo de saída de onda (contém conversor digital para análogo)
-   Dispositivo de controles de saída (contém controles de volume e mudo)
-   Dispositivo de entrada wave (contém conversor análogo a digital)
-   Dispositivo de controles de entrada (contém controle de volume e multiplexador)

Normalmente, as interfaces do usuário de aplicativos de áudio referem-se a dispositivos de ponto de extremidade de áudio, não a dispositivos de adaptador. Windows O Vista simplifica o design de aplicativos amigáveis ao dar suporte diretamente à abstração do dispositivo de ponto de extremidade.

Alguns dispositivos de ponto de extremidade podem se conectar permanentemente a um dispositivo de adaptador. Por exemplo, um computador pode conter dispositivos internos, como um player de CD, um microfone ou alto-falantes integrados ao chassi do sistema. Normalmente, o usuário não remove fisicamente esses dispositivos de ponto de extremidade.

Outros dispositivos de ponto de extremidade podem se conectar a um adaptador de áudio por meio de tomadas de áudio. O usuário conecta e desconecta esses dispositivos externos. Por exemplo, um dispositivo de ponto de extremidade de áudio, como um microfone externo ou fones de ouvido, está em uma extremidade de um cabo cuja outra extremidade se conecta a um conector em um dispositivo de adaptador.

O adaptador se comunica com o processador do sistema por meio de um barramento de sistema (normalmente, PCI ou PCI Express) ou barramento externo (USB ou IEEE 1394) que dá suporte Plug and Play (PnP). Durante a enumeração do dispositivo, o Plug and Play manager identifica os dispositivos no adaptador de áudio e registra esses dispositivos para torná-los disponíveis para uso pelo sistema operacional e por aplicativos.

Ao contrário da conexão entre um adaptador e um barramento externo, como USB ou o barramento IEEE 1394, a conexão entre um dispositivo de ponto de extremidade e um dispositivo de adaptador não dá suporte à detecção de dispositivos PnP. No entanto, alguns adaptadores de áudio suportam a detecção de presença de *tomada:* quando um plug é inserido ou removido de um conector, o hardware gera uma interrupção para notificar o driver do adaptador sobre a alteração na configuração de hardware. O gerenciador de ponto de extremidade no Windows Vista pode explorar essa funcionalidade de hardware para notificar os aplicativos de quais dispositivos de ponto de extremidade estão presentes a qualquer momento. Dessa forma, a operação do gerenciador de ponto de extremidade é análoga à do gerenciador Plug and Play, que acompanha os dispositivos de adaptador que estão presentes no sistema.

No Windows Vista, o sistema de áudio acompanha os dispositivos de ponto de extremidade e os dispositivos de adaptador. O gerenciador de ponto de extremidade registra dispositivos de ponto de extremidade e o gerenciador Plug and Play registra dispositivos de adaptador. Registrar dispositivos de ponto de extremidade torna mais fácil para aplicativos amigáveis permitir que os usuários se refiram aos dispositivos de ponto de extremidade que os usuários manipulam diretamente em vez de fazer referência a dispositivos de adaptador que podem estar ocultos dentro do chassi do computador. Os dispositivos de ponto de extremidade relatados pelo sistema operacional acompanham com fidelidade as alterações dinâmicas na configuração do hardware de áudio que tem detecção de presença de jack. Embora um dispositivo de ponto de extremidade permaneça conectado, o sistema enumera esse dispositivo. Quando o usuário desconecta um dispositivo de ponto de extremidade, o sistema deixa de enumerá-lo.

Em versões anteriores do Windows, incluindo Windows 98, Windows Me, Windows 2000 e Windows XP, o sistema apresenta explicitamente apenas dispositivos PnP para aplicativos. Portanto, os aplicativos devem inferir a existência de dispositivos de ponto de extremidade. Um sistema operacional que não tem suporte explícito para dispositivos de ponto de extremidade força os aplicativos cliente a fazer mais do trabalho em si. Por exemplo, um aplicativo de captura de áudio deve executar as seguintes etapas para habilitar a captura de um microfone externo:

1.  Enumere todos os dispositivos de captura de áudio (esses são dispositivos de adaptador) que foram previamente registrados pelo gerenciador do PnP.
2.  Depois de selecionar um dispositivo de captura, abra um fluxo de captura no dispositivo chamando a função **waveInOpen** ou usando a API **directSoundCapture** ou DirectShow.
3.  Chame a função mixerOpen e use as outras funções **mixerXxx** para procurar uma linha DE MICROFONE SRC MIXERLINE COMPONENTTYPE que corresponde ao dispositivo de captura aberto \_ na etapa \_ \_ 2. Essa é uma suposição instruda.
4.  Desbloqueie o caminho de dados do microfone. Se o caminho de dados incluir um nó de mudo, o cliente deverá desabilitar a mutação do sinal do microfone. Se o dispositivo de captura contiver um multiplexador para seleção entre várias entradas, o cliente deverá selecionar a entrada do microfone.

Esse processo é propenso a erros porque o software que executa essas operações pode falhar se encontrar uma configuração de hardware que seus designers não previam ou para as quais não foram testados.

No Windows Vista, que dá suporte a dispositivos de ponto de extremidade, o processo de conexão com o mesmo dispositivo de ponto de extremidade é muito mais simples:

1.  Selecione um microfone de uma coleção de dispositivos de ponto de extremidade.
2.  Ative uma interface de captura de áudio nesse microfone.

O sistema operacional faz todo o trabalho necessário para identificar e habilitar o dispositivo de ponto de extremidade. Por exemplo, se o caminho de dados do microfone incluir um multiplexador, o sistema selecionará automaticamente a entrada do microfone para o multiplexador.

O comportamento do subsistema de áudio é mais confiável e determinístico se os aplicativos, em vez de implementar seus próprios algoritmos de identificação de ponto de extremidade, podem relegar a tarefa de identificar dispositivos de ponto de extremidade para o sistema operacional. Os fornecedores de software não precisam mais verificar se seus algoritmos de identificação de ponto de extremidade funcionam corretamente com todos os dispositivos e configurações de hardware de áudio disponíveis– eles podem simplesmente depender do sistema operacional para identificação do ponto de extremidade. Da mesma forma, os fornecedores de hardware não precisam mais verificar se cada aplicativo cliente relevante pode identificar prontamente qualquer dispositivo de ponto de extremidade que esteja conectado ao adaptador de áudio– eles precisam apenas verificar se o sistema operacional pode identificar um dispositivo de ponto de extremidade conectado ao adaptador de áudio.

Os tópicos a seguir fornecem informações adicionais sobre dispositivos de ponto de extremidade de áudio:

-   [Sobre a API MMDevice](mmdevice-api.md)
-   [Enumerando dispositivos de áudio](enumerating-audio-devices.md)
-   [Cadeias de caracteres de ID do ponto de extremidade](endpoint-id-strings.md)
-   [Propriedades do Dispositivo](device-properties.md)
-   [Eventos de dispositivo](device-events.md)
-   [Funções de dispositivo](device-roles.md)
-   [Formatos de dispositivo](device-formats.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação](programming-guide.md)
</dt> </dl>

 

 



