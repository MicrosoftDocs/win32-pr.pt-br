---
description: DirectShow Visão geral do sistema
ms.assetid: aea1ab83-4c48-4b61-8a20-0ee6ad62ebe3
title: DirectShow Visão geral do sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fb7855277029adc563cc032740d3a59b3691fcf12ed2b2595d37a1abd0d923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966346"
---
# <a name="directshow-system-overview"></a>DirectShow Visão geral do sistema

**O desafio do multimídia**

Trabalhar com multimídia apresenta vários desafios importantes:

-   Os fluxos de multimídia contêm grandes quantidades de dados, que devem ser processados muito rapidamente.
-   Áudio e vídeo devem ser sincronizados para que sejam iniciados e interrompidos ao mesmo tempo e sejam reproduzidos na mesma taxa.
-   Os dados podem vir de várias fontes, incluindo arquivos locais, redes de computador, difusões de televisão e câmeras de vídeo.
-   Os dados vêm em uma variedade de formatos, como Audio-Video intercalado (AVI), ASF (Advanced Streaming Format), MPEG (Motion Picture Experts Group) e DV (Digital Video).
-   O programador não sabe com antecedência quais dispositivos de hardware estarão presentes no sistema do usuário final.

**a solução DirectShow**

o DirectShow foi projetado para lidar com cada um desses desafios. sua principal meta de design é simplificar a tarefa de criar aplicativos de mídia digital na plataforma Windows, isolando aplicativos das complexidades de transportes de dados, diferenças de hardware e sincronização.

para obter a taxa de transferência necessária para transmitir vídeo e áudio, DirectShow usa Direct3D e DirectSound sempre que possível. Essas tecnologias renderizam dados com eficiência para as placas gráficas e som do usuário. DirectShow sincroniza a reprodução ao encapsular dados de mídia em amostras com carimbo de data/hora. para lidar com a variedade de fontes, formatos e dispositivos de hardware que são possíveis, DirectShow usa uma arquitetura modular, na qual o aplicativo combina e corresponde a diferentes componentes de software chamados *filtros*.

DirectShow fornece filtros que dão suporte à captura e ao ajuste de dispositivos com base no Windows Driver Model (WDM), bem como filtros que dão suporte a vídeo mais antigo para cartões de captura do Windows (VfW) e codecs escritos para as interfaces do gerenciador de compactação de áudio (ACM) e do gerenciador de compactação de vídeo (VCM).

o diagrama a seguir mostra a relação entre um aplicativo, os componentes DirectShow e alguns componentes de hardware e software aos quais o DirectShow dá suporte.

![arquitetura de alto nível](images/arch-oview2.png)

conforme ilustrado aqui, DirectShow filtros se comunicam com, e controlam, uma grande variedade de dispositivos, incluindo o sistema de arquivos local, o sintonizador de TV e os cartões de captura de vídeo, codecs VfW, a tela de vídeo (por meio do DirectDraw ou GDI) e a placa de som (por meio do DirectSound). portanto, DirectShow isola o aplicativo de muitas das complexidades desses dispositivos. o DirectShow também fornece filtros nativos de compactação e descompactação para determinados formatos de arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre DirectShow](about-directshow.md)
</dt> </dl>

 

 



