---
description: Os administradores podem criar, excluir e recriar diários de alterações.
ms.assetid: 26cbacc2-d26b-434b-91b5-31aedc96da13
title: Criando, modificando e excluindo um diário de alterações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d4cf9a597baa14fc929028eab262479da30797a2e423b779083f028927ce50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150862"
---
# <a name="creating-modifying-and-deleting-a-change-journal"></a>Criando, modificando e excluindo um diário de alterações

Os administradores podem criar, excluir e recriar diários de alterações no. Um administrador deve excluir um diário quando o valor de USN (número de sequência de atualização) atual se aproximar do valor USN máximo possível, conforme indicado pelo membro **MaxUsn** da estrutura de [**\_ \_ dados do diário USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-usn_journal_data_v0) . Um administrador também pode excluir e recriar um diário de alterações para recuperar espaço em disco. Para executar essa e todas as outras operações de diário de alteração não programática, você deve ter privilégios de administrador do sistema. Ou seja, você deve ser um membro do grupo Administradores.

Para criar ou modificar um diário de alterações em um volume especificado programaticamente, use o código de controle do [**\_ \_ \_ diário fsctl Create USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) .

Quando você cria um novo diário de alterações ou modifica um existente, o sistema de arquivos NTFS define informações para esse diário de alterações de informações na estrutura de [**\_ \_ \_ dados criar diário de USN**](/windows/desktop/api/WinIoCtl/ns-winioctl-create_usn_journal_data) , que [**fsctl \_ criar \_ \_ diário de USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_create_usn_journal) usa como entrada. **Criar \_ Os \_ \_ dados do diário de USN** têm os membros **MaximumSize** e **AllocationDelta**.

**MaximumSize** é o tamanho máximo de destino para o diário de alterações em bytes. O diário de alterações pode crescer maior que esse valor, mas em pontos de verificação do sistema de arquivos NTFS o sistema de arquivos NTFS examina o diário e o corta quando seu tamanho excede o valor de **MaximumSize** mais o valor de **AllocationDelta**. (Em pontos de verificação do sistema de arquivos NTFS, o sistema operacional grava registros no arquivo de log do sistema de arquivos NTFS que permite que o sistema de arquivos NTFS determine qual processamento é necessário para se recuperar de uma falha.)

**AllocationDelta** é o número de bytes adicionados ao final e removido do início do diário de alterações cada vez que a memória é alocada ou desalocada. Em outras palavras, a alocação e a desalocação ocorrem em unidades desse tamanho. Um inteiro múltiplo de um tamanho de cluster é um valor razoável para esse membro.

Se um administrador modificar um diário de alterações existente para ter um valor **MaximumSize** maior, por exemplo, se um volume estiver sendo reindexado com muita frequência, o diário de alterações simplesmente receberá novas entradas até que ela exceda o novo tamanho máximo.

Para excluir um diário de alterações, use o código de controle do [**diário de fsctl \_ delete \_ USN \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) . Quando você usa essa operação, ela percorre todos os arquivos no volume e redefine o USN para cada arquivo como zero. Em seguida, a operação exclui o diário de alterações existente. Essa operação persiste entre as reinicializações do sistema até que ele seja concluído. Qualquer tentativa de ler, criar ou modificar o diário de alterações durante esse processo falha com a exclusão do **diário de erros do código \_ de erro \_ \_ em \_ andamento**.

Você também pode usar o código de controle do [**\_ \_ \_ diário fsctl Delete USN**](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_usn_journal) para determinar se uma exclusão iniciada por algum outro processo está em andamento. Por exemplo, seu aplicativo, quando ele é iniciado, pode determinar se uma exclusão está em andamento. Como as exclusões do diário persistem entre reinicializações do sistema, os serviços e aplicativos iniciados na reinicialização do sistema devem verificar se há uma exclusão em andamento.

Os diários de alterações não são necessariamente criados na inicialização. Para criar um diário de alterações, um administrador pode fazê-lo explicitamente ou iniciar outro serviço que exija um diário de alterações.

 

 
