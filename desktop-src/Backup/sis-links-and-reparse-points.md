---
title: Links do SIS e pontos de nova análise
description: O SIS é um driver de filtro NTFS que substitui arquivos duplicados por links de cópia em gravação (chamados de links do SIS) que apontam para um único arquivo de backup, reduzindo o disco e a sobrecarga de cache desses arquivos.
ms.assetid: 1600a9ff-413c-4059-b04c-c862f6cf8f32
keywords:
- Backup de pontos de nova análise
- Backup de armazenamento de instância única (SIS), links do SIS
- Backup de repositório de instância única (SIS), pontos de nova análise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4987e7c64a83e7d0b02ed91899a182616be7943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084774"
---
# <a name="sis-links-and-reparse-points"></a><span data-ttu-id="2324e-106">Links do SIS e pontos de nova análise</span><span class="sxs-lookup"><span data-stu-id="2324e-106">SIS Links and Reparse Points</span></span>

<span data-ttu-id="2324e-107">O SIS é um driver de filtro NTFS que substitui arquivos duplicados por links de cópia em gravação (chamados de links do SIS) que apontam para um único arquivo de backup, reduzindo o disco e a sobrecarga de cache desses arquivos.</span><span class="sxs-lookup"><span data-stu-id="2324e-107">SIS is an NTFS filter driver that replaces duplicate files with copy-on-write links (referred to as SIS links) that point to a single backing file, reducing the disk and cache overhead of those files.</span></span> <span data-ttu-id="2324e-108">Esse arquivo de backup está contido em um [repositório comum](the-sis-common-store-and-common-store-files.md).</span><span class="sxs-lookup"><span data-stu-id="2324e-108">This backing file is contained in a [common store](the-sis-common-store-and-common-store-files.md).</span></span> <span data-ttu-id="2324e-109">A implementação da arquitetura do SIS faz uso de [pontos de nova análise](/windows/desktop/FileIO/reparse-points) que contêm informações sobre os links do SIS.</span><span class="sxs-lookup"><span data-stu-id="2324e-109">The implementation of the SIS architecture makes use of [reparse points](/windows/desktop/FileIO/reparse-points) that contain information about the SIS links.</span></span>

<span data-ttu-id="2324e-110">Os links do SIS são implementados como arquivos esparsos, geralmente com a maioria dos intervalos do arquivo não alocados e um ponto de nova análise.</span><span class="sxs-lookup"><span data-stu-id="2324e-110">SIS links are implemented as sparse files, usually with most ranges of the file unallocated, and a reparse point.</span></span> <span data-ttu-id="2324e-111">A estrutura e o conteúdo de um ponto de nova análise são opacos para seus aplicativos de backup e restauração; no entanto, seus aplicativos enviam e recuperam os dados dentro desses pontos de nova análise de e para funções de API do SIS que processam as informações neles.</span><span class="sxs-lookup"><span data-stu-id="2324e-111">The structure and contents of a reparse point is opaque to your backup and restore applications; however, your applications send and retrieve the data within these reparse points to and from SIS API functions that process the information in them.</span></span> <span data-ttu-id="2324e-112">As informações em um ponto de nova análise referem-se a um único arquivo de backup que contém os dados de arquivo reais.</span><span class="sxs-lookup"><span data-stu-id="2324e-112">The information in a reparse point refers to a single backing file that contains the actual file data.</span></span> <span data-ttu-id="2324e-113">Esse arquivo de backup é chamado de [arquivo de armazenamento comum](the-sis-common-store-and-common-store-files.md)e existe no repositório comum.</span><span class="sxs-lookup"><span data-stu-id="2324e-113">This backing file is called a [common-store file](the-sis-common-store-and-common-store-files.md), and it exists in the common store.</span></span>

<span data-ttu-id="2324e-114">Ao restaurar um link do SIS, o aplicativo de restauração deve executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="2324e-114">When restoring a SIS link, your restore application should perform the following steps:</span></span>

1.  <span data-ttu-id="2324e-115">Determine o arquivo de repositório comum ou os arquivos aos quais o link do SIS aponta.</span><span class="sxs-lookup"><span data-stu-id="2324e-115">Determine the common-store file or files to which the SIS link points.</span></span>
2.  <span data-ttu-id="2324e-116">Se o arquivo ou os arquivos não existirem no armazenamento comum, restaure o arquivo ou os arquivos juntamente com o link do SIS.</span><span class="sxs-lookup"><span data-stu-id="2324e-116">If the file or files do not exist in the common store, restore the file or files along with the SIS link.</span></span>
3.  <span data-ttu-id="2324e-117">Se o link do SIS apontar para um arquivo de armazenamento comum ou arquivos que existem no disco, restaure apenas o link do SIS.</span><span class="sxs-lookup"><span data-stu-id="2324e-117">If the SIS link points to a common-store file or files that exist on the disk, then restore only the SIS link.</span></span> <span data-ttu-id="2324e-118">Lembre-se de que os dados em arquivos de armazenamento comum nunca são alterados, portanto, se um determinado arquivo de repositório comum ainda estiver no disco no momento da restauração, ele terá o mesmo conteúdo de quando foi feito o backup e não haverá necessidade de substituí-lo.</span><span class="sxs-lookup"><span data-stu-id="2324e-118">Recall that the data in common-store files never changes, so if a given common-store file is still on the disk at restore time, it has the same contents as when it was backed up and there is no need to overwrite it.</span></span>

<span data-ttu-id="2324e-119">A única sobrecarga adicional necessária para backups assistidos por SIS é que seu aplicativo de backup deve fazer backup do link do SIS e dos dados associados aos arquivos de backup.</span><span class="sxs-lookup"><span data-stu-id="2324e-119">The only additional overhead required for SIS-assisted backups is that your backup application must back up the SIS link and the data associated with the backing files.</span></span> <span data-ttu-id="2324e-120">Todas as operações de backup e restauração do SIS são locais para um volume específico.</span><span class="sxs-lookup"><span data-stu-id="2324e-120">All SIS backup and restore operations are local to a specific volume.</span></span>

 

 