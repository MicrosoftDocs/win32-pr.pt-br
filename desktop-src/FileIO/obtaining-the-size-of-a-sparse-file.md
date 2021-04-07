---
description: Obtenha o tamanho alocado ou o tamanho total de um arquivo usando a função GetCompressedFileSize ou GetFiles.
ms.assetid: 1894ea01-49ff-41e3-9912-1cd75966bd3f
title: Obtendo o tamanho de um arquivo esparso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e93a1c6a33f0d6913e0e6848e4593ea0e0bf0259
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827357"
---
# <a name="obtaining-the-size-of-a-sparse-file"></a>Obtendo o tamanho de um arquivo esparso

Use a função [**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea) para obter o tamanho real alocado em disco para um arquivo esparso. Esse total não inclui o tamanho das regiões que foram desalocadas porque elas foram preenchidas com zeros. Use a função [**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) para determinar o tamanho total de um arquivo, incluindo o tamanho das regiões esparsas que foram desalocadas.

 

 



