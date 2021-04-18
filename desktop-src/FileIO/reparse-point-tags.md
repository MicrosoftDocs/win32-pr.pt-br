---
description: Cada ponto de nova análise tem uma marca de identificador para que você possa diferenciar com eficiência os diferentes tipos de pontos de nova análise, sem precisar examinar os dados definidos pelo usuário no ponto de nova análise.
ms.assetid: d02a2f50-d374-4149-bc04-49b7db052f62
title: Marcas de ponto de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a53b65034347e2a2c07afcd6c1f03e31f73cef7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105756776"
---
# <a name="reparse-point-tags"></a><span data-ttu-id="c30f3-103">Marcas de ponto de nova análise</span><span class="sxs-lookup"><span data-stu-id="c30f3-103">Reparse Point Tags</span></span>

<span data-ttu-id="c30f3-104">Cada ponto de nova análise tem uma marca de identificador para que você possa diferenciar com eficiência os diferentes tipos de pontos de nova análise, sem precisar examinar os dados definidos pelo usuário no ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="c30f3-104">Each reparse point has an identifier tag so that you can efficiently differentiate between the different types of reparse points, without having to examine the user-defined data in the reparse point.</span></span> <span data-ttu-id="c30f3-105">O sistema usa um conjunto de marcas predefinidas e um intervalo de marcas reservado para a Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c30f3-105">The system uses a set of predefined tags and a range of tags reserved for Microsoft.</span></span> <span data-ttu-id="c30f3-106">Se você usar qualquer uma das marcas reservadas ao definir um ponto de nova análise, a operação falhará.</span><span class="sxs-lookup"><span data-stu-id="c30f3-106">If you use any of the reserved tags when setting a reparse point, the operation fails.</span></span> <span data-ttu-id="c30f3-107">As marcas não incluídas nesses intervalos não são reservadas e estão disponíveis para seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c30f3-107">Tags not included in these ranges are not reserved and are available for your application.</span></span>

<span data-ttu-id="c30f3-108">Ao definir um ponto de nova análise, você deve marcar os dados a serem colocados no ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="c30f3-108">When you set a reparse point, you must tag the data to be placed in the reparse point.</span></span> <span data-ttu-id="c30f3-109">Depois que o ponto de nova análise tiver sido estabelecido, um novo conjunto de operações falhará se a marca para os novos dados não corresponder à marca dos dados existentes.</span><span class="sxs-lookup"><span data-stu-id="c30f3-109">After the reparse point has been established, a new set operation fails if the tag for the new data does not match the tag for the existing data.</span></span> <span data-ttu-id="c30f3-110">Se as marcas corresponderem, a operação set substituirá o ponto de nova análise existente.</span><span class="sxs-lookup"><span data-stu-id="c30f3-110">If the tags match, the set operation overwrites the existing reparse point.</span></span>

<span data-ttu-id="c30f3-111">Para recuperar a marca de ponto de nova análise, use a função [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) .</span><span class="sxs-lookup"><span data-stu-id="c30f3-111">To retrieve the reparse point tag, use the [**FindFirstFile**](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea) function.</span></span> <span data-ttu-id="c30f3-112">Se o membro **dwFileAttributes** incluir o atributo de **\_ \_ \_ ponto de nova análise de atributo de arquivo** , o membro **dwReserved0** especificará o ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="c30f3-112">If the **dwFileAttributes** member includes the **FILE\_ATTRIBUTE\_REPARSE\_POINT** attribute, then the **dwReserved0** member specifies the reparse point.</span></span>

## <a name="tag-contents"></a><span data-ttu-id="c30f3-113">Conteúdo da tag</span><span class="sxs-lookup"><span data-stu-id="c30f3-113">Tag Contents</span></span>

<span data-ttu-id="c30f3-114">As marcas de nova análise são armazenadas como valores **DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c30f3-114">Reparse tags are stored as **DWORD** values.</span></span> <span data-ttu-id="c30f3-115">Os bits definem determinados atributos, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="c30f3-115">The bits define certain attributes, as shown in the following diagram.</span></span>

``` syntax
   3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
   1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
  +-+-+-+-+-----------------------+-------------------------------+
  |M|R|N|R|     Reserved bits     |      Reparse tag value        |
  +-+-+-+-+-----------------------+-------------------------------+
```

<span data-ttu-id="c30f3-116">Os baixos 16 bits determinam o tipo de ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="c30f3-116">The low 16 bits determine the kind of reparse point.</span></span> <span data-ttu-id="c30f3-117">Os altos 16 bits têm 12 bits reservados para uso futuro e 4 bits que denotam atributos específicos das marcas e os dados representados pelo ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="c30f3-117">The high 16 bits have 12 bits reserved for future use and 4 bits that denote specific attributes of the tags and the data represented by the reparse point.</span></span> <span data-ttu-id="c30f3-118">A tabela a seguir descreve esses bits.</span><span class="sxs-lookup"><span data-stu-id="c30f3-118">The following table describes these bits.</span></span>



