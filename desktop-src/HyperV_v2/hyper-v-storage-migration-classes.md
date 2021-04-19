---
description: A API de migração do Hyper-V define os seguintes elementos de programação.
ms.assetid: E1FE7351-2F14-4C8F-AF5C-9009CC61CE22
title: Referência da API de migração do Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e40a05bc976cf1722aba558eeca9c7b04cdf7287
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810355"
---
# <a name="hyper-v-migration-api-reference"></a><span data-ttu-id="f1f0c-103">Referência da API de migração do Hyper-V</span><span class="sxs-lookup"><span data-stu-id="f1f0c-103">Hyper-V migration API reference</span></span>

<span data-ttu-id="f1f0c-104">A API de migração do Hyper-V define os seguintes elementos de programação.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-104">The Hyper-V migration API defines the following programming elements.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f1f0c-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="f1f0c-105">In this section</span></span>



| <span data-ttu-id="f1f0c-106">Tópico</span><span class="sxs-lookup"><span data-stu-id="f1f0c-106">Topic</span></span>                                                                                                                                | <span data-ttu-id="f1f0c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1f0c-107">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1f0c-108">**Msvm \_ MigrationJob**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-108">**Msvm\_MigrationJob**</span></span>](msvm-migrationjob.md)<br/>                                                                           | <span data-ttu-id="f1f0c-109">Essa classe representa um trabalho de operação de migração criado para armazenamento ou migração de sistema virtual pelo serviço de migração de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-109">This class represents a migration operation job created for storage or virtual system migration by the virtual system migration service.</span></span><br/>                                                 |
| [<span data-ttu-id="f1f0c-110">**Msvm \_ VirtualSystemMigrationCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-110">**Msvm\_VirtualSystemMigrationCapabilities**</span></span>](msvm-virtualsystemmigrationcapabilities.md)<br/>                               | <span data-ttu-id="f1f0c-111">Define o meio pelo qual um cliente pode descobrir os métodos fornecidos pelo serviço de migração e o intervalo válido de dados de configuração de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-111">Defines the means by which a client can discover the methods provided by the migration service, and valid range of virtual system migration setting data.</span></span><br/>                                |
| [<span data-ttu-id="f1f0c-112">**Msvm \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-112">**Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>](msvm-virtualsystemmigrationnetworksettingdata.md)<br/>                   | <span data-ttu-id="f1f0c-113">Representa a rede na qual o serviço de migração de sistema virtual está escutando a migração de sistema virtual de entrada.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-113">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span><br/>                                                                 |
| [<span data-ttu-id="f1f0c-114">**Msvm \_ VirtualSystemMigrationService**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-114">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)<br/>                                         | <span data-ttu-id="f1f0c-115">Representa o serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-115">Represents the virtual system migration service.</span></span> <span data-ttu-id="f1f0c-116">Ele é usado para migrar um sistema virtual ou para migrar o armazenamento de um sistema virtual de uma plataforma de virtualização para outra.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-116">It is used for migrating a virtual system or for migrating the storage of a virtual system from one virtualization platform to another.</span></span><br/> |
| [<span data-ttu-id="f1f0c-117">**Msvm \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-117">**Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>](msvm-virtualsystemmigrationservicesettingdata.md)<br/>                   | <span data-ttu-id="f1f0c-118">Representa as configurações do serviço de migração de sistema virtual em um host.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-118">Represents the settings for the virtual system migration service on a host.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="f1f0c-119">**Msvm \_ VirtualSystemMigrationServiceSettingDataComponent**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-119">**Msvm\_VirtualSystemMigrationServiceSettingDataComponent**</span></span>](msvm-virtualsystemmigrationservicesettingdatacomponent.md)<br/> | <span data-ttu-id="f1f0c-120">Uma associação usada para representar as configurações de rede de migração do sistema virtual do serviço de migração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-120">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span><br/>                                                                      |
| [<span data-ttu-id="f1f0c-121">**Msvm \_ VirtualSystemMigrationSettingData**</span><span class="sxs-lookup"><span data-stu-id="f1f0c-121">**Msvm\_VirtualSystemMigrationSettingData**</span></span>](msvm-virtualsystemmigrationsettingdata.md)<br/>                                 | <span data-ttu-id="f1f0c-122">Representa as configurações de migração para migrar um sistema virtual e o armazenamento anexado a um sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="f1f0c-122">Represents the migration settings for migrating a virtual system and the storage attached to a virtual system.</span></span><br/>                                                                           |



 

 

 




