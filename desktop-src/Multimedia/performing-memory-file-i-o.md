---
title: Executando e/s de arquivo de memória
description: Executando e/s de arquivo de memória
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- e/s de arquivo multimídia, memória
- e/s de arquivo, memória
- entrada e saída (e/s), memória
- E/s (entrada e saída), memória
- e/s de memória
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a2b1e2e47ffccc21b2684dcb6bd285b7e55470776fb57eb382a969091a19e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805886"
---
# <a name="performing-memory-file-io"></a>Executando e/s de arquivo de memória

Os serviços de e/s de arquivo de multimídia permitem que você trate um bloco de memória como um arquivo. Isso pode ser útil se você já tiver uma imagem de arquivo na memória. Os arquivos de memória permitem reduzir o número de condições de caso especial em seu código, pois, para fins de e/s, você pode tratar arquivos de memória como se fossem arquivos baseados em disco. Você também pode usar arquivos de memória com a área de transferência.

Assim como ocorre com os buffers de e/s, os arquivos de memória podem usar a memória alocada pelo aplicativo ou o Gerenciador de e/s de arquivos. Além disso, os arquivos de memória podem ser expansíveis ou não expansíveis. Quando o Gerenciador de e/s de arquivos atinge o final de um arquivo de memória expansível, ele expande o arquivo de memória por um incremento predefinido.

Para abrir um arquivo de memória, use a função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) com o parâmetro *SzFilename* definido como **NULL** e o \_ sinalizador ReadWrite MMIO definido no parâmetro *dwOpenFlags* . Defina o parâmetro *lpmmioinfo* para apontar para uma estrutura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) que tenha sido configurada da seguinte maneira:

1.  Defina o membro **pIOProc** como **nulo**.
2.  Defina o membro **fccIOProc** como um \_ mem FOURCC.
3.  Defina o membro **pchBuffer** para apontar para o bloco de memória. Para solicitar que o Gerenciador de e/s de arquivo aloque o bloco de memória, defina **pchBuffer** como **nulo**.
4.  Defina o membro **cchBuffer** para o tamanho inicial do bloco de memória.
5.  Defina o membro **adwInfo** para o tamanho mínimo de expansão do bloco de memória. Para um arquivo de memória não expansível, defina **adwInfo** como **nulo**.
6.  Defina todos os outros membros como zero.

Não há restrições para a alocação de memória para uso como um arquivo de memória não expansível.

 

 