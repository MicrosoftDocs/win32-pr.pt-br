---
description: O Monitor de Rede BLOB (objeto binário grande) é uma estrutura de dados genérica que contém informações de configuração e localização de NICs (placas de interface de rede).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: Monitor de Rede BLOBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d15ce2a8f85860720c6f38b0d6c019a33e57df0a1b589ba23455db0319d0436
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119799546"
---
# <a name="network-monitor-blobs"></a>Monitor de Rede BLOBs

O Monitor de Rede BLOB (objeto binário grande) é uma estrutura de dados genérica que contém informações de configuração e localização de NICs (placas de interface de rede). Use BLOBs para representar NICs e para filtrar entradas em uma lista de NICs. O BLOBS também pode conter dados específicos do aplicativo sem afetar os outros dados que eles contêm. A implementação de BLOB é opaca para todos os níveis que devem acessar BLOBs com APIs de BLOB.

## <a name="blob-structure"></a>Estrutura BLOB

Um BLOB pode ser considerado como uma árvore hierárquica usada para designar cadeias de caracteres. Essa árvore tem três camadas: Proprietário, Categoria e Marca. Proprietário é uma cadeia de caracteres que indica, em geral, quem lê uma entrada. A Categoria também é uma cadeia de caracteres, que designa um grupo funcional geral de marcas no proprietário. A Marca é o nome real da entrada.

As características estruturais dos BLOBs incluem:

-   Os auxiliares de BLOB em um processo são protegidos uns dos outros por um mutex integrado em cada BLOB.
-   Cada BLOB tem um número de versão interno para que os auxiliares possam lidar com formulários BLOB atuais e futuros. Poderão ocorrer conflitos de versão se você enviar um BLOB para outro computador por meio de uma chamada de procedimento remoto.
-   O PRÓPRIO BLOB é um ponteiro para um nulo. Esteja ciente de que os aplicativos devem alocar BLOBs com **o modificador const** para evitar alterar o conteúdo.
-   Cada um dos designadores, bem como seus valores, são cadeias de caracteres. Esteja ciente de que as cadeias de caracteres retornadas pelas **funções GetString** são, na verdade, ponteiros para o BLOB e não devem ser alteradas. Por esse motivo, essas cadeias de caracteres devem ser especificadas como **const char** _ pX* para impedir que os aplicativos \_ as mudem acidentalmente.

Em geral, todos os parâmetros com o designador **const** incentivam o chamador a evitar alterar os valores em vez de proibir que as funções auxiliares os mudem. Na verdade, as funções auxiliares geralmente alterarão esses valores.

 

 



