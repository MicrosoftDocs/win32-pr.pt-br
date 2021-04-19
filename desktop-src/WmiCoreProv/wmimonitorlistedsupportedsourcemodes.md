---
description: Lista os modos de origem com suporte para um monitor de vídeo em seu descritor de monitor, se existir algum.
ms.assetid: cca59d28-bd93-4df2-989e-0516dd8eae83
title: Classe WmiMonitorListedSupportedSourceModes
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedSupportedSourceModes
- WmiMonitorListedSupportedSourceModes.Active
- WmiMonitorListedSupportedSourceModes.InstanceName
- WmiMonitorListedSupportedSourceModes.NumOfMonitorSourceModes
- WmiMonitorListedSupportedSourceModes.PreferredMonitorSourceModeIndex
- WmiMonitorListedSupportedSourceModes.MonitorSourceModes
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 35cb4b3548654c72686a8843cc697f109f661d87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105785196"
---
# <a name="wmimonitorlistedsupportedsourcemodes-class"></a><span data-ttu-id="2f09e-103">Classe WmiMonitorListedSupportedSourceModes</span><span class="sxs-lookup"><span data-stu-id="2f09e-103">WmiMonitorListedSupportedSourceModes class</span></span>

<span data-ttu-id="2f09e-104">O **WmiMonitorListedSupportedSourceModes** lista os modos de origem com suporte para um monitor de vídeo em seu descritor de monitor, se existir algum.</span><span class="sxs-lookup"><span data-stu-id="2f09e-104">The **WmiMonitorListedSupportedSourceModes** lists the supported source modes for a video monitor in its monitor descriptor, if any exist.</span></span> <span data-ttu-id="2f09e-105">Para monitores que não têm nenhuma descrição, essa lista de modos é gerada com base no tipo de monitor, conforme especificado pelo driver do barramento do monitor.</span><span class="sxs-lookup"><span data-stu-id="2f09e-105">For monitors that have no description, this list of modes is generated based on the type of monitor, as specified by the monitor bus driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f09e-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f09e-106">Syntax</span></span>

``` syntax
class WmiMonitorListedSupportedSourceModes : MSMonitorClass
{
  boolean             Active;
  string              InstanceName;
  uint16              NumOfMonitorSourceModes;
  uint16              PreferredMonitorSourceModeIndex;
  VideoModeDescriptor MonitorSourceModes[];
};
```

## <a name="members"></a><span data-ttu-id="2f09e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2f09e-107">Members</span></span>

<span data-ttu-id="2f09e-108">A classe **WmiMonitorListedSupportedSourceModes** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2f09e-108">The **WmiMonitorListedSupportedSourceModes** class has these types of members:</span></span>

-   [<span data-ttu-id="2f09e-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f09e-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2f09e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2f09e-110">Properties</span></span>

<span data-ttu-id="2f09e-111">A classe **WmiMonitorListedSupportedSourceModes** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2f09e-111">The **WmiMonitorListedSupportedSourceModes** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2f09e-112">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="2f09e-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f09e-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2f09e-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2f09e-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f09e-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f09e-115">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="2f09e-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="2f09e-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="2f09e-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f09e-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2f09e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2f09e-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f09e-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2f09e-119">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="2f09e-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="2f09e-120">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="2f09e-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="2f09e-121">**MonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="2f09e-121">**MonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f09e-122">Tipo de dados: matriz **VideoModeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="2f09e-122">Data type: **VideoModeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="2f09e-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f09e-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f09e-124">Lista modos de origem do monitor representados por instâncias da classe [**VideoModeDescriptor**](videomodedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="2f09e-124">Lists monitor source modes represented by instances of the [**VideoModeDescriptor**](videomodedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="2f09e-125">**NumOfMonitorSourceModes**</span><span class="sxs-lookup"><span data-stu-id="2f09e-125">**NumOfMonitorSourceModes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f09e-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f09e-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f09e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f09e-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f09e-128">Número de modo de origem do monitor com suporte listado.</span><span class="sxs-lookup"><span data-stu-id="2f09e-128">Number of listed supported monitor source mode.</span></span>

</dd> <dt>

<span data-ttu-id="2f09e-129">**PreferredMonitorSourceModeIndex**</span><span class="sxs-lookup"><span data-stu-id="2f09e-129">**PreferredMonitorSourceModeIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2f09e-130">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="2f09e-130">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="2f09e-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2f09e-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2f09e-132">Índice de modo de origem do monitor preferencial.</span><span class="sxs-lookup"><span data-stu-id="2f09e-132">Preferred monitor source mode index.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2f09e-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f09e-133">Requirements</span></span>



| <span data-ttu-id="2f09e-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f09e-134">Requirement</span></span> | <span data-ttu-id="2f09e-135">Valor</span><span class="sxs-lookup"><span data-stu-id="2f09e-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f09e-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f09e-136">Minimum supported client</span></span><br/> | <span data-ttu-id="2f09e-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2f09e-137">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2f09e-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2f09e-138">Minimum supported server</span></span><br/> | <span data-ttu-id="2f09e-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2f09e-139">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2f09e-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="2f09e-140">Namespace</span></span><br/>                | <span data-ttu-id="2f09e-141">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="2f09e-141">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="2f09e-142">MOF</span><span class="sxs-lookup"><span data-stu-id="2f09e-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2f09e-143"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2f09e-143"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="2f09e-144">DLL</span><span class="sxs-lookup"><span data-stu-id="2f09e-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f09e-145"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f09e-145"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f09e-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="2f09e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f09e-147">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="2f09e-147">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




