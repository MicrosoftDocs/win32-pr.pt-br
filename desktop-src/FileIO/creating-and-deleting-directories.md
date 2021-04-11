---
description: Um aplicativo pode criar e excluir diretórios programaticamente.
ms.assetid: 52d1d8a8-e5a7-44f5-9bf2-2a496ef79d32
title: Criando e excluindo diretórios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140547594271e13bc78bfa78336f167f228879a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091023"
---
# <a name="creating-and-deleting-directories"></a>Criando e excluindo diretórios

Um aplicativo pode criar e excluir diretórios programaticamente.

Para criar um novo diretório, use a função [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya), [**CreateDirectoryEx**](/windows/desktop/api/WinBase/nf-winbase-createdirectoryexa)ou [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda) . Um diretório recebe o nome especificado quando ele é criado. As convenções para nomear um diretório seguem as convenções para nomear um arquivo. Para obter uma descrição dessas convenções, consulte [nomeando um arquivo](naming-a-file.md).

Para excluir um diretório existente, use a função [**RemoveDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-removedirectorya) ou [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) . Antes de remover um diretório, você deve garantir que o diretório esteja vazio e que você tenha o privilégio de acesso de exclusão para o diretório. Para fazer o último, chame a função [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .

 

 
