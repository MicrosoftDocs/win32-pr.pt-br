---
description: Determine se um sistema de arquivos dá suporte a arquivos esparsos chamando a função GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Operações de arquivo esparsas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9835d550a414c047e578eb90fc9b55afbefb760d31d8333a290f00da7162f839
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015104"
---
# <a name="sparse-file-operations"></a>Operações de arquivo esparsas

Para determinar se um sistema de arquivos dá suporte a arquivos esparsos, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine o sinalizador de bit **FILE SUPPORTS \_ \_ SPARSE \_ FILES** retornado por meio do *parâmetro lpFileSystemFlags.*

A maioria dos aplicativos não está ciente de arquivos esparsos e não criará arquivos esparsos. O fato de que um aplicativo está lendo um arquivo esparso é transparente para o aplicativo. Um aplicativo que esteja ciente de arquivos esparsos deve determinar se seu conjunto de dados é adequado para ser mantido em um arquivo esparso. Depois que essa determinação for feita, o aplicativo deverá declarar explicitamente um arquivo como esparso, usando o código de controle [**FSCTL \_ SET \_ SPARSE.**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse)

Depois que um aplicativo tiver definido um arquivo para ser esparso, o aplicativo poderá usar o código de controle [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para definir uma região do arquivo como zero. Além disso, o aplicativo pode usar o código de controle [**FSCTL \_ \_ QUERY ALLOCATED \_ RANGES**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) para acelerar pesquisas de dados não zero no arquivo esparso.

Quando você executa uma operação de gravação (com uma função ou operação diferente de [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) cujos dados consistem em nada além de zeros, zeros serão gravados no disco durante todo o comprimento da gravação. Para zerar um intervalo do arquivo e manter a esparsidade, use **FSCTL \_ SET \_ ZERO \_ DATA**.

Um aplicativo com conhecimento de esparso também pode definir um arquivo existente para ser esparso. Se um aplicativo definir um arquivo existente para ser esparso, ele deverá verificar o arquivo para regiões que contêm zeros e usar [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para redefinir essas regiões, possivelmente desalocando algum armazenamento em disco físico. Um aplicativo atualizado para reconhecimento de arquivo esparso deve executar essa conversão.

Quando você executa uma operação de leitura de uma parte zerada de um arquivo esparso, o sistema operacional pode não ler da unidade de disco rígido. Em vez disso, o sistema reconhece que a parte do arquivo a ser lido contém zeros e retorna um buffer cheio de zeros sem realmente ler do disco.

Assim como com qualquer outro arquivo, o sistema pode gravar ou ler dados de qualquer posição em um arquivo esparso. Dados não zero gravados em uma parte anteriormente zerada do arquivo podem resultar na alocação de espaço em disco. Zeros que estão sendo gravados em dados não zero (somente com [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) podem resultar em uma desalocação de espaço em disco.

> [!Note]  
> O aplicativo deve manter a moderação escrevendo zeros com [**FSCTL \_ SET \_ ZERO \_ DATA**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).

 

Ferramentas de desfragmentação que lidam com arquivos compactados em sistemas de arquivos NTFS tratarão corretamente arquivos esparsos em volumes do sistema de arquivos NTFS. Arquivos esparsos grandes e altamente fragmentados podem exceder a limitação de NTFS em extensão de disco antes que o espaço disponível seja usado. Para obter mais informações, consulte Estender um arquivo pode falhar com o erro ["Disco Cheio",](https://support.microsoft.com/default.aspx/kb/957180)mesmo que o volume tenha espaço livre.

 

 
