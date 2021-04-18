---
description: Lista os intervalos de frequência com suporte no monitor.
ms.assetid: e4713650-5f8c-4808-8b4f-1d29c54ab4e3
title: Classe WmiMonitorListedFrequencyRanges
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorListedFrequencyRanges
- WmiMonitorListedFrequencyRanges.Active
- WmiMonitorListedFrequencyRanges.InstanceName
- WmiMonitorListedFrequencyRanges.NumOfMonitorFreqRanges
- WmiMonitorListedFrequencyRanges.MonitorFreqRanges
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e13828f6d5e844147fc0b041617c8452c503ceef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793825"
---
# <a name="wmimonitorlistedfrequencyranges-class"></a><span data-ttu-id="03c85-103">Classe WmiMonitorListedFrequencyRanges</span><span class="sxs-lookup"><span data-stu-id="03c85-103">WmiMonitorListedFrequencyRanges class</span></span>

<span data-ttu-id="03c85-104">A classe WMI **WmiMonitorListedFrequencyRanges** lista os intervalos de frequência com suporte no monitor.</span><span class="sxs-lookup"><span data-stu-id="03c85-104">The **WmiMonitorListedFrequencyRanges** WMI class lists the frequency ranges supported by the monitor.</span></span> <span data-ttu-id="03c85-105">Esses intervalos são encontrados na definição de entrada de vídeo da VESA (vídeo Electronics Standard Association) Enhanced display de identificação de vídeo (E-EDID), ou no arquivo INF do Windows que contém dados de driver de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="03c85-105">These ranges are found in Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) block or in the Windows INF file that contains device driver data.</span></span>

## <a name="syntax"></a><span data-ttu-id="03c85-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="03c85-106">Syntax</span></span>

``` syntax
class WmiMonitorListedFrequencyRanges : MSMonitorClass
{
  boolean                  Active;
  string                   InstanceName;
  uint16                   NumOfMonitorFreqRanges;
  FrequencyRangeDescriptor MonitorFreqRanges[];
};
```

## <a name="members"></a><span data-ttu-id="03c85-107">Membros</span><span class="sxs-lookup"><span data-stu-id="03c85-107">Members</span></span>

<span data-ttu-id="03c85-108">A classe **WmiMonitorListedFrequencyRanges** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="03c85-108">The **WmiMonitorListedFrequencyRanges** class has these types of members:</span></span>

-   [<span data-ttu-id="03c85-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03c85-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="03c85-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="03c85-110">Properties</span></span>

<span data-ttu-id="03c85-111">A classe **WmiMonitorListedFrequencyRanges** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="03c85-111">The **WmiMonitorListedFrequencyRanges** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="03c85-112">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="03c85-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c85-113">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="03c85-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="03c85-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03c85-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03c85-115">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="03c85-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="03c85-116">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="03c85-116">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c85-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="03c85-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="03c85-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03c85-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="03c85-119">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="03c85-119">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="03c85-120">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="03c85-120">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="03c85-121">**MonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="03c85-121">**MonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c85-122">Tipo de dados: matriz **FrequencyRangeDescriptor**</span><span class="sxs-lookup"><span data-stu-id="03c85-122">Data type: **FrequencyRangeDescriptor** array</span></span>
</dt> <dt>

<span data-ttu-id="03c85-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03c85-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03c85-124">Lista de intervalos de frequência de monitor representados por instâncias da classe [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) .</span><span class="sxs-lookup"><span data-stu-id="03c85-124">List of monitor frequency ranges represented by instances of the [**FrequencyRangeDescriptor**](frequencyrangedescriptor.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="03c85-125">**NumOfMonitorFreqRanges**</span><span class="sxs-lookup"><span data-stu-id="03c85-125">**NumOfMonitorFreqRanges**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="03c85-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="03c85-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="03c85-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="03c85-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="03c85-128">Número de intervalos de frequência de monitor com suporte listados.</span><span class="sxs-lookup"><span data-stu-id="03c85-128">Number of listed supported monitor frequency ranges.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="03c85-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03c85-129">Requirements</span></span>



| <span data-ttu-id="03c85-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="03c85-130">Requirement</span></span> | <span data-ttu-id="03c85-131">Valor</span><span class="sxs-lookup"><span data-stu-id="03c85-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03c85-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03c85-132">Minimum supported client</span></span><br/> | <span data-ttu-id="03c85-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="03c85-133">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="03c85-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="03c85-134">Minimum supported server</span></span><br/> | <span data-ttu-id="03c85-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="03c85-135">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="03c85-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="03c85-136">Namespace</span></span><br/>                | <span data-ttu-id="03c85-137">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="03c85-137">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="03c85-138">MOF</span><span class="sxs-lookup"><span data-stu-id="03c85-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03c85-139"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="03c85-139"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="03c85-140">DLL</span><span class="sxs-lookup"><span data-stu-id="03c85-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03c85-141"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03c85-141"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03c85-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="03c85-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03c85-143">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="03c85-143">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




