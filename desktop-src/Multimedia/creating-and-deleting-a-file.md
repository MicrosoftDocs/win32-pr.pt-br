---
title: Criando e excluindo um arquivo
description: Criando e excluindo um arquivo
ms.assetid: a4b4a310-7230-4f1d-b084-c47db39adaac
keywords:
- E/S de arquivo multimídia, criando arquivos
- E/S de arquivo, criando arquivos
- entrada e saída (E/S), criando arquivos
- E/S (entrada e saída), criando arquivos
- criando arquivos de E/S
- E/S de arquivo multimídia, excluindo arquivos
- E/S de arquivo, excluindo arquivos
- entrada e saída (E/S), excluindo arquivos
- E/S (entrada e saída), excluindo arquivos
- excluindo arquivos de E/S
- Função mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91a2ee8e70508e2c5dc3b24c084cf0b081b6629a519703ef43a15845ef3ec76a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119785726"
---
# <a name="creating-and-deleting-a-file"></a>Criando e excluindo um arquivo

Para criar um arquivo, defina o *parâmetro dwOpenFlags* da [**função mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) como MMIO \_ CREATE. O exemplo a seguir cria um arquivo e o abre para leitura e escrita.


```C++
HMMIO hFile; 

hFile = mmioOpen("NEWFILE.TXT", NULL, MMIO_CREATE | MMIO_READWRITE); 
if (hFile != NULL) 
    // File created successfully. 
else 
    // File cannot be created. 
```



Se o arquivo que você está criando já existir, ele será truncado até o comprimento zero.

Para excluir um arquivo, defina o *parâmetro dwOpenFlags* da **função mmioOpen** como MMIO \_ DELETE. Depois de excluir um arquivo, ele não pode ser recuperado por nenhum meio padrão. Se seu aplicativo estiver excluindo um arquivo por solicitação de um usuário, consulte o usuário antes de excluir o arquivo para garantir que o usuário deseja excluí-lo.

 

 