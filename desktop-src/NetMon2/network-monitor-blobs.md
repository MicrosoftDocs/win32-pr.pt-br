---
description: O BLOB (objeto binário grande) Monitor de Rede é uma estrutura de dados genérica que contém informações de configuração e local de NICs (placas de interface de rede).
ms.assetid: 910bf929-aa89-434d-83c3-07c80c627405
title: BLOBs de Monitor de Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dce6dd6ca8643eabe8ab49387c0ef39eb49b6f2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800106"
---
# <a name="network-monitor-blobs"></a>BLOBs de Monitor de Rede

O BLOB (objeto binário grande) Monitor de Rede é uma estrutura de dados genérica que contém informações de configuração e local de NICs (placas de interface de rede). Use BLOBs para representar NICs e para filtrar entradas em uma lista de NICs. Os BLOBs também podem conter dados específicos do aplicativo sem afetar os outros dados que eles contêm. A implementação de BLOB é opaca para todos os níveis que devem acessar BLOBs com APIs de BLOB.

## <a name="blob-structure"></a>Estrutura do BLOB

Um BLOB pode ser considerado uma árvore hierárquica usada para designar cadeias de caracteres. Esta árvore tem três camadas: proprietário, categoria e marca. Owner é uma cadeia de caracteres que indica, em geral, que lê uma entrada. A categoria também é uma cadeia de caracteres, que designa um agrupamento funcional geral de marcas sob o proprietário. A marca é o nome real da entrada.

As características estruturais dos BLOBs incluem:

-   Os auxiliares de BLOB em um processo são protegidos uns dos outros por um mutex embutido em cada BLOB.
-   Cada BLOB tem um número de versão interno para que os auxiliares possam lidar com formulários de BLOB presentes e futuros. Poderão ocorrer conflitos de versão se você enviar um BLOB para outro computador por meio de uma chamada de procedimento remoto.
-   O BLOB em si é um ponteiro para void. Lembre-se de que os aplicativos devem alocar BLOBs com o modificador **const** para evitar alterar o conteúdo.
-   Cada um dos designadores, bem como seus valores, são cadeias de caracteres. Lembre-se de que as cadeias de caracteres retornadas por funções **GetString** são, na verdade, ponteiros para o blob e não devem ser alteradas. Por esse motivo, essas cadeias de caracteres devem ser especificadas como **const char** _ \_ PX * para impedir que os aplicativos as alterem acidentalmente.

Em geral, todos os parâmetros com o designador **const** incentivam o chamador a evitar a alteração dos valores em vez de proibir as funções auxiliares de alterá-las. Na verdade, as funções auxiliares geralmente alterarão esses valores.

 

 



