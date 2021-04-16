---
description: Descreve várias considerações de programação para NTFS Transacional.
ms.assetid: a1ef1ce1-42f6-4627-ab64-e7f41fa23e94
title: Considerações de programação para NTFS Transacional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79dc7eba4de1258c294d3e41f8042f3cb01dc87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757854"
---
# <a name="programming-considerations-for-transactional-ntfs"></a>Considerações de programação para NTFS Transacional

Para obter uma descrição de várias considerações de programação para NTFS Transacional, consulte as seguintes seções:

-   [Quais alterações de arquivo são transacionadas](#which-file-changes-are-transacted)
-   [Compactação](#compression)
-   [Criando um arquivo ou diretório](#creating-a-file-or-directory)
-   [Excluindo um arquivo](#deleting-a-file)
-   [Excluindo um diretório](#deleting-a-directory)
-   [Problemas de bloqueio de diretório](#directory-locking-issues)
-   [Enumeração de diretório](#directory-enumeration)
-   [Arquivos mapeados para memória](#memory-mapped-files)
-   [Fluxos nomeados](#named-streams)
-   [Renomeando um arquivo ou diretório](#renaming-a-file-or-directory)
-   [Pontos de reanálise](#reparse-points)
-   [Códigos de Erro](#error-codes)
-   [Sistema de arquivos criptografados](#encrypted-file-system)
-   [Funções de e/s de arquivo e NTFS Transacional](#file-io-functions-and-transactional-ntfs)
    -   [Funções transacionadas](#transacted-functions)
    -   [Funções de e/s de arquivo alteradas pelo TxF](#file-io-functions-changed-by-txf)

## <a name="which-file-changes-are-transacted"></a>Quais alterações de arquivo são transacionadas

A maioria das alterações de arquivo, como alterações no conteúdo do arquivo, fluxos, pontos de nova análise, atributos e o namespace do sistema de arquivos, são transacionadas. Quando uma dessas alterações é feita em um identificador de arquivo transacionado, a alteração é isolada de outras transações e a alteração é desfeita se a transação é revertida.

As alterações que não afetam o conteúdo do arquivo, os metadados ou o namespace do sistema de arquivos, como alterações na compactação ou desfragmentação, não são transacionadas. Essas alterações não são isoladas de outras transações e não são desfeitas se a transação é revertida.

## <a name="compression"></a>Compactação

O estado de compactação de um arquivo aberto em uma transação não pode ser alterado.

## <a name="creating-a-file-or-directory"></a>Criando um arquivo ou diretório

Um arquivo ou diretório criado em uma transação não é visível para nada fora da transação atual. Fora dessa transação, qualquer tentativa de criar um arquivo com o mesmo nome falhará com o erro de erro de **\_ \_ conflito transacional**, reservando efetivamente o nome do arquivo para quando a transação for confirmada ou for revertida.

## <a name="deleting-a-file"></a>Excluindo um arquivo

Um arquivo ou diretório que é excluído chamando a função [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda) permanece visível para todos os leitores externos.

> [!Note]  
> Todos os identificadores transacionados para o arquivo devem ser fechados antes do fim da transação. Se os identificadores não forem fechados corretamente, a exclusão não ocorrerá. Todos os identificadores abertos para o arquivo devem ser fechados antes de executar a confirmação para que a operação de exclusão seja considerada parte da transação. Isso ocorre porque o sistema não exclui realmente um arquivo até que o último identificador para ele seja fechado, mesmo quando a operação não é transacionada, como parte do subsistema de e/s de arquivo do Windows.

 

## <a name="deleting-a-directory"></a>Excluindo um diretório

Um diretório que é excluído chamando a função [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda) permanece visível para todos os leitores externos.

> [!Note]  
> As mesmas restrições existem para identificadores abertos em operações de diretório transacionadas como arquivos. Para obter mais informações, consulte [excluindo um arquivo](#deleting-a-file).

 

## <a name="directory-locking-issues"></a>Problemas de bloqueio de diretório

Se um arquivo for modificado em uma transação, todos os componentes de diretório do caminho para o arquivo serão referidos como *fixos em relação a Rename* até que a transação termine. Ou seja, o sistema impede que você os renomeie até que a transação seja confirmada ou revertida. Uma tentativa de renomear um diretório que seja um ancestral para um arquivo que foi modificado em uma transação em andamento falhará e o erro não poderá **\_ interromper a \_ \_ \_ dependência transacional**.

## <a name="directory-enumeration"></a>Enumeração de diretório

O conteúdo de um diretório pode ser alterado enquanto uma enumeração está em andamento como resultado do uso de APIs que enumeram, por exemplo, as funções [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) e [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) .

As alterações em um diretório fora de uma transação não são isoladas da transação e ficam visíveis imediatamente dentro da transação. Por exemplo, se um gravador não transacionado adicionar um arquivo a um diretório, o novo arquivo será imediatamente visível dentro da transação, de modo que chamar a função [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda) ou [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) retornará o novo arquivo.

As alterações feitas em um diretório dentro de uma transação são isoladas até que a transação seja confirmada. Por exemplo, um arquivo criado no diretório como parte da transação. Um leitor não transacionado que chama a função [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) ou [**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea) não verá o arquivo recém-criado até que a transação seja confirmada.

## <a name="memory-mapped-files"></a>Arquivos mapeados na memória

O cliente deve chamar a função [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile) , fechar o objeto de mapeamento de arquivo e fechar o identificador de arquivo antes de confirmar a transação associada em um arquivo mapeado para a memória.

## <a name="named-streams"></a>Fluxos nomeados

Os fluxos nomeados são totalmente transacionais, mas o bloqueio é feito no nível do arquivo, não no nível do fluxo. Gravadores de fora de uma transação que tentam modificar qualquer fluxo em um arquivo bloqueado recebem o erro erro de **\_ compartilhamento de \_ violação**.

Não é possível renomear um fluxo secundário em uma transação.

## <a name="renaming-a-file-or-directory"></a>Renomeando um arquivo ou diretório

Para renomear um arquivo como uma operação transacionada, chame [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda) para mover o arquivo.

## <a name="reparse-points"></a>Pontos de reanálise

As alterações nos pontos de nova análise são transacionadas, o que significa que, se um novo ponto de nova análise for atribuído a um arquivo em uma transação, ele não será visível para as outras transações. Da mesma forma, as alterações ou a remoção de um ponto de nova análise existente não estarão visíveis até a confirmação.

## <a name="error-codes"></a>Códigos de erro

O KTM (kernel Transaction Manager) usa os códigos de erro do sistema no intervalo de 6700 a 6799. O NTFS Transacional (TxF) usa códigos de erro do Windows no intervalo de 6800 a 6899. Para obter mais informações, consulte WinError. h e códigos de erro do sistema (6000-8199).

## <a name="encrypted-file-system"></a>Sistema de arquivos criptografados

O TxF não oferece suporte a operações em arquivos EFS. Não é possível abrir um arquivo criptografado com EFS para transações. A chamada da função [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) em um arquivo EFS falhará, com o **erro o \_ EFS \_ não \_ permitido \_ na \_ transação**. Da mesma forma, chamar a função [**EncryptFile**](/windows/desktop/api/WinBase/nf-winbase-encryptfilea) em um arquivo em uma transação falhará, com o erro de erro **\_ EFS \_ não \_ permitido \_ na \_ transação**.

## <a name="file-io-functions-and-transactional-ntfs"></a>Funções de e/s de arquivo e NTFS Transacional

O TxF fornece novas funções transacionadas que usam um nome de arquivo e altera o comportamento de funções de API de e/s de arquivo existentes que usam um identificador de arquivo.

### <a name="transacted-functions"></a>Funções transacionadas

Se você não chamar uma das seguintes funções transacionadas no lugar de sua versão não transacionada, a operação não será transacionada:

-   [**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
-   [**CreateDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-createdirectorytransacteda)
-   [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
-   [**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
-   [**CreateSymbolicLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinktransacteda)
-   [**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
-   [**FindFirstFileNameTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirstfilenametransactedw)
-   [**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
-   [**FindFirstStreamTransactedW**](/windows/desktop/api/WinBase/nf-winbase-findfirststreamtransactedw)
-   [**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
-   [**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
-   [**GetFullPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfullpathnametransacteda)
-   [**GetLongPathNameTransacted**](/windows/desktop/api/WinBase/nf-winbase-getlongpathnametransacteda)
-   [**MoveFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-movefiletransacteda)
-   [**RemoveDirectoryTransacted**](/windows/desktop/api/WinBase/nf-winbase-removedirectorytransacteda)
-   [**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)

Por exemplo, a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) agora tem uma versão transacionada: [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).

### <a name="file-io-functions-changed-by-txf"></a>Funções de e/s de arquivo alteradas pelo TxF

A tabela a seguir lista as funções cujo comportamento é afetado pelo NTFS Transacional. Por exemplo, o comportamento da função [**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile) irá variar dependendo se o parâmetro *hFile* foi criado pela função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou pela função [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda) .



| Função                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CloseHandle"></span><span id="closehandle"></span><span id="CLOSEHANDLE"></span>[**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle)<br/>                                                                                                                                                                                                                                                                                                             | Os aplicativos devem fechar todos os identificadores associados a uma transação antes que a transação seja confirmada. Um aplicativo deve fechar um identificador transacionado aberto com o **\_ sinalizador \_ de arquivo Delete \_ em \_ Close** antes de confirmar a transação para que a operação de exclusão ocorra.<br/>                                                                                                                                     |
| <span id="CreateFileMapping"></span><span id="createfilemapping"></span><span id="CREATEFILEMAPPING"></span>[**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)<br/>                                                                                                                                                                                                                                                                                 | Se houver uma transação associada a *hFile*, o objeto de mapeamento de arquivo que essa função cria será associado à mesma transação. As modificações feitas por meio de exibições desse objeto de mapeamento de arquivos são transacionadas. Os aplicativos devem chamar [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), desmapear todas as exibições e fechar todos os identificadores para o objeto de mapeamento de arquivo antes de confirmar as alterações transacionadas.<br/> |
| <span id="FindNextFile"></span><span id="findnextfile"></span><span id="FINDNEXTFILE"></span>[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)<br/>                                                                                                                                                                                                                                                                                                         | Se houver uma transação associada ao identificador de enumeração de arquivo, os arquivos retornados estarão sujeitos às regras de isolamento da transação.<br/>                                                                                                                                                                                                                                                                    |
| <span id="FSCTL_SET_COMPRESSION"></span><span id="fsctl_set_compression"></span>[**\_compactação do conjunto de fsctl \_**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression)<br/>                                                                                                                                                                                                                                                                                                  | Não é possível alterar o estado de compactação de um arquivo aberto pelo [**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda).<br/>                                                                                                                                                                                                                                                                                               |
| <span id="GetFileInformationByHandle__________and__________GetFileInformationByHandleEx"></span><span id="getfileinformationbyhandle__________and__________getfileinformationbyhandleex"></span><span id="GETFILEINFORMATIONBYHANDLE__________AND__________GETFILEINFORMATIONBYHANDLEEX"></span>[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle) e [ **GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)<br/> | Se houver uma transação associada ao identificador de arquivo, a função retornará informações para a exibição de arquivo isolado.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetFileSize_and__________GetFileSizeEx"></span><span id="getfilesize_and__________getfilesizeex"></span><span id="GETFILESIZE_AND__________GETFILESIZEEX"></span>[**GetFiles**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesize) e [ **GetFileSizeEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfilesizeex)<br/>                                                                                                                                                                                  | Se houver uma transação associada ao identificador de arquivo, a função retornará informações para a exibição de arquivo isolado.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="GetVolumeInformation"></span><span id="getvolumeinformation"></span><span id="GETVOLUMEINFORMATION"></span>[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)<br/>                                                                                                                                                                                                                                                                 | Se o volume der suporte a transações do sistema de arquivos, a função retornará o **arquivo \_ com suporte a \_ Transações** em *lpFileSystemFlags*.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="MapViewOfFile_and__________MapViewOfFileEx"></span><span id="mapviewoffile_and__________mapviewoffileex"></span><span id="MAPVIEWOFFILE_AND__________MAPVIEWOFFILEEX"></span>[**MapViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffile) e [ **MapViewOfFileEx**](/windows/desktop/api/memoryapi/nf-memoryapi-mapviewoffileex)<br/>                                                                                                                                                                | Se houver uma transação associada ao identificador de arquivo usado para criar o objeto de mapeamento de arquivo que está sendo mapeado, a exibição associada será transacionada. Se a exibição for usada para fazer alterações transacionais em um arquivo, o usuário deverá chamar [**FlushViewOfFile**](/windows/desktop/api/memoryapi/nf-memoryapi-flushviewoffile), fechar o objeto de mapeamento de arquivo e fechar o identificador de arquivo antes de confirmar a transação associada.<br/>              |
| <span id="ReadDirectoryChangesW"></span><span id="readdirectorychangesw"></span><span id="READDIRECTORYCHANGESW"></span>[**ReadDirectoryChangesW**](/windows/desktop/api/WinBase/nf-winbase-readdirectorychangesw)<br/>                                                                                                                                                                                                                                                            | Se houver uma transação associada ao identificador de diretório, as notificações refletirão a exibição isolada do diretório. As alterações em arquivos fora da exibição transacionada do diretório não são incluídas nas notificações.<br/>                                                                                                                                                                                |
| <span id="ReadFile___________ReadFileEx__and__________ReadFileScatter"></span><span id="readfile___________readfileex__and__________readfilescatter"></span><span id="READFILE___________READFILEEX__AND__________READFILESCATTER"></span>[**ReadFile**](/windows/desktop/api/FileAPI/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex)e [**ReadFileScatter**](/windows/desktop/api/FileAPI/nf-fileapi-readfilescatter)<br/>                                                                                  | Se houver uma transação associada ao identificador de arquivo, a função retornará dados da exibição transacionada do arquivo. É garantido que um identificador de leitura transacionado mostre a mesma exibição de um arquivo durante a duração do identificador.<br/>                                                                                                                                                                                 |
| <span id="SetEndOfFile"></span><span id="setendoffile"></span><span id="SETENDOFFILE"></span>[**SetEndOfFile**](/windows/desktop/api/FileAPI/nf-fileapi-setendoffile)<br/>                                                                                                                                                                                                                                                                                                         | Se houver uma transação associada ao identificador, a alteração na posição final do arquivo será transacionada.<br/>                                                                                                                                                                                                                                                                                                       |
| <span id="SetFileInformationByHandle"></span><span id="setfileinformationbyhandle"></span><span id="SETFILEINFORMATIONBYHANDLE"></span>[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)<br/>                                                                                                                                                                                                                                   | Se houver uma transação associada ao identificador, as alterações feitas serão transacionadas para as classes de informações **FileBasicInfo**, **FileRenameInfo**, **FileAllocationInfo**, **FileEndOfFileInfo** e **FileDispositionInfo**.<br/>                                                                                                                                                                          |
| <span id="SetFileShortName"></span><span id="setfileshortname"></span><span id="SETFILESHORTNAME"></span>[**SetFileShortName**](/windows/desktop/api/WinBase/nf-winbase-setfileshortnamea)<br/>                                                                                                                                                                                                                                                                                     | Se houver uma transação associada ao identificador, a alteração no nome curto do arquivo será transacionada.<br/>                                                                                                                                                                                                                                                                                                          |
| <span id="SetFileTime"></span><span id="setfiletime"></span><span id="SETFILETIME"></span>[**SetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-setfiletime)<br/>                                                                                                                                                                                                                                                                                                             | Se houver uma transação associada ao identificador, a alteração na hora do arquivo será transacionada.<br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="WriteFile__________WriteFileEx__and_________WriteFileGather"></span><span id="writefile__________writefileex__and_________writefilegather"></span><span id="WRITEFILE__________WRITEFILEEX__AND_________WRITEFILEGATHER"></span>[**WriteFile**](/windows/desktop/api/FileAPI/nf-fileapi-writefile), [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)e [**WriteFileGather**](/windows/desktop/api/FileAPI/nf-fileapi-writefilegather)<br/>                                                                              | Se houver uma transação associada ao identificador de arquivo, a gravação do arquivo será transacionada.<br/>                                                                                                                                                                                                                                                                                                                          |



 

 

