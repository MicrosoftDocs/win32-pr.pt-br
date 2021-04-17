---
description: Como os links simbólicos afetam as funções de arquivo padrão que usam nomes de caminho para especificar um ou mais arquivos.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Efeitos de link simbólico em funções de sistemas de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105769352"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a>Efeitos de link simbólico em funções de sistemas de arquivos

Várias funções de arquivo padrão que usam nomes de caminho para especificar um ou mais arquivos são afetadas pelo uso de links simbólicos. Este tópico lista essas funções e descreve as alterações no comportamento:

-   [CopyFile e CopyFileTransacted](#copyfile-and-copyfiletransacted)
-   [CopyFileEx](#copyfileex)
-   [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted)
-   [CreateHardLink e CreateHardLinkTransacted](#createhardlink-and-createhardlinktransacted)
-   [Excluirfile e DeleteFileTransacted](#deletefile-and-deletefiletransacted)
-   [FindFirstChangeNotification](#findfirstchangenotification)
-   [FindFirstFile e FindFirstFileTransacted](#findfirstfile-and-findfirstfiletransacted)
-   [FindFirstFileEx](#findfirstfileex)
-   [FindNextFile](#findnextfile)
-   [Getbinarytype](#getbinarytype)
-   [GetCompressedFileSize e GetCompressedFileSizeTransacted](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [GetDiskFreeSpace](#getdiskfreespaceex)
-   [GetDiskFreeSpaceEx](#getdiskfreespaceex)
-   [GetFileAttributes](#getfileattributesex)
-   [GetFileAttributesEx](#getfileattributesex)
-   [GetFileSecurity](#getfilesecurity)
-   [GetTempPath](#gettemppath)
-   [GetVolumeInformation](#getvolumeinformation)
-   [SetFileAttributes](#setfileattributes)
-   [SetFileSecurity](#setfilesecurity)
-   [Tópicos relacionados](#related-topics)

Nas descrições a seguir, os seguintes termos são usados:

-   Arquivo de origem — o arquivo original a ser copiado.
-   Arquivo de destino — a cópia recém-criada do arquivo.
-   Target — a entidade à qual um link simbólico aponta.

> [!Note]  
> O comportamento das funções que aceitam um identificador criado usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , como a função [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , será diferente se a função **CreateFile** for ou não chamada com o sinalizador **File \_ Flag \_ Open \_ reparse \_ Point** . Para obter mais informações, consulte [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e a seguinte seção [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted) .

 

## <a name="copyfile-and-copyfiletransacted"></a>CopyFile e CopyFileTransacted

Se o arquivo de origem for um link simbólico, o arquivo real copiado será o destino do link simbólico.

Se o arquivo de destino já existir e for um link simbólico, o link simbólico será substituído pelo arquivo de origem.

## <a name="copyfileex"></a>CopyFileEx

Se **Copy \_ File \_ Copy \_ SYMLINK** for especificado e:

-   Se o arquivo de origem for um link simbólico, o link simbólico será copiado, não o arquivo de destino.
-   Se o arquivo de origem não for um link simbólico, não haverá alteração no comportamento.
-   Se o arquivo de destino for um link simbólico existente, o link simbólico será substituído, não o arquivo de destino.
-   Se **o \_ arquivo de cópia falhar, \_ \_ se \_ existir** também for especificado e o arquivo de destino for um link simbólico existente, a operação falhará em todos os casos.

Se **Copy \_ File \_ Copy \_ SYMLINK** não for especificado e:

-   Se **o \_ arquivo de cópia falhar, \_ \_ se \_ existir** também for especificado e o arquivo de destino for um link simbólico existente, a operação falhará somente se o destino do link simbólico existir.
-   Se **o \_ arquivo de cópia \_ falhar \_ se \_ Exists** não for especificado, não haverá alteração no comportamento.

**Windows Server 2003 e Windows XP:** Não há suporte para o sinalizador **SYMLINK de cópia de arquivo de cópia \_ \_ \_** . Se o arquivo de origem for um link simbólico, o arquivo real copiado será o destino do link simbólico.

## <a name="createfile-and-createfiletransacted"></a>CreateFile e CreateFileTransacted

Se a chamada para essa função criar um novo arquivo, não haverá alteração no comportamento.

Se **o \_ sinalizador de arquivo \_ abrir \_ \_ ponto de nova análise** for especificado e:

-   Se um arquivo existente for aberto e for um link simbólico, o identificador retornado será um identificador para o link simbólico.
-   Se a especificação **criar \_ sempre**, **truncar o sinalizador \_ existente** ou **arquivo \_ \_ excluir \_ no \_ fechamento** for especificada, o arquivo afetado será um link simbólico.

Se **o \_ sinalizador de arquivo \_ abrir \_ \_ ponto de nova análise** não for especificado e:

-   Se um arquivo existente for aberto e for um link simbólico, o identificador retornado será um identificador para o destino.
-   Se a especificação **criar \_ sempre**, **truncar o sinalizador \_ existente** ou **arquivo \_ \_ excluir \_ no \_ fechamento** for especificada, o arquivo afetado será o destino.

## <a name="createhardlink-and-createhardlinktransacted"></a>CreateHardLink e CreateHardLinkTransacted

Se o caminho apontar para um link simbólico, a função criará um link físico para o destino.

## <a name="deletefile-and-deletefiletransacted"></a>Excluirfile e DeleteFileTransacted

Se o caminho apontar para um link simbólico, o link simbólico será excluído, não o destino. Para excluir um destino, você deve chamar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e especificar **a \_ \_ exclusão \_ do sinalizador de arquivo ao \_ fechar**.

## <a name="findfirstchangenotification"></a>FindFirstChangeNotification

Se o caminho apontar para um link simbólico, o identificador de notificação será criado para o destino. Se um aplicativo tiver se registrado para receber notificações de alteração para um diretório que contém links simbólicos, o aplicativo só será notificado quando os links simbólicos forem alterados, não os arquivos de destino.

## <a name="findfirstfile-and-findfirstfiletransacted"></a>FindFirstFile e FindFirstFileTransacted

Se o caminho aponta para um link simbólico, o buffer de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contém informações sobre o link simbólico, não para o destino.

## <a name="findfirstfileex"></a>FindFirstFileEx

Se o caminho aponta para um link simbólico, o buffer de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contém informações sobre o link simbólico, não para o destino.

## <a name="findnextfile"></a>FindNextFile

Se o caminho aponta para um link simbólico, o buffer de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contém informações sobre o link simbólico, não para o destino.

## <a name="getbinarytype"></a>Getbinarytype

Se o caminho apontar para um link simbólico, o arquivo de destino será usado.

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a>GetCompressedFileSize e GetCompressedFileSizeTransacted

Se o caminho apontar para um link simbólico, a função retornará o tamanho do arquivo do destino.

## <a name="getdiskfreespace"></a>GetDiskFreeSpace

Se o caminho apontar para um link simbólico, a operação será executada no destino.

## <a name="getdiskfreespaceex"></a>GetDiskFreeSpaceEx

Se o caminho apontar para um link simbólico, a operação será executada no destino.

## <a name="getfileattributes"></a>GetFileAttributes

Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.

## <a name="getfileattributesex"></a>GetFileAttributesEx

Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.

## <a name="getfilesecurity"></a>GetFileSecurity

Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.

## <a name="gettemppath"></a>GetTempPath

Se o caminho apontar para um link simbólico, o nome do caminho temporário manterá todos os links simbólicos.

## <a name="getvolumeinformation"></a>GetVolumeInformation

Se o caminho apontar para um link simbólico, a função retornará informações de volume para o destino.

## <a name="setfileattributes"></a>SetFileAttributes

Se o caminho apontar para um link simbólico, a função recuperará atributos para o link simbólico.

## <a name="setfilesecurity"></a>SetFileSecurity

Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[**CopyFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[**CreateHardLinkTransacted**](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[**DeleteFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[**FindFirstChangeNotification**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[**FindFirstFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[**FindFirstFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[**FindNextFile**](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[**Getbinarytype**](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[**GetCompressedFileSize**](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[**GetCompressedFileSizeTransacted**](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[**GetDiskFreeSpace**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[**GetTempPath**](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileSecurity**](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
