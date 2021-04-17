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
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="ed578-103">Efeitos de link simbólico em funções de sistemas de arquivos</span><span class="sxs-lookup"><span data-stu-id="ed578-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="ed578-104">Várias funções de arquivo padrão que usam nomes de caminho para especificar um ou mais arquivos são afetadas pelo uso de links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="ed578-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="ed578-105">Este tópico lista essas funções e descreve as alterações no comportamento:</span><span class="sxs-lookup"><span data-stu-id="ed578-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="ed578-106">CopyFile e CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="ed578-107">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="ed578-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="ed578-108">CreateFile e CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="ed578-109">CreateHardLink e CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="ed578-110">Excluirfile e DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="ed578-111">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="ed578-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="ed578-112">FindFirstFile e FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="ed578-113">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="ed578-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="ed578-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="ed578-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="ed578-115">Getbinarytype</span><span class="sxs-lookup"><span data-stu-id="ed578-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="ed578-116">GetCompressedFileSize e GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="ed578-117">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="ed578-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="ed578-118">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="ed578-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="ed578-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="ed578-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="ed578-120">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="ed578-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="ed578-121">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="ed578-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="ed578-122">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="ed578-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="ed578-123">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="ed578-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="ed578-124">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="ed578-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="ed578-125">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="ed578-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="ed578-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed578-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="ed578-127">Nas descrições a seguir, os seguintes termos são usados:</span><span class="sxs-lookup"><span data-stu-id="ed578-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="ed578-128">Arquivo de origem — o arquivo original a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="ed578-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="ed578-129">Arquivo de destino — a cópia recém-criada do arquivo.</span><span class="sxs-lookup"><span data-stu-id="ed578-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="ed578-130">Target — a entidade à qual um link simbólico aponta.</span><span class="sxs-lookup"><span data-stu-id="ed578-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="ed578-131">O comportamento das funções que aceitam um identificador criado usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , como a função [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , será diferente se a função **CreateFile** for ou não chamada com o sinalizador **File \_ Flag \_ Open \_ reparse \_ Point** .</span><span class="sxs-lookup"><span data-stu-id="ed578-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="ed578-132">Para obter mais informações, consulte [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e a seguinte seção [CreateFile e CreateFileTransacted](#createfile-and-createfiletransacted) .</span><span class="sxs-lookup"><span data-stu-id="ed578-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="ed578-133">CopyFile e CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="ed578-134">Se o arquivo de origem for um link simbólico, o arquivo real copiado será o destino do link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="ed578-135">Se o arquivo de destino já existir e for um link simbólico, o link simbólico será substituído pelo arquivo de origem.</span><span class="sxs-lookup"><span data-stu-id="ed578-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="ed578-136">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="ed578-136">CopyFileEx</span></span>

<span data-ttu-id="ed578-137">Se **Copy \_ File \_ Copy \_ SYMLINK** for especificado e:</span><span class="sxs-lookup"><span data-stu-id="ed578-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="ed578-138">Se o arquivo de origem for um link simbólico, o link simbólico será copiado, não o arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="ed578-139">Se o arquivo de origem não for um link simbólico, não haverá alteração no comportamento.</span><span class="sxs-lookup"><span data-stu-id="ed578-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="ed578-140">Se o arquivo de destino for um link simbólico existente, o link simbólico será substituído, não o arquivo de destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="ed578-141">Se **o \_ arquivo de cópia falhar, \_ \_ se \_ existir** também for especificado e o arquivo de destino for um link simbólico existente, a operação falhará em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="ed578-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="ed578-142">Se **Copy \_ File \_ Copy \_ SYMLINK** não for especificado e:</span><span class="sxs-lookup"><span data-stu-id="ed578-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="ed578-143">Se **o \_ arquivo de cópia falhar, \_ \_ se \_ existir** também for especificado e o arquivo de destino for um link simbólico existente, a operação falhará somente se o destino do link simbólico existir.</span><span class="sxs-lookup"><span data-stu-id="ed578-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="ed578-144">Se **o \_ arquivo de cópia \_ falhar \_ se \_ Exists** não for especificado, não haverá alteração no comportamento.</span><span class="sxs-lookup"><span data-stu-id="ed578-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="ed578-145">**Windows Server 2003 e Windows XP:** Não há suporte para o sinalizador **SYMLINK de cópia de arquivo de cópia \_ \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="ed578-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="ed578-146">Se o arquivo de origem for um link simbólico, o arquivo real copiado será o destino do link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="ed578-147">CreateFile e CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="ed578-148">Se a chamada para essa função criar um novo arquivo, não haverá alteração no comportamento.</span><span class="sxs-lookup"><span data-stu-id="ed578-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="ed578-149">Se **o \_ sinalizador de arquivo \_ abrir \_ \_ ponto de nova análise** for especificado e:</span><span class="sxs-lookup"><span data-stu-id="ed578-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="ed578-150">Se um arquivo existente for aberto e for um link simbólico, o identificador retornado será um identificador para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="ed578-151">Se a especificação **criar \_ sempre**, **truncar o sinalizador \_ existente** ou **arquivo \_ \_ excluir \_ no \_ fechamento** for especificada, o arquivo afetado será um link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="ed578-152">Se **o \_ sinalizador de arquivo \_ abrir \_ \_ ponto de nova análise** não for especificado e:</span><span class="sxs-lookup"><span data-stu-id="ed578-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="ed578-153">Se um arquivo existente for aberto e for um link simbólico, o identificador retornado será um identificador para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="ed578-154">Se a especificação **criar \_ sempre**, **truncar o sinalizador \_ existente** ou **arquivo \_ \_ excluir \_ no \_ fechamento** for especificada, o arquivo afetado será o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="ed578-155">CreateHardLink e CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="ed578-156">Se o caminho apontar para um link simbólico, a função criará um link físico para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="ed578-157">Excluirfile e DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="ed578-158">Se o caminho apontar para um link simbólico, o link simbólico será excluído, não o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="ed578-159">Para excluir um destino, você deve chamar [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) e especificar **a \_ \_ exclusão \_ do sinalizador de arquivo ao \_ fechar**.</span><span class="sxs-lookup"><span data-stu-id="ed578-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="ed578-160">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="ed578-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="ed578-161">Se o caminho apontar para um link simbólico, o identificador de notificação será criado para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="ed578-162">Se um aplicativo tiver se registrado para receber notificações de alteração para um diretório que contém links simbólicos, o aplicativo só será notificado quando os links simbólicos forem alterados, não os arquivos de destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="ed578-163">FindFirstFile e FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="ed578-164">Se o caminho aponta para um link simbólico, o buffer de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contém informações sobre o link simbólico, não para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="ed578-165">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="ed578-165">FindFirstFileEx</span></span>

<span data-ttu-id="ed578-166">Se o caminho aponta para um link simbólico, o buffer de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contém informações sobre o link simbólico, não para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="ed578-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="ed578-167">FindNextFile</span></span>

<span data-ttu-id="ed578-168">Se o caminho aponta para um link simbólico, o buffer de [**\_ \_ dados de localização do Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contém informações sobre o link simbólico, não para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="ed578-169">Getbinarytype</span><span class="sxs-lookup"><span data-stu-id="ed578-169">GetBinaryType</span></span>

<span data-ttu-id="ed578-170">Se o caminho apontar para um link simbólico, o arquivo de destino será usado.</span><span class="sxs-lookup"><span data-stu-id="ed578-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="ed578-171">GetCompressedFileSize e GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="ed578-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="ed578-172">Se o caminho apontar para um link simbólico, a função retornará o tamanho do arquivo do destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="ed578-173">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="ed578-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="ed578-174">Se o caminho apontar para um link simbólico, a operação será executada no destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="ed578-175">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="ed578-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="ed578-176">Se o caminho apontar para um link simbólico, a operação será executada no destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="ed578-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="ed578-177">GetFileAttributes</span></span>

<span data-ttu-id="ed578-178">Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="ed578-179">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="ed578-179">GetFileAttributesEx</span></span>

<span data-ttu-id="ed578-180">Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="ed578-181">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="ed578-181">GetFileSecurity</span></span>

<span data-ttu-id="ed578-182">Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="ed578-183">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="ed578-183">GetTempPath</span></span>

<span data-ttu-id="ed578-184">Se o caminho apontar para um link simbólico, o nome do caminho temporário manterá todos os links simbólicos.</span><span class="sxs-lookup"><span data-stu-id="ed578-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="ed578-185">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="ed578-185">GetVolumeInformation</span></span>

<span data-ttu-id="ed578-186">Se o caminho apontar para um link simbólico, a função retornará informações de volume para o destino.</span><span class="sxs-lookup"><span data-stu-id="ed578-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="ed578-187">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="ed578-187">SetFileAttributes</span></span>

<span data-ttu-id="ed578-188">Se o caminho apontar para um link simbólico, a função recuperará atributos para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="ed578-189">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="ed578-189">SetFileSecurity</span></span>

<span data-ttu-id="ed578-190">Se o caminho apontar para um link simbólico, a função retornará atributos para o link simbólico.</span><span class="sxs-lookup"><span data-stu-id="ed578-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed578-191">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ed578-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed578-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="ed578-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="ed578-193">**CopyFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed578-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="ed578-194">**CopyFileEx**</span><span class="sxs-lookup"><span data-stu-id="ed578-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="ed578-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="ed578-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="ed578-196">**CreateFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed578-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="ed578-197">**CreateHardLink**</span><span class="sxs-lookup"><span data-stu-id="ed578-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="ed578-198">**CreateHardLinkTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed578-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="ed578-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="ed578-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="ed578-200">**DeleteFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed578-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="ed578-201">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="ed578-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="ed578-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="ed578-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="ed578-203">**FindFirstFileEx**</span><span class="sxs-lookup"><span data-stu-id="ed578-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="ed578-204">**FindFirstFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed578-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="ed578-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="ed578-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="ed578-206">**Getbinarytype**</span><span class="sxs-lookup"><span data-stu-id="ed578-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="ed578-207">**GetCompressedFileSize**</span><span class="sxs-lookup"><span data-stu-id="ed578-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="ed578-208">**GetCompressedFileSizeTransacted**</span><span class="sxs-lookup"><span data-stu-id="ed578-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="ed578-209">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="ed578-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="ed578-210">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="ed578-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="ed578-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="ed578-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="ed578-212">**GetFileAttributesEx**</span><span class="sxs-lookup"><span data-stu-id="ed578-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="ed578-213">**GetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="ed578-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="ed578-214">**GetTempPath**</span><span class="sxs-lookup"><span data-stu-id="ed578-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="ed578-215">**GetVolumeInformation**</span><span class="sxs-lookup"><span data-stu-id="ed578-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="ed578-216">**SetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="ed578-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="ed578-217">**SetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="ed578-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
