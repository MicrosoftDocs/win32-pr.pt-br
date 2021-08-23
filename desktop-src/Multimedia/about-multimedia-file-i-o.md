---
title: Sobre e/S de arquivo multimídia
description: Sobre e/S de arquivo multimídia
ms.assetid: d72ba20c-0085-4d5c-9fc6-b9024b575027
keywords:
- Windows multimídia, E/S de arquivo
- multimídia, E/S de arquivo
- entrada multimídia, E/S de arquivo
- E/S de arquivo multimídia, sobre
- E/S de arquivo, sobre
- entrada e saída (E/S), sobre
- E/S (entrada e saída),sobre
- E/S básica
- formato de arquivo de intercâmbio de recursos (PDF)
- CHANG (formato de arquivo de intercâmbio de recursos)
- E/S DO BLUES
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584b736ba41fb0ea7dd5f3e6411e1783964db21a9819fbb98364708196dc2943
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526636"
---
# <a name="about-multimedia-file-io"></a>Sobre e/S de arquivo multimídia

A maioria dos aplicativos multimídia exige entrada e saída de arquivo (E/S) — ou seja, a capacidade de criar, ler e gravar arquivos de disco. Os serviços de E/S de arquivo multimídia fornecem E/S de arquivo armazenado em buffer e sem buffer e suporte para arquivos DEIS. Os serviços são extensíveis com procedimentos personalizados de E/S que podem ser compartilhados entre aplicativos.

A maioria dos aplicativos precisa apenas dos serviços básicos de E/S de arquivo e os serviços de E/S de arquivo DOLS. Aplicativos sensíveis ao desempenho de E/S de arquivo, como aplicativos que transmitem dados do compact disc em tempo real, podem otimizar o desempenho usando serviços para acessar diretamente o buffer de E/S do arquivo. Aplicativos que acessam sistemas de armazenamento personalizados, como arquivos e bancos de dados, podem fornecer seu próprio procedimento de E/S que lê e grava elementos do sistema de armazenamento.

 

 




