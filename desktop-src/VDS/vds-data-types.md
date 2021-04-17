---
description: Os tipos de dados com suporte pelo VDS definem valores de retorno de função, parâmetros de função e membros de estrutura. Os tipos de dados definem o tamanho e o significado desses elementos.
ms.assetid: f17e8c7e-e3cb-49ca-9060-2299dda55770
title: Tipos de dados VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a868606110d9cf1c3cad5c3036789d041a5d86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105797520"
---
# <a name="vds-data-types"></a><span data-ttu-id="e06d1-104">Tipos de dados VDS</span><span class="sxs-lookup"><span data-stu-id="e06d1-104">VDS Data Types</span></span>

<span data-ttu-id="e06d1-105">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e06d1-105">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e06d1-106">Os tipos de dados com suporte pelo VDS definem valores de retorno de função, parâmetros de função e membros de estrutura.</span><span class="sxs-lookup"><span data-stu-id="e06d1-106">The data types supported by VDS define function return values, function parameters, and structure members.</span></span> <span data-ttu-id="e06d1-107">Os tipos de dados definem o tamanho e o significado desses elementos.</span><span class="sxs-lookup"><span data-stu-id="e06d1-107">Data types define the size and meaning of these elements.</span></span>



| <span data-ttu-id="e06d1-108">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="e06d1-108">Data type</span></span>                                                                                      | <span data-ttu-id="e06d1-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="e06d1-109">Description</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e06d1-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**\_ID do objeto VDS \_**</span><span class="sxs-lookup"><span data-stu-id="e06d1-110"><span id="VDS_OBJECT_ID"></span><span id="vds_object_id"></span>**VDS\_OBJECT\_ID**</span></span><br/> | <span data-ttu-id="e06d1-111">ID do objeto VDS.</span><span class="sxs-lookup"><span data-stu-id="e06d1-111">VDS object ID.</span></span> <span data-ttu-id="e06d1-112">Não há garantia de que esses valores sejam exclusivos entre as reinicializações.</span><span class="sxs-lookup"><span data-stu-id="e06d1-112">These values are not guaranteed to be unique across reboots.</span></span> <br/> <span data-ttu-id="e06d1-113">Esse tipo é declarado em VDS. h (VdsHwPrv. h para provedores de hardware) como um GUID.</span><span class="sxs-lookup"><span data-stu-id="e06d1-113">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a GUID.</span></span> <br/> |
| <span data-ttu-id="e06d1-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**\_ID do caminho VDS \_**</span><span class="sxs-lookup"><span data-stu-id="e06d1-114"><span id="VDS_PATH_ID"></span><span id="vds_path_id"></span>**VDS\_PATH\_ID**</span></span><br/>       | <span data-ttu-id="e06d1-115">ID do caminho do VDS para e/s de vários caminhos (MPIO).</span><span class="sxs-lookup"><span data-stu-id="e06d1-115">VDS path ID for multipath I/O (MPIO).</span></span> <br/> <span data-ttu-id="e06d1-116">Esse tipo é declarado em VDS. h (VdsHwPrv. h para provedores de hardware) como um UINT64.</span><span class="sxs-lookup"><span data-stu-id="e06d1-116">This type is declared in Vds.h (VdsHwPrv.h for hardware providers) as a UINT64.</span></span><br/>                                      |



 

 

