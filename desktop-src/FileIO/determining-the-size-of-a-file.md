---
description: A função GetFileSize recupera o tamanho de um arquivo.
ms.assetid: 4d3a3925-72e8-4350-b46d-e2c25791e862
title: Determinando o tamanho de um arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf4185d0bb695d73dc3afd03bb1ee7d6fe95cf606960fbdc41c4ce0b33b732
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150609"
---
# <a name="determining-the-size-of-a-file"></a>Determinando o tamanho de um arquivo

A [**função GetFileSize**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) recupera o tamanho de um arquivo.

Como a implementação de arquivos do sistema de arquivos NTFS permite vários fluxos dentro de um arquivo, qualquer aplicativo que você escreve que acessa arquivos deve levar em conta a possibilidade de que o criador do arquivo possa incluir vários fluxos no arquivo. Se vários fluxos não são verificados em um arquivo, o aplicativo pode menosprezar o tamanho total do arquivo, entre outros erros.

 

 



