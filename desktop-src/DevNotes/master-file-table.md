---
description: A tabela de arquivos mestre (MFT) armazena as informações necessárias para recuperar arquivos de uma partição NTFS.
ms.assetid: 673fb4d0-7b6f-44fe-bfd6-1962e14ccdf5
title: Tabela de arquivos mestre (notas do desenvolvedor)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ae8656a44b6dadd7d4ff601ddc64623935f5881
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920148"
---
# <a name="master-file-table"></a><span data-ttu-id="6ea1c-103">Tabela de arquivos mestre</span><span class="sxs-lookup"><span data-stu-id="6ea1c-103">Master File Table</span></span>

<span data-ttu-id="6ea1c-104">\[Este documento se aplica somente à versão 3 de volumes NTFS.\]</span><span class="sxs-lookup"><span data-stu-id="6ea1c-104">\[This document applies only to version 3 of NTFS volumes.\]</span></span>

<span data-ttu-id="6ea1c-105">A tabela de arquivos mestre (MFT) armazena as informações necessárias para recuperar arquivos de uma partição NTFS.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-105">The master file table (MFT) stores the information required to retrieve files from an NTFS partition.</span></span>

<span data-ttu-id="6ea1c-106">Um arquivo pode ter um ou mais registros de MFT e pode conter um ou mais atributos.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-106">A file may have one or more MFT records, and can contain one or more attributes.</span></span> <span data-ttu-id="6ea1c-107">No NTFS, uma referência de arquivo é a referência de segmento de MFT do registro de arquivo base.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-107">In NTFS, a file reference is the MFT segment reference of the base file record.</span></span> <span data-ttu-id="6ea1c-108">Para obter mais informações, [**consulte \_ \_ referência de segmento de MFT**](mft-segment-reference.md).</span><span class="sxs-lookup"><span data-stu-id="6ea1c-108">For more information, see [**MFT\_SEGMENT\_REFERENCE**](mft-segment-reference.md).</span></span>

<span data-ttu-id="6ea1c-109">A MFT contém segmentos de registro de arquivo; os primeiros 16 deles são reservados para arquivos especiais, como o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6ea1c-109">The MFT contains file record segments; the first 16 of these are reserved for special files, such as the following:</span></span>

-   <span data-ttu-id="6ea1c-110">0: MFT ($Mft)</span><span class="sxs-lookup"><span data-stu-id="6ea1c-110">0: MFT ($Mft)</span></span>
-   <span data-ttu-id="6ea1c-111">5: diretório raiz ( \\ )</span><span class="sxs-lookup"><span data-stu-id="6ea1c-111">5: root directory (\\)</span></span>
-   <span data-ttu-id="6ea1c-112">6: arquivo de alocação de cluster de volume ($Bitmap)</span><span class="sxs-lookup"><span data-stu-id="6ea1c-112">6: volume cluster allocation file ($Bitmap)</span></span>
-   <span data-ttu-id="6ea1c-113">8: arquivo de cluster inválido ($BadClus)</span><span class="sxs-lookup"><span data-stu-id="6ea1c-113">8: bad-cluster file ($BadClus)</span></span>

<span data-ttu-id="6ea1c-114">Cada segmento de registro de arquivo começa com um cabeçalho de segmento de registro de arquivo.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-114">Each file record segment starts with a file record segment header.</span></span> <span data-ttu-id="6ea1c-115">Para obter mais informações, [**consulte \_ \_ \_ cabeçalho de segmento de registro de arquivo**](file-record-segment-header.md).</span><span class="sxs-lookup"><span data-stu-id="6ea1c-115">For more information, see [**FILE\_RECORD\_SEGMENT\_HEADER**](file-record-segment-header.md).</span></span> <span data-ttu-id="6ea1c-116">Cada segmento de registro de arquivo é seguido por um ou mais atributos.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-116">Each file record segment is followed by one or more attributes.</span></span> <span data-ttu-id="6ea1c-117">Cada atributo começa com um cabeçalho de registro de atributo.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-117">Each attribute starts with an attribute record header.</span></span> <span data-ttu-id="6ea1c-118">Para obter mais informações, [**consulte \_ \_ cabeçalho de registro de atributo**](attribute-record-header.md).</span><span class="sxs-lookup"><span data-stu-id="6ea1c-118">For more information, see [**ATTRIBUTE\_RECORD\_HEADER**](attribute-record-header.md).</span></span> <span data-ttu-id="6ea1c-119">O registro de atributo inclui o tipo de atributo (como $DATA ou $BITMAP), um nome opcional e o valor do atributo.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-119">The attribute record includes the attribute type (such as $DATA or $BITMAP), an optional name, and the attribute value.</span></span> <span data-ttu-id="6ea1c-120">O fluxo de dados do usuário é um atributo, assim como todos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-120">The user data stream is an attribute, as are all streams.</span></span> <span data-ttu-id="6ea1c-121">A lista de atributos é encerrada com 0xFFFFFFFF ($END).</span><span class="sxs-lookup"><span data-stu-id="6ea1c-121">The attribute list is terminated with 0xFFFFFFFF ($END).</span></span>

