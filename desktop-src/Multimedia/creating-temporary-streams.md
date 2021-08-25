---
title: criando Fluxos temporários
description: criando Fluxos temporários
ms.assetid: 8fe75ae1-0111-4b02-a00d-1ef2ca462452
keywords:
- Função AVIStreamCreate
- Função AVIStreamRelease
- Função AVIMakeCompressedStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c33ce8d4ec6fd88a7283588d35955432cbe01a4855565928dca83d40afa8b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785696"
---
# <a name="creating-temporary-streams"></a>criando Fluxos temporários

Os fluxos temporários podem ser benéficos de várias maneiras. Você pode usar um fluxo temporário como um fluxo de trabalho, por exemplo, ao alterar o formato de fluxo. Ou você pode criar um fluxo temporário para manter partes de outros fluxos que foram copiados.

Você pode criar um fluxo na memória que não esteja associado a nenhum arquivo usando a função [**AVIStreamCreate**](/windows/desktop/api/Vfw/nf-vfw-avistreamcreate) . Essa função retorna o endereço da interface para o novo fluxo em um local especificado e é usada internamente por outras funções que criam fluxos temporários.

Você pode criar um fluxo compactado a partir de um fluxo não compactado usando a função [**AVIMakeCompressedStream**](/windows/desktop/api/Vfw/nf-vfw-avimakecompressedstream) . Você identifica o fluxo a ser compactado, o método de compactação e as opções de compactação e o manipulador para o novo fluxo.

Quando você terminar de usar um fluxo criado com **AVIStreamCreate** ou **AVIMakeCompressedStream**, feche o fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . O **AVIStreamRelease** libera os recursos usados pelo fluxo temporário.

 

 




