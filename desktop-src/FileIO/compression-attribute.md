---
description: Em um volume do sistema de arquivos NTFS, cada arquivo e diretório têm um atributo de compactação.
ms.assetid: 8aca120c-22a7-4dc8-a921-dfcec1277452
title: Atributo de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2e8e86eebe919476851f35f77cf10d6a07035d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837426"
---
# <a name="compression-attribute"></a><span data-ttu-id="32b76-103">Atributo de compactação</span><span class="sxs-lookup"><span data-stu-id="32b76-103">Compression Attribute</span></span>

<span data-ttu-id="32b76-104">Em um volume do sistema de arquivos NTFS, cada arquivo e diretório têm um *atributo de compactação*.</span><span class="sxs-lookup"><span data-stu-id="32b76-104">On an NTFS file system volume, each file and directory has a *compression attribute*.</span></span> <span data-ttu-id="32b76-105">Outros sistemas de arquivos também podem implementar um atributo de compactação para arquivos e diretórios individuais.</span><span class="sxs-lookup"><span data-stu-id="32b76-105">Other file systems may also implement a compression attribute for individual files and directories.</span></span>

<span data-ttu-id="32b76-106">Você pode determinar se um sistema de arquivos dá suporte a um atributo de compactação para arquivos e diretórios chamando a função [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) e examinando o sinalizador de bit de **\_ \_ compactação do arquivo de arquivo** .</span><span class="sxs-lookup"><span data-stu-id="32b76-106">You can determine whether a file system supports a compression attribute for files and directories by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_FILE\_COMPRESSION** bit flag.</span></span>

<span data-ttu-id="32b76-107">Use a função [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) ou [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) para determinar o atributo de compactação de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="32b76-107">Use the [**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa) or [**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa) function to determine the compression attribute of a file or directory.</span></span>

<span data-ttu-id="32b76-108">Se o atributo de compactação de um arquivo for definido (**atributo de arquivo \_ \_ compactado**), todos os dados no arquivo serão compactados.</span><span class="sxs-lookup"><span data-stu-id="32b76-108">If a file's compression attribute is set (**FILE\_ATTRIBUTE\_COMPRESSED**), all data in the file is compressed.</span></span> <span data-ttu-id="32b76-109">Se o atributo estiver claro, nenhum dos dados no arquivo será compactado.</span><span class="sxs-lookup"><span data-stu-id="32b76-109">If the attribute is clear, none of the data in the file is compressed.</span></span> <span data-ttu-id="32b76-110">Não há nenhum estado parcialmente compactado de uma perspectiva de programação no modo de usuário; o atributo de compactação é um indicador booliano simples do estado de compactação.</span><span class="sxs-lookup"><span data-stu-id="32b76-110">There is no partially compressed state from a user-mode programming perspective; the compression attribute is a simple Boolean indicator of compression state.</span></span>

<span data-ttu-id="32b76-111">O atributo de compactação de um diretório fornece um atributo de compactação padrão para arquivos e subdiretórios recém-criados.</span><span class="sxs-lookup"><span data-stu-id="32b76-111">A directory's compression attribute provides a default compression attribute for newly created files and subdirectories.</span></span> <span data-ttu-id="32b76-112">Quando você chama [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) ou [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) para criar um novo arquivo ou diretório, o novo arquivo ou diretório herda o atributo de compactação de seu diretório pai.</span><span class="sxs-lookup"><span data-stu-id="32b76-112">When you call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) or [**CreateDirectory**](/windows/desktop/api/FileAPI/nf-fileapi-createdirectorya) to create a new file or directory, the new file or directory inherits the compression attribute of its parent directory.</span></span>

<span data-ttu-id="32b76-113">Para modificar o **atributo \_ \_ compactado atributo de arquivo** para um arquivo ou diretório, você deve usar a função [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) com o código de controle de [**\_ \_ compactação Set fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) .</span><span class="sxs-lookup"><span data-stu-id="32b76-113">To modify the **FILE\_ATTRIBUTE\_COMPRESSED** attribute for a file or directory, you must use the [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) function with the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="32b76-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32b76-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32b76-115">**Constantes de atributo de arquivo**</span><span class="sxs-lookup"><span data-stu-id="32b76-115">**File Attribute Constants**</span></span>](file-attribute-constants.md)
</dt> </dl>

 

 
