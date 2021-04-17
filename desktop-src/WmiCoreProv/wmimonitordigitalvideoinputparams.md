---
description: Representa parâmetros de entrada para vídeo digital.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: Classe WmiMonitorDigitalVideoInputParams
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105791629"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="ff0ac-103">Classe WmiMonitorDigitalVideoInputParams</span><span class="sxs-lookup"><span data-stu-id="ff0ac-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="ff0ac-104">O **WmiMonitorDigitalVideoInputParams** representa parâmetros de entrada para vídeo digital.</span><span class="sxs-lookup"><span data-stu-id="ff0ac-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="ff0ac-105">Os dados nessa classe correspondem aos dados na definição de entrada de vídeo do padrão de dados de identificação de vídeo estendido (E-EDID) avançado de associação de vídeo de eletrônicos (VESA).</span><span class="sxs-lookup"><span data-stu-id="ff0ac-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="ff0ac-106">Uma instância dessa classe está disponível somente quando o valor da propriedade **VideoInputType** da classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) é "digital".</span><span class="sxs-lookup"><span data-stu-id="ff0ac-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="ff0ac-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ff0ac-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="ff0ac-108">Membros</span><span class="sxs-lookup"><span data-stu-id="ff0ac-108">Members</span></span>

<span data-ttu-id="ff0ac-109">A classe **WmiMonitorDigitalVideoInputParams** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ff0ac-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="ff0ac-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ff0ac-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ff0ac-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ff0ac-111">Properties</span></span>

<span data-ttu-id="ff0ac-112">A classe **WmiMonitorDigitalVideoInputParams** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ff0ac-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ff0ac-113">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff0ac-114">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff0ac-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ff0ac-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff0ac-116">Indica o monitor ativo.</span><span class="sxs-lookup"><span data-stu-id="ff0ac-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="ff0ac-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff0ac-118">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ff0ac-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ff0ac-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ff0ac-120">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ff0ac-121">Nome da instância de monitor específica.</span><span class="sxs-lookup"><span data-stu-id="ff0ac-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="ff0ac-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ff0ac-123">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ff0ac-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ff0ac-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ff0ac-125">VESA DFP 1. x ou compatível.</span><span class="sxs-lookup"><span data-stu-id="ff0ac-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="ff0ac-126">Se definido, a interface é compatível com sinal com tela plana digital VESA (DFP) 1. x transição de sinal diferencial minimizada (TMDS) CRGB, 1 pixel/relógio, até 8 bits/cor bit mais significativo (MSB) alinhado, DE alto para ativo.</span><span class="sxs-lookup"><span data-stu-id="ff0ac-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ff0ac-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff0ac-127">Requirements</span></span>



| <span data-ttu-id="ff0ac-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff0ac-128">Requirement</span></span> | <span data-ttu-id="ff0ac-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ff0ac-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff0ac-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff0ac-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff0ac-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff0ac-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ff0ac-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff0ac-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff0ac-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff0ac-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ff0ac-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="ff0ac-134">Namespace</span></span><br/>                | <span data-ttu-id="ff0ac-135">\\WMI raiz</span><span class="sxs-lookup"><span data-stu-id="ff0ac-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="ff0ac-136">MOF</span><span class="sxs-lookup"><span data-stu-id="ff0ac-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff0ac-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff0ac-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff0ac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ff0ac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff0ac-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff0ac-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff0ac-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff0ac-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff0ac-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="ff0ac-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




