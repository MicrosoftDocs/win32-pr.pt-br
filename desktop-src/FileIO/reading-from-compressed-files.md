---
description: Um aplicativo pode descompactar uma parte de um arquivo compactado por vez usando as funções LZSeek e LZRead.
ms.assetid: 9ceec1d4-37cd-4717-a731-dfb9cddb268c
title: Lendo de arquivos compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0c670e1ae473332451df72ddc394a234fa49e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757853"
---
# <a name="reading-from-compressed-files"></a>Lendo de arquivos compactados

Além de descompactar um arquivo completo em uma única operação, um aplicativo pode descompactar um arquivo compactado uma parte por vez usando as funções [**LZSeek**](/windows/desktop/api/LzExpand/nf-lzexpand-lzseek) e [**LZRead**](/windows/desktop/api/LzExpand/nf-lzexpand-lzread) . Essas funções são particularmente úteis quando é necessário para extrair partes de arquivos grandes. Por exemplo, um fabricante de fontes pode ter arquivos compactados contendo métricas de fonte, além de dados de caractere. Para usar as informações nesses arquivos, um aplicativo precisará descompactar o arquivo; no entanto, a maioria dos aplicativos usaria apenas parte do arquivo em um determinado momento. Para obter informações sobre métricas de fonte, o aplicativo extrairia dados do cabeçalho. Para obter informações do texto, o aplicativo reposicionará o ponteiro de arquivo chamando **LZSeek** e extrairá os dados de caractere chamando **LZRead**.

 

 



