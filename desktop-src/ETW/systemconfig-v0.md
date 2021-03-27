---
description: Essa classe é a classe pai para eventos de configuração de hardware. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: Classe SystemConfig_V0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827955"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="aa485-104">\_Classe SystemConfig V0</span><span class="sxs-lookup"><span data-stu-id="aa485-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="aa485-105">Essa classe é a classe pai para eventos de configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="aa485-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="aa485-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="aa485-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa485-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa485-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="aa485-108">Membros</span><span class="sxs-lookup"><span data-stu-id="aa485-108">Members</span></span>

<span data-ttu-id="aa485-109">A classe **SystemConfig \_ V0** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="aa485-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa485-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa485-110">Remarks</span></span>

<span data-ttu-id="aa485-111">Para eventos de configuração de hardware no Windows XP, consulte a classe [**HWConfig**](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="aa485-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa485-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa485-112">Requirements</span></span>



| <span data-ttu-id="aa485-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa485-113">Requirement</span></span> | <span data-ttu-id="aa485-114">Valor</span><span class="sxs-lookup"><span data-stu-id="aa485-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="aa485-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa485-115">Minimum supported client</span></span><br/> | <span data-ttu-id="aa485-116">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="aa485-116">None supported</span></span><br/>                            |
| <span data-ttu-id="aa485-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa485-117">Minimum supported server</span></span><br/> | <span data-ttu-id="aa485-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aa485-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="aa485-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa485-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa485-120">**MSNT \_ SystemTrace**</span><span class="sxs-lookup"><span data-stu-id="aa485-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="aa485-121">**SystemConfig**</span><span class="sxs-lookup"><span data-stu-id="aa485-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="aa485-122">**SystemConfig \_ V0 \_ CPU**</span><span class="sxs-lookup"><span data-stu-id="aa485-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="aa485-123">**SystemConfig \_ V0 \_ LogDisk**</span><span class="sxs-lookup"><span data-stu-id="aa485-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="aa485-124">**SystemConfig \_ V0 \_ NIC**</span><span class="sxs-lookup"><span data-stu-id="aa485-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="aa485-125">**SystemConfig \_ V0 \_ PhyDisk**</span><span class="sxs-lookup"><span data-stu-id="aa485-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="aa485-126">**SystemConfig \_ V0 \_ Power**</span><span class="sxs-lookup"><span data-stu-id="aa485-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="aa485-127">**SystemConfig \_ V0 \_ Services**</span><span class="sxs-lookup"><span data-stu-id="aa485-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="aa485-128">**Vídeo do SystemConfig \_ V0 \_**</span><span class="sxs-lookup"><span data-stu-id="aa485-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




