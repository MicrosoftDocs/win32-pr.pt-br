---
description: O sistema de arquivos NTFS associa um identificador de 64 bits sem assinatura a cada diário de alteração.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Usando o identificador de diário de alteração
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483c171b69bcee0faf8df9f325d4ee8ffcb6e904f6aa0cd3c720b83df326e3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015064"
---
# <a name="using-the-change-journal-identifier"></a>Usando o identificador de diário de alteração

O sistema de arquivos NTFS associa um identificador de 64 bits sem assinatura a cada diário de alteração. O diário é carimbado com esse identificador quando ele é criado. O sistema de arquivos carimba o diário com um novo identificador em que os registros USN (número de sequência de atualização) existentes são ou podem ser inutilizáveis.

Por exemplo, o sistema de arquivos NTFS é um diário de alteração com um novo identificador quando um volume é movido de uma versão do NTFS para outra e, em seguida, de volta. Essa movimentação pode ocorrer em um ambiente de inicialização dupla ou ao trabalhar com mídia removível.

Para obter o identificador do diário de alterações atual em um volume especificado, use o código de controle [**FSCTL \_ QUERY \_ USN \_ JOURNAL.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) Para executar essa e todas as outras operações de diário de alteração, você deve ter privilégios de administrador do sistema. Ou seja, você deve ser um membro do grupo Administradores.

Quando um administrador exclui e cria novamente o diário de alteração, por exemplo, quando o valor USN atual se aproxima do valor máximo de USN possível, os valores de USN começam novamente do zero. Quando o sistema de arquivos NTFS carimba um diário com um novo identificador em vez de re-criar o diário, ele não redefine o USN para zero, mas continua do USN atual. Em ambos os casos, todos os USNs existentes são menores que quaisquer USNs futuras.

Quando você precisar de informações sobre um conjunto específico de registros, use o código de controle [**FSCTL \_ QUERY \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) para obter o identificador de diário de alteração. Em seguida, use o código de controle [**FSCTL \_ READ \_ USN \_ JOURNAL**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ler os registros de diário de interesse. O sistema de arquivos NTFS retorna apenas registros válidos para o diário especificado pelo identificador.

Seu aplicativo precisa de USNs dos registros e do identificador para ler o diário. Esse requisito fornece uma verificação de integridade para casos em que seu aplicativo deve ignorar os registros existentes no arquivo e onde os registros foram gravados em instâncias anteriores do diário para o mesmo volume.

Para obter os registros nos quais você está interessado, você deve começar no registro mais antigo (ou seja, com o USN mais baixo) e examinar para frente até localizar o primeiro registro de interesse.

 

 
