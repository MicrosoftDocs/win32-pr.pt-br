---
title: Criando arquivos MIDI
description: Criando arquivos MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Multimídia do Windows, criando arquivos MIDI
- multimídia, criando arquivos MIDI
- áudio de multimídia, criando arquivos MIDI
- áudio, criando arquivos MIDI
- MIDI (interface digital de instrumento musical), criando arquivos
- MIDI (interface digital de instrumentos musicais), criando arquivos
- Criando arquivos MIDI, sobre
- Associação de fabricantes de MIDI (MMA)
- MMA (Associação de fabricantes de MIDI)
- Especificação detalhada de MIDI
- Especificação de arquivos MIDI padrão
- Especificação MIDI (GM) geral
- Especificação de GM (MIDI geral)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ccc25e73d6a28afc9001f2862870f1fa1a9ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005238"
---
# <a name="creating-midi-files"></a>Criando arquivos MIDI

As especificações de MIDI (interface digital de instrumento musical) são publicadas pelo e são materiais com direitos autorais da MMA (Associação de fabricantes de MIDI). A lista a seguir descreve as especificações que são do maior interesse geral:

## <a name="midi-detailed-specification"></a>Especificação detalhada de MIDI

A especificação de MIDI detalhado explica os protocolos de hardware e software MIDI. Isso é útil para o desenvolvimento de aplicativos multimídia que implementam o suporte a MIDI usando funções de MIDI para gravar, editar e/ou reproduzir dados MIDI.

## <a name="standard-midi-files-10"></a>Arquivos MIDI padrão 1,0

A especificação de arquivos MIDI padrão define uma maneira de trocar dados de MIDI com carimbo de data/hora entre diferentes aplicativos no mesmo ou em plataformas de hardware diferentes. Isso é útil para desenvolvedores que gravam aplicativos que lêem e analisam arquivos de disco que contêm dados MIDI e/ou gravam arquivos de dados MIDI no disco.

## <a name="general-midi-system---level-1"></a>Sistema MIDI geral-nível 1

A especificação MIDI geral (GM) define uma configuração de MIDI mínima de um "sistema MIDI geral". Esse sistema consiste em uma classe específica de dispositivos de reprodução de MIDI e é de seu interesse para desenvolvedores de multimídia que criam arquivos MIDI. A maioria das placas de som do PC e sintetizadores MIDI fabricados atualmente são compatíveis com a especificação GM. Os arquivos MIDI que são criados para a especificação do GM geralmente devem soar como se destinam a soar, não importa em qual dispositivo compatível com GM eles são executados.

Para permitir que os arquivos MIDI sejam um formato viável para representar música na computação multimídia, o Windows segue a especificação geral do sistema MIDI 1. Os tópicos a seguir fornecem diretrizes adicionais de criação de MIDI:

-   [Diretrizes de criação para arquivos MIDI](authoring-guidelines-for-midi-files.md)
-   [Atribuições de patch de MIDI padrão](standard-midi-patch-assignments.md)
-   [Atribuições de chave MIDI padrão](standard-midi-key-assignments.md)

 

 




