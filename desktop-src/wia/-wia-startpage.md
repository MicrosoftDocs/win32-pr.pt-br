---
description: O WIA (Windows Image Acquisition) é a plataforma de aquisição de imagens ainda na família de sistemas operacionais Windows, começando com o Windows Millennium Edition (Windows me) e o Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: WIA (Windows Image Acquisition)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 664b5accaa1312eae3baf6161e41c9c65e718c69
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443087"
---
# <a name="windows-image-acquisition-wia"></a>WIA (Windows Image Acquisition)

O WIA (Windows Image Acquisition) é a plataforma de aquisição de imagens ainda na família de sistemas operacionais Windows, começando com o Windows Millennium Edition (Windows me) e o Windows XP.

-   [Introdução](#introduction)
-   [Benefícios da aquisição de imagens do Windows 2,0](#benefits-of-windows-image-acquisition-20)
    -   [Para gravadores de aplicativos](#for-application-writers)
    -   [Para fabricantes de dispositivos](#for-device-manufactures)
    -   [Para usuários do scanner](#for-scanner-users)
-   [Desenvolvimento de aquisição de imagens do Windows](#development-of-windows-image-acquisition)
-   [Visão geral da aquisição de imagens do Windows](#overview-of-windows-image-acquisition)
-   [Fatos sobre a aquisição de imagem do Windows 2,0](#facts-about-windows-image-acquisition-20)
-   [Público do desenvolvedor](#developer-audience)
-   [Requisitos de tempo de execução](#run-time-requirements)
-   [Tópicos da WIA](#wia-topics)

## <a name="introduction"></a>Introdução

A plataforma WIA permite que aplicativos de geração de imagens/gráficos interajam com o hardware de geração de imagens e padronize a interação entre diferentes aplicativos e scanners. Isso permite que esses aplicativos diferentes se comuniquem e interajam com esses diferentes scanners sem exigir que os gravadores de aplicativo e os fabricantes de scanner personalizem seus aplicativos ou drivers para cada combinação de dispositivo de aplicativo.

![gráfico mostrando a arquitetura básica do WIA como uma camada bidirecional entre aplicativos e dispositivos de geração de imagens. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Benefícios da aquisição de imagens do Windows 2,0

A WIA fornece benefícios para desenvolvedores de aplicativos, fabricantes de dispositivos e usuários de scanners que precisam interagir com hardware de imagem.

### <a name="for-application-writers"></a>Para gravadores de aplicativos

-   O Windows executa um processo de certificação para drivers WIA para que os aplicativos WIA sejam compatíveis em nível base com todos os scanners baseados em WIA.
-   Os drivers WIA são carregados no processo do serviço WIA, fornecendo, assim, um ambiente de driver mais estável.
-   Os aplicativos podem ser iniciados no botão verificação do scanner por meio de eventos de push com suporte pelo subsistema WIA.
-   O WIA inclui um filtro de segmentação padrão que todos os drivers podem aproveitar; dessa forma, os aplicativos não precisam escrever código para verificação de várias regiões para fins como, por exemplo, separar um grande número de fotos espalhadas por um scanner de mesa.

### <a name="for-device-manufactures"></a>Para fabricantes de dispositivos

-   O processo de certificação de driver WIA ajuda os desenvolvedores de driver a estabelecerem que seu driver é compatível com WIA.
-   Os drivers WIA podem aproveitar um filtro de segmentação interno, filtro de processamento de imagens e manipulador de erros, se escolherem fazer isso.
-   Os scanners baseados em WIA funcionam imediatamente no Windows com os aplicativos de verificação do Windows, como o Windows fax e o scan e o Paint.
-   Os drivers WIA oferecem melhor integração com o Windows, como a experiência completa do dispositivo.
-   A versão Windows Vista inclui um driver de classe WSD-WIA que permite que todos os dispositivos em conformidade com o protocolo Web Services for scanner (WS-Scan) funcionem com aplicativos WIA sem nenhum driver ou software adicional.

### <a name="for-scanner-users"></a>Para usuários do scanner

-   Os scanners baseados em WIA podem ser usados de aplicativos do Windows, como o fax e a verificação do Windows e a pintura sem a necessidade de qualquer software adicional.
-   Os aplicativos e scanners baseados em WIA também podem aproveitar os complementos do WIA, como o filtro de segmentação, que permite recursos como o processamento de várias imagens no scanner e a verificação de todos os arquivos individuais sem a intervenção do usuário.
-   Os dispositivos baseados em WIA oferecem uma integração muito melhor com outros recursos do Windows, como o recurso de estágio do dispositivo para o Windows 7.
-   A WIA fornece uma experiência de verificação mais robusta, estável e confiável, isolando o driver e o aplicativo.

## <a name="development-of-windows-image-acquisition"></a>Desenvolvimento de aquisição de imagens do Windows

A arquitetura de geração de imagens no Windows 2000 e no Windows 95 ou posterior consistiu em uma abstração de hardware de nível baixo, STI (arquitetura de imagem ainda) e um conjunto de APIs de alto nível conhecido como TWAIN. No Windows XP e no Windows me WIA foi introduzido. O WIA é uma arquitetura de geração de imagens que se baseia em STI e não requer TWAIN, embora o TWAIN ainda tenha suporte junto com o WIA.

O WIA 1,0 foi introduzido no Windows me e no Windows XP e dá suporte a scanners, câmeras digitais e equipamentos de vídeo digital. O WIA 2,0 foi lançado com o Windows Vista. A WIA 2,0 é destinada a scanners, mas continua a oferecer suporte para aplicativos e dispositivos WIA 1,0 herdados por meio de uma camada de compatibilidade WIA 1,0 para a WIA 2,0 fornecida pelo serviço WIA. No entanto, o suporte a conteúdo de vídeo foi removido do WIA para Windows Vista. Recomendamos a API de dispositivos portáteis do Windows (WPD) para câmeras digitais e equipamentos de vídeo digital no futuro. O WIA 1,0, bem como os drivers STI TWAIN ainda têm suporte diretamente no Windows Vista e no Windows 7 juntamente com drivers de dispositivo e aplicativos de geração de imagens nativos do WIA 2,0.

## <a name="overview-of-windows-image-acquisition"></a>Visão geral da aquisição de imagens do Windows

O WIA fornece uma estrutura que permite que um dispositivo apresente seus recursos exclusivos ao sistema operacional e permite que aplicativos de geração de imagens invoquem esses recursos exclusivos.

A plataforma WIA inclui um protocolo de aquisição de dados, uma DDI (interface e modelo de driver de dispositivo), uma API e um serviço WIA dedicado. A plataforma também inclui um conjunto de drivers de modo kernel internos que dão suporte à comunicação com dispositivos de geração de imagens conectados localmente por meio de interfaces USB, serial/paralela, SCSI e FireWire. O subsistema WIA também inclui uma camada de compatibilidade transparente que permite que aplicativos compatíveis com TWAIN empreguem e usem dispositivos baseados em driver WIA.

Os dispositivos de imagem conectados à rede que dão suporte ao protocolo WSD (serviços Web para dispositivos) também podem ser usados de aplicativos de geração de imagens compatíveis com WIA no Windows Vista e Windows 7 prontos para uso por meio de um driver de classe WSD-WIA fornecido como parte do Windows Vista. O driver de classe converte chamadas WIA em chamadas WSD e vice-versa e faz com que os aplicativos WIA já existentes funcionem com scanners baseados em WSD sem nenhum driver adicional.

Os drivers WIA são compostos por um componente de interface do usuário e um componente de driver de núcleo, carregados em dois espaços de processo diferentes: interface de usuário no espaço do aplicativo e o núcleo do driver no espaço de serviço WIA. O serviço é executado no contexto do sistema local no Windows XP e executado no contexto de serviço local, começando com o Windows Server 2003 e o Windows Vista para segurança aprimorada contra bugs ou drivers mal-intencionados.

![gráfico mostrando a arquitetura do WIA e como ele funciona como um serviço.](images/wia-arch.png)

O conjunto de API WIA expõe aplicativos de geração de imagens para a funcionalidade de hardware de aquisição de imagem ainda, fornecendo suporte para:

-   Enumeração de dispositivos de aquisição de imagem disponíveis.
-   Criando conexões a vários dispositivos simultaneamente.
-   Consultando Propriedades de dispositivos de maneira padrão e expansível.
-   Aquisição de dados do dispositivo usando mecanismos de transferência padrão e de alto desempenho.
-   Manter Propriedades de imagem entre transferências de dados.
-   Notificação de status do dispositivo e manipulação de eventos de verificação.

O Windows adicionou suporte de script ao WIA ao liberar a biblioteca de automação WIA no 2002 que foi incorporado no Windows Vista como camada de automação WIA (aquisição de imagem do Windows) e continua a fazer parte do Windows 7. A biblioteca de automação do WIA fornece recursos de aquisição de imagem de ponta a ponta para ambientes de desenvolvimento de aplicativos habilitados para automação e linguagens de programação, como o Microsoft Visual Basic 6,0, o Active Server Pages (ASP), o VBScript e o C \# .

Para o Windows 7, as APIs WIA têm suporte adicional para complementar o suporte à varredura por push já existente.

-   Verificação iniciada automaticamente do dispositivo com parâmetros de verificação configurados no scanner no painel frontal do dispositivo.
-   Seleção de origem automática para verificação iniciada pelo dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Fatos sobre a aquisição de imagem do Windows 2,0

-   O mecanismo de transferência de dados no WIA 2,0 é baseado em fluxo. A abstração de fluxo remove a distinção entre diferentes tipos de transferência e também permite o intercâmbio de metadados acordados mutuamente entre o dispositivo e o aplicativo.
-   O subsistema WIA 2,0 também inclui um complemento básico de driver de filtro de processamento de imagens que é opcionalmente substituível pelo driver do scanner, se o driver optar por fornecer um filtro de processamento de imagem personalizado. O filtro interno permite o pós-processamento do processamento de imagens adquiridas por meio do verificador. O filtro de processamento de imagens também permite visualizações de software ao vivo quando pequenas configurações, como brilho e contraste, são ajustadas.
-   O filtro de segmentação é outro componente de WIA útil que pode ser substituído por um filtro mais personalizado pelo driver do scanner. O filtro de segmentação pode ser usado para verificação de várias regiões. A verificação de várias regiões, como exemplo, permite que um aplicativo detecte automaticamente diferentes regiões de verificação sem qualquer intervenção do usuário, como identificar várias fotos que dependem aleatoriamente da mesa do scanner.
-   O WIA 2,0 fornece um manipulador de erro substituível/extensível para lidar normalmente e, possivelmente, recuperar de erros de software, hardware e configuração e atrasos. O manipulador de erro é outro componente WIA que pode ser substituído por uma versão mais personalizada pelo driver do scanner. Essa extensão fornece mensagens de status e de erro durante as aquisições de dados, como "aquecimento da lâmpada", "tampa aberta", "obstrução de papel" e assim por diante. Essa extensão também permite o suporte de limpeza para "operações de cancelamento".

## <a name="developer-audience"></a>Público do desenvolvedor

A API WIA foi projetada para uso por programadores C/C++. É necessário estar familiarizado com as interfaces GUI do Windows e Component Object Model (COM).

Para os desenvolvedores familiarizados com o Microsoft Visual Basic 6,0, o Active Server Pages (ASP) ou o scripting, a WIA fornece uma camada de automação para o Windows XP Service Pack 1 (SP1) ou posterior que se baseia e simplifica o acesso à Fundação fornecida pelo C/C++. Para obter informações sobre a camada de automação, consulte [camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

> [!Note]  
> A camada de automação WIA substitui o script da aquisição de imagem do Windows (WIA) 1,0.

 

## <a name="run-time-requirements"></a>Requisitos de Run-Time

Os aplicativos que usam a API WIA exigem o Windows XP ou posterior.

## <a name="wia-topics"></a>Tópicos da WIA

Os tópicos da WIA são organizados conforme mostrado na tabela a seguir.



|  Tópico                                                                                                                            | Descrição                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Sobre a aquisição de imagens do Windows](-wia-about-windows-image-acquisition.md)                                                  | Informações gerais sobre WIA                                                                     |
| [Drivers de aquisição de imagem do Windows](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Desenvolvimento de driver WIA                                                                            |
| [Camada de automação de aquisição de imagem do Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Camada de automação WIA                                                                              |
| [Tutorial do WIA](-wia-wia-tutorial.md)                                                                                        | Explicação do código incluído no Software Development Kit (SDK) que se concentra em tarefas específicas |
| [Referência](-wia-reference.md)                                                                                              | Informações sobre interfaces, métodos, objetos e tipos de dados WIA usados em C/C++ e scripts.      |



 

 

 
