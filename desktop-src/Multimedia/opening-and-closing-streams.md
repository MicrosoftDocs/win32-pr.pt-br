---
title: Abrindo e fechando fluxos
description: Abrindo e fechando fluxos
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- Função AVIFileGetStream
- Função AVIStreamRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec4462e261f1480129c073b70ddc61f91a422c8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005234"
---
# <a name="opening-and-closing-streams"></a>Abrindo e fechando fluxos

A abertura de fluxos de dados é semelhante à abertura de arquivos. Você pode abrir um fluxo usando a função [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) . Essa função cria uma interface de fluxo, coloca um identificador do fluxo na interface e retorna um ponteiro para a interface. O **AVIFileGetStream** também mantém uma contagem de referência dos aplicativos que abriram um fluxo, mas não aqueles que o fecharam.

Se você quiser acessar um único fluxo em um arquivo, poderá abrir o arquivo e o fluxo usando a função [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) . Essa função combina as operações e os argumentos de função das funções [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileGetStream** .

Para acessar mais de um fluxo em um arquivo, use **AVIFileOpen** uma vez seguido por várias chamadas para **AVIFileGetStream**.

Você pode incrementar a contagem de referência de um fluxo usando a função [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) para manter um fluxo aberto ao usar uma função que normalmente fecharia o fluxo.

Você pode fechar um fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Essa função decrementa a contagem de referência do fluxo e o fecha quando a contagem de referência chega a zero. Seus aplicativos devem balancear a contagem de referência incluindo uma chamada para **AVIStreamRelease** para cada uso da função [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** ou **AVIStreamOpenFromFile** . Quando você libera um fluxo que foi aberto usando **AVIStreamOpenFromFile**, o avifile fecha o arquivo que contém o fluxo. Se o seu aplicativo liberar um arquivo que tem fluxos de dados abertos, o AVIFile não fechará os fluxos até que todos os fluxos sejam liberados.

 

 




