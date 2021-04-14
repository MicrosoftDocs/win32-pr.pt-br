---
description: Visão geral do sistema DirectShow
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: Visão geral do sistema DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833fed4031c95ddb4ecbf91e7bb27c27741acc18
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500184"
---
# <a name="directshow-system-overview"></a>Visão geral do sistema DirectShow

**O desafio do multimídia**

Trabalhar com multimídia apresenta vários desafios importantes:

-   Os fluxos de multimídia contêm grandes quantidades de dados, que devem ser processados muito rapidamente.
-   Áudio e vídeo devem ser sincronizados para que sejam iniciados e interrompidos ao mesmo tempo e sejam reproduzidos na mesma taxa.
-   Os dados podem vir de várias fontes, incluindo arquivos locais, redes de computador, difusões de televisão e câmeras de vídeo.
-   Os dados vêm em uma variedade de formatos, como Audio-Video intercalado (AVI), ASF (Advanced Streaming Format), MPEG (Motion Picture Experts Group) e DV (Digital Video).
-   O programador não sabe com antecedência quais dispositivos de hardware estarão presentes no sistema do usuário final.

**A solução do DirectShow**

O DirectShow foi projetado para atender a cada um desses desafios. Sua principal meta de design é simplificar a tarefa de criar aplicativos de mídia digital na plataforma Windows, isolando aplicativos das complexidades de transportes de dados, diferenças de hardware e sincronização.

Para obter a taxa de transferência necessária para transmitir vídeo e áudio, o DirectShow usa Direct3D e DirectSound sempre que possível. Essas tecnologias renderizam dados com eficiência para as placas gráficas e som do usuário. O DirectShow sincroniza a reprodução ao encapsular dados de mídia em amostras com carimbo de data/hora. Para lidar com a variedade de fontes, formatos e dispositivos de hardware que são possíveis, o DirectShow usa uma arquitetura modular, na qual o aplicativo combina e corresponde a diferentes componentes de software chamados *filtros*.

O DirectShow fornece filtros que dão suporte à captura e ao ajuste de dispositivos baseados no Windows Driver Model (WDM), bem como filtros que dão suporte a placas de captura VfW (vídeo mais antigo para Windows) e codecs escritos para as interfaces do Gerenciador de compactação de áudio (ACM) e do Gerenciador de compactação de vídeo (VCM).

O diagrama a seguir mostra a relação entre um aplicativo, os componentes do DirectShow e alguns dos componentes de hardware e software que o DirectShow suporta.

![arquitetura de alto nível](images/arch-oview2.png)

Conforme ilustrado aqui, os filtros do DirectShow se comunicam com, e controlam, uma ampla variedade de dispositivos, incluindo o sistema de arquivos local, o sintonizador de TV e os cartões de captura de vídeo, os codecs VfW, a tela de vídeo (por meio do DirectDraw ou GDI) e a placa de som (por meio do DirectSound). Portanto, o DirectShow isola o aplicativo de muitas das complexidades desses dispositivos. O DirectShow também fornece filtros nativos de compactação e descompactação para determinados formatos de arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o DirectShow](about-directshow.md)
</dt> </dl>

 

 



