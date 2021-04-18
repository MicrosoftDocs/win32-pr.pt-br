---
description: Objeto de plex de LUN
ms.assetid: db6eabaa-1b84-4613-ab2a-8d5904305e08
title: Objeto de plex de LUN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f1b51657ccbfc0f1bd3d73e54128cac3f0b507c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105781530"
---
# <a name="lun-plex-object"></a><span data-ttu-id="4de0f-103">Objeto de plex de LUN</span><span class="sxs-lookup"><span data-stu-id="4de0f-103">LUN Plex Object</span></span>

<span data-ttu-id="4de0f-104">\[A partir do Windows 8 e do Windows Server 2012, a interface com do [serviço de disco virtual](virtual-disk-service-portal.md) é substituída pela [API de gerenciamento de armazenamento do Windows](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span><span class="sxs-lookup"><span data-stu-id="4de0f-104">\[Beginning with Windows 8 and Windows Server 2012, the [Virtual Disk Service](virtual-disk-service-portal.md) COM interface is superseded by the [Windows Storage Management API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal).\]</span></span>

<span data-ttu-id="4de0f-105">Um objeto de plex de LUN modela um plex de LUN que está contido por um LUN.</span><span class="sxs-lookup"><span data-stu-id="4de0f-105">A LUN plex object models a LUN plex that is contained by a LUN.</span></span> <span data-ttu-id="4de0f-106">Somente um LUN espelhado pode ter vários plexes; todos os outros tipos de LUN têm um plex.</span><span class="sxs-lookup"><span data-stu-id="4de0f-106">Only a mirrored LUN can have multiple plexes; all other LUN types have one plex.</span></span> <span data-ttu-id="4de0f-107">Cada plex contém uma cópia dos dados no LUN.</span><span class="sxs-lookup"><span data-stu-id="4de0f-107">Each plex contains a copy of the data on the LUN.</span></span> <span data-ttu-id="4de0f-108">Novos plexes podem ser adicionados a um LUN e, com exceção do plex original, os plexes existentes podem ser removidos.</span><span class="sxs-lookup"><span data-stu-id="4de0f-108">New plexes can be added to a LUN, and, with the exception of the original plex, existing plexes can be removed.</span></span> <span data-ttu-id="4de0f-109">O VDS dá suporte a quatro tipos de plex de LUN: simples, estendido, distribuído e distribuído com paridade.</span><span class="sxs-lookup"><span data-stu-id="4de0f-109">VDS supports four LUN plex types: simple, spanned, striped, and striped with parity.</span></span> <span data-ttu-id="4de0f-110">Para obter uma descrição de cada um desses tipos de LUN, consulte o [objeto LUN](lun-object.md).</span><span class="sxs-lookup"><span data-stu-id="4de0f-110">For a description of each of these LUN types, see the [LUN Object](lun-object.md).</span></span>

<span data-ttu-id="4de0f-111">Use o método [**IVdsLun:: addplex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) para adicionar um plex a um LUN e o método [**IVdsLun:: RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) para excluir o Plex.</span><span class="sxs-lookup"><span data-stu-id="4de0f-111">Use the [**IVdsLun::AddPlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-addplex) method to add a plex to a LUN and the [**IVdsLun::RemovePlex**](/windows/desktop/api/Vds/nf-vds-ivdslun-removeplex) method to delete the plex.</span></span> <span data-ttu-id="4de0f-112">Você pode consultar os plexes de LUN invocando o método [**IVdsLun:: QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) .</span><span class="sxs-lookup"><span data-stu-id="4de0f-112">You can query for LUN plexes by invoking the [**IVdsLun::QueryPlexes**](/windows/desktop/api/Vds/nf-vds-ivdslun-queryplexes) method.</span></span> <span data-ttu-id="4de0f-113">Você pode obter um ponteiro para um plex de LUN específico selecionando o objeto de plex desejado da enumeração que é retornada pelo método **QueryPlexes** .</span><span class="sxs-lookup"><span data-stu-id="4de0f-113">You can get a pointer to a specific LUN plex by selecting the desired plex object from the enumeration that is returned by the **QueryPlexes** method.</span></span> <span data-ttu-id="4de0f-114">Com um objeto de Plex, você pode consultar as extensões de unidade e dicas automágicas e aplicar novas dicas.</span><span class="sxs-lookup"><span data-stu-id="4de0f-114">With a plex object, you can query for the drive extents and automagic hints, and apply new hints.</span></span>

<span data-ttu-id="4de0f-115">Além de um identificador de objeto, um nome e um número de série, as propriedades de objeto de plex de LUN incluem o tipo de Plex, o tamanho, o status, a integridade, o estado de transição e os sinalizadores; uma lista de desmascaramento e tamanho de distribuição; e uma configuração de prioridade de recriação.</span><span class="sxs-lookup"><span data-stu-id="4de0f-115">In addition to an object identifier, a name, and a serial number, LUN plex object properties include the plex type, size, status, health, transition state, and flags; an unmasking list and stripe size; and a rebuild priority setting.</span></span>

<span data-ttu-id="4de0f-116">A tabela a seguir lista as interfaces, as enumerações e as estruturas relacionadas.</span><span class="sxs-lookup"><span data-stu-id="4de0f-116">The following table lists related interfaces, enumerations, and structures.</span></span>



| <span data-ttu-id="4de0f-117">Tipo</span><span class="sxs-lookup"><span data-stu-id="4de0f-117">Type</span></span>                                              | <span data-ttu-id="4de0f-118">Elemento</span><span class="sxs-lookup"><span data-stu-id="4de0f-118">Element</span></span>                                                                                                                                                          |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4de0f-119">Interfaces que são sempre expostas por este objeto</span><span class="sxs-lookup"><span data-stu-id="4de0f-119">Interfaces that are always exposed by this object</span></span> | <span data-ttu-id="4de0f-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span><span class="sxs-lookup"><span data-stu-id="4de0f-120">[**IVdsLunPlex**](/windows/desktop/api/Vds/nn-vds-ivdslunplex).</span></span>                                                                                                                              |
| <span data-ttu-id="4de0f-121">Enumerações associadas</span><span class="sxs-lookup"><span data-stu-id="4de0f-121">Associated enumerations</span></span>                           | <span data-ttu-id="4de0f-122">[**VDS \_ \_ \_ Sinalizador de plex de LUN**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**\_ \_ \_ status de plex de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status)e [**\_ \_ \_ tipo de plex de LUN VDS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span><span class="sxs-lookup"><span data-stu-id="4de0f-122">[**VDS\_LUN\_PLEX\_FLAG**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_flag), [**VDS\_LUN\_PLEX\_STATUS**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_status), and [**VDS\_LUN\_PLEX\_TYPE**](/windows/desktop/api/Vds/ne-vds-vds_lun_plex_type).</span></span> |
| <span data-ttu-id="4de0f-123">Estruturas associadas</span><span class="sxs-lookup"><span data-stu-id="4de0f-123">Associated structures</span></span>                             | <span data-ttu-id="4de0f-124">[**VDS \_ \_ \_ prop Plex de LUN**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span><span class="sxs-lookup"><span data-stu-id="4de0f-124">[**VDS\_LUN\_PLEX\_PROP**](/windows/desktop/api/Vds/ns-vds-vds_lun_plex_prop).</span></span>                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="4de0f-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4de0f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4de0f-126">Objetos de provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="4de0f-126">Hardware Provider Objects</span></span>](hardware-provider-objects.md)
</dt> <dt>

[<span data-ttu-id="4de0f-127">Objeto LUN</span><span class="sxs-lookup"><span data-stu-id="4de0f-127">LUN Object</span></span>](lun-object.md)
</dt> </dl>

 

 
