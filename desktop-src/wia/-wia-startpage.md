---
description: Windows A WIA (Aquisição de Imagem) é a plataforma de aquisição de imagem ainda na família Windows de sistemas operacionais, começando com o Windows Windows Edition Windows Me) e o Windows XP.
ms.assetid: 8f32422e-25ec-48bc-9d79-57dbb3b53e93
title: WIA (Windows Image Acquisition)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e467d76f054a8cccb4c309f69b211d0d3d6fbe949625324c871319028aa78ebc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056996"
---
# <a name="windows-image-acquisition-wia"></a>WIA (Windows Image Acquisition)

Windows A WIA (Aquisição de Imagem) é a plataforma de aquisição de imagem ainda na família Windows de sistemas operacionais, começando com o Windows Windows Edition Windows Me) e o Windows XP.

-   [Introdução](#introduction)
-   [Benefícios da aquisição Windows imagem 2.0](#benefits-of-windows-image-acquisition-20)
    -   [Para autores de aplicativos](#for-application-writers)
    -   [Para fabricantes de dispositivos](#for-device-manufactures)
    -   [Para usuários do scanner](#for-scanner-users)
-   [Desenvolvimento de aquisição Windows imagem](#development-of-windows-image-acquisition)
-   [Visão geral da aquisição Windows imagem](#overview-of-windows-image-acquisition)
-   [Fatos sobre Windows aquisição de imagem 2.0](#facts-about-windows-image-acquisition-20)
-   [Público-alvo do desenvolvedor](#developer-audience)
-   [Requisitos de tempo de executar](#run-time-requirements)
-   [Tópicos do WIA](#wia-topics)

## <a name="introduction"></a>Introdução

A plataforma WIA permite que aplicativos de geração de imagens/gráficos interajam com o hardware de geração de imagens e padroniza a interação entre diferentes aplicativos e scanners. Isso permite que esses diferentes aplicativos se comajam e interajam com esses scanners diferentes sem exigir que os autores de aplicativos e os fabricantes do scanner personalizem seus aplicativos ou drivers para cada combinação de aplicativo-dispositivo.

![gráfico mostrando a arquitetura básica do wia como uma camada de duas vias entre aplicativos de geração de imagens e dispositivos. ](images/wia-diagram1.png)

## <a name="benefits-of-windows-image-acquisition-20"></a>Benefícios da aquisição Windows imagem 2.0

O WIA oferece benefícios para desenvolvedores de aplicativos, fabricantes de dispositivos e usuários do scanner que precisam interagir com o hardware de geração de imagens.

### <a name="for-application-writers"></a>Para autores de aplicativos

-   Windows executa um processo de certificação para drivers WIA para que os aplicativos WIA sejam compatíveis no nível base com todos os scanners baseados em WIA.
-   Os drivers WIA são carregados no processo de serviço WIA, fornecendo um ambiente de driver mais estável.
-   Os aplicativos podem ser iniciados no botão de verificação do scanner por meio de eventos de push com suporte pelo subsistema WIA.
-   O WIA inclui um filtro de segmentação padrão que todos os drivers podem aproveitar; Dessa forma, os aplicativos não têm que escrever código para verificação de várias regiões para fins como separar um grande número de fotos distribuídas em um scanner de flatbed.

### <a name="for-device-manufactures"></a>Para fabricantes de dispositivos

-   O processo de certificação de driver WIA ajuda os desenvolvedores de driver a estabelecer que seu driver é compatível com WIA.
-   Os drivers WIA podem aproveitar um filtro de segmentação integrado, um filtro de processamento de imagem e um manipulador de erros, se optarem por fazer isso.
-   Os scanners baseados em WIA funcionam imediatamente no Windows com Windows de verificação de aplicativos, como fax Windows e verificação e Paint.
-   Os drivers WIA oferecem melhor integração com Windows, como a experiência completa do dispositivo.
-   Windows A versão do Vista inclui um driver de classe WSD-WIA que permite que todos os dispositivos em conformidade com o protocolo WS-Scan (Serviços Web para Scanner) funcionem com aplicativos WIA sem nenhum driver ou software adicional.

### <a name="for-scanner-users"></a>Para usuários do scanner

-   Os scanners baseados em WIA podem ser usados Windows aplicativos como fax Windows e verificação e Paint sem a necessidade de nenhum software adicional.
-   Os scanners e aplicativos baseados em WIA também podem aproveitar os complementos do WIA, como o filtro de segmentação, que permite recursos como o processamento de várias imagens no scanner e a verificação de todos em arquivos individuais sem intervenção do usuário.
-   Os dispositivos baseados em WIA oferecem uma integração muito melhor com outros recursos Windows, como o recurso Device Stage para Windows 7.
-   O WIA fornece uma experiência de verificação mais robusta, estável e confiável, isolando o driver e o aplicativo.

## <a name="development-of-windows-image-acquisition"></a>Desenvolvimento de aquisição Windows imagem

A arquitetura de geração de imagens no Windows 2000 e no Windows 95 ou posterior consistia em uma abstração de hardware de baixo nível, a ARQUITETURA DE Imagem Ainda (NUMA) e um conjunto de APIs de alto nível conhecido como LTD. No Windows XP e Windows Me WIA foi introduzido. O WIA é uma arquitetura de geração de imagens que se baseia no TAMBÉM E não requer o VALOR, embora o TAMBÉM ainda tenha suporte junto com o WIA.

O WIA 1.0 foi introduzido no Windows Me e Windows XP e dá suporte a scanners, câmeras digitais e equipamentos de vídeo digital. O WIA 2.0 foi lançado com Windows Vista. O WIA 2.0 é destinado a scanners, mas continua a oferecer suporte para aplicativos e dispositivos WIA 1.0 herdados por meio de uma camada de compatibilidade WIA 1.0 para WIA 2.0 fornecida pelo serviço WIA. No entanto, o suporte ao conteúdo de vídeo foi removido do WIA para Windows Vista. É recomendável Windows API wpd (dispositivos portáteis) para câmeras digitais e equipamentos de vídeo digital no futuro. O WIA 1.0, bem como os drivers DOIS, ainda têm suporte diretamente no Windows Vista e no Windows 7, juntamente com drivers de dispositivo WIA 2.0 nativos e aplicativos de imagens.

## <a name="overview-of-windows-image-acquisition"></a>Visão geral da aquisição Windows imagem

O WIA fornece uma estrutura que permite que um dispositivo apresente seus recursos exclusivos ao sistema operacional e permite que aplicativos de imagens invoquem esses recursos exclusivos.

A plataforma WIA inclui um protocolo de aquisição de dados, um DDI (Device Driver Model and Interface), uma API e um serviço WIA dedicado. A plataforma também inclui um conjunto de drivers de modo kernel integrados que suportam comunicação com dispositivos de imagens conectados localmente por meio de interfaces USB, serial/paralela, SCSI e FireWire. O subsistema WIA também inclui uma camada de compatibilidade transparente que permite que os aplicativos compatíveis com o WIFI utilizem e usem dispositivos baseados em driver WIA.

Dispositivos de imagens conectados à rede que são compatíveis com o protocolo WSD (Serviços Web para Dispositivos) também podem ser usados em aplicativos de imagens em conformidade com WIA no Vista do Windows e no Windows 7, por meio de um driver de classe WSD-WIA enviado como parte do Windows Vista. O driver de classe converte chamadas WIA em chamadas WSD e vice-versa e faz com que os aplicativos WIA já existentes funcionem com scanners baseados em WSD sem nenhum driver adicional.

Os drivers WIA são feitos de um componente de interface do usuário e um componente de driver principal, carregados em dois espaços de processo diferentes: interface do usuário no espaço do aplicativo e o núcleo do driver no espaço de serviço WIA. O serviço é executado no contexto do Sistema Local no Windows XP e é executado no contexto do Serviço Local, começando com o Windows Server 2003 e o Windows Vista para aumentar a segurança contra drivers mal-intencionados ou mal-intencionados.

![gráfico mostrando a arquitetura do wia e como ele opera como um serviço.](images/wia-arch.png)

O conjunto de API do WIA expõe aplicativos de geração de imagens para a funcionalidade de hardware de aquisição de imagem, fornecendo suporte para:

-   Enumeração de dispositivos de aquisição de imagem disponíveis.
-   Criando conexões com vários dispositivos simultaneamente.
-   Consultar propriedades de dispositivos de maneira padrão e expansível.
-   Aquisição de dados do dispositivo usando mecanismos de transferência padrão e de alto desempenho.
-   Manter propriedades de imagem entre transferências de dados.
-   Notificação do status do dispositivo e manipulação de eventos de verificação.

Windows adicionado suporte a scripts ao WIA liberando a Biblioteca de Automação do WIA em 2002 que foi incorporada no Windows Vista como camada de automação wia (aquisição de imagem) do Windows e continua fazendo parte do Windows 7. A Biblioteca de Automação do WIA fornece recursos de aquisição de imagem de ponta a ponta para ambientes de desenvolvimento de aplicativos habilitados para automação e linguagens de programação, como Microsoft Visual Basic 6.0, ASP (Páginas Active Server), VBScript e \# C.

Por Windows 7, as APIs wia têm suporte adicional para complementar o suporte de verificação por push já existente.

-   Verificação iniciada pelo dispositivo automaticamente com parâmetros de verificação configurados no scanner no painel frontal do dispositivo.
-   Seleção automática de origem para verificação iniciada pelo dispositivo.

## <a name="facts-about-windows-image-acquisition-20"></a>Fatos sobre Windows aquisição de imagem 2.0

-   O mecanismo de transferência de dados no WIA 2.0 é baseado em fluxo. A abstração de fluxo remove a distinção entre diferentes tipos de transferência e também permite a troca de metadados mutuamente combinados entre o dispositivo e o aplicativo.
-   O subsistema WIA 2.0 também inclui um complemento de driver de filtro de processamento de imagem básico que é opcionalmente substituível pelo driver do scanner, se o driver optar por fornecer um filtro de processamento de imagem personalizado. O filtro integrado permite o pós-processamento de imagens adquiridas por meio do scanner. O filtro de processamento de imagem também permite visualizações de software ao vivo quando configurações pequenas, como brilho e contraste, são ajustadas.
-   O filtro de segmentação é outro componente DE WIA útil que pode ser substituído por um filtro mais personalizado pelo driver do scanner. O filtro de segmentação pode ser usado para verificação de várias regiões. A verificação de várias regiões, por exemplo, permite que um aplicativo detecte automaticamente diferentes regiões de verificação sem nenhuma intervenção do usuário, como identificar várias fotos aleatoriamente no flatbed do scanner.
-   O WIA 2.0 fornece um manipulador de erros substituível/extensível para tratar normalmente e possivelmente recuperar erros e atrasos de software, hardware e configuração. O manipulador de erros é outro componente WIA que pode ser substituído por uma versão mais personalizada pelo driver do scanner. Essa extensão fornece mensagens de status e erro durante aquisições de dados, como "Aquecimento da lâmpada", "Cobrir aberto", "Papel emperramento" e assim por diante. Essa extensão também permite o suporte mais limpo para "Cancelar operações".

## <a name="developer-audience"></a>Público-alvo do desenvolvedor

A API do WIA foi projetada para uso por programadores C/C++. A familiaridade com as interfaces DE WINDOWS gui e Component Object Model (COM) é necessária.

Para desenvolvedores familiarizados com o Microsoft Visual Basic 6.0, as PÁGINAS do Active Server (ASP) ou scripts, o WIA fornece uma camada de automação para o Windows SP1 (Pacote de Serviço XP 1) ou posterior que se baseia e simplifica o acesso à base fornecida pelo C/C++. Para obter informações sobre a camada de automação, [consulte Windows de Automação](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)de Aquisição de Imagem .

> [!Note]  
> A Camada de Automação do WIA é Windows script WIA (Aquisição de Imagem) 1.0.

 

## <a name="run-time-requirements"></a>Run-Time requisitos

Os aplicativos que usam a API wia exigem Windows XP ou posterior.

## <a name="wia-topics"></a>Tópicos do WIA

Os tópicos do WIA são organizados conforme mostrado na tabela a seguir.



|  Tópico                                                                                                                            | Descrição                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [Sobre a aquisição Windows imagem](-wia-about-windows-image-acquisition.md)                                                  | Informações gerais sobre o WIA                                                                     |
| [Windows Drivers de aquisição de imagem](/windows-hardware/drivers/image/windows-image-acquisition-drivers)                  | Desenvolvimento de driver WIA                                                                            |
| [Windows Camada de automação de aquisição de imagem](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage) | Camada de Automação do WIA                                                                              |
| [Tutorial do WIA](-wia-wia-tutorial.md)                                                                                        | Explicação do código incluído no Software Development Kit (SDK) que se concentra em tarefas específicas |
| [Referência](-wia-reference.md)                                                                                              | Informações sobre interfaces, métodos, objetos e tipos de dados WIA usados em C/C++ e scripts.      |



 

 

 
