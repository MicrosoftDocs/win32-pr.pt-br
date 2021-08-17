---
title: Criando arquivos MIDI
description: Criando arquivos MIDI
ms.assetid: 2fca3b41-14f9-4eaf-9fdb-8f952c834302
keywords:
- Windows multimídia, criando arquivos MIDI
- multimídia, criando arquivos MIDI
- áudio multimídia, criando arquivos MIDI
- áudio, criando arquivos MIDI
- MIDI (Interface Digital do Instrument Instrument), criando arquivos
- MIDI (Interface Digital do Instrument Instrument), criando arquivos
- criando arquivos MIDI, sobre
- MMA (Associação de Fabricantes MIDI)
- MMA (Associação de Fabricantes MIDI)
- Especificação detalhada do MIDI
- Especificação de Arquivos MIDI Padrão
- Especificação geral de MIDI (GM)
- Especificação gm (MIDI geral)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e2a229a8e9208645fa7ffae296c004b833156b240f063066be2a8732175054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144600"
---
# <a name="creating-midi-files"></a>Criando arquivos MIDI

As especificações da MIDI (Interface Digital) do Instrument Instrument são publicadas pelo e são material protegido por direitos autorais da MMA (Associação de Fabricantes MIDI). A lista a seguir descreve as especificações que são de maior interesse geral:

## <a name="midi-detailed-specification"></a>Especificação detalhada do MIDI

A Especificação Detalhada do MIDI explica os protocolos de hardware e software MIDI. Isso é útil para aqueles que desenvolvem aplicativos multimídia que implementam suporte a MIDI usando funções MIDI para registrar, editar e/ou reproduzir dados MIDI.

## <a name="standard-midi-files-10"></a>Arquivos MIDI Padrão 1.0

A especificação de Arquivos MIDI Padrão define uma maneira de trocar dados MIDI com carimbo de data/hora entre diferentes aplicativos na mesma plataforma de hardware ou em diferentes plataformas de hardware. Isso é útil para desenvolvedores que escrevem aplicativos que leem e analisaram arquivos de disco contendo dados MIDI e/ou gravar arquivos de dados MIDI no disco.

## <a name="general-midi-system---level-1"></a>Sistema MIDI geral – Nível 1

A especificação geral MIDI (GM) define uma configuração MIDI mínima de um "Sistema MIDI Geral". Esse sistema consiste em uma classe específica de dispositivos de reprodução MIDI e é de interesse para desenvolvedores multimídia que autor de arquivos MIDI. A maioria das placas de som de PC e sintetizadores MIDI fabricados atualmente são compatíveis com a especificação GM. Os arquivos MIDI que são destinados à especificação GM geralmente devem parecer como deveriam parecer, independentemente do dispositivo compatível com GM em que eles são tocadas.

Para permitir que os arquivos MIDI sejam um formato viável para representar música na computação multimídia, o Windows segue a especificação Geral do Sistema MIDI Nível 1. Os tópicos a seguir fornecem diretrizes de autor MIDI adicionais:

-   [Diretrizes de autor para arquivos MIDI](authoring-guidelines-for-midi-files.md)
-   [Atribuições de patch MIDI Padrão](standard-midi-patch-assignments.md)
-   [Atribuições de chave MIDI padrão](standard-midi-key-assignments.md)

 

 




