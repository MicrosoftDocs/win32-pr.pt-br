---
description: Para usar os recursos do sistema operacional com eficiência, um aplicativo deve fechar os arquivos quando eles não forem mais necessários usando a função CloseHandle. Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.
ms.assetid: 6cf9694a-00c4-4750-8822-c25a1a102fd4
title: Fechando e excluindo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3da31fe7ff38a1bbd1555e2685ceab9ae432574
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811888"
---
# <a name="closing-and-deleting-files"></a>Fechando e excluindo arquivos

Para usar os recursos do sistema operacional com eficiência, um aplicativo deve fechar os arquivos quando eles não forem mais necessários usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) . Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.

A função [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) pode ser usada para excluir um arquivo no fechamento. Um arquivo não pode ser excluído até que todos os identificadores sejam fechados. Se um arquivo não puder ser excluído, seu nome não poderá ser reutilizado. Para reutilizar um nome de arquivo imediatamente, renomeie o arquivo existente.

Se você estiver excluindo um arquivo ou diretório aberto em um computador remoto e ele já tiver sido aberto no computador remoto sem o conjunto de permissões de compartilhamento de leitura, não chame [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) para abrir o arquivo ou diretório para exclusão primeiro. Isso resultará em uma violação de compartilhamento.

 

 
