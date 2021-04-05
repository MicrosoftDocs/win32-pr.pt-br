---
title: Método CheckApplicabilityMethod da classe MDM_WindowsLicensing
description: Verifica se a chave do produto (Product Key) inserida pode ser usada para uma atualização de edição, ativação ou alteração de uma chave de produto do Windows 10 para dispositivos de desktop. Consulte também CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Método CheckApplicabilityMethod
- Método CheckApplicabilityMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, método CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085976"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="def8e-107">Método CheckApplicabilityMethod da classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="def8e-107">CheckApplicabilityMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="def8e-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="def8e-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="def8e-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="def8e-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="def8e-110">Verifica se a chave do produto (Product Key) inserida pode ser usada para uma atualização de edição, ativação ou alteração de uma chave de produto do Windows 10 para dispositivos de desktop.</span><span class="sxs-lookup"><span data-stu-id="def8e-110">Checks if the entered product key can be used for an edition upgrade, activation or changing a product key of Windows 10 for desktop devices.</span></span> <span data-ttu-id="def8e-111">Consulte também [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="def8e-111">See also, [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="def8e-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="def8e-112">Syntax</span></span>


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="def8e-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="def8e-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="def8e-114">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="def8e-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="def8e-115">A chave do produto.</span><span class="sxs-lookup"><span data-stu-id="def8e-115">The product key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="def8e-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="def8e-116">Return value</span></span>

<span data-ttu-id="def8e-117">TRUE ou FALSE</span><span class="sxs-lookup"><span data-stu-id="def8e-117">TRUE or FALSE</span></span>

## <a name="requirements"></a><span data-ttu-id="def8e-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="def8e-118">Requirements</span></span>



| <span data-ttu-id="def8e-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="def8e-119">Requirement</span></span> | <span data-ttu-id="def8e-120">Valor</span><span class="sxs-lookup"><span data-stu-id="def8e-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="def8e-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def8e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="def8e-122">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="def8e-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="def8e-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="def8e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="def8e-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="def8e-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="def8e-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="def8e-125">Namespace</span></span><br/>                | <span data-ttu-id="def8e-126">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="def8e-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="def8e-127">MOF</span><span class="sxs-lookup"><span data-stu-id="def8e-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="def8e-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="def8e-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="def8e-129">DLL</span><span class="sxs-lookup"><span data-stu-id="def8e-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="def8e-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="def8e-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="def8e-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="def8e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="def8e-132">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="def8e-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="def8e-133">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="def8e-133">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

