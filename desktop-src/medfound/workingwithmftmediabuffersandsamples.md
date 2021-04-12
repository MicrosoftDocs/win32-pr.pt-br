---
description: Trabalhando com exemplos e buffers de mídia de MFT
ms.assetid: dda4048e-bc4c-40ac-a6bd-34984f3717e0
title: Trabalhando com exemplos e buffers de mídia de MFT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6373f6d75b4122409b54649eed6f90e95c2f50c7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297916"
---
# <a name="working-with-mft-media-buffers-and-samples"></a>Trabalhando com exemplos e buffers de mídia de MFT

O codec MFTs passa dados de mídia para frente e para trás usando os buffers de mídia e exemplos.

Um buffer de mídia é um objeto COM que gerencia um bloco de memória, normalmente, para manter os dados de mídia. Quando os dados são passados para ou de um MFT, eles são sempre passados na forma de um buffer de mídia.

Todos os buffers de mídia expõem a interface **IMFMediaBuffer** . Essa interface é projetada para qualquer tipo de dados. Os buffers que contêm dados de vídeo geralmente também expõem **IMF2DBuffer**.

Um buffer de mídia tem um tamanho máximo, que é a quantidade de memória alocada para o buffer. Para localizar o tamanho máximo, chame **IMFMediaBuffer:: GetMaxLength**. Em qualquer ponto no tempo, um buffer de mídia também tem um comprimento atual, que é a quantidade de dados válidos no buffer, variando de zero bytes até o tamanho máximo. Para obter o comprimento atual, chame **IMFMediaBuffer:: GetCurrentLength**. Quando o buffer é criado, o comprimento atual é zero. Se você gravar dados no buffer, chame **IMFMediaBuffer:: SetCurrentLength** para atualizar o comprimento atual.

Para acessar a memória no buffer, chame **IMFMediaBuffer:: Lock**. Esse método retorna um ponteiro para o início do bloco de memória. Quando terminar de usar o ponteiro, chame **IMFMediaBuffer:: Unlock**. O método **Lock** não é um mecanismo de sincronização de threads; Ele não garante que outros threads não possam acessar o buffer. O método **Lock** é usado para garantir que a memória acessada permaneça válida até que você chame o método **Unlock** .

Um objeto de exemplo de mídia (no contexto do SDK do Media Foundation) é um objeto que contém uma lista ordenada de zero ou mais buffers. Amostras de mídia expõem a interface **IMFSample** .

Para criar um novo exemplo, chame a função **MFCreateSample** . Inicialmente, a lista de buffers do exemplo está vazia. Para adicionar um buffer ao final da lista, chame **IMFSample:: addbuffer**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> <dt>

[Trabalhando com codec MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



