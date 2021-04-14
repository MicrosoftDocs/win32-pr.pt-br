---
title: Criando fluxos temporários
description: Criando fluxos temporários
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Função AVIStreamCreate
- Função AVIStreamRelease
- Função AVIMakeCompressedStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209259f46e25275094dcd1eb5eeddd4f336ee906
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453584"
---
# <a name="creating-temporary-streams"></a>Criando fluxos temporários

Os fluxos temporários podem ser benéficos de várias maneiras. Você pode usar um fluxo temporário como um fluxo de trabalho, por exemplo, ao alterar o formato de fluxo. Ou você pode criar um fluxo temporário para manter partes de outros fluxos que foram copiados.

Você pode criar um fluxo na memória que não esteja associado a nenhum arquivo usando a função [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) . Essa função retorna o endereço da interface para o novo fluxo em um local especificado e é usada internamente por outras funções que criam fluxos temporários.

Você pode criar um fluxo compactado a partir de um fluxo não compactado usando a função [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) . Você identifica o fluxo a ser compactado, o método de compactação e as opções de compactação e o manipulador para o novo fluxo.

Quando você terminar de usar um fluxo criado com **AVIStreamCreate** ou **AVIMakeCompressedStream**, feche o fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . O **AVIStreamRelease** libera os recursos usados pelo fluxo temporário.

 

 




