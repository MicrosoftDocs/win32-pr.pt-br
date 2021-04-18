---
description: O sistema de arquivos NTFS associa um identificador não assinado de 64 bits a cada diário de alterações.
ms.assetid: 5ae79460-b69a-4901-a417-1d5358dcba29
title: Usando o identificador do diário de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 692acf98403e45b6bdafd3cd4791a64dd1beb532
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758813"
---
# <a name="using-the-change-journal-identifier"></a>Usando o identificador do diário de alterações

O sistema de arquivos NTFS associa um identificador não assinado de 64 bits a cada diário de alterações. O diário é carimbado com esse identificador quando ele é criado. O sistema de arquivos marca o diário com um novo identificador em que os registros USN (número de sequência de atualização) existentes são ou podem ser inutilizáveis.

Por exemplo, o sistema de arquivos NTFS remarca um diário de alterações com um novo identificador quando um volume é movido de uma versão do NTFS para outra e, em seguida, de volta. Essa movimentação pode acontecer em um ambiente de inicialização dupla ou ao trabalhar com mídia removível.

Para obter o identificador do diário de alterações atual em um volume especificado, use o código de controle do [**\_ diário de \_ USN \_ do fsctl Query**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) . Para executar essa e todas as outras operações de diário de alterações, você deve ter privilégios de administrador do sistema. Ou seja, você deve ser um membro do grupo Administradores.

Quando um administrador exclui e recria o diário de alterações, por exemplo, quando o valor USN atual se aproxima do valor USN máximo possível, os valores USN começam novamente a partir de zero. Quando o sistema de arquivos NTFS carimba um diário com um novo identificador em vez de recriar o diário, ele não redefine o USN para zero, mas continua do USN atual. Em ambos os casos, todos os USNs existentes são menores do que quaisquer USNs futuros.

Quando você precisar de informações sobre um conjunto específico de registros, use o código de controle do [**diário de fsctl \_ consulta do \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_usn_journal) para obter o identificador do diário de alterações. Em seguida, use o código de controle do [**\_ \_ \_ diário USN fsctl ler**](/windows/win32/api/winioctl/ni-winioctl-fsctl_read_usn_journal) para ler os registros de diário de interesse. O sistema de arquivos NTFS retorna apenas os registros que são válidos para o diário especificado pelo identificador.

Seu aplicativo precisa dos USNs dos registros e do identificador para ler o diário. Esse requisito fornece uma verificação de integridade para casos em que o aplicativo deve ignorar os registros existentes no arquivo e onde os registros foram gravados em instâncias anteriores do diário para o mesmo volume.

Para obter os registros nos quais você está interessado, você deve iniciar no registro mais antigo (ou seja, com o USN mais baixo) e fazer uma varredura para frente até localizar o primeiro registro de interesse.

 

 
