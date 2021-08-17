---
description: Um aplicativo pode descompactar um único arquivo compactado usando as funções LZOpenFile, LZCopy e LZClose.
ms.assetid: e43df292-ed56-4023-92e8-de261e3b58a1
title: Descompactando um único arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99152a36a2846bfe35a9d92bc3d8fd2eb6b5c3a7f0877179262801a9141bcc61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150832"
---
# <a name="decompressing-a-single-file"></a>Descompactando um único arquivo

Um aplicativo pode descompactar um único arquivo compactado executando as seguintes tarefas:

1.  Abra o arquivo de origem chamando a [**função LZOpenFile.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea)
2.  Abra o arquivo de destino chamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copie o arquivo de origem para o arquivo de destino chamando a [**função LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) e passando os alças retornados por [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
4.  Feche os arquivos chamando a [**função LZClose.**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose)

 

 



