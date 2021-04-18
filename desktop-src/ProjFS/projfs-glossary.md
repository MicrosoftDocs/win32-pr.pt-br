---
title: Glossário do sistema de arquivos projetado do Windows
description: Termos especiais usados em ProjFS.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: c6eac8faa83e2c898e4b1a3ada5c24ef81151b22
ms.sourcegitcommit: a48b68a75323edfb902eb04fbe6d0ecba6988c21
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/21/2020
ms.locfileid: "105773924"
---
# <a name="windows-projected-file-system-glossary"></a><span data-ttu-id="bf659-103">Glossário do sistema de arquivos projetado do Windows</span><span class="sxs-lookup"><span data-stu-id="bf659-103">Windows Projected File System glossary</span></span>

<span data-ttu-id="bf659-104">Termos especiais usados em ProjFS.</span><span class="sxs-lookup"><span data-stu-id="bf659-104">Special terms used in ProjFS.</span></span>

<dl>
<dt>

<span data-ttu-id="bf659-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**repositório de backup**</span><span class="sxs-lookup"><span data-stu-id="bf659-105"><span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**backing store**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-106">Dados hierárquicos mantidos pelo provedor que são projetados no sistema de arquivos como arquivos e diretórios.</span><span class="sxs-lookup"><span data-stu-id="bf659-106">Provider-maintained hierarchical data that is projected into the file system as files and directories.</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**espaço reservado sujo**</span><span class="sxs-lookup"><span data-stu-id="bf659-107"><span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**dirty placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-108">Um arquivo ou diretório que foi modificado localmente e não é mais um cache de seu estado no repositório do provedor.</span><span class="sxs-lookup"><span data-stu-id="bf659-108">A file or directory that has been locally modified and is no longer a cache of its state in the provider's store.</span></span>  <span data-ttu-id="bf659-109">Consulte [estado do cache na raiz de virtualização](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-109">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**arquivo/diretório completo**</span><span class="sxs-lookup"><span data-stu-id="bf659-110"><span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**full file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-111">Um arquivo ou diretório que foi criado no sistema de arquivos local ou um arquivo que foi modificado, fazendo com que ele não seja mais um cache de seu estado no repositório de backup.</span><span class="sxs-lookup"><span data-stu-id="bf659-111">A file or directory that was created in the local file system, or a file that has been modified, making it no longer a cache of its state in the backing store.</span></span>  <span data-ttu-id="bf659-112">Consulte [estado do cache na raiz de virtualização](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-112">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**espaço reservado para alimentador**</span><span class="sxs-lookup"><span data-stu-id="bf659-113"><span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**hydrated placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-114">Um arquivo cujo conteúdo e metadados foram armazenados em cache no disco.</span><span class="sxs-lookup"><span data-stu-id="bf659-114">A file whose content and metadata have been cached to disk.</span></span>  <span data-ttu-id="bf659-115">Consulte [estado do cache na raiz de virtualização](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-115">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**reservado**</span><span class="sxs-lookup"><span data-stu-id="bf659-116"><span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**placeholder**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-117">Um arquivo ou diretório que não está totalmente presente no disco.</span><span class="sxs-lookup"><span data-stu-id="bf659-117">A file or directory that is not fully present on disk.</span></span>  <span data-ttu-id="bf659-118">Consulte [estado do cache na raiz de virtualização](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-118">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**marca para exclusão**</span><span class="sxs-lookup"><span data-stu-id="bf659-119"><span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**tombstone**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-120">Um espaço reservado especial oculto que representa um item que foi excluído do sistema de arquivos local.</span><span class="sxs-lookup"><span data-stu-id="bf659-120">A special hidden placeholder that represents an item that has been deleted from the local file system.</span></span>  <span data-ttu-id="bf659-121">Consulte [estado do cache na raiz de virtualização](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-121">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**arquivo/diretório virtual**</span><span class="sxs-lookup"><span data-stu-id="bf659-122"><span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**virtual file/directory**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-123">Um arquivo ou diretório que não existe fisicamente no disco, mas é projetado em resultados de enumeração.</span><span class="sxs-lookup"><span data-stu-id="bf659-123">A file or directory that does not physically exist on disk, but is projected into enumeration results.</span></span>  <span data-ttu-id="bf659-124">Consulte [estado do cache na raiz de virtualização](cache-state.md).</span><span class="sxs-lookup"><span data-stu-id="bf659-124">See [Cache State in the Virtualization Root](cache-state.md).</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**instância de virtualização**</span><span class="sxs-lookup"><span data-stu-id="bf659-125"><span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**virtualization instance**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-126">Um objeto na memória que gerencia a comunicação entre o provedor e o ProjFS para o conjunto de arquivos e diretórios localizados em uma raiz de virtualização específica.</span><span class="sxs-lookup"><span data-stu-id="bf659-126">An in-memory object that manages communication between the provider and ProjFS for the set of files and directories located under a particular virtualization root.</span></span>
</dd>

<dt>

<span data-ttu-id="bf659-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**raiz de virtualização**</span><span class="sxs-lookup"><span data-stu-id="bf659-127"><span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**virtualization root**</span></span>
</dt>
<dd>

<span data-ttu-id="bf659-128">Um diretório no sistema de arquivos sob o qual os dados do provedor são projetados.</span><span class="sxs-lookup"><span data-stu-id="bf659-128">A directory in the file system under which the provider's data is projected.</span></span>
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->