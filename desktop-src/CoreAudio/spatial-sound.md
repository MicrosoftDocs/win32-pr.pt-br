---
description: O som espacial da Microsoft é a solução em nível de plataforma da Microsoft para suporte a sons espaciais no Xbox, no Windows e no HoloLens 2, permitindo indicações de áudio surround e elevação (acima ou abaixo do ouvinte).
ms.assetid: 4F962F1A-CA4A-4018-BA97-516EA3519650
title: 'Som espacial para desenvolvedores '
ms.custom: contperf-fy21q1
ms.topic: article
ms.date: 09/18/2020
ms.openlocfilehash: 9db3614ea7932af874da351e7a92980d51b90011
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/04/2021
ms.locfileid: "104560080"
---
# <a name="spatial-sound-for-developers"></a>Som espacial para desenvolvedores 
> [!Note] 
> Esta documentação é destinada a um público do desenvolvedor. Para obter suporte ao usuário final para habilitar o som espacial em seu dispositivo, consulte [como ativar o som espacial no Windows 10](https://support.microsoft.com/help/4563140/how-to-turn-on-spatial-sound-in-windows-10).

O som espacial da Microsoft é a solução em nível de plataforma da Microsoft para suporte a sons espaciais no Xbox, no Windows e no HoloLens 2, permitindo indicações de áudio surround e elevação (acima ou abaixo do ouvinte). O som espacial pode ser aproveitado por aplicativos da área de trabalho do Windows (Win32), bem como aplicativos Plataforma Universal do Windows (UWP) em plataformas com suporte. As APIs de som espacial permitem que os desenvolvedores criem objetos de áudio que emitem áudio de posições em espaço 3D. Os objetos de áudio dinâmicos permitem que você emita áudio de uma posição arbitrária no espaço, o que pode ser alterado ao longo do tempo. Você também pode especificar que os objetos de áudio emitem som de um dos 17 canais estáticos predefinidos (8.1.4.4) que podem representar alto-falantes reais ou virtualizados. O formato de saída real é selecionado pelo usuário e pode ser extraído de implementações de som espacial da Microsoft; o áudio será apresentado a palestrantes existentes, fones de ouvido e receptores de Home Theater sem a necessidade de alterações de código ou conteúdo. A plataforma dá suporte total à codificação Dolby Atmos em tempo real para saída de fone de ouvido de HDMI e estéreo, DTS: X para fones de ouvido e codificação do Windows Sonic para fones de ouvido para fones estéreo. Por fim, os aplicativos de som espacial da Microsoft obedecem à política de combinação do sistema e seu áudio também será misturado com aplicativos com reconhecimento não espacial. O suporte a sons espaciais da Microsoft também é integrado ao Media Foundation; os aplicativos que usam o Media Foundation podem reproduzir com êxito o conteúdo Dolby Atmos sem implementação adicional.

O som espacial com som espacial da Microsoft dá suporte a TVs, Home Theaters e barras de som que dão suporte a Dolby Atmos. O som espacial também pode ser usado com qualquer par de fones de ouvido que o consumidor possa ter, com áudio renderizado pela plataforma usando o Windows Sonic para fones de ouvido, Dolby Atmos para fones de ouvido ou Headphone do DTS: X.


## <a name="enabling-microsoft-spatial-sound"></a>Habilitando o som espacial da Microsoft

Seja como desenvolvedor ou consumidor, um usuário deve habilitar o som espacial da Microsoft em seu dispositivo para ouvir o som espacial.

### <a name="windows"></a>Windows
Em computadores Windows, isso é feito por meio da página Propriedades de um determinado dispositivo de saída de som. No painel de controle **som** , selecione um dispositivo de saída e clique em **Propriedades do dispositivo**. Na seção **som espacial** da página, se o dispositivo der suporte a som espacial, você poderá selecionar um dos formatos disponíveis na lista suspensa **formato de som espacial** .

![habilitar o som espacial no painel de controle de som](images/spatialsoundsettingswindows1.png)

Você também pode habilitar o som espacial da Microsoft clicando com o botão direito do mouse no ícone de **volume** na barra de tarefas.

![habilitar o som espacial da barra de tarefas](images/spatialsoundsettingswindows2.png)

### <a name="xbox-one"></a>Xbox One
No Xbox One, os recursos de som espacial da Microsoft estão sempre disponíveis para o consumidor e são habilitados por meio do aplicativo configurações em **geral-> Volume & saída de áudio**.


![habilitar o som espacial no Xbox One no aplicativo de configurações ](images/audiosettingsbitstream.png)

Após o Dolby Atmos for Home Theater ser selecionado como um "formato fragmentado", o suporte para esse formato é verificado por meio de dados de identificação de exibição estendida HDMI (EDID). Se o dispositivo HDMI não oferecer suporte ao formato, uma mensagem de erro será exibida para o usuário. Observe que selecionar essa opção na primeira vez requer que o usuário Baixe o aplicativo Dolby Access.

Se um formato diferente de "fragmentado out" for selecionado para **áudio HDMI** , a lista suspensa **formato fragmentado** será desabilitada.

![som espacial desabilitado no Xbox One no aplicativo de configurações ](images/audiosettingsplain.png)

Selecione Dolby Atmos for fone de ouvido, DTS Headphone: X ou Windows Sonic para fones de ouvido na lista suspensa **formato do headset** em **áudio do headset**

![habilitar o som espacial para fones de ouvido no Xbox um no aplicativo de configurações ](images/audiosettingsheadphone.png)

Quando o som espacial da Microsoft não estiver disponível (por exemplo, ao jogar para os auto-falantes estéreo inseridos no laptop ou se o usuário não tiver habilitado explicitamente o som espacial da Microsoft acima), o número de objetos dinâmicos disponíveis retornados por [**ISpatialAudioClient:: GetMaxDynamicObjectCount**](/windows/desktop/api/spatialaudioclient/nf-spatialaudioclient-ispatialaudioclient-getmaxdynamicobjectcount) para um aplicativo será 0.

### <a name="hololens-2"></a>HoloLens 2

No HoloLens 2, o som espacial da Microsoft é habilitado por padrão e usa o descarregamento de DSP de hardware projetado especificamente para o Windows Sonic para fones de ouvido.

## <a name="microsoft-spatial-sound-and-audio-middleware"></a>Middleware de áudio e som espacial da Microsoft

Muitos desenvolvedores de aplicativos e jogos usam soluções de mecanismo de renderização de áudio de terceiros, que geralmente incluem ferramentas sofisticadas de criação e Auditioning. A Microsoft estabeleceu um parceria com vários desses provedores de soluções para implementar o som espacial da Microsoft em seus ambientes de criação existentes. Isso geralmente significa que as APIs discutidas aqui são abstratas da exibição do aplicativo; Eles são encapsulados como plug-ins de DSP (processamento de sinal digital) que o aplicativo pode instanciar e que o implementador de áudio do aplicativo pode usar para misturar a uma base de canal de som espacial da Microsoft, submix ou enviar vozes individuais para plug-ins de instância de objeto dinâmico conforme desejado. Consulte o provedor de solução de middleware de áudio para obter o nível de suporte para o som espacial da Microsoft.

## <a name="microsoft-spatial-sound-for-audio-renderers"></a>Som espacial da Microsoft para renderizadores de áudio

Muitos renderizadores de áudio visam um ponto de extremidade de WASAPI (API de sessão de áudio do Windows) [**IAudioClient**](/windows/desktop/api/Audioclient/nn-audioclient-iaudioclient) , em que o aplicativo alimenta buffers de dados de áudio mistos e de formato compatível com um coletor de áudio WASAPI; os buffers entregues são então consumidos para misturar com outros clientes, processamento final do nível do sistema e renderização.

Os pontos de extremidade espaciais de som espacial da Microsoft são implementados como [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient), que tem muitas semelhanças para **IAudioClient**. Ele dá suporte a objetos de som *estáticos* que formam uma base de canal, com suporte para canais de até 8.1.4.4 (8 canais em todo o ouvinte – esquerda, direita, centro, lado esquerdo, lado direito, voltar à esquerda, voltar à direita e de trás; 1 canal de efeitos de baixa frequência; 4 canais acima do ouvinte; 4 canais abaixo do ouvinte). E ele dá suporte a objetos de som *dinâmicos* , que podem ser arbitrariamente posicionados no espaço 3D.

O padrão de codificação de implementação geral para **ISpatialAudioClient** é:

-   Crie objetos de áudio estáticos e/ou dinâmicos.
-   Alimentar o buffer de áudio de cada objeto em cada quadro para que o sistema possa renderizá-lo.
-   Atualizar posições 3D de objetos dinâmicos sob demanda – com frequência (ou raramente) como o aplicativo se desejar.

Observe que o formato de saída atual (alto-falantes ou fones de ouvido; O Windows Sonic para fones de ouvido, o Dolby Atmos ou o Headphone do DTS: X) é dissociado da implementação acima – o desenvolvedor do aplicativo pode se concentrar no som espacial sem a necessidade de dinamizar com base no formato. Os aplicativos que desejam seu comportamento para a divergência com base no formato de saída podem consultar o formato em uso, mas a abstração significa que um aplicativo não é necessário para lidar com esses formatos.

## <a name="microsoft-spatial-sound-integration-with-audio-renderers"></a>Integração de som espacial da Microsoft com renderizadores de áudio

Como [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) é um coletor de áudio que consome dados, um processador de áudio tem várias opções de como interagir com e entregar dados de áudio para ele. Há três técnicas de integração comumente usadas (e para títulos que usam o middleware de áudio, você pode ver plug-ins equivalentes disponíveis com base nessas opções):

-   **7.1.4 panorâmicas e mestre de voz**: renderizadores que já dão suporte a pontos de extremidade 7,1 podem optar por simplesmente adicionar suporte aos quatro canais de altura adicionais aos quais a cama do canal estático **ISpatialAudioClient** dá suporte. Qualquer movimento panorâmico anteriormente (provavelmente já aproveitando as coordenadas x, y, z) pode ser atualizado para incluir agora esses canais de altura. Isso geralmente oferece menos interrupções ao processador e fluxos de trabalho de áudio de aplicativo, sinal, fluxo e controle de combinação. Sobre fones de ouvido, observe que a combinação completa de aplicativos será espacial – portanto, até mesmo música estéreo pode ser percebida como "externamente" do ouvinte.
-   **Manter o ponto de extremidade existente, além de adicionar um barramento de 7.1.4 (e os panorâmicas)**: alguns títulos podem optar por manter dois pontos de extremidade: seu ponto de extremidades WASAPI estéreo existente (para que o conteúdo "direto para ouvidos" não se destinasse a ser espacial) junto com uma base de canal estático **ISpatialAudioClient** com suporte a 7.1.4 (ou até mesmo a 8.1.4.4). É claro que gerenciar interações entre duas combinações apresenta desafios adicionais aos criadores de conteúdo, embora a sincronização seja mantida, pois as instâncias WASAPI e ISAC ativas em um determinado momento usam o mesmo tamanho de buffer e relógio para processamento.
-   **Usar objetos de som dinâmicos para determinadas vozes ou subcombinações**: a oferta talvez o posicionamento mais detalhado/preciso, mas potencialmente criando opacidade de combinação, essa técnica envolve o uso de objetos de som dinâmicos **ISpatialAudioClient** . Observe que os metadados mais o buffer de áudio é entregue ao renderizador, portanto, esses sons serão opacos para o restante da combinação de aplicativos. Além disso, como há um número limitado de objetos de som dinâmico disponíveis, o renderizador precisará considerar a implementação de técnicas de priorização – remoção, colocalização de som, mesclagem à base do canal estático e assim por diante. Os jogos usaram com frequência essa técnica para sons individuais "Heroes", como um Helicopter que se moverá acima do ouvinte.

Os renderizadores também podem misturar e combinar entre essas abordagens.

## <a name="microsoft-spatial-sound-runtime-resource-implications"></a>Implicações de recursos de tempo de execução de som espacial da Microsoft

No Windows e no Xbox, o número de vozes disponíveis varia de acordo com o formato em uso. Os formatos Dolby Atmos dão suporte a 32 objetos ativos totais (portanto, se uma cama de canal 7.1.4 estiver em uso, 20 objetos de som dinâmicos adicionais poderão estar ativos). O Windows Sonic para fones de ouvido dá suporte a 128 objetos ativos totais, com o canal LFE (efeitos de baixa frequência) que, na verdade, não está sendo contado como um objeto; portanto, quando uma cama de canal 8.1.4.4 está em uso, 112 objetos de som dinâmicos podem estar ativos.

Para Plataforma Universal do Windows aplicativos executados nos consoles do Xbox One Game, a codificação em tempo real (para o Dolby Atmos for Home Theater, o Dolby Atmos para fones de ouvido, o Headphone do DTS: X e o Windows Sonic para fones de ouvido) é executada no hardware sem custo de CPU.

| Formatar                       | Máximo de objetos estáticos (cama do canal) | Máximo de objetos dinâmicos <br> Xbox One | Máximo de objetos dinâmicos <br> Windows | Máximo de objetos dinâmicos <br> HoloLens 2
|------------------------------|----------------------------------|-------------------------------------------|------------------------------------------|------------------------------------------|
| Dolby Atmos (HDMI)           | 12 (7.1.4)                       | 20                                        | 20                                       | NA |
| Dolby Atmos (fones de ouvido & palestrantes internos)     | 17 (8.1.4.4)                     | 16                                        | 16                                       | NA |
| Fone de ouvido DTS: X (fones de ouvido) | 17 (8.1.4.4)        | 16                                        | 32                                      | NA |
| Windows Sonic para fones de ouvido | 17 (8.1.4.4)        | 15                                        | 112                                      | 31 |


Os aplicativos também devem considerar as seguintes implicações de recursos:

-   **Largura de banda de armazenamento/disco**: o conteúdo linear pré-autorizado para o 7.1.4 normalmente será maior do que 7,1 de conteúdo linear (embora os codecs de perceptiva geralmente aproveitem a correlação de canais para tornar isso muito menor do que o 50% mais canais reais de dados de áudio)
-   **Outros custos de processamento de sinal digital**: alguns efeitos globais anteriores agora podem ser instância por objeto de som dinâmico. Além disso, alguns criadores de conteúdo talvez queiram atualizar alguns efeitos de DSP para dar suporte a canais adicionais ou usá-los de forma exclusiva.

## <a name="microsoft-spatial-sound-and-sound-spatialization-cues"></a>Indicações de espacial de som e som espaciais da Microsoft

O som espacial da Microsoft se concentra na simulação de posicionamento de som em uma esfera ideal em volta do ouvinte. O Windows Sonic para fones de ouvido, o Headphone do DTS: X e o Dolby Atmos implementam o mapeamento e a virtualização do palestrante para fones de ouvido, mas observe que muitos outros aspectos da simulação espacial do som, normalmente implementados em modos habilitados para o conteúdo, são deixados para os mecanismos existentes. Os criadores de conteúdo continuam a usar as ferramentas e os processos de jogos existentes que tinham anteriormente para tais indicações espaciais como Doppler, atenuação e filtragem baseadas em distância, oclusão e obstrução e reverberation ambiental.

## <a name="additional-resources"></a>Recursos adicionais

-   [Repositório GitHub de exemplos de sons espaciais da Microsoft](https://github.com/Microsoft/Xbox-ATG-Samples/tree/master/UWPSamples/Audio)
-   O Dolby oferece vários recursos de suporte relacionados ao Dolby Atmos e ao aplicativo de acesso Dolby em <https://developer.dolby.com> .

## <a name="spatial-sound-interfaces"></a>Interfaces de som espaciais



| Interface                                                                              | Descrição                                                                                                                    |
|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient)                                     | Permite que um cliente crie fluxos de áudio que emitem áudio de uma posição em espaço 3D.                                          |
| [**ISpatialAudioObject**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobject)                                     | Representa um objeto que fornece dados de áudio a serem processados de uma posição no espaço 3D, em relação ao usuário.                |
| [**ISpatialAudioObjectRenderStream**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstream)             | Fornece métodos para controlar um fluxo de processamento de objeto de áudio espacial, incluindo iniciar, parar e redefinir o fluxo. |
| [**ISpatialAudioObjectRenderStreamNotify**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioobjectrenderstreamnotify) | Fornece notificações para clientes de áudio espacial responderem às alterações no estado de um ISpatialAudioObjectRenderStream.     |



 

> [!Note]  
> Ao usar as interfaces [**ISpatialAudioClient**](/windows/desktop/api/spatialaudioclient/nn-spatialaudioclient-ispatialaudioclient) em um título de XDK (Xbox One Development Kit), primeiro você deve chamar **EnableSpatialAudio** antes de chamar [**IMMDeviceEnumerator:: EnumAudioEndpoints**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-enumaudioendpoints) ou [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint). A falha em fazer isso resultará em um \_ erro E nointerface ser retornado da chamada para Activate. **EnableSpatialAudio** só está disponível para títulos XDK e não precisa ser chamado para plataforma universal do Windows aplicativos em execução no Xbox One, nem para nenhum dispositivo não Xbox.

 

## <a name="spatial-sound-structures"></a>Estruturas de som espacial



| Estrutura                                                                                                 | Descrição                                                                  |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**SpatialAudioObjectRenderStreamActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioobjectrenderstreamactivationparams) | Representa os parâmetros de ativação para um fluxo de renderização de áudio espacial.          |
| [**SpatialAudioClientActivationParams**](/windows/desktop/api/spatialaudioclient/ns-spatialaudioclient-spatialaudioclientactivationparams)                          | Representa parâmetros de ativação opcionais para um fluxo de renderização de áudio espacial. |



 

## <a name="spatial-sound-enumerations"></a>Enumerações de som espacial



| Enumeração                                | Descrição                                   |
|--------------------------------------------|-----------------------------------------------|
| [**AudioObjectType**](/windows/desktop/api/spatialaudioclient/ne-spatialaudioclient-audioobjecttype) | Especifica o tipo de um ISpatialAudioObject. |



 

 

 