| <span data-ttu-id="c30f3-119">bit</span><span class="sxs-lookup"><span data-stu-id="c30f3-119">Bit</span></span> | <span data-ttu-id="c30f3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="c30f3-120">Description</span></span>                                                                                                  |
|-----|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c30f3-121">M</span><span class="sxs-lookup"><span data-stu-id="c30f3-121">M</span></span>   | <span data-ttu-id="c30f3-122">Microsoft de bits.</span><span class="sxs-lookup"><span data-stu-id="c30f3-122">Microsoft bit.</span></span> <span data-ttu-id="c30f3-123">Se esse bit estiver definido, a marca será de propriedade da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c30f3-123">If this bit is set, the tag is owned by Microsoft.</span></span> <span data-ttu-id="c30f3-124">Todas as outras marcas devem usar zero para este bit.</span><span class="sxs-lookup"><span data-stu-id="c30f3-124">All other tags must use zero for this bit.</span></span> |
| <span data-ttu-id="c30f3-125">R</span><span class="sxs-lookup"><span data-stu-id="c30f3-125">R</span></span>   | <span data-ttu-id="c30f3-126">Reservado deve ser zero para todas as marcas que não sejam da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c30f3-126">Reserved; must be zero for all non-Microsoft tags.</span></span>                                                           |
| <span data-ttu-id="c30f3-127">N</span><span class="sxs-lookup"><span data-stu-id="c30f3-127">N</span></span>   | <span data-ttu-id="c30f3-128">Bit alternativo de nome.</span><span class="sxs-lookup"><span data-stu-id="c30f3-128">Name surrogate bit.</span></span> <span data-ttu-id="c30f3-129">Se esse bit for definido, o arquivo ou diretório representará outra entidade nomeada no sistema.</span><span class="sxs-lookup"><span data-stu-id="c30f3-129">If this bit is set, the file or directory represents another named entity in the system.</span></span> |



 

<span data-ttu-id="c30f3-130">As macros a seguir existem para auxiliar no teste de marcas:</span><span class="sxs-lookup"><span data-stu-id="c30f3-130">The following macros exist to assist in testing tags:</span></span>

-   [<span data-ttu-id="c30f3-131">**IsReparseTagMicrosoft**</span><span class="sxs-lookup"><span data-stu-id="c30f3-131">**IsReparseTagMicrosoft**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagmicrosoft)
-   [<span data-ttu-id="c30f3-132">**IsReparseTagNameSurrogate**</span><span class="sxs-lookup"><span data-stu-id="c30f3-132">**IsReparseTagNameSurrogate**</span></span>](/windows/desktop/api/Winnt/nf-winnt-isreparsetagnamesurrogate)

<span data-ttu-id="c30f3-133">Cada macro retornará um valor diferente de zero se o bit associado for definido.</span><span class="sxs-lookup"><span data-stu-id="c30f3-133">Each macro returns a nonzero value if the associated bit is set.</span></span>

<span data-ttu-id="c30f3-134">A seguir estão os valores de marca de nova análise predefinidos da Microsoft; Eles são definidos em WinNT. h:</span><span class="sxs-lookup"><span data-stu-id="c30f3-134">The following are Microsoft's predefined reparse tag values; they are defined in WinNT.h:</span></span>

