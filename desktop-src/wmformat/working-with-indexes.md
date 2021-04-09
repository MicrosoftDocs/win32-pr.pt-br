---
title: Trabalhando com índices
description: Trabalhando com índices
ms.assetid: 7daa4b29-0597-462d-ad65-135d0ef7362d
keywords:
- SDK do Windows Media Format, índices
- ASF (Advanced Systems Format), índices
- ASF (formato de sistemas avançados), índices
- índices, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34057046223daf2e16950e0e38b1b0db5df32c4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822442"
---
# <a name="working-with-indexes"></a>Trabalhando com índices

O SDK do Windows Media Format dá suporte à busca e ao seu conteúdo. A busca permite que você especifique um local na linha do tempo do arquivo para começar a reprodução. A habilitação permite que você encaminhe e retroceda rapidamente a saída de um arquivo. Os arquivos devem ser indexados para aproveitar esses recursos. Um índice é uma série de valores que representam as posições no arquivo (horas de apresentação, números de quadro ou códigos de tempo SMTP) com deslocamentos correspondentes na seção de dados do arquivo para cada. A indexação é mais importante para fluxos de vídeo, pois o tempo de apresentação de fluxo de áudio pode ser facilmente estimado. No entanto, alguns fluxos de áudio também podem exigir índices. Por padrão, o gravador irá indexar todos os novos arquivos ASF. Se forem feitas alterações no conteúdo de um arquivo, você deverá atualizar o índice por conta própria usando o objeto indexador.

O indexador dá suporte à indexação temporal e com base em quadros, bem como à indexação com base em códigos de tempo SMPTE (se houver). O gravador criará um índice temporal por padrão para cada novo fluxo de vídeo codificado em um arquivo. Você deve configurar e chamar explicitamente o indexador para criar um índice de código de tempo baseado em quadro ou SMPTE.

Quando são feitas alterações no conteúdo de um arquivo ASF, ele deve ser indexado novamente.

As seções a seguir apresentam o código de exemplo para executar tarefas comuns de indexação.

-   [Para desabilitar a indexação automática](to-disable-automatic-indexing.md)
-   [Para configurar o indexador](to-configure-the-indexer.md)
-   [Para indexar um arquivo ASF](to-index-an-asf-file.md)
-   [Para interromper a indexação em andamento](to-stop-indexing-in-progress.md)

Além disso, o aplicativo de exemplo DSCopy ilustra o uso do indexador. Para obter mais informações, consulte [aplicativos de exemplo](sample-applications.md).

 

 




