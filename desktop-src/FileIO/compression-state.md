---
description: Cada arquivo e diretório em um volume que dá suporte à compactação para arquivos e diretórios individuais tem um estado de compactação.
ms.assetid: 9db1b2e2-864e-45b5-8227-400cad75222e
title: Estado de compactação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e182921a6c5e1b79c08fbafb6a8104c4bd8ca1cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169739"
---
# <a name="compression-state"></a><span data-ttu-id="81f7e-103">Estado de compactação</span><span class="sxs-lookup"><span data-stu-id="81f7e-103">Compression State</span></span>

<span data-ttu-id="81f7e-104">Cada arquivo e diretório em um volume que dá suporte à compactação para arquivos e diretórios individuais tem um *estado de compactação*.</span><span class="sxs-lookup"><span data-stu-id="81f7e-104">Each file and directory on a volume that supports compression for individual files and directories has a *compression state*.</span></span>

<span data-ttu-id="81f7e-105">Enquanto o atributo de compactação de um arquivo ou diretório indica simplesmente se o arquivo ou diretório está compactado ou não compactado, o estado de compactação também especifica o formato de todos os dados compactados.</span><span class="sxs-lookup"><span data-stu-id="81f7e-105">Whereas the compression attribute of a file or directory indicates simply whether the file or directory is compressed or not compressed, the compression state also specifies the format of any compressed data.</span></span>

<span data-ttu-id="81f7e-106">Use o código de controle [**\_ obter \_ compactação fsctl**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) para determinar o estado de compactação de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="81f7e-106">Use the [**FSCTL\_GET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) control code to determine the compression state of a file or directory.</span></span>

<span data-ttu-id="81f7e-107">O estado de compactação é codificado como um valor de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="81f7e-107">Compression state is encoded as a 16-bit value.</span></span> <span data-ttu-id="81f7e-108">Um valor de estado de compactação de formato de COMPACTação \_ \_ None indica que um arquivo não está compactado.</span><span class="sxs-lookup"><span data-stu-id="81f7e-108">A compression state value of COMPRESSION\_FORMAT\_NONE indicates that a file is not compressed.</span></span> <span data-ttu-id="81f7e-109">Um valor padrão de formato de COMPACTação \_ \_ indica que um arquivo está compactado, usando o formato de compactação padrão.</span><span class="sxs-lookup"><span data-stu-id="81f7e-109">A value of COMPRESSION\_FORMAT\_DEFAULT indicates that a file is compressed, using the default compression format.</span></span> <span data-ttu-id="81f7e-110">Qualquer outro valor indica que um arquivo está compactado, usando o formato de compactação especificado pelo valor de estado de compactação.</span><span class="sxs-lookup"><span data-stu-id="81f7e-110">Any other value indicates that a file is compressed, using the compression format specified by the compression state value.</span></span>

<span data-ttu-id="81f7e-111">Use o código de controle [**fsctl \_ set \_ Compression**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) para definir o estado de compactação de um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="81f7e-111">Use the [**FSCTL\_SET\_COMPRESSION**](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) control code to set the compression state of a file or directory.</span></span> <span data-ttu-id="81f7e-112">Essa operação também define o atributo de compactação do arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="81f7e-112">This operation also sets the compression attribute of the file or directory.</span></span>

<span data-ttu-id="81f7e-113">Definir o estado de compactação de um arquivo para um valor diferente de zero compacta o arquivo, usando o formato de compactação codificado pelo valor do estado de compactação.</span><span class="sxs-lookup"><span data-stu-id="81f7e-113">Setting the compression state of a file to a nonzero value compresses the file, using the compression format encoded by the compression state value.</span></span> <span data-ttu-id="81f7e-114">Definir o estado de compactação de um arquivo como zero descompacta o arquivo.</span><span class="sxs-lookup"><span data-stu-id="81f7e-114">Setting a file's compression state to zero decompresses the file.</span></span> <span data-ttu-id="81f7e-115">Essas são operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="81f7e-115">These are synchronous operations.</span></span> <span data-ttu-id="81f7e-116">O arquivo é compactado ou descompactado imediatamente quando você define seu estado de compactação.</span><span class="sxs-lookup"><span data-stu-id="81f7e-116">The file is compressed or decompressed immediately when you set its compression state.</span></span>

<span data-ttu-id="81f7e-117">Definir o estado de compactação de um diretório não causa nenhuma compactação ou descompactação imediata.</span><span class="sxs-lookup"><span data-stu-id="81f7e-117">Setting a directory's compression state does not cause any immediate compression or decompression.</span></span> <span data-ttu-id="81f7e-118">Em vez disso, definir o estado de compactação de um diretório define um estado de compactação padrão que será fornecido a todos os arquivos e subdiretórios recém-criados.</span><span class="sxs-lookup"><span data-stu-id="81f7e-118">Instead, setting a directory's compression state sets a default compression state that will be given to all newly created files and subdirectories.</span></span>

 

 
