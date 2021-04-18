---
description: Representa as informações mantidas no Gerenciador de partições sobre um disco que faz parte de um cluster.
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: Estrutura de DISK_CLUSTER_INFO (Ntdddisk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753484"
---
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="9745d-103">Estrutura de informações de \_ cluster de disco \_</span><span class="sxs-lookup"><span data-stu-id="9745d-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="9745d-104">Representa as informações mantidas no Gerenciador de partições sobre um disco que faz parte de um cluster.</span><span class="sxs-lookup"><span data-stu-id="9745d-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="9745d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9745d-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="9745d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="9745d-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9745d-107">**Versão**</span><span class="sxs-lookup"><span data-stu-id="9745d-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="9745d-108">O número de versão.</span><span class="sxs-lookup"><span data-stu-id="9745d-108">The version number.</span></span> <span data-ttu-id="9745d-109">Esse valor deve ser definido como o tamanho dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="9745d-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="9745d-110">**Sinalizadores**</span><span class="sxs-lookup"><span data-stu-id="9745d-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="9745d-111">Uma combinação de sinalizadores relacionados a discos e clusters.</span><span class="sxs-lookup"><span data-stu-id="9745d-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="9745d-112">Valor</span><span class="sxs-lookup"><span data-stu-id="9745d-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="9745d-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9745d-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="9745d-114"><dt>**Disco \_ Sinalizador de CLUSTER \_ \_ habilitado**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9745d-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="9745d-115">O disco é usado como parte do serviço de cluster.</span><span class="sxs-lookup"><span data-stu-id="9745d-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="9745d-116"><dt>**Disco \_ Sinalizador de CLUSTER \_ \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9745d-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="9745d-117">Os volumes no disco são expostos por CSVFS em todos os nós do cluster.</span><span class="sxs-lookup"><span data-stu-id="9745d-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="9745d-118"><dt>**Disco \_ \_Sinalizador \_ de cluster em \_ manutenção**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9745d-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="9745d-119">O recurso de cluster associado a este disco está em modo de manutenção.</span><span class="sxs-lookup"><span data-stu-id="9745d-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="9745d-120"><dt>**Disco \_ A chegada de PnP do sinalizador de CLUSTER foi \_ \_ \_ \_ concluída**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="9745d-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="9745d-121">O driver de disco de cluster para o modo kernel (Clusdisk) recebeu uma notificação PnP da chegada do disco.</span><span class="sxs-lookup"><span data-stu-id="9745d-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9745d-122">**FlagsMask**</span><span class="sxs-lookup"><span data-stu-id="9745d-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="9745d-123">Os sinalizadores que estão sendo modificados no membro **flags** .</span><span class="sxs-lookup"><span data-stu-id="9745d-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="9745d-124">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="9745d-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="9745d-125">**True** para enviar uma notificação de alteração de layout; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="9745d-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9745d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9745d-126">Requirements</span></span>



| <span data-ttu-id="9745d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9745d-127">Requirement</span></span> | <span data-ttu-id="9745d-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9745d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9745d-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9745d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9745d-130">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="9745d-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="9745d-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9745d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9745d-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9745d-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9745d-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9745d-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="9745d-134"><dt>Ntdddisk. h</dt></span><span class="sxs-lookup"><span data-stu-id="9745d-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9745d-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9745d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9745d-136">Estruturas de gerenciamento de disco</span><span class="sxs-lookup"><span data-stu-id="9745d-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="9745d-137">**\_informações do \_ cluster de obtenção de disco de IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9745d-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="9745d-138">**\_informações do \_ cluster do conjunto de discos do IOCTL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9745d-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




