---
title: Método VerifyHealthMethod da classe MDM_HealthAttestation
description: Método para notificar o dispositivo para preparar uma solicitação de verificação de certificado de integridade. Consulte também VerifyHealth.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Método VerifyHealthMethod
- Método VerifyHealthMethod, classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, método VerifyHealthMethod
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769021"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a><span data-ttu-id="c0522-107">Método VerifyHealthMethod da classe MDM \_ HealthAttestation</span><span class="sxs-lookup"><span data-stu-id="c0522-107">VerifyHealthMethod method of the MDM\_HealthAttestation class</span></span>

<span data-ttu-id="c0522-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="c0522-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c0522-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="c0522-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c0522-110">Método para notificar o dispositivo para preparar uma solicitação de verificação de certificado de integridade.</span><span class="sxs-lookup"><span data-stu-id="c0522-110">Method to notify the device to prepare a health certificate verification request.</span></span> <span data-ttu-id="c0522-111">Consulte também [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span><span class="sxs-lookup"><span data-stu-id="c0522-111">See also, [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0522-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0522-112">Syntax</span></span>


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a><span data-ttu-id="c0522-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0522-113">Parameters</span></span>

<span data-ttu-id="c0522-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c0522-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0522-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0522-115">Requirements</span></span>



| <span data-ttu-id="c0522-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0522-116">Requirement</span></span> | <span data-ttu-id="c0522-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c0522-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0522-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0522-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c0522-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="c0522-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c0522-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0522-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c0522-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c0522-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c0522-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c0522-122">Namespace</span></span><br/>                | <span data-ttu-id="c0522-123">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="c0522-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c0522-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c0522-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0522-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0522-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c0522-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c0522-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0522-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0522-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0522-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0522-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0522-129">**\_HEALTHATTESTATION MDM**</span><span class="sxs-lookup"><span data-stu-id="c0522-129">**MDM\_HealthAttestation**</span></span>](mdm-healthattestation.md)
</dt> <dt>

[<span data-ttu-id="c0522-130">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="c0522-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

