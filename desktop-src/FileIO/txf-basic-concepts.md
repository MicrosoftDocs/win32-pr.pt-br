---
description: Descreve a consistência de leitura confirmada, isolamento de confirmação de leitura e conceitos de bloqueio transacional em NTFS Transacional.
ms.assetid: 18579c4a-a832-4c89-8fb1-cd2542e4375e
title: Conceitos básicos do TxF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c71b2ed4e906fab881fac93a686dcf3aff6e8a95fa72d785ef14320ef92c05ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950965"
---
# <a name="basic-txf-concepts"></a>Conceitos básicos do TxF

## <a name="read-isolation"></a>Isolamento de leitura

O NTFS Transacional (TxF) fornece consistência de leitura confirmada.

Um [*gravador transacionado*](glossary.md) refere-se a um identificador de arquivo transacionado aberto com qualquer permissão que não faça parte do acesso de leitura genérico, mas que faz parte do acesso de gravação genérico. Um *gravador transacionado* exibe a versão mais recente de um arquivo que inclui todas as alterações feitas pela mesma transação. Pode haver apenas um gravador transacionado por arquivo. Os gravadores não transacionais sempre são bloqueados por um gravador transacionado, mesmo que o arquivo seja aberto com permissões de gravação compartilhada.

Um [*leitor transacionado*](glossary.md) refere-se a um identificador de arquivo transacionado aberto com qualquer permissão que faça parte do acesso de leitura genérico, mas que não faz parte do acesso de gravação genérico. Um *leitor transacionado* exibe uma versão confirmada do arquivo que existia no momento em que o identificador de arquivo foi aberto. O leitor transacionado é isolado dos efeitos dos gravadores transacionados. Isso fornece uma exibição consistente do arquivo apenas para a vida útil do identificador de arquivo e bloqueia gravadores não transacionados.

> [!Note]  
> Quando um identificador é aberto para modificação com a função [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) , todas as aberturas subsequentes do arquivo nessa transação se aplicam somente leitura ou não são convertidas pelo sistema para serem um gravador transacionado para fins de isolamento e outras semânticas transacionais. Isso significa que, subsequentemente, quando um identificador é aberto para acesso somente leitura, o identificador não recebe uma exibição do arquivo antes do início da transação; Ele recebe a exibição da transação ativa do arquivo.

 

Um identificador de arquivo não transacionado não verá nenhuma alteração feita dentro de uma transação até que a transação seja confirmada. O identificador de arquivo não transacionado recebe uma exibição isolada que é semelhante a um leitor transacionado, mas ao contrário de um leitor transacionado, ele recebe a atualização do arquivo quando um gravador transacionado confirma a transação.

## <a name="isolation-levels"></a>Níveis de isolamento

O TxF fornece isolamento de leitura confirmada. Isso significa que as atualizações de arquivo não são vistas fora da transação. Além disso, se um arquivo for aberto mais de uma vez durante a leitura de arquivos na transação, você poderá ver resultados diferentes com cada abertura subsequente. Os arquivos que estavam disponíveis na primeira vez que você os acessou podem não estar disponíveis (porque foram excluídos) ou vice-versa.

## <a name="transactional-locking"></a>Bloqueio transacional

A criação de um gravador transacionado em um arquivo *bloqueia transacionalmente* o arquivo. Depois que um arquivo é bloqueado por uma transação, outras operações do sistema de arquivos externas à transação de bloqueio que tentam modificar o arquivo bloqueado de forma transacional falharão com a **\_ \_ violação de compartilhamento de erro** ou com o erro de **\_ \_ conflito transacional**.

A tabela a seguir resume o bloqueio transacional.



Arquivo aberto atualmente por

Tentativa de abertura de arquivo por

Transacionado

Não transacionado

Leitor

Leitor/gravador

Leitor

Leitor/gravador

Leitor transacionado

Sim

Sim

Sim

Não2

Leitor/gravador transacionado

Sim

Não2

Sim

Não2

Leitor não transacionado

Sim

Sim

Sim

Sim

Leitor/gravador não transacionado

Nº 1

Nº 1

Sim

Sim

1. Falha com **erro de \_ \_ conflito transacional**<br/> 2. falha com **\_ \_ violação de compartilhamento de erro**<br/>



 

Se você abrir um fluxo nomeado para uma modificação que esteja usando uma transação, o arquivo inteiro será necessário para ser bloqueado.

Além do bloqueio transacional, as regras de compartilhamento de arquivos NTFS típicas se aplicam.

Você precisa considerar os dois modos de compartilhamento de arquivos a seguir em paralelo:

-   O modo de bloqueio transacional.
-   Modos normais de compartilhamento de arquivos.

O modo mais restritivo é aquele que se aplica.

 

 