<span data-ttu-id="6ea1c-122">Veja a seguir alguns exemplos de atributos.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-122">The following are some example attributes.</span></span>

-   <span data-ttu-id="6ea1c-123">O arquivo de $Mft contém um atributo de $DATA sem nome que é a sequência de segmentos de registro de MFT, em ordem.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-123">The $Mft file contains an unnamed $DATA attribute that is the sequence of MFT record segments, in order.</span></span>
-   <span data-ttu-id="6ea1c-124">O arquivo de $Mft contém um atributo de $BITMAP sem nome que indica quais registros de MFT estão em uso.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-124">The $Mft file contains an unnamed $BITMAP attribute that indicates which MFT records are in use.</span></span>
-   <span data-ttu-id="6ea1c-125">O arquivo de $Bitmap contém um atributo de $DATA sem nome que indica quais clusters estão em uso.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-125">The $Bitmap file contains an unnamed $DATA attribute that indicates which clusters are in use.</span></span>
-   <span data-ttu-id="6ea1c-126">O arquivo de $BadClus contém um atributo de $DATA chamado $BAD que contém uma entrada que corresponde a cada cluster defeituoso.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-126">The $BadClus file contains a $DATA attribute named $BAD that contains an entry that corresponds to each bad cluster.</span></span>

<span data-ttu-id="6ea1c-127">Quando não há mais espaço para armazenar atributos no segmento de registro de arquivo, segmentos de registro de arquivo adicionais são alocados e inseridos no primeiro segmento (ou base) de registro de arquivo em um atributo chamado lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-127">When there is no more space for storing attributes in the file record segment, additional file record segments are allocated and inserted in the first (or base) file record segment in an attribute called the attribute list.</span></span> <span data-ttu-id="6ea1c-128">A lista de atributos indica onde cada atributo associado ao arquivo pode ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-128">The attribute list indicates where each attribute associated with the file can be found.</span></span> <span data-ttu-id="6ea1c-129">Isso inclui todos os atributos no registro de arquivo base, exceto para a própria lista de atributos.</span><span class="sxs-lookup"><span data-stu-id="6ea1c-129">This includes all attributes in the base file record, except for the attribute list itself.</span></span> <span data-ttu-id="6ea1c-130">Para obter mais informações, consulte a [**\_ \_ entrada da lista de atributos**](attribute-list-entry.md).</span><span class="sxs-lookup"><span data-stu-id="6ea1c-130">For more information, see [**ATTRIBUTE\_LIST\_ENTRY**](attribute-list-entry.md).</span></span>

<span data-ttu-id="6ea1c-131">As estruturas relacionadas ao MFT incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6ea1c-131">Structures related to the MFT include the following:</span></span>

-   [<span data-ttu-id="6ea1c-132">**\_entrada da lista de atributos \_**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-132">**ATTRIBUTE\_LIST\_ENTRY**</span></span>](attribute-list-entry.md)
-   [<span data-ttu-id="6ea1c-133">**\_cabeçalho de registro de atributo \_**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-133">**ATTRIBUTE\_RECORD\_HEADER**</span></span>](attribute-record-header.md)
-   [<span data-ttu-id="6ea1c-134">**nome do arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-134">**FILE\_NAME**</span></span>](file-name.md)
-   [<span data-ttu-id="6ea1c-135">**\_cabeçalho de \_ segmento de registro de arquivo \_**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-135">**FILE\_RECORD\_SEGMENT\_HEADER**</span></span>](file-record-segment-header.md)
-   [<span data-ttu-id="6ea1c-136">**\_referência de segmento de MFT \_**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-136">**MFT\_SEGMENT\_REFERENCE**</span></span>](mft-segment-reference.md)
-   [<span data-ttu-id="6ea1c-137">**cabeçalho de vários \_ setores \_**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-137">**MULTI\_SECTOR\_HEADER**</span></span>](multi-sector-header.md)
-   [<span data-ttu-id="6ea1c-138">**\_informações padrão**</span><span class="sxs-lookup"><span data-stu-id="6ea1c-138">**STANDARD\_INFORMATION**</span></span>](standard-information.md)

## <a name="related-topics"></a><span data-ttu-id="6ea1c-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6ea1c-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6ea1c-140">[Referência técnica do NTFS](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="6ea1c-140">[NTFS Technical Reference](/previous-versions/windows/it-pro/windows-server-2003/cc758691(v=ws.10))</span></span>
</dt> </dl>

 

 
