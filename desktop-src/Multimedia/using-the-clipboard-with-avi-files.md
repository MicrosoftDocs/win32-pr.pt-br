---
title: Usando a área de transferência com arquivos AVI
description: Usando a área de transferência com arquivos AVI
ms.assetid: 76ef7cc9-9afd-462a-b9fe-2b62f8113a9a
keywords:
- Função AVIPutFileOnClipboard
- Função AVIGetFromClipboard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe46f463f22aa2d015d4ffd8496eb95c37053a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635942"
---
# <a name="using-the-clipboard-with-avi-files"></a>Usando a área de transferência com arquivos AVI

A área de transferência fornece armazenamento temporário conveniente que um aplicativo pode usar para copiar ou transferir arquivos AVI. O AVIFile inclui funções de área de transferência que você pode usar com arquivos de disco ou memória.

Você pode copiar um arquivo para a área de transferência usando a função [**AVIPutFileOnClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviputfileonclipboard) . Para gravar um arquivo que está na área de transferência na memória ou no disco, use a função [**AVIGetFromClipboard**](/windows/desktop/api/Vfw/nf-vfw-avigetfromclipboard) .

Você pode limpar um arquivo da área de transferência usando a função [**AVIClearClipboard**](/windows/desktop/api/Vfw/nf-vfw-aviclearclipboard) . Essa função não limpa outros tipos de informações, como texto, da área de transferência. Se você usar funções da área de transferência em seu aplicativo, desmarque a área de transferência com **AVIClearClipboard** antes de fechar o aplicativo ou fechar o arquivo na área de transferência. Você pode chamar **AVIClearClipboard** em seu aplicativo se o **AVIPutFileOnClipboard** foi ou não usado.

> [!Note]  
> Se o seu aplicativo copia um arquivo para a área de transferência e o arquivo contém dados de fluxo que podem ser alterados, você pode criar um arquivo de memória de fluxos clonados usando a função [**AVIMakeFileFromStreams**](/windows/desktop/api/Vfw/nf-vfw-avimakefilefromstreams) . Em seguida, você pode inserir o arquivo na área de transferência e liberar o arquivo original sem invalidar-o.

 

 

 




