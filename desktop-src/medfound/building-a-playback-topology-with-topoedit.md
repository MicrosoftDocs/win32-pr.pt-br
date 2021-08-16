---
description: Criando uma topologia de reprodução com TopoEdit
ms.assetid: 4d4c4ff9-dad1-4c79-a44a-2ad20f1bbca0
title: Criando uma topologia de reprodução com TopoEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a71ae353c11108fe7c844d8ddd6441e652e007646b91f44c6fe2b480a22a8a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035424"
---
# <a name="building-a-playback-topology-with-topoedit"></a>Criando uma topologia de reprodução com TopoEdit

O TopoEdit pode criar uma topologia de reprodução para um arquivo de mídia local adicionando e conectando automaticamente os nós de origem, transformação e saída. TopoEdit não resolve automaticamente a topologia. Para reproduzir a topologia, resolva-a e, em seguida, use os controles de transporte.

## <a name="to-build-and-play-a-topology-for-a-media-file"></a>Para compilar e reproduzir uma topologia para um arquivo de mídia

1.  No menu **arquivo** , clique em **processar arquivo**.

    Isso abre a caixa de diálogo **selecionar origem da mídia** .

2.  Navegue até a pasta onde o arquivo de mídia está localizado.
3.  No campo **nome do arquivo:** , insira o nome do arquivo.
4.  Clique em **Abrir**.

    O **painel topologia** mostra a topologia conectada. Internamente, o TopoEdit executa as seguintes tarefas:

    -   Enumera os fluxos no arquivo de mídia e cria os nós de origem.
    -   Dependendo do tipo de mídia dos nós de origem, o adiciona nós de transformação, como decodificadores.
    -   Adiciona o coletor de processamento de áudio de streaming (SAR) para fluxo de áudio e o coletor de processador de vídeo avançado (EVR) para o fluxo de vídeo.
    -   Conecta as entradas de nó e as saídas de nó.

5.  No menu **topologia** , clique em **resolver topologia**.
6.  Clique no botão **reproduzir** na barra de ferramentas para reproduzir a topologia. A imagem a seguir mostra o botão **reproduzir** :::image type="icon" source="images/536e8908-ef44-4d25-98f1-c06b5ef37591.jpg"::: .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controles de reprodução no TopoEdit](playback-controls-in-topoedit.md)
</dt> <dt>

[Resolvendo uma topologia com TopoEdit](resolving-a-topology-with-topoedit.md)
</dt> <dt>

[TopoEdit](topoedit.md)
</dt> </dl>

 

 



