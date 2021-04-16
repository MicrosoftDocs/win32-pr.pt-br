---
description: Contém métodos que obtêm o conteúdo bruto da definição de entrada de vídeo dos dados de identificação de vídeo avançado (VESA) avançados de associação de exibição estendida de vídeo (E-EDID) v. 1. x Standard 128-bytes de dados.
ms.assetid: c13d4ddd-d171-44d5-9e70-3a6f89ad55da
title: Classe WmiMonitorDescriptorMethods
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDescriptorMethods
- WmiMonitorDescriptorMethods.Active
- WmiMonitorDescriptorMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 578c08c48ada4859b69e00655c5eea8c075515fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757663"
---
# <a name="wmimonitordescriptormethods-class"></a><span data-ttu-id="6fc9b-103">Classe WmiMonitorDescriptorMethods</span><span class="sxs-lookup"><span data-stu-id="6fc9b-103">WmiMonitorDescriptorMethods class</span></span>

<span data-ttu-id="6fc9b-104">A classe WMI **WmiMonitorDescriptorMethods** contém métodos que obtêm o conteúdo bruto da definição de entrada de vídeo dos dados de identificação de vídeo (VESA) avançados de associação de exibição estendida (E-EDID) v. 1. x os blocos de dados padrão de 128 bytes.</span><span class="sxs-lookup"><span data-stu-id="6fc9b-104">The **WmiMonitorDescriptorMethods** WMI class contains methods that obtain the raw content of Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) v.1.x standard 128-byte data blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="6fc9b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6fc9b-105">Syntax</span></span>

``` syntax
class WmiMonitorDescriptorMethods : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a><span data-ttu-id="6fc9b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6fc9b-106">Members</span></span>

<span data-ttu-id="6fc9b-107">A classe **WmiMonitorDescriptorMethods** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6fc9b-107">The **WmiMonitorDescriptorMethods** class has these types of members:</span></span>

-   [<span data-ttu-id="6fc9b-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fc9b-108">Methods</span></span>](#wmimonitordescriptormethods-class)
-   [<span data-ttu-id="6fc9b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6fc9b-109">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="6fc9b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="6fc9b-110">Methods</span></span>

<span data-ttu-id="6fc9b-111">A classe **WmiMonitorDescriptorMethods** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="6fc9b-111">The **WmiMonitorDescriptorMethods** class has these methods.</span></span>



| <span data-ttu-id="6fc9b-112">Método</span><span class="sxs-lookup"><span data-stu-id="6fc9b-112">Method</span></span>                                                                                           | <span data-ttu-id="6fc9b-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="6fc9b-113">Description</span></span>                                                                   |
|:-------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [<span data-ttu-id="6fc9b-114">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-114">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md) | <span data-ttu-id="6fc9b-115">Acessa os dados brutos para um bloco de descritor do EDID v. 1. x especificado.</span><span class="sxs-lookup"><span data-stu-id="6fc9b-115">Accesses the raw data for a specified EDID v.1.x descriptor block.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="6fc9b-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6fc9b-116">Properties</span></span>

<span data-ttu-id="6fc9b-117">A classe **WmiMonitorDescriptorMethods** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6fc9b-117">The **WmiMonitorDescriptorMethods** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6fc9b-118">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-118">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fc9b-119">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-119">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="6fc9b-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fc9b-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6fc9b-121">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="6fc9b-121">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="6fc9b-122">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-122">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6fc9b-123">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6fc9b-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6fc9b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6fc9b-125">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-125">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="6fc9b-126">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="6fc9b-126">Name of the specific monitor instance.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6fc9b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6fc9b-127">Requirements</span></span>



| <span data-ttu-id="6fc9b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6fc9b-128">Requirement</span></span> | <span data-ttu-id="6fc9b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6fc9b-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6fc9b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc9b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6fc9b-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6fc9b-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="6fc9b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6fc9b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6fc9b-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6fc9b-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="6fc9b-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="6fc9b-134">Namespace</span></span><br/>                | <span data-ttu-id="6fc9b-135">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="6fc9b-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="6fc9b-136">MOF</span><span class="sxs-lookup"><span data-stu-id="6fc9b-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6fc9b-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9b-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="6fc9b-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6fc9b-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fc9b-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fc9b-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fc9b-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="6fc9b-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fc9b-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="6fc9b-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




