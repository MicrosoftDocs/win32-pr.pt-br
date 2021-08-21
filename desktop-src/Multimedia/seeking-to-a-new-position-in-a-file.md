---
title: Buscando uma nova posição em um arquivo
description: Buscando uma nova posição em um arquivo
ms.assetid: 276c3e43-bf9f-4a0a-b33a-7eaa701e92a6
keywords:
- e/s de arquivo multimídia, migrando para o início dos arquivos
- e/s de arquivo, migrando para o início dos arquivos
- entrada e saída (e/s), migrando para o início dos arquivos
- E/s (entrada e saída), movendo para o início dos arquivos
- migrando para O início dos arquivos de e/s
- e/s de arquivo multimídia, buscando nova posição nos arquivos
- e/s de arquivo, buscando nova posição nos arquivos
- entrada e saída (e/s), buscando nova posição nos arquivos
- E/s (entrada e saída), buscando nova posição nos arquivos
- Buscando nova posição em arquivos de e/s
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97e51ab51065bcdf89af84f2fd622558261dd4cf42cac3e50fe54fb116a7ad9b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118136580"
---
# <a name="seeking-to-a-new-position-in-a-file"></a>Buscando uma nova posição em um arquivo

O exemplo a seguir passa para o início de um arquivo aberto usando a função [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) .


```C++
mmioSeek(hFile, 0L, SEEK_SET); 
```



O exemplo a seguir passa para o final de um arquivo aberto.


```C++
mmioSeek(hFile, 0L, SEEK_END); 
```



O exemplo a seguir passa para uma posição de 10 bytes do final de um arquivo aberto.


```C++
mmioSeek(hFile, -10L, SEEK_END); 

```



 

 