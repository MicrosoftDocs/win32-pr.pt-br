---
description: Esta seção descreve a interface de programação de aplicativo para o VDS (serviço de disco virtual).
ms.assetid: d00fc772-331f-4d71-a418-e34acdfb6652
title: Referência do VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369111add0b3f4b7e2742c764a6cbf8b1d8bfdd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105775654"
---
# <a name="vds-reference"></a><span data-ttu-id="e9f6f-103">Referência do VDS</span><span class="sxs-lookup"><span data-stu-id="e9f6f-103">VDS Reference</span></span>

<span data-ttu-id="e9f6f-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="e9f6f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="e9f6f-105">Esta seção descreve a interface de programação de aplicativo para o VDS (serviço de disco virtual).</span><span class="sxs-lookup"><span data-stu-id="e9f6f-105">This section describes the application programming interface to the Virtual Disk Service (VDS).</span></span>

<span data-ttu-id="e9f6f-106">Os desenvolvedores de aplicativos usam interfaces, estruturas, enumerações e constantes simbólicas nessa API para consultar e configurar o armazenamento — de discos a matrizes de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-106">Application developers use the interfaces, structures, enumerations, and symbolic constants in this API to query and configure storage—from disks to storage arrays.</span></span> <span data-ttu-id="e9f6f-107">Para obter uma visão detalhada da relação entre os tipos do VDS, consulte o [modelo de objeto do VDS](vds-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="e9f6f-107">For a detailed look at the relationship among VDS types, see the [VDS Object Model](vds-object-model.md).</span></span>

<span data-ttu-id="e9f6f-108">Os fabricantes de armazenamento implementam muitas das interfaces definidas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-108">Storage manufacturers implement many of the interfaces defined in this section.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e9f6f-109">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="e9f6f-109">In this Section</span></span>

<dl> <dt>

[<span data-ttu-id="e9f6f-110">Constantes do VDS</span><span class="sxs-lookup"><span data-stu-id="e9f6f-110">VDS Constants</span></span>](vds-constants.md)
</dt> <dd>

<span data-ttu-id="e9f6f-111">Lista as constantes simbólicas na API do VDS.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-111">Lists the symbolic constants in the VDS API.</span></span>

</dd> <dt>

[<span data-ttu-id="e9f6f-112">Tipos de dados VDS</span><span class="sxs-lookup"><span data-stu-id="e9f6f-112">VDS Data Types</span></span>](vds-data-types.md)
</dt> <dd>

<span data-ttu-id="e9f6f-113">Lista os tipos de dados usados com o VDS.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-113">Lists the data types used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="e9f6f-114">Enumerações VDS</span><span class="sxs-lookup"><span data-stu-id="e9f6f-114">VDS Enumerations</span></span>](vds-enumerations.md)
</dt> <dd>

<span data-ttu-id="e9f6f-115">Descreve as enumerações usadas com o VDS.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-115">Describes the enumerations used with VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="e9f6f-116">Interfaces VDS</span><span class="sxs-lookup"><span data-stu-id="e9f6f-116">VDS Interfaces</span></span>](vds-interfaces.md)
</dt> <dd>

<span data-ttu-id="e9f6f-117">Descreve as interfaces VDS e os métodos que eles expõem.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-117">Describes VDS interfaces and the methods they expose.</span></span>

</dd> <dt>

[<span data-ttu-id="e9f6f-118">Estruturas VDS</span><span class="sxs-lookup"><span data-stu-id="e9f6f-118">VDS Structures</span></span>](vds-structures.md)
</dt> <dd>

<span data-ttu-id="e9f6f-119">Descreve as estruturas passadas como parâmetros para métodos VDS.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-119">Describes the structures passed as parameters to VDS methods.</span></span>

</dd> <dt>

[<span data-ttu-id="e9f6f-120">Códigos de retorno comuns do serviço de disco virtual</span><span class="sxs-lookup"><span data-stu-id="e9f6f-120">Virtual Disk Service Common Return Codes</span></span>](virtual-disk-service-common-return-codes.md)
</dt> <dd>

<span data-ttu-id="e9f6f-121">Descreve os códigos de erro mais comuns que são específicos do VDS.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-121">Describes the most common error codes that are specific to VDS.</span></span>

</dd> <dt>

[<span data-ttu-id="e9f6f-122">Glossário do serviço de disco virtual</span><span class="sxs-lookup"><span data-stu-id="e9f6f-122">Virtual Disk Service Glossary</span></span>](virtual-disk-service-glossary-all.md)
</dt> <dd>

<span data-ttu-id="e9f6f-123">Glossário de termos técnicos usados na documentação do VDS.</span><span class="sxs-lookup"><span data-stu-id="e9f6f-123">Glossary of technical terms used in VDS documentation.</span></span>

</dd> </dl>

 

 
