---
description: Contém o tipo de conexão do monitor.
ms.assetid: f5658246-fbb8-4530-8dfb-f1ca792fe9d5
title: Classe WmiMonitorConnectionParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorConnectionParams
- WmiMonitorConnectionParams.Active
- WmiMonitorConnectionParams.InstanceName
- WmiMonitorConnectionParams.VideoOutputTechnology
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a88b80773ec60b161df51fc759cc932d5c53c931
ms.sourcegitcommit: cfcac5a083b72fd7f2a5188166d470cc0e95d02d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/08/2021
ms.locfileid: "109626688"
---
# <a name="wmimonitorconnectionparams-class"></a><span data-ttu-id="7b616-103">Classe WmiMonitorConnectionParams</span><span class="sxs-lookup"><span data-stu-id="7b616-103">WmiMonitorConnectionParams class</span></span>

<span data-ttu-id="7b616-104">A classe WMI WmiMonitorConnectionParams contém o tipo de conexão do monitor.</span><span class="sxs-lookup"><span data-stu-id="7b616-104">The WmiMonitorConnectionParams WMI class contains the connection type of the monitor.</span></span>

<span data-ttu-id="7b616-105">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7b616-105">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b616-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7b616-106">Syntax</span></span>

``` syntax
class WmiMonitorConnectionParams
{
  boolean Active;
  string  InstanceName;
  uint32  VideoOutputTechnology;
};
```

## <a name="members"></a><span data-ttu-id="7b616-107">Membros</span><span class="sxs-lookup"><span data-stu-id="7b616-107">Members</span></span>

<span data-ttu-id="7b616-108">A classe **WmiMonitorConnectionParams** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7b616-108">The **WmiMonitorConnectionParams** class has these types of members:</span></span>

-   [<span data-ttu-id="7b616-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b616-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b616-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7b616-110">Properties</span></span>

<span data-ttu-id="7b616-111">A classe **WmiMonitorConnectionParams** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7b616-111">The **WmiMonitorConnectionParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7b616-112">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="7b616-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b616-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="7b616-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7b616-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b616-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b616-115">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="7b616-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7b616-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7b616-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b616-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="7b616-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7b616-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b616-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7b616-119">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="7b616-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7b616-120">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="7b616-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="7b616-121">**VideoOutputTechnology**</span><span class="sxs-lookup"><span data-stu-id="7b616-121">**VideoOutputTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7b616-122">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="7b616-122">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="7b616-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7b616-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7b616-124">Tipo de conexão de tecnologia de saída de vídeo.</span><span class="sxs-lookup"><span data-stu-id="7b616-124">Video output technology connection type.</span></span> <span data-ttu-id="7b616-125">Os valores válidos são documentados na enumeração de [ \_ tecnologia de \_ saída \_ de vídeo D3DKMDT](/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology) .</span><span class="sxs-lookup"><span data-stu-id="7b616-125">Valid values are documented in the [D3DKMDT\_VIDEO\_OUTPUT\_TECHNOLOGY](/windows-hardware/drivers/ddi/d3dkmdt/ne-d3dkmdt-_d3dkmdt_video_output_technology) enumeration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b616-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b616-126">Requirements</span></span>



| <span data-ttu-id="7b616-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b616-127">Requirement</span></span> | <span data-ttu-id="7b616-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7b616-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b616-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b616-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7b616-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7b616-130">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7b616-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7b616-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7b616-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7b616-132">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7b616-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b616-133">Namespace</span></span><br/>                | <span data-ttu-id="7b616-134">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="7b616-134">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7b616-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7b616-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7b616-136"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7b616-136"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7b616-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7b616-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b616-138"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b616-138"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b616-139">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7b616-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b616-140">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="7b616-140">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




