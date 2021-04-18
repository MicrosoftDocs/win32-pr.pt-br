---
description: Cada pipe nomeado tem um nome exclusivo que o distingue de outros pipes nomeados na lista de sistemas de objetos nomeados. Um servidor de pipe especifica um nome para o pipe ao chamar a função CreateNamedPipe para criar uma ou mais instâncias de um pipe nomeado.
ms.assetid: 8f7e717a-648b-421e-ab79-a4abbae670be
title: Nomes de pipe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e470a09fa4cfe1b2f259ca3fd5b53f79045787fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796282"
---
# <a name="pipe-names"></a>Nomes de pipe

Cada pipe nomeado tem um nome exclusivo que o distingue de outros pipes nomeados na lista de objetos nomeados do sistema. Um servidor de pipe especifica um nome para o pipe ao chamar a função [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) para criar uma ou mais instâncias de um pipe nomeado. Os clientes de pipe especificam o nome do pipe quando chamam a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para se conectar a uma instância do pipe nomeado.

Use o seguinte formulário ao especificar o nome de um pipe na função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea)ou [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) :

\\\\*Nome do Server* \\ \\*pipeName* do pipe

em que *ServerName* é o nome de um computador remoto ou um ponto, para especificar o computador local. A cadeia de caracteres do nome do pipe especificada por *pipeName* pode incluir qualquer caractere diferente de uma barra invertida, incluindo números e caracteres especiais. A cadeia de caracteres do nome do pipe inteiro pode ter até 256 caracteres. Os nomes dos pipes não diferenciam maiúsculas de minúsculas.

O servidor de pipe não pode criar um pipe em outro computador, portanto, [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) deve usar um ponto para o nome do servidor, conforme mostrado no exemplo a seguir.

\\\\.\\ \\*pipeName* do pipe

Um servidor de pipe pode fornecer o nome do pipe para seus clientes de pipe, para que eles possam se conectar ao pipe. O cliente de pipe descobre o nome do pipe de alguma fonte persistente, como uma entrada de registro, um arquivo ou outro aplicativo. Caso contrário, os clientes devem saber o nome do pipe em tempo de compilação.

 

 
