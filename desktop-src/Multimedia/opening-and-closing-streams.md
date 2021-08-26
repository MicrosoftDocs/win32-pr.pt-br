---
title: abrindo e fechando Fluxos
description: abrindo e fechando Fluxos
ms.assetid: 7dcaccbe-63d8-410a-ae00-16ce9e252ad0
keywords:
- Função AVIFileGetStream
- Função AVIStreamRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35f678f2858d590956bc3ba724abacd12d2047e337fc8428934e0e32005bb24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038306"
---
# <a name="opening-and-closing-streams"></a>abrindo e fechando Fluxos

A abertura de fluxos de dados é semelhante à abertura de arquivos. Você pode abrir um fluxo usando a função [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream) . Essa função cria uma interface de fluxo, coloca um identificador do fluxo na interface e retorna um ponteiro para a interface. O **AVIFileGetStream** também mantém uma contagem de referência dos aplicativos que abriram um fluxo, mas não aqueles que o fecharam.

Se você quiser acessar um único fluxo em um arquivo, poderá abrir o arquivo e o fluxo usando a função [**AVIStreamOpenFromFile**](/windows/desktop/api/Vfw/nf-vfw-avistreamopenfromfilea) . Essa função combina as operações e os argumentos de função das funções [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileGetStream** .

Para acessar mais de um fluxo em um arquivo, use **AVIFileOpen** uma vez seguido por várias chamadas para **AVIFileGetStream**.

Você pode incrementar a contagem de referência de um fluxo usando a função [**AVIStreamAddRef**](/windows/desktop/api/Vfw/nf-vfw-avistreamaddref) para manter um fluxo aberto ao usar uma função que normalmente fecharia o fluxo.

Você pode fechar um fluxo usando a função [**AVIStreamRelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) . Essa função decrementa a contagem de referência do fluxo e o fecha quando a contagem de referência chega a zero. Seus aplicativos devem balancear a contagem de referência incluindo uma chamada para **AVIStreamRelease** para cada uso da função [**AVIFileGetStream**](/windows/desktop/api/Vfw/nf-vfw-avifilegetstream), [**AVIFileCreateStream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream), **AVIStreamAddRef** ou **AVIStreamOpenFromFile** . Quando você libera um fluxo que foi aberto usando **AVIStreamOpenFromFile**, o avifile fecha o arquivo que contém o fluxo. Se o seu aplicativo liberar um arquivo que tem fluxos de dados abertos, o AVIFile não fechará os fluxos até que todos os fluxos sejam liberados.

 

 




