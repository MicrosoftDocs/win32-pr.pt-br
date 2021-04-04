---
title: Método RebootNowMethod da classe MDM_Reboot
description: Esse método executa uma reinicialização do dispositivo.
ms.assetid: b1bacad8-06db-4e56-9f3d-46c9a0036729
keywords:
- Método RebootNowMethod
- Método RebootNowMethod, classe MDM_Reboot
- Classe MDM_Reboot, método RebootNowMethod
topic_type:
- apiref
api_name:
- MDM_Reboot.RebootNowMethod
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d35d297858588ade6655ea84876c6e75abd719
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085204"
---
# <a name="rebootnowmethod-method-of-the-mdm_reboot-class"></a><span data-ttu-id="603cf-106">Método RebootNowMethod da classe MDM \_ reboot</span><span class="sxs-lookup"><span data-stu-id="603cf-106">RebootNowMethod method of the MDM\_Reboot class</span></span>

<span data-ttu-id="603cf-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="603cf-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="603cf-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="603cf-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="603cf-109">Esse método executa uma reinicialização do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="603cf-109">This method executes a reboot of the device.</span></span> <span data-ttu-id="603cf-110">Consulte também [RebootNow](/windows/client-management/mdm/reboot-csp).</span><span class="sxs-lookup"><span data-stu-id="603cf-110">See also, [RebootNow](/windows/client-management/mdm/reboot-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="603cf-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="603cf-111">Syntax</span></span>


```mof
uint32 RebootNowMethod();
```



## <a name="parameters"></a><span data-ttu-id="603cf-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="603cf-112">Parameters</span></span>

<span data-ttu-id="603cf-113">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="603cf-113">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="603cf-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="603cf-114">Requirements</span></span>



| <span data-ttu-id="603cf-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="603cf-115">Requirement</span></span> | <span data-ttu-id="603cf-116">Valor</span><span class="sxs-lookup"><span data-stu-id="603cf-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="603cf-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="603cf-117">Minimum supported client</span></span><br/> | <span data-ttu-id="603cf-118">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="603cf-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="603cf-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="603cf-119">Minimum supported server</span></span><br/> | <span data-ttu-id="603cf-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="603cf-120">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="603cf-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="603cf-121">Namespace</span></span><br/>                | <span data-ttu-id="603cf-122">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="603cf-122">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="603cf-123">MOF</span><span class="sxs-lookup"><span data-stu-id="603cf-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="603cf-124"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="603cf-124"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl>      |
| <span data-ttu-id="603cf-125">DLL</span><span class="sxs-lookup"><span data-stu-id="603cf-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="603cf-126"><dt>\\DMWmiBridgeProv.dllMOFs</dt></span><span class="sxs-lookup"><span data-stu-id="603cf-126"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="603cf-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="603cf-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="603cf-128">**Reinicialização do MDM \_**</span><span class="sxs-lookup"><span data-stu-id="603cf-128">**MDM\_Reboot**</span></span>](mdm-reboot.md)
</dt> </dl>

 

