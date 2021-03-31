---
title: Os arquivos de armazenamento e Common-Store comuns do SIS
description: Todos os arquivos de backup mantidos pelo backup do SIS (Single-Instance Store) são chamados de arquivos de armazenamento comuns.
ms.assetid: c6231c30-9d5a-428d-a94d-9dc8db933432
keywords:
- Backup de repositórios comuns
- Backup do SIS (Single-Instance Store), armazenamentos comuns
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b2f86b778b0a8db916fe580b8f833214523eb2e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823889"
---
# <a name="the-sis-common-store-and-common-store-files"></a><span data-ttu-id="5a894-105">Os arquivos de armazenamento e Common-Store comuns do SIS</span><span class="sxs-lookup"><span data-stu-id="5a894-105">The SIS Common Store and Common-Store Files</span></span>

<span data-ttu-id="5a894-106">Todos os arquivos de backup mantidos pelo backup do SIS (Single-Instance Store) são chamados *de arquivos de armazenamento comuns*.</span><span class="sxs-lookup"><span data-stu-id="5a894-106">All backing files maintained by single-instance store (SIS) backup are called *common-store files*.</span></span> <span data-ttu-id="5a894-107">Existe um *repositório comum* em cada volume mantido no SIS e contém todos os arquivos de armazenamento comum existentes nesse volume.</span><span class="sxs-lookup"><span data-stu-id="5a894-107">One *common store* exists on each SIS-maintained volume and contains all of the common-store files that exist on that volume.</span></span> <span data-ttu-id="5a894-108">Esse diretório está localizado no diretório raiz do volume e é denominado " \\ SIS Common Store".</span><span class="sxs-lookup"><span data-stu-id="5a894-108">This directory is located in the root directory of the volume and is named "\\SIS Common Store".</span></span> <span data-ttu-id="5a894-109">O repositório comum é implementado como um diretório protegido contra acesso de usuário normal, pois os arquivos de armazenamento comum devem ser acessados diretamente apenas por funções de API de backup do SIS e aplicativos de backup e restauração.</span><span class="sxs-lookup"><span data-stu-id="5a894-109">The common store is implemented as a directory that is protected against normal user access, because common-store files are intended to be accessed directly only by SIS backup API functions and not backup and restore applications.</span></span>

<span data-ttu-id="5a894-110">As propriedades de um arquivo de repositório comum são as seguintes:</span><span class="sxs-lookup"><span data-stu-id="5a894-110">The properties of a common-store file are the following:</span></span>

-   <span data-ttu-id="5a894-111">Um arquivo de armazenamento comum pode ter um ou mais links apontando para ele.</span><span class="sxs-lookup"><span data-stu-id="5a894-111">A common-store file may have one or more links pointing to it.</span></span>
-   <span data-ttu-id="5a894-112">Depois de criado, o conteúdo de um arquivo de armazenamento comum nunca é alterado.</span><span class="sxs-lookup"><span data-stu-id="5a894-112">After it is created, the contents of a common-store file never change.</span></span>
-   <span data-ttu-id="5a894-113">Os nomes de arquivos de armazenamento comuns são globalmente exclusivos, ou seja, são exclusivos em todos os volumes em todos os sistemas do mundo, e a associação entre um nome de arquivo de repositório comum e seus dados é globalmente estática.</span><span class="sxs-lookup"><span data-stu-id="5a894-113">The names of common-store files are globally unique—that is, they are unique across all volumes across all systems in the world, and the binding between a common-store file name and its data is globally static.</span></span>

<span data-ttu-id="5a894-114">Quando o SIS é habilitado em um volume, uma cópia dos arquivos duplicados é criada para o armazenamento comum, e todos os arquivos duplicados são substituídos por [links do SIS](sis-links-and-reparse-points.md) apontando para o arquivo de repositório comum.</span><span class="sxs-lookup"><span data-stu-id="5a894-114">When SIS is enabled on a volume, one copy of the duplicate files is then created to the common store, and all of the duplicate files are replaced with [SIS links](sis-links-and-reparse-points.md) pointing to the common-store file.</span></span> <span data-ttu-id="5a894-115">Para obter mais informações, consulte [habilitando ou desabilitando o SIS em um volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) na documentação do TechNet.</span><span class="sxs-lookup"><span data-stu-id="5a894-115">For more information, see [Enabling or Disabling SIS on a Volume](/previous-versions/windows/it-pro/windows-server-storage-solutions/dd573313(v=ws.10)) in the TechNet documentation.</span></span>

<span data-ttu-id="5a894-116">Quando um dos links do SIS é acessado para uma operação de gravação, o filtro SIS primeiro restaura o conteúdo original do arquivo de link do SIS do arquivo de armazenamento comum, o ponto de nova análise vinculando o arquivo de link do SIS ao repositório comum é removido e, em seguida, a operação de gravação é executada no arquivo de destino original.</span><span class="sxs-lookup"><span data-stu-id="5a894-116">When one of the SIS links is accessed for a write operation, the SIS filter first restores the original contents of the SIS link file from the common-store file, the reparse point linking the SIS link file to the common store is removed, and then the write operation is performed on the original destination file.</span></span>

<span data-ttu-id="5a894-117">O arquivo de repositório comum é removido somente quando o último link SIS apontando para ele é excluído.</span><span class="sxs-lookup"><span data-stu-id="5a894-117">The common-store file is removed only when the last SIS link pointing to it is deleted.</span></span>

 

 