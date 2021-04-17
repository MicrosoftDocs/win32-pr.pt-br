---
title: Implementação de arquivo de IStorage-Compound
description: A implementação do arquivo composto do IStorage permite criar e gerenciar subarmazenamentos e fluxos em um objeto de armazenamento que reside em um objeto de arquivo composto.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd STG, implementação de arquivo composto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105753704"
---
# <a name="istorage-compound-file-implementation"></a><span data-ttu-id="911bf-104">Implementação de arquivo de IStorage-Compound</span><span class="sxs-lookup"><span data-stu-id="911bf-104">IStorage-Compound File Implementation</span></span>

<span data-ttu-id="911bf-105">A implementação do arquivo composto do [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) permite criar e gerenciar subarmazenamentos e fluxos em um objeto de armazenamento que reside em um objeto de arquivo composto.</span><span class="sxs-lookup"><span data-stu-id="911bf-105">The compound file implementation of [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) allows you to create and manage substorages and streams within a storage object residing in a compound file object.</span></span> <span data-ttu-id="911bf-106">Para criar um objeto de arquivo composto e obter um ponteiro **IStorage** , chame a função de API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span><span class="sxs-lookup"><span data-stu-id="911bf-106">To create a compound file object and get an **IStorage** pointer, call the API function [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex).</span></span> <span data-ttu-id="911bf-107">Para abrir um objeto de arquivo composto existente e obter seu ponteiro raiz **IStorage** , chame [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span><span class="sxs-lookup"><span data-stu-id="911bf-107">To open an existing compound file object and get its root **IStorage** pointer, call [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).</span></span>

<span data-ttu-id="911bf-108">Os aplicativos que usam o armazenamento composto devem ser registrados no HKEY \_ classes \_ root \\ SystemFileAssociations e devem fornecer seus próprios manipuladores de propriedade.</span><span class="sxs-lookup"><span data-stu-id="911bf-108">Applications that use compound storage should be registered in HKEY\_CLASSES\_ROOT\\SystemFileAssociations and should provide their own property handlers.</span></span> <span data-ttu-id="911bf-109">Para obter mais informações, consulte a seção "registrando verbos e outras informações de associação de arquivo" do [registro do aplicativo](/windows/desktop/shell/app-registration).</span><span class="sxs-lookup"><span data-stu-id="911bf-109">For more information, see the "Registering Verbs and Other File Association Information" section of [Application Registration](/windows/desktop/shell/app-registration).</span></span>

## <a name="when-to-use"></a><span data-ttu-id="911bf-110">Quando usar</span><span class="sxs-lookup"><span data-stu-id="911bf-110">When to Use</span></span>

<span data-ttu-id="911bf-111">A maioria dos aplicativos usa essa implementação para criar e gerenciar armazenamentos e fluxos.</span><span class="sxs-lookup"><span data-stu-id="911bf-111">Most applications use this implementation to create and manage storages and streams.</span></span>

## <a name="methods"></a><span data-ttu-id="911bf-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="911bf-112">Methods</span></span>

<dl> <dt>

<span data-ttu-id="911bf-113"><span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)</span><span class="sxs-lookup"><span data-stu-id="911bf-113"><span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-114">Cria e abre um objeto de fluxo com o nome especificado contido neste objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-114">Creates and opens a stream object with the specified name contained in this storage object.</span></span> <span data-ttu-id="911bf-115">O nome não deve exceder 31 caracteres de comprimento (não incluindo o terminador de cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="911bf-115">The name must not exceed 31 characters in length (not including the string terminator).</span></span> <span data-ttu-id="911bf-116">Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE.</span><span class="sxs-lookup"><span data-stu-id="911bf-116">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="911bf-117">Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada.</span><span class="sxs-lookup"><span data-stu-id="911bf-117">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="911bf-118">A implementação de arquivo composto fornecido pelo COM do método [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) não oferece suporte aos seguintes comportamentos:</span><span class="sxs-lookup"><span data-stu-id="911bf-118">The COM-provided compound file implementation of the [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method does not support the following behaviors:</span></span>

-   <span data-ttu-id="911bf-119">\_Não há suporte para o sinalizador STGM DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="911bf-119">The STGM\_DELETEONRELEASE flag is not supported.</span></span>
-   <span data-ttu-id="911bf-120">Não há suporte para o modo transacionado ( \_ transacionado STGM) para objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="911bf-120">Transacted mode (STGM\_TRANSACTED) is not supported for stream objects.</span></span>
-   <span data-ttu-id="911bf-121">Não há suporte para a abertura do mesmo fluxo mais de uma vez no mesmo armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-121">Opening the same stream more than once from the same storage is not supported.</span></span> <span data-ttu-id="911bf-122">O \_ sinalizador de modo de compartilhamento exclusivo do STGM share \_ deve ser especificado no parâmetro *grfMode* .</span><span class="sxs-lookup"><span data-stu-id="911bf-122">The STGM\_SHARE\_EXCLUSIVE sharing-mode flag must be specified in the *grfMode* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-123"><span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)</span><span class="sxs-lookup"><span data-stu-id="911bf-123"><span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-124">Abre um objeto de fluxo existente dentro desse objeto de armazenamento usando os modos de acesso especificados no parâmetro *grfMode* .</span><span class="sxs-lookup"><span data-stu-id="911bf-124">Opens an existing stream object within this storage object using the access modes specified in the *grfMode* parameter.</span></span> <span data-ttu-id="911bf-125">Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE.</span><span class="sxs-lookup"><span data-stu-id="911bf-125">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="911bf-126">Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada.</span><span class="sxs-lookup"><span data-stu-id="911bf-126">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="911bf-127">A implementação do arquivo composto fornecido pelo COM do método [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) não oferece suporte ao seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="911bf-127">The COM-provided compound file implementation of the [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method does not support the following behavior:</span></span>

-   <span data-ttu-id="911bf-128">O \_ sinalizador STGM DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="911bf-128">The STGM\_DELETEONRELEASE flag.</span></span>
-   <span data-ttu-id="911bf-129">Modo transacionado (STGM \_ transacionado) para objetos de fluxo.</span><span class="sxs-lookup"><span data-stu-id="911bf-129">Transacted mode (STGM\_TRANSACTED) for stream objects.</span></span>
-   <span data-ttu-id="911bf-130">Abrindo o mesmo fluxo mais de uma vez do mesmo armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-130">Opening the same stream more than once from the same storage.</span></span> <span data-ttu-id="911bf-131">O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="911bf-131">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-132"><span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)</span><span class="sxs-lookup"><span data-stu-id="911bf-132"><span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-133">Cria e abre um novo objeto de armazenamento com o nome especificado no modo de acesso especificado.</span><span class="sxs-lookup"><span data-stu-id="911bf-133">Creates and opens a new storage object with the specified name in the specified access mode.</span></span> <span data-ttu-id="911bf-134">O nome não deve exceder 31 caracteres de comprimento (não incluindo o terminador de cadeia de caracteres).</span><span class="sxs-lookup"><span data-stu-id="911bf-134">The name must not exceed 31 characters in length (not including the string terminator).</span></span> <span data-ttu-id="911bf-135">Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE.</span><span class="sxs-lookup"><span data-stu-id="911bf-135">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="911bf-136">Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada.</span><span class="sxs-lookup"><span data-stu-id="911bf-136">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="911bf-137">A implementação do arquivo composto fornecido pelo COM do método [**IStorage:: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) não oferece suporte ao seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="911bf-137">The COM-provided compound file implementation of the [**IStorage::CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) method does not support the following behavior:</span></span>

-   <span data-ttu-id="911bf-138">O \_ sinalizador de prioridade STGM para armazenamentos não raiz.</span><span class="sxs-lookup"><span data-stu-id="911bf-138">The STGM\_PRIORITY flag for nonroot storages.</span></span>
-   <span data-ttu-id="911bf-139">Abrindo o mesmo objeto de armazenamento mais de uma vez do mesmo armazenamento pai.</span><span class="sxs-lookup"><span data-stu-id="911bf-139">Opening the same storage object more than once from the same parent storage.</span></span> <span data-ttu-id="911bf-140">O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="911bf-140">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>
-   <span data-ttu-id="911bf-141">O \_ sinalizador STGM DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="911bf-141">The STGM\_DELETEONRELEASE flag.</span></span> <span data-ttu-id="911bf-142">Se esse sinalizador for especificado, a função retornará STG \_ E \_ INVALIDFLAG.</span><span class="sxs-lookup"><span data-stu-id="911bf-142">If this flag is specified, the function returns STG\_E\_INVALIDFLAG.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-143"><span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)</span><span class="sxs-lookup"><span data-stu-id="911bf-143"><span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-144">Abre um objeto de armazenamento existente com o nome especificado no modo de acesso especificado.</span><span class="sxs-lookup"><span data-stu-id="911bf-144">Opens an existing storage object with the specified name in the specified access mode.</span></span> <span data-ttu-id="911bf-145">Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE.</span><span class="sxs-lookup"><span data-stu-id="911bf-145">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="911bf-146">Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada.</span><span class="sxs-lookup"><span data-stu-id="911bf-146">This is a compound file restriction, not a structured storage restriction.</span></span> <span data-ttu-id="911bf-147">A implementação do arquivo composto fornecido pelo COM do método [**IStorage:: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) não oferece suporte ao seguinte comportamento:</span><span class="sxs-lookup"><span data-stu-id="911bf-147">The COM-provided compound file implementation of the [**IStorage::OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) method does not support the following behavior:</span></span>

-   <span data-ttu-id="911bf-148">O \_ sinalizador de prioridade STGM para armazenamentos não raiz.</span><span class="sxs-lookup"><span data-stu-id="911bf-148">The STGM\_PRIORITY flag for nonroot storages.</span></span>
-   <span data-ttu-id="911bf-149">Abrindo o mesmo objeto de armazenamento mais de uma vez do mesmo armazenamento pai.</span><span class="sxs-lookup"><span data-stu-id="911bf-149">Opening the same storage object more than once from the same parent storage.</span></span> <span data-ttu-id="911bf-150">O \_ sinalizador exclusivo de compartilhamento de STGM \_ deve ser especificado.</span><span class="sxs-lookup"><span data-stu-id="911bf-150">The STGM\_SHARE\_EXCLUSIVE flag must be specified.</span></span>
-   <span data-ttu-id="911bf-151">O \_ sinalizador STGM DELETEONRELEASE.</span><span class="sxs-lookup"><span data-stu-id="911bf-151">The STGM\_DELETEONRELEASE flag.</span></span> <span data-ttu-id="911bf-152">Se esse sinalizador for especificado, a função retornará STG \_ E \_ INVALIDFUNCTION.</span><span class="sxs-lookup"><span data-stu-id="911bf-152">If this flag is specified, the function returns STG\_E\_INVALIDFUNCTION.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-153"><span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage:: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)</span><span class="sxs-lookup"><span data-stu-id="911bf-153"><span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage::CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-154">Copia apenas os subarmazenamentos e os fluxos deste objeto de armazenamento aberto em outro objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-154">Copies only the substorages and streams of this open storage object into another storage object.</span></span> <span data-ttu-id="911bf-155">O parâmetro *rgiidExclude* pode ser definido para o \_ IStream de IID para copiar somente os subarmazenamentos ou para o IStorage de IID \_ para copiar somente os fluxos.</span><span class="sxs-lookup"><span data-stu-id="911bf-155">The *rgiidExclude* parameter can be set to IID\_IStream to copy only substorages, or to IID\_IStorage to copy only streams.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-156"><span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage:: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)</span><span class="sxs-lookup"><span data-stu-id="911bf-156"><span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage::MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-157">Copia ou move um subarmazenamento ou fluxo deste objeto de armazenamento para outro objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-157">Copies or moves a substorage or stream from this storage object to another storage object.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-158"><span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage:: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)</span><span class="sxs-lookup"><span data-stu-id="911bf-158"><span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage::Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-159">Garante que todas as alterações feitas em um objeto de armazenamento aberto no modo transacionado sejam refletidas no armazenamento pai; para um armazenamento raiz, reflete as alterações no dispositivo real; por exemplo, um arquivo em disco.</span><span class="sxs-lookup"><span data-stu-id="911bf-159">Ensures that any changes made to a storage object open in transacted mode are reflected in the parent storage; for a root storage, reflects the changes in the actual device; for example, a file on disk.</span></span> <span data-ttu-id="911bf-160">Para um objeto de armazenamento raiz aberto no modo direto, esse método não tem efeito, exceto para liberar todos os buffers de memória para o disco.</span><span class="sxs-lookup"><span data-stu-id="911bf-160">For a root storage object opened in direct mode, this method has no effect except to flush all memory buffers to the disk.</span></span> <span data-ttu-id="911bf-161">Para objetos de armazenamento não raiz no modo direto, esse método não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="911bf-161">For nonroot storage objects in direct mode, this method has no effect.</span></span>

<span data-ttu-id="911bf-162">A implementação de arquivos compostos fornecidos pelo COM usa um processo de confirmação de duas fases, a menos que STGC \_ substitua seja especificado no parâmetro *grfCommitFlags* .</span><span class="sxs-lookup"><span data-stu-id="911bf-162">The COM-provided compound files implementation uses a two-phase commit process unless STGC\_OVERWRITE is specified in the *grfCommitFlags* parameter.</span></span> <span data-ttu-id="911bf-163">Esse processo de duas fases garante a robustez dos dados, caso a operação de confirmação falhe.</span><span class="sxs-lookup"><span data-stu-id="911bf-163">This two-phase process ensures the robustness of data, in case the commit operation fails.</span></span> <span data-ttu-id="911bf-164">Primeiro, todos os novos dados são gravados no espaço não utilizado no arquivo subjacente.</span><span class="sxs-lookup"><span data-stu-id="911bf-164">First, all new data is written to unused space in the underlying file.</span></span> <span data-ttu-id="911bf-165">Se necessário, o novo espaço é alocado para o arquivo.</span><span class="sxs-lookup"><span data-stu-id="911bf-165">If necessary, new space is allocated to the file.</span></span> <span data-ttu-id="911bf-166">Depois que essa etapa for concluída, uma tabela no arquivo será atualizada usando uma operação de gravação de setor único para indicar que os novos dados serão usados no lugar do antigo.</span><span class="sxs-lookup"><span data-stu-id="911bf-166">After this step has been completed, a table in the file is updated using a single-sector write operation to indicate that the new data is to be used in place of the old.</span></span> <span data-ttu-id="911bf-167">Os dados antigos tornam-se espaço livre para serem usados na próxima operação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="911bf-167">The old data becomes free space to be used at the next commit operation.</span></span> <span data-ttu-id="911bf-168">Assim, os dados antigos estarão disponíveis e poderão ser restaurados se ocorrer um erro durante a confirmação das alterações.</span><span class="sxs-lookup"><span data-stu-id="911bf-168">Thus, the old data is available and can be restored if an error occurs when committing changes.</span></span> <span data-ttu-id="911bf-169">Se STGC \_ overwrite for especificado, uma única operação de confirmação de fase será usada.</span><span class="sxs-lookup"><span data-stu-id="911bf-169">If STGC\_OVERWRITE is specified, a single phase commit operation is used.</span></span> <span data-ttu-id="911bf-170">Para obter mais informações sobre sinalizadores de modo transacionado, consulte enumeração [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) .</span><span class="sxs-lookup"><span data-stu-id="911bf-170">For more information about transacted mode flags, see [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-171"><span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage:: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)</span><span class="sxs-lookup"><span data-stu-id="911bf-171"><span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage::Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-172">Descarta todas as alterações feitas no objeto de armazenamento desde a última operação de confirmação.</span><span class="sxs-lookup"><span data-stu-id="911bf-172">Discards all changes that have been made to the storage object since the last commit operation.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-173"><span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage:: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)</span><span class="sxs-lookup"><span data-stu-id="911bf-173"><span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage::EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-174">Cria e recupera um ponteiro para um objeto enumerador que pode ser usado para enumerar os objetos de armazenamento e de fluxo contidos neste objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-174">Creates and retrieves a pointer to an enumerator object that can be used to enumerate the storage and stream objects contained within this storage object.</span></span> <span data-ttu-id="911bf-175">A implementação do arquivo composto fornecido pelo COM tira um instantâneo dessas informações.</span><span class="sxs-lookup"><span data-stu-id="911bf-175">The COM-provided compound file implementation takes a snapshot of that information.</span></span> <span data-ttu-id="911bf-176">Portanto, as alterações nos fluxos e armazenamentos não são refletidas no enumerador até que um novo enumerador seja obtido.</span><span class="sxs-lookup"><span data-stu-id="911bf-176">Therefore, changes to the streams and storages are not reflected in the enumerator until a new enumerator is obtained.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-177"><span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)</span><span class="sxs-lookup"><span data-stu-id="911bf-177"><span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage::DestroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-178">Remove o elemento especificado (subarmazenamento ou fluxo) deste objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-178">Removes the specified element (substorage or stream) from this storage object.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-179"><span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage:: renomeelement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)</span><span class="sxs-lookup"><span data-stu-id="911bf-179"><span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage::RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-180">Renomeia o subarmazenamento ou fluxo especificado neste objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-180">Renames the specified substorage or stream in this storage object.</span></span> <span data-ttu-id="911bf-181">Os caracteres de 000 a 01F, servindo como o primeiro caractere do nome de fluxo/armazenamento, são reservados para uso pelo OLE.</span><span class="sxs-lookup"><span data-stu-id="911bf-181">The 000 through 01f characters, serving as the first character of the stream/storage name, are reserved for use by OLE.</span></span> <span data-ttu-id="911bf-182">Essa é uma restrição de arquivo composto, não uma restrição de armazenamento estruturada.</span><span class="sxs-lookup"><span data-stu-id="911bf-182">This is a compound file restriction, not a structured storage restriction.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-183"><span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage:: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)</span><span class="sxs-lookup"><span data-stu-id="911bf-183"><span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage::SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-184">Define a modificação, o acesso e os tempos de criação do elemento de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="911bf-184">Sets the modification, access, and creation times of the specified storage element.</span></span> <span data-ttu-id="911bf-185">A implementação de arquivo composto fornecida pelo COM mantém tempos de modificação e alteração para objetos de armazenamento interno.</span><span class="sxs-lookup"><span data-stu-id="911bf-185">The COM-provided compound-file implementation maintains modification and change times for internal storage objects.</span></span> <span data-ttu-id="911bf-186">Os objetos de armazenamento raiz dão suporte para qualquer suporte do sistema de arquivos subjacente (ou por [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)).</span><span class="sxs-lookup"><span data-stu-id="911bf-186">Root storage objects support whatever is supported by the underlying file system (or by [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)).</span></span> <span data-ttu-id="911bf-187">A implementação do arquivo composto não mantém carimbos de data/hora para fluxos internos.</span><span class="sxs-lookup"><span data-stu-id="911bf-187">The compound file implementation does not maintain any time stamps for internal streams.</span></span> <span data-ttu-id="911bf-188">Os carimbos de data/hora sem suporte são relatados como zero, o que permite que o chamador teste o suporte.</span><span class="sxs-lookup"><span data-stu-id="911bf-188">Unsupported time stamps are reported as zero, which allows the caller to test for support.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-189"><span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage:: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)</span><span class="sxs-lookup"><span data-stu-id="911bf-189"><span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-190">Atribui o CLSID especificado a este objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-190">Assigns the specified CLSID to this storage object.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-191"><span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage:: SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)</span><span class="sxs-lookup"><span data-stu-id="911bf-191"><span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage::SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-192">Armazena até 32 bits de informações de estado neste objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="911bf-192">Stores up to 32 bits of state information in this storage object.</span></span> <span data-ttu-id="911bf-193">O estado definido por esse método é somente para uso externo.</span><span class="sxs-lookup"><span data-stu-id="911bf-193">The state set by this method is for external use only.</span></span> <span data-ttu-id="911bf-194">A implementação do arquivo composto fornecido pelo COM não executa nenhuma ação com base no estado.</span><span class="sxs-lookup"><span data-stu-id="911bf-194">The COM-provided compound file implementation does not perform any action based on the state.</span></span>

</dd> <dt>

<span data-ttu-id="911bf-195"><span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage:: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)</span><span class="sxs-lookup"><span data-stu-id="911bf-195"><span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage::Stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)</span></span>
</dt> <dd>

<span data-ttu-id="911bf-196">Recupera a estrutura [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) para este objeto de armazenamento aberto.</span><span class="sxs-lookup"><span data-stu-id="911bf-196">Retrieves the [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) structure for this open storage object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="911bf-197">Comentários</span><span class="sxs-lookup"><span data-stu-id="911bf-197">Remarks</span></span>

<span data-ttu-id="911bf-198">Se o objeto de armazenamento for aberto no modo simples, o uso dos métodos acima será restrito.</span><span class="sxs-lookup"><span data-stu-id="911bf-198">If the storage object is opened in simple mode, use of the above methods is restricted.</span></span> <span data-ttu-id="911bf-199">Um armazenamento estará no modo simples se for aberto com o \_ elemento simples STGM especificado no parâmetro *grfMode* da função [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) .</span><span class="sxs-lookup"><span data-stu-id="911bf-199">A storage is in simple mode if it is opened with the STGM\_SIMPLE element specified in the *grfMode* parameter of the [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) or [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) function.</span></span> <span data-ttu-id="911bf-200">Para obter mais informações sobre armazenamentos de modo simples, consulte [**constantes STGM**](stgm-constants.md).</span><span class="sxs-lookup"><span data-stu-id="911bf-200">For more information about simple-mode storages, see [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="911bf-201">Se o objeto de armazenamento de modo simples foi obtido da função **StgCreateStorageEx** , o método [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) pode ser chamado, mas o método [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) não pode.</span><span class="sxs-lookup"><span data-stu-id="911bf-201">If the simple-mode storage object was obtained from the **StgCreateStorageEx** function, then the [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method can be called but the [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) method cannot.</span></span> <span data-ttu-id="911bf-202">Se o objeto de armazenamento de modo simples foi obtido da função **StgOpenStorageEx** , o método **OpenStream** pode ser chamado, mas o método **CreateStream** não pode.</span><span class="sxs-lookup"><span data-stu-id="911bf-202">If the simple mode storage object was obtained from the **StgOpenStorageEx** function, then the **OpenStream** method can be called but the **CreateStream** method cannot.</span></span>

<span data-ttu-id="911bf-203">Quando um objeto de armazenamento de modo simples é usado para criar um fluxo, o tamanho mínimo desse fluxo normalmente é de 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="911bf-203">When a simple-mode storage object is used to create a stream, the minimum size of that stream typically is 4096 bytes.</span></span> <span data-ttu-id="911bf-204">Se menos dados forem gravados no fluxo, o tamanho será arredondado para até 4096 bytes.</span><span class="sxs-lookup"><span data-stu-id="911bf-204">If less data is written to the stream, the size is rounded up to 4096 bytes.</span></span>

## <a name="related-topics"></a><span data-ttu-id="911bf-205">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="911bf-205">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="911bf-206">Limites de implementação de arquivo composto</span><span class="sxs-lookup"><span data-stu-id="911bf-206">Compound File Implementation Limits</span></span>](structured-storage-interfaces.md)
</dt> <dt>

[<span data-ttu-id="911bf-207">**IFillLockBytes**</span><span class="sxs-lookup"><span data-stu-id="911bf-207">**IFillLockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[<span data-ttu-id="911bf-208">**ILockBytes**</span><span class="sxs-lookup"><span data-stu-id="911bf-208">**ILockBytes**</span></span>](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[<span data-ttu-id="911bf-209">**IRootStorage**</span><span class="sxs-lookup"><span data-stu-id="911bf-209">**IRootStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[<span data-ttu-id="911bf-210">**IStorage**</span><span class="sxs-lookup"><span data-stu-id="911bf-210">**IStorage**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[<span data-ttu-id="911bf-211">**IStream**</span><span class="sxs-lookup"><span data-stu-id="911bf-211">**IStream**</span></span>](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[<span data-ttu-id="911bf-212">**StgCreateDocfile**</span><span class="sxs-lookup"><span data-stu-id="911bf-212">**StgCreateDocfile**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[<span data-ttu-id="911bf-213">**StgCreateStorageEx**</span><span class="sxs-lookup"><span data-stu-id="911bf-213">**StgCreateStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[<span data-ttu-id="911bf-214">**StgOpenStorage**</span><span class="sxs-lookup"><span data-stu-id="911bf-214">**StgOpenStorage**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[<span data-ttu-id="911bf-215">**StgOpenStorageEx**</span><span class="sxs-lookup"><span data-stu-id="911bf-215">**StgOpenStorageEx**</span></span>](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 