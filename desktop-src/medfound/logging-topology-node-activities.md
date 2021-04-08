---
description: Registrando atividades do nó de topologia
ms.assetid: 853b3900-1214-43b9-bf0e-e45c1159c5f1
title: Registrando atividades do nó de topologia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ca83d0513b97d053e27388bd0f2a418dfb253
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010636"
---
# <a name="logging-topology-node-activities"></a>Registrando atividades do nó de topologia

TopoEdit fornece a opção para coletar informações de log para um nó de transformação ou um nó de saída de uma topologia.

## <a name="to-setup-logging"></a>Para configurar o log

1.  No **painel topologia**, selecione um nó de transformação ou um nó de saída clicando nele.

2.  No menu **ferramentas** , clique em **Spy selecione nó selecionado**.

Durante a compilação da topologia, todas as chamadas de método no nó selecionado são registradas em um arquivo de texto. Isso é salvo na pasta em que o arquivo de mídia está localizado. O arquivo de log é salvo com o nome do nó e o identificador do nó de topologia exclusivo. Isso garante que nenhum outro nó grave no log. Para obter o identificador programaticamente, chame [**IMFTopologyNode:: GetTopoNodeID**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-gettoponodeid).

Veja a seguir um trecho de um arquivo de log.

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729720 1 02729760) returns 80004001`

`GetInputCurrentType(0 02C9F4A4) returns c00d6d60`

`GetStreamCount(02C9F518 02C9F514) returns 0`

`GetStreamIDs(1 02729760 1 02729720) returns 80004001`

`SetInputType(0 0012F8D8 0) returns 0`

`--> Arg(2, in) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=WMAudioV8, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=2048, AVG_BYTES_PER_SECOND=12000, BITS_PER_SAMPLE=16, USER_DATA=<BLOB>, {9D62927D-36BE-4CF2-B5C4-A3926E3E8711}=5760, {9D62927F-36BE-4CF2-B5C4-A3926E3E8711}=674,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputCurrentType(0 02C9F4B0) returns c00d6d60`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729640 1 02729720) returns 80004001`

`GetOutputAvailableType(0 0 02C9F4B0) returns 0`

`--> Arg(3, out) Media type: Audio: MAJOR_TYPE=Audio, PREFER_WAVEFORMATEX=1, SUBTYPE=Float, NUM_CHANNELS=2, SAMPLES_PER_SECOND=48000, BLOCK_ALIGNMENT=8, AVG_BYTES_PER_SECOND=384000, BITS_PER_SAMPLE=32, ALL_SAMPLES_INDEPENDENT=1, FIXED_SIZE_SAMPLES=1,`

`GetStreamCount(02C9F560 02C9F55C) returns 0`

`GetStreamIDs(1 02729720 1 02729640) returns 80004001`

`GetOutputAvailableType(0 1 02C9F4B0) returns 0`

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



