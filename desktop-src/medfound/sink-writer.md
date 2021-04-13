---
description: O gravador do coletor é um componente para codificar arquivos de áudio ou de vídeo.
ms.assetid: 23AF25B8-B94C-48BC-83D8-5863ACFFD4CA
title: Gravador do coletor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6b30d75e369de343bae61ba56dfd05c0d5d12a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296526"
---
# <a name="sink-writer"></a>Gravador do coletor

O gravador do coletor é um componente para codificar arquivos de áudio ou de vídeo.

O diagrama a seguir mostra, em um alto nível, como um aplicativo usa o gravador de coletor para codificar e áudio/vídeo.

![um diagrama que mostra o gravador do coletor.](images/encoding09.png)

O gravador de coletor hospeda um coletor de mídia e, opcionalmente, um ou mais codificadores. Os codificadores convertem dados não compactados de áudio ou vídeo em fragmentado codificados. O coletor de mídia gera o fragmentado para um arquivo. O gravador do coletor executa as seguintes tarefas:

-   Carrega o coletor de mídia.
-   Localiza e carrega os codificadores.
-   Gerencia o fluxo de dados para os codificadores e o coletor de mídia.

O aplicativo passa dados de áudio/vídeo para o gravador de coletor como entrada. Não importa como o aplicativo obtém ou gera os dados de entrada. Uma opção é usar o [leitor de origem](source-reader.md), conforme mostrado no diagrama a seguir. No entanto, o gravador de coletor não requer o uso do leitor de origem. Esses dois componentes são independentes.

![um diagrama que mostra o leitor de origem e o gravador de coletor.](images/encoding02.png)

## <a name="in-this-section"></a>Nesta seção

-   [Usando o gravador do coletor](using-the-sink-writer.md)
-   [Tutorial: usando o gravador de coletor para codificar vídeo](tutorial--using-the-sink-writer-to-encode-video.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificando e criando arquivos](encoding-and-file-authoring.md)
</dt> <dt>

[Visão geral da codificação no Media Foundation](overview-of-encoding-in-media-foundation.md)
</dt> </dl>

 

 



