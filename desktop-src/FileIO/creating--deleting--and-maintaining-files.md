---
description: Funções a serem usadas para criar, excluir e manter arquivos.
ms.assetid: b9cf0ddf-efda-4997-bcc3-3056026c1264
title: Criando, excluindo e mantendo arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 921388e84ac44a42e0c24880b1b56971ba84c12b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787537"
---
# <a name="creating-deleting-and-maintaining-files"></a><span data-ttu-id="64ed7-103">Criando, excluindo e mantendo arquivos</span><span class="sxs-lookup"><span data-stu-id="64ed7-103">Creating, Deleting, and Maintaining Files</span></span>

<span data-ttu-id="64ed7-104">Os tópicos a seguir descrevem como criar, excluir e manter arquivos.</span><span class="sxs-lookup"><span data-stu-id="64ed7-104">The following topics describe how to create, delete, and maintain files.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="64ed7-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="64ed7-105">In this section</span></span>



| <span data-ttu-id="64ed7-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="64ed7-106">Topic</span></span>                                                                   | <span data-ttu-id="64ed7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="64ed7-107">Description</span></span>                                                                                                                                                                                                                                                                 |
|-------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="64ed7-108">Nomeando arquivos, caminhos e namespaces</span><span class="sxs-lookup"><span data-stu-id="64ed7-108">Naming Files, Paths, and Namespaces</span></span>](naming-a-file.md)<br/>     | <span data-ttu-id="64ed7-109">Regras, convenções e limitações de nomes para arquivos e diretórios, incluindo convenções de nomenclatura, nomes de arquivo curtos versus nomes de arquivo longos, caminhos totalmente qualificados versus caminhos relativos, limitação de comprimento de caminho máximo, nomes de arquivo 8,3 e namespaces.</span><span class="sxs-lookup"><span data-stu-id="64ed7-109">Rules, conventions, and limitations of names for files and directories, including naming conventions, short file names vs. long file names, fully qualified paths vs. relative paths, maximum path length limitation, 8.3 file names, and namespaces.</span></span><br/>            |
| [<span data-ttu-id="64ed7-110">Criando e abrindo arquivos</span><span class="sxs-lookup"><span data-stu-id="64ed7-110">Creating and Opening Files</span></span>](creating-and-opening-files.md)<br/> | <span data-ttu-id="64ed7-111">Considerações para criar ou abrir um arquivo usando a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="64ed7-111">Considerations for creating or opening a file by using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="64ed7-112">Movendo e substituindo arquivos</span><span class="sxs-lookup"><span data-stu-id="64ed7-112">Moving and Replacing Files</span></span>](moving-and-replacing-files.md)<br/> | <span data-ttu-id="64ed7-113">Considerações para mover e substituir arquivos usando as funções CopyFileEx, CreateFile, ReplaceFile e MoveFileEx.</span><span class="sxs-lookup"><span data-stu-id="64ed7-113">Considerations for moving and replacing files by using the CopyFileEx, CreateFile, Replacefile, and MoveFileEx functions.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="64ed7-114">Fechando e excluindo arquivos</span><span class="sxs-lookup"><span data-stu-id="64ed7-114">Closing and Deleting Files</span></span>](closing-and-deleting-files.md)<br/> | <span data-ttu-id="64ed7-115">Para usar os recursos do sistema operacional com eficiência, um aplicativo deve fechar os arquivos quando eles não forem mais necessários usando a função [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) .</span><span class="sxs-lookup"><span data-stu-id="64ed7-115">To use operating system resources efficiently, an application should close files when they are no longer needed by using the [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) function.</span></span> <span data-ttu-id="64ed7-116">Se um arquivo estiver aberto quando um aplicativo for encerrado, o sistema o fechará automaticamente.</span><span class="sxs-lookup"><span data-stu-id="64ed7-116">If a file is open when an application terminates, the system closes it automatically.</span></span><br/> |
| [<span data-ttu-id="64ed7-117">Desfragmentando arquivos</span><span class="sxs-lookup"><span data-stu-id="64ed7-117">Defragmenting Files</span></span>](defragmenting-files.md)<br/>               | <span data-ttu-id="64ed7-118">A *desfragmentação* é o processo de mover partes de arquivos em um disco para desfragmentar arquivos, ou seja, o processo de mover clusters de arquivos em um disco para torná-los contíguos.</span><span class="sxs-lookup"><span data-stu-id="64ed7-118">*Defragmentation* is the process of moving portions of files around on a disk to defragment files, that is, the process of moving file clusters on a disk to make them contiguous.</span></span><br/>                                                                               |



 

 

