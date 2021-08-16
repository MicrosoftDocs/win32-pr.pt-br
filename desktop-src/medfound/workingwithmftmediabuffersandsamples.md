---
description: Trabalhando com buffers e exemplos de mídia MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Trabalhando com buffers e exemplos de mídia MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d964f1c2f2a5fd5f92d5af87213c6977fc51bee76caf3a281861788e2a2fb922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736447"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Trabalhando com buffers e exemplos de mídia MFT

Os MFTs codec passam dados de mídia para frente e para trás usando buffers de mídia e exemplos.

Um buffer de mídia é um objeto COM que gerencia um bloco de memória, normalmente para conter dados de mídia. Quando os dados são passados para ou de um MFT, eles sempre são passados na forma de um buffer de mídia.

Todos os buffers de mídia expõem a interface **IMFMediaBuffer.** Essa interface foi projetada para qualquer tipo de dados. Buffers que contêm dados de vídeo geralmente também **expõem IMF2DBuffer.**

Um buffer de mídia tem um tamanho máximo, que é a quantidade de memória alocada para o buffer. Para encontrar o tamanho máximo, chame **IMFMediaBuffer::GetMaxLength.** A qualquer momento, um buffer de mídia também tem um comprimento atual, que é a quantidade de dados válidos no buffer, variando de zero bytes até o tamanho máximo. Para obter o tamanho atual, chame **IMFMediaBuffer::GetCurrentLength.** Quando o buffer é criado, o comprimento atual é zero. Se você gravar dados no buffer, chame **IMFMediaBuffer::SetCurrentLength** para atualizar o comprimento atual.

Para acessar a memória no buffer, chame **IMFMediaBuffer::Lock**. Esse método retorna um ponteiro para o início do bloco de memória. Quando terminar de usar o ponteiro, chame **IMFMediaBuffer::Unlock**. O **método Lock** não é um mecanismo de sincronização de thread; ele não garante que outros threads não podem acessar o buffer. O **método Lock** é usado para garantir que a memória acessada permaneça válida até que você chame o método **Unlock.**

Um objeto de exemplo de mídia (no contexto do SDK do Media Foundation) é um objeto que contém uma lista ordenada de zero ou mais buffers. Exemplos de mídia expõem a interface **IMFSample.**

Para criar um novo exemplo, chame a **função MFCreateSample.** Inicialmente, a lista de buffers do exemplo está vazia. Para adicionar um buffer ao final da lista, chame **IMFSample::AddBuffer**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com DMOs codec](workingwithcodecdmos.md)
</dt> <dt>

[Trabalhando com MFTs codec](workingwithcodecmfts.md)
</dt> </dl>

 

 



