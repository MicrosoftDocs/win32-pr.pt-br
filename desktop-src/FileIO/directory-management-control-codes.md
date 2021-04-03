---
description: Códigos de controle usados com compactação e descompactação de arquivo e com pontos de nova análise.
ms.assetid: e2e671c7-ef65-4401-8016-649e86f84fec
title: Códigos de controle de gerenciamento de diretório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ef0463860e3c899178ec5b8f9d44bd05cf4278e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829677"
---
# <a name="directory-management-control-codes"></a><span data-ttu-id="79e61-103">Códigos de controle de gerenciamento de diretório</span><span class="sxs-lookup"><span data-stu-id="79e61-103">Directory Management Control Codes</span></span>

<span data-ttu-id="79e61-104">Os códigos de controle a seguir são usados com [compactação e descompactação de arquivo](file-compression-and-decompression.md).</span><span class="sxs-lookup"><span data-stu-id="79e61-104">The following control codes are used with [file compression and decompression](file-compression-and-decompression.md).</span></span>



| <span data-ttu-id="79e61-105">Código de controle</span><span class="sxs-lookup"><span data-stu-id="79e61-105">Control Code</span></span>                                             | <span data-ttu-id="79e61-106">Significado</span><span class="sxs-lookup"><span data-stu-id="79e61-106">Meaning</span></span>                                                                                                                                     |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79e61-107">**FSCTL \_ obter \_ compactação**</span><span class="sxs-lookup"><span data-stu-id="79e61-107">**FSCTL\_GET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_compression) | <span data-ttu-id="79e61-108">Recupera o estado de compactação atual de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por fluxo.</span><span class="sxs-lookup"><span data-stu-id="79e61-108">Retrieves the current compression state of a file or directory on a volume whose file system supports per-stream compression.</span></span><br/>    |
| [<span data-ttu-id="79e61-109">**\_compactação do conjunto de fsctl \_**</span><span class="sxs-lookup"><span data-stu-id="79e61-109">**FSCTL\_SET\_COMPRESSION**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_compression) | <span data-ttu-id="79e61-110">Define o estado de compactação de um arquivo ou diretório em um volume cujo sistema de arquivos dá suporte à compactação por arquivo e por diretório.</span><span class="sxs-lookup"><span data-stu-id="79e61-110">Sets the compression state of a file or directory on a volume whose file system supports per-file and per-directory compression.</span></span><br/> |



 

<span data-ttu-id="79e61-111">Os códigos de controle a seguir são usados com [pontos de nova análise](reparse-points.md).</span><span class="sxs-lookup"><span data-stu-id="79e61-111">The following control codes are used with [reparse points](reparse-points.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="79e61-112">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="79e61-112">In this section</span></span>



| <span data-ttu-id="79e61-113">Código de controle</span><span class="sxs-lookup"><span data-stu-id="79e61-113">Control Code</span></span>                                                                   | <span data-ttu-id="79e61-114">Description</span><span class="sxs-lookup"><span data-stu-id="79e61-114">Description</span></span>                                                                                                           |
|--------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="79e61-115">**FSCTL \_ excluir \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="79e61-115">**FSCTL\_DELETE\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_delete_reparse_point)<br/> | <span data-ttu-id="79e61-116">Exclui um ponto de nova análise do arquivo ou diretório especificado.</span><span class="sxs-lookup"><span data-stu-id="79e61-116">Deletes a reparse point from the specified file or directory.</span></span><br/>                                              |
| [<span data-ttu-id="79e61-117">**FSCTL \_ obter \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="79e61-117">**FSCTL\_GET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_get_reparse_point)<br/>       | <span data-ttu-id="79e61-118">Recupera os dados do ponto de nova análise associados ao arquivo ou diretório identificado pelo identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="79e61-118">Retrieves the reparse point data associated with the file or directory identified by the specified handle.</span></span><br/> |
| [<span data-ttu-id="79e61-119">**FSCTL \_ definir \_ ponto de nova análise \_**</span><span class="sxs-lookup"><span data-stu-id="79e61-119">**FSCTL\_SET\_REPARSE\_POINT**</span></span>](/windows/win32/api/winioctl/ni-winioctl-fsctl_set_reparse_point)<br/>       | <span data-ttu-id="79e61-120">Define um ponto de nova análise em um arquivo ou diretório.</span><span class="sxs-lookup"><span data-stu-id="79e61-120">Sets a reparse point on a file or directory.</span></span><br/>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="79e61-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="79e61-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79e61-122">Códigos de controle de gerenciamento de arquivos</span><span class="sxs-lookup"><span data-stu-id="79e61-122">File Management Control Codes</span></span>](file-management-control-codes.md)
</dt> <dt>

[<span data-ttu-id="79e61-123">Códigos de controle de gerenciamento de volume</span><span class="sxs-lookup"><span data-stu-id="79e61-123">Volume Management Control Codes</span></span>](volume-management-control-codes.md)
</dt> </dl>

 

