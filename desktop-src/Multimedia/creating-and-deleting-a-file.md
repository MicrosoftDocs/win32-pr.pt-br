---
title: Criando e excluindo um arquivo
description: Criando e excluindo um arquivo
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- e/s de arquivo multimídia, criando arquivos
- e/s de arquivo, criando arquivos
- entrada e saída (e/s), criando arquivos
- E/s (entrada e saída), criando arquivos
- Criando arquivos de e/s
- e/s de arquivo multimídia, excluindo arquivos
- e/s de arquivo, excluindo arquivos
- entrada e saída (e/s), excluindo arquivos
- E/s (entrada e saída), excluindo arquivos
- excluindo arquivos de e/s
- função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22cd6330874d0b5da74d69193359c025c709c79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103640617"
---
# <a name="creating-and-deleting-a-file"></a>Criando e excluindo um arquivo

Para criar um arquivo, defina o parâmetro *dwOpenFlags* da função [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) como MMIO \_ Create. O exemplo a seguir cria um arquivo e o abre para leitura e gravação.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Se o arquivo que você está criando já existir, ele será truncado para comprimento zero.

Para excluir um arquivo, defina o parâmetro *dwOpenFlags* da função **mmioOpen** como MMIO \_ Delete. Depois de excluir um arquivo, ele não pode ser recuperado por nenhum meio padrão. Se seu aplicativo estiver excluindo um arquivo na solicitação de um usuário, consulte o usuário antes de excluir o arquivo para certificar-se de que o usuário deseja excluí-lo.

 

 