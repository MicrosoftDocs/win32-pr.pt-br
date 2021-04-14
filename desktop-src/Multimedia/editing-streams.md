---
title: Edição de fluxos
description: Edição de fluxos
ms.assetid: 1653ff90-e96a-43fc-b509-6d8ad4ddcd2c
keywords:
- Função CreateEditableStream
- Função EditStreamCut
- Função EditStreamCopy
- Função EditStreamPaste
- Função EditStreamClone
- Função EditStreamSetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29eb687eb36ff9dfe0b1d3477bff095bdd78a135
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453651"
---
# <a name="editing-streams"></a>Edição de fluxos

Você pode criar um fluxo que pode ser editado usando a função [**CreateEditableStream**](/windows/desktop/api/Vfw/nf-vfw-createeditablestream) . Essa função inicializa o ambiente para editar um fluxo. Isso inclui a criação de uma interface para o novo fluxo e as tabelas de edição internas que controlam as alterações feitas no fluxo. **CreateEditableStream** retorna um ponteiro de fluxo para um fluxo editável que é exigido por outras funções de edição de fluxo. O ponteiro de fluxo editável também pode ser usado por outras funções AVIFile que aceitam ponteiros de fluxo.

Você pode recortar um ou mais exemplos de um fluxo editável usando a função [**EditStreamCut**](/windows/desktop/api/Vfw/nf-vfw-editstreamcut) . Para remover exemplos do fluxo editável, essa função adiciona uma entrada à tabela de edição. Em seguida, a função coloca uma cópia dos exemplos recortados em um novo fluxo temporário cujo ponteiro de interface é retornado em uma variável.

Você pode copiar um ou mais exemplos de um fluxo editável para um fluxo temporário usando a função [**EditStreamCopy**](/windows/desktop/api/Vfw/nf-vfw-editstreamcopy) . **EditStreamCopy** coloca cópias dos exemplos em um novo fluxo temporário cujo ponteiro de interface é retornado em uma variável.

Você pode copiar um ou mais exemplos de um fluxo e colá-los em um fluxo editável usando a função [**EditStreamPaste**](/windows/desktop/api/Vfw/nf-vfw-editstreampaste) . Para inserir os exemplos na posição especificada, essa função adiciona uma entrada na tabela de edição do fluxo editável de destino.

Você pode duplicar um fluxo editável usando a função [**EditStreamClone**](/windows/desktop/api/Vfw/nf-vfw-editstreamclone) . Essa função retorna um ponteiro para a interface de fluxo do novo fluxo. Você pode copiar esses fluxos para a área de transferência ou usá-los para manter uma trilha de edições feitas em um fluxo.

Você pode alterar várias das características de um fluxo editável usando a função [**EditStreamSetInfo**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetinfoa) . Essa função atualiza a configuração de prioridade, idioma, escala e taxa, hora de início, configuração de qualidade, dimensões e coordenadas de retângulo de destino e a descrição textual do fluxo. Esses itens são armazenados na estrutura [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) associada ao fluxo editável.

Você também pode alterar a descrição textual de um fluxo editável usando a função [**EditStreamSetName**](/windows/desktop/api/Vfw/nf-vfw-editstreamsetnamea) . Essa função atualiza o membro **szName** da estrutura **AVISTREAMINFO** associada ao fluxo editável.

As funções de edição funcionam em fluxos. Você precisa recortar e colar cada fluxo individualmente e, em seguida, usar a função [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) para criar um novo ponteiro de arquivo.

> [!Note]  
> As tabelas de edição em um fluxo editável mantêm todas as alterações de um fluxo. O fluxo de origem nunca é alterado.

 

 

 




