---
title: O Armazenamento Comum do SIS e Common-Store arquivos
description: Todos os arquivos de backup mantidos pelo backup do SIS (armazenamento de instância única) são chamados de arquivos de armazenamento comum.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Backup de lojas comuns
- Backup de armazenamento de instância única (SIS), armazenamentos comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f19337a967fd858c149bc9d4261abc44214d4c76023abe022b5e1c5efd5f8ed3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119529466"
---
# <a name="the-sis-common-store-and-common-store-files"></a>O Armazenamento Comum do SIS e Common-Store arquivos

Todos os arquivos de backup mantidos pelo backup do SIS (armazenamento de instância única) são chamados *de arquivos de armazenamento comum.* Existe *um armazenamento* comum em cada volume mantido pelo SIS e contém todos os arquivos de armazenamento comum que existem nesse volume. Esse diretório está localizado no diretório raiz do volume e é denominado " \\ Armazenamento Comum do SIS". O armazenamento comum é implementado como um diretório que é protegido contra o acesso normal do usuário, porque os arquivos de armazenamento comum devem ser acessados diretamente apenas por funções de API de backup do SIS e não por aplicativos de backup e restauração.

As propriedades de um arquivo de armazenamento comum são as seguintes:

-   Um arquivo de armazenamento comum pode ter um ou mais links apontando para ele.
-   Depois que ele é criado, o conteúdo de um arquivo de armazenamento comum nunca muda.
-   Os nomes dos arquivos de armazenamento comum são globalmente exclusivos, ou seja, são exclusivos em todos os volumes em todos os sistemas do mundo e a associação entre um nome de arquivo de armazenamento comum e seus dados é globalmente estática.

Quando o SIS está habilitado em um volume, uma cópia dos arquivos duplicados é criada no armazenamento comum e todos os arquivos duplicados são substituídos por [links do SIS](sis-links-and-reparse-points.md) apontando para o arquivo de armazenamento comum. Para obter mais informações, consulte [Habilitando ou desabilitando o SIS em um volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) na documentação do TechNet.

Quando um dos links do SIS é acessado para uma operação de gravação, o filtro do SIS restaura primeiro o conteúdo original do arquivo de link do SIS do arquivo de armazenamento comum, o ponto de nova análise que vincula o arquivo de link do SIS ao armazenamento comum é removido e, em seguida, a operação de gravação é executada no arquivo de destino original.

O arquivo de armazenamento comum é removido somente quando o último link do SIS apontando para ele é excluído.

 

 