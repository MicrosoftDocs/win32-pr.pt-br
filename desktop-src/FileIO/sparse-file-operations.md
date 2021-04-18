---
description: Determine se um sistema de arquivos dá suporte a arquivos esparsos chamando a função GetVolumeInformation.
ms.assetid: a08f6bbc-c139-4396-8964-4aa63285f3f5
title: Operações de arquivo esparsos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c23d26fc1c52db32ca7674aec2fc487a826e9a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756938"
---
# <a name="sparse-file-operations"></a>Operações de arquivo esparsos

Para determinar se um sistema de arquivos dá suporte a arquivos esparsos, chame a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examine o arquivo que dá suporte ao sinalizador de bits de **\_ \_ \_ arquivos esparsos** retornado por meio do parâmetro *lpFileSystemFlags* .

A maioria dos aplicativos não reconhece arquivos esparsos e não criará arquivos esparsos. O fato de que um aplicativo está lendo um arquivo esparso é transparente para o aplicativo. Um aplicativo que reconhece arquivos esparsos deve determinar se seu conjunto de dados é adequado para ser mantido em um arquivo esparso. Depois que essa determinação é feita, o aplicativo deve declarar explicitamente um arquivo como esparso, usando o código de controle [**\_ \_ esparso Set fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_sparse) .

Depois que um aplicativo tiver definido um arquivo para ser esparso, o aplicativo poderá usar o código de controle de [**dados do fsctl \_ set \_ zero \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para definir uma região do arquivo como zero. Além disso, o aplicativo pode usar o código de controle de [**\_ \_ \_ intervalos alocados de consulta fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_query_allocated_ranges) para acelerar pesquisas de dados diferentes de zero no arquivo esparso.

Quando você executa uma operação de gravação (com uma função ou operação diferente de [**fsctl \_ define \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) cujos dados consistem em nada, menos zeros, os zeros serão gravados no disco durante todo o tamanho da gravação. Para zerar um intervalo do arquivo e manter a irgrosseira, use **fsctl \_ definir \_ zero \_ Data**.

Um aplicativo com reconhecimento de uma antigrosseira também pode definir um arquivo existente como esparso. Se um aplicativo definir um arquivo existente como esparso, ele deverá verificar o arquivo em busca de regiões que contêm zeros e usar [**fsctl \_ definir \_ \_ dados zero**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data) para redefinir essas regiões, possivelmente desalocando algum armazenamento de disco físico. Um aplicativo atualizado para o reconhecimento de arquivos esparsos deve executar essa conversão.

Quando você executa uma operação de leitura de uma parte zerada de um arquivo esparso, o sistema operacional pode não ler a partir da unidade de disco rígido. Em vez disso, o sistema reconhece que a parte do arquivo a ser lido contém zeros e retorna um buffer cheio de zeros sem realmente ler do disco.

Assim como acontece com qualquer outro arquivo, o sistema pode gravar dados ou ler dados de qualquer posição em um arquivo esparso. Dados diferentes de zero gravados em uma parte anterior zerada do arquivo podem resultar em alocação de espaço em disco. Os zeros que estão sendo gravados em dados diferentes de zero (somente com [**fsctl \_ set \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data)) podem resultar em uma desalocação do espaço em disco.

> [!Note]  
> Cabe ao aplicativo manter a irgrosseira gravando zeros com [**fsctl \_ define \_ zero \_ Data**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_zero_data).

 

As ferramentas de desfragmentação que lidam com arquivos compactados em sistemas de arquivos NTFS manipulam corretamente arquivos esparsos em volumes do sistema de arquivos NTFS. Arquivos esparsos grandes e altamente fragmentados podem exceder a limitação de NTFS em extensões de disco antes que o espaço disponível seja usado. Para obter mais informações, consulte [a extensão de um arquivo pode falhar com o erro "disco cheio", embora o volume tenha espaço livre](https://support.microsoft.com/default.aspx/kb/957180).

 

 