-   <span data-ttu-id="c30f3-135">**IO_REPARSE_TAG_AF_UNIX**</span><span class="sxs-lookup"><span data-stu-id="c30f3-135">**IO_REPARSE_TAG_AF_UNIX**</span></span>
-   <span data-ttu-id="c30f3-136">**IO_REPARSE_TAG_APPEXECLINK**</span><span class="sxs-lookup"><span data-stu-id="c30f3-136">**IO_REPARSE_TAG_APPEXECLINK**</span></span>
-   <span data-ttu-id="c30f3-137">**IO_REPARSE_TAG_CLOUD**</span><span class="sxs-lookup"><span data-stu-id="c30f3-137">**IO_REPARSE_TAG_CLOUD**</span></span>
-   <span data-ttu-id="c30f3-138">**IO_REPARSE_TAG_CLOUD_1**</span><span class="sxs-lookup"><span data-stu-id="c30f3-138">**IO_REPARSE_TAG_CLOUD_1**</span></span>
-   <span data-ttu-id="c30f3-139">**IO_REPARSE_TAG_CLOUD_2**</span><span class="sxs-lookup"><span data-stu-id="c30f3-139">**IO_REPARSE_TAG_CLOUD_2**</span></span>
-   <span data-ttu-id="c30f3-140">**IO_REPARSE_TAG_CLOUD_3**</span><span class="sxs-lookup"><span data-stu-id="c30f3-140">**IO_REPARSE_TAG_CLOUD_3**</span></span>
-   <span data-ttu-id="c30f3-141">**IO_REPARSE_TAG_CLOUD_4**</span><span class="sxs-lookup"><span data-stu-id="c30f3-141">**IO_REPARSE_TAG_CLOUD_4**</span></span>
-   <span data-ttu-id="c30f3-142">**IO_REPARSE_TAG_CLOUD_5**</span><span class="sxs-lookup"><span data-stu-id="c30f3-142">**IO_REPARSE_TAG_CLOUD_5**</span></span>
-   <span data-ttu-id="c30f3-143">**IO_REPARSE_TAG_CLOUD_6**</span><span class="sxs-lookup"><span data-stu-id="c30f3-143">**IO_REPARSE_TAG_CLOUD_6**</span></span>
-   <span data-ttu-id="c30f3-144">**IO_REPARSE_TAG_CLOUD_7**</span><span class="sxs-lookup"><span data-stu-id="c30f3-144">**IO_REPARSE_TAG_CLOUD_7**</span></span>
-   <span data-ttu-id="c30f3-145">**IO_REPARSE_TAG_CLOUD_8**</span><span class="sxs-lookup"><span data-stu-id="c30f3-145">**IO_REPARSE_TAG_CLOUD_8**</span></span>
-   <span data-ttu-id="c30f3-146">**IO_REPARSE_TAG_CLOUD_9**</span><span class="sxs-lookup"><span data-stu-id="c30f3-146">**IO_REPARSE_TAG_CLOUD_9**</span></span>
-   <span data-ttu-id="c30f3-147">**IO_REPARSE_TAG_CLOUD_A**</span><span class="sxs-lookup"><span data-stu-id="c30f3-147">**IO_REPARSE_TAG_CLOUD_A**</span></span>
-   <span data-ttu-id="c30f3-148">**IO_REPARSE_TAG_CLOUD_B**</span><span class="sxs-lookup"><span data-stu-id="c30f3-148">**IO_REPARSE_TAG_CLOUD_B**</span></span>
-   <span data-ttu-id="c30f3-149">**IO_REPARSE_TAG_CLOUD_C**</span><span class="sxs-lookup"><span data-stu-id="c30f3-149">**IO_REPARSE_TAG_CLOUD_C**</span></span>
-   <span data-ttu-id="c30f3-150">**IO_REPARSE_TAG_CLOUD_D**</span><span class="sxs-lookup"><span data-stu-id="c30f3-150">**IO_REPARSE_TAG_CLOUD_D**</span></span>
-   <span data-ttu-id="c30f3-151">**IO_REPARSE_TAG_CLOUD_E**</span><span class="sxs-lookup"><span data-stu-id="c30f3-151">**IO_REPARSE_TAG_CLOUD_E**</span></span>
-   <span data-ttu-id="c30f3-152">**IO_REPARSE_TAG_CLOUD_F**</span><span class="sxs-lookup"><span data-stu-id="c30f3-152">**IO_REPARSE_TAG_CLOUD_F**</span></span>
-   <span data-ttu-id="c30f3-153">**IO_REPARSE_TAG_CLOUD_MASK**</span><span class="sxs-lookup"><span data-stu-id="c30f3-153">**IO_REPARSE_TAG_CLOUD_MASK**</span></span>
-   <span data-ttu-id="c30f3-154">**IO_REPARSE_TAG_CSV**</span><span class="sxs-lookup"><span data-stu-id="c30f3-154">**IO_REPARSE_TAG_CSV**</span></span>
-   <span data-ttu-id="c30f3-155">**IO_REPARSE_TAG_DEDUP**</span><span class="sxs-lookup"><span data-stu-id="c30f3-155">**IO_REPARSE_TAG_DEDUP**</span></span>
-   <span data-ttu-id="c30f3-156">**IO_REPARSE_TAG_DFS**</span><span class="sxs-lookup"><span data-stu-id="c30f3-156">**IO_REPARSE_TAG_DFS**</span></span>
-   <span data-ttu-id="c30f3-157">**IO_REPARSE_TAG_DFSR**</span><span class="sxs-lookup"><span data-stu-id="c30f3-157">**IO_REPARSE_TAG_DFSR**</span></span>
-   <span data-ttu-id="c30f3-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span><span class="sxs-lookup"><span data-stu-id="c30f3-158">**IO_REPARSE_TAG_FILE_PLACEHOLDER**</span></span>
-   <span data-ttu-id="c30f3-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span><span class="sxs-lookup"><span data-stu-id="c30f3-159">**IO_REPARSE_TAG_GLOBAL_REPARSE**</span></span>
-   <span data-ttu-id="c30f3-160">**IO_REPARSE_TAG_HSM**</span><span class="sxs-lookup"><span data-stu-id="c30f3-160">**IO_REPARSE_TAG_HSM**</span></span>
-   <span data-ttu-id="c30f3-161">**IO_REPARSE_TAG_HSM2**</span><span class="sxs-lookup"><span data-stu-id="c30f3-161">**IO_REPARSE_TAG_HSM2**</span></span>
-   <span data-ttu-id="c30f3-162">**IO_REPARSE_TAG_MOUNT_POINT**</span><span class="sxs-lookup"><span data-stu-id="c30f3-162">**IO_REPARSE_TAG_MOUNT_POINT**</span></span>
-   <span data-ttu-id="c30f3-163">**IO_REPARSE_TAG_NFS**</span><span class="sxs-lookup"><span data-stu-id="c30f3-163">**IO_REPARSE_TAG_NFS**</span></span>
-   <span data-ttu-id="c30f3-164">**IO_REPARSE_TAG_ONEDRIVE**</span><span class="sxs-lookup"><span data-stu-id="c30f3-164">**IO_REPARSE_TAG_ONEDRIVE**</span></span>
-   <span data-ttu-id="c30f3-165">**IO_REPARSE_TAG_PROJFS**</span><span class="sxs-lookup"><span data-stu-id="c30f3-165">**IO_REPARSE_TAG_PROJFS**</span></span>
-   <span data-ttu-id="c30f3-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="c30f3-166">**IO_REPARSE_TAG_PROJFS_TOMBSTONE**</span></span>
-   <span data-ttu-id="c30f3-167">**IO_REPARSE_TAG_SIS**</span><span class="sxs-lookup"><span data-stu-id="c30f3-167">**IO_REPARSE_TAG_SIS**</span></span>
-   <span data-ttu-id="c30f3-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span><span class="sxs-lookup"><span data-stu-id="c30f3-168">**IO_REPARSE_TAG_STORAGE_SYNC**</span></span>
-   <span data-ttu-id="c30f3-169">**IO_REPARSE_TAG_SYMLINK**</span><span class="sxs-lookup"><span data-stu-id="c30f3-169">**IO_REPARSE_TAG_SYMLINK**</span></span>
-   <span data-ttu-id="c30f3-170">**IO_REPARSE_TAG_UNHANDLED**</span><span class="sxs-lookup"><span data-stu-id="c30f3-170">**IO_REPARSE_TAG_UNHANDLED**</span></span>
-   <span data-ttu-id="c30f3-171">**IO_REPARSE_TAG_WCI**</span><span class="sxs-lookup"><span data-stu-id="c30f3-171">**IO_REPARSE_TAG_WCI**</span></span>
-   <span data-ttu-id="c30f3-172">**IO_REPARSE_TAG_WCI_1**</span><span class="sxs-lookup"><span data-stu-id="c30f3-172">**IO_REPARSE_TAG_WCI_1**</span></span>
-   <span data-ttu-id="c30f3-173">**IO_REPARSE_TAG_WCI_LINK**</span><span class="sxs-lookup"><span data-stu-id="c30f3-173">**IO_REPARSE_TAG_WCI_LINK**</span></span>
-   <span data-ttu-id="c30f3-174">**IO_REPARSE_TAG_WCI_LINK_1**</span><span class="sxs-lookup"><span data-stu-id="c30f3-174">**IO_REPARSE_TAG_WCI_LINK_1**</span></span>
-   <span data-ttu-id="c30f3-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span><span class="sxs-lookup"><span data-stu-id="c30f3-175">**IO_REPARSE_TAG_WCI_TOMBSTONE**</span></span>
-   <span data-ttu-id="c30f3-176">**IO_REPARSE_TAG_WIM**</span><span class="sxs-lookup"><span data-stu-id="c30f3-176">**IO_REPARSE_TAG_WIM**</span></span>
-   <span data-ttu-id="c30f3-177">**IO_REPARSE_TAG_WOF**</span><span class="sxs-lookup"><span data-stu-id="c30f3-177">**IO_REPARSE_TAG_WOF**</span></span>

<span data-ttu-id="c30f3-178">Para garantir a exclusividade das marcas, a Microsoft fornece um mecanismo para distribuir novas marcas.</span><span class="sxs-lookup"><span data-stu-id="c30f3-178">To ensure uniqueness of tags, Microsoft provides a mechanism to distribute new tags.</span></span> <span data-ttu-id="c30f3-179">Para obter mais informações, consulte o [Kit de IFS (sistema de arquivos instalável)](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span><span class="sxs-lookup"><span data-stu-id="c30f3-179">For more information, see the [Installable File System (IFS) Kit](https://www.microsoft.com/whdc/devtools/ifskit/reparse.mspx).</span></span>

 

 



