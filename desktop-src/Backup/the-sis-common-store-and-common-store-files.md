---
title: Os arquivos de armazenamento e Common-Store comuns do SIS
description: Todos os arquivos de backup mantidos pelo backup do SIS (Single-Instance Store) são chamados de arquivos de armazenamento comuns.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Backup de repositórios comuns
- Backup do SIS (Single-Instance Store), armazenamentos comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823889"
---
# <a name="the-sis-common-store-and-common-store-files"></a>Os arquivos de armazenamento e Common-Store comuns do SIS

Todos os arquivos de backup mantidos pelo backup do SIS (Single-Instance Store) são chamados *de arquivos de armazenamento comuns*. Existe um *repositório comum* em cada volume mantido no SIS e contém todos os arquivos de armazenamento comum existentes nesse volume. Esse diretório está localizado no diretório raiz do volume e é denominado " \\ SIS Common Store". O repositório comum é implementado como um diretório protegido contra acesso de usuário normal, pois os arquivos de armazenamento comum devem ser acessados diretamente apenas por funções de API de backup do SIS e aplicativos de backup e restauração.

As propriedades de um arquivo de repositório comum são as seguintes:

-   Um arquivo de armazenamento comum pode ter um ou mais links apontando para ele.
-   Depois de criado, o conteúdo de um arquivo de armazenamento comum nunca é alterado.
-   Os nomes de arquivos de armazenamento comuns são globalmente exclusivos, ou seja, são exclusivos em todos os volumes em todos os sistemas do mundo, e a associação entre um nome de arquivo de repositório comum e seus dados é globalmente estática.

Quando o SIS é habilitado em um volume, uma cópia dos arquivos duplicados é criada para o armazenamento comum, e todos os arquivos duplicados são substituídos por [links do SIS](sis-links-and-reparse-points.md) apontando para o arquivo de repositório comum. Para obter mais informações, consulte [habilitando ou desabilitando o SIS em um volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) na documentação do TechNet.

Quando um dos links do SIS é acessado para uma operação de gravação, o filtro SIS primeiro restaura o conteúdo original do arquivo de link do SIS do arquivo de armazenamento comum, o ponto de nova análise vinculando o arquivo de link do SIS ao repositório comum é removido e, em seguida, a operação de gravação é executada no arquivo de destino original.

O arquivo de repositório comum é removido somente quando o último link SIS apontando para ele é excluído.

 

 