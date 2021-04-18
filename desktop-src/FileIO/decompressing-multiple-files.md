---
description: Um aplicativo pode descompactar vários arquivos usando as funções LZOpenFile, LZCopy e LZClose.
ms.assetid: 582d57c7-70a4-4711-bae5-4abfb7a196b1
title: Descompactando vários arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 206c7c233a5e0fda70326a45dfcde4e4194586d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784008"
---
# <a name="decompressing-multiple-files"></a>Descompactando vários arquivos

Um aplicativo pode descompactar vários arquivos executando as seguintes tarefas:

1.  Abra os arquivos de origem chamando a função [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea) .
2.  Abra os arquivos de destino chamando [**LZOpenFile**](/windows/desktop/api/LzExpand/nf-lzexpand-lzopenfilea).
3.  Copie os arquivos de origem para os arquivos de destino chamando a função [**LZCopy**](/windows/desktop/api/LzExpand/nf-lzexpand-lzcopy) .
4.  Feche os arquivos chamando a função [**LZClose**](/windows/desktop/api/LzExpand/nf-lzexpand-lzclose) .

 

 



