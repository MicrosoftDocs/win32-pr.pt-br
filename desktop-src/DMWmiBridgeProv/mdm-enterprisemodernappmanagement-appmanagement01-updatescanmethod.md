---
title: Método UpdateScanMethod da classe MDM_EnterpriseModernAppManagement_AppManagement01
description: Método para iniciar a verificação de Windows Update. Consulte também UpdateScan.
ms.assetid: 61d17072-0fe5-4d5b-8e9e-fed536883ac9
keywords:
- Método UpdateScanMethod
- Método UpdateScanMethod, classe MDM_EnterpriseModernAppManagement_AppManagement01
- Classe MDM_EnterpriseModernAppManagement_AppManagement01, método UpdateScanMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppManagement01.UpdateScanMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af6cb5b744243b78f737ea44fbc27ef40708c6f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769022"
---
# <a name="updatescanmethod-method-of-the-mdm_enterprisemodernappmanagement_appmanagement01-class"></a><span data-ttu-id="dab28-107">Método UpdateScanMethod da \_ classe AppManagement01 do MDM EnterpriseModernAppManagement \_</span><span class="sxs-lookup"><span data-stu-id="dab28-107">UpdateScanMethod method of the MDM\_EnterpriseModernAppManagement\_AppManagement01 class</span></span>

<span data-ttu-id="dab28-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="dab28-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="dab28-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="dab28-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="dab28-110">Método para iniciar a verificação de Windows Update.</span><span class="sxs-lookup"><span data-stu-id="dab28-110">Method for starting the Windows Update scan.</span></span> <span data-ttu-id="dab28-111">Consulte também [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="dab28-111">See also, [UpdateScan](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="dab28-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dab28-112">Syntax</span></span>


```mof
uint32 UpdateScanMethod();
```



## <a name="parameters"></a><span data-ttu-id="dab28-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dab28-113">Parameters</span></span>

<span data-ttu-id="dab28-114">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dab28-114">This method has no parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="dab28-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dab28-115">Requirements</span></span>



| <span data-ttu-id="dab28-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dab28-116">Requirement</span></span> | <span data-ttu-id="dab28-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dab28-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dab28-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dab28-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dab28-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="dab28-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="dab28-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dab28-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dab28-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="dab28-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="dab28-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="dab28-122">Namespace</span></span><br/>                | <span data-ttu-id="dab28-123">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="dab28-123">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="dab28-124">MOF</span><span class="sxs-lookup"><span data-stu-id="dab28-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dab28-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dab28-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="dab28-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dab28-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dab28-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dab28-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab28-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="dab28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab28-129">**\_AppManagement01 ENTERPRISEMODERNAPPMANAGEMENT \_ MDM**</span><span class="sxs-lookup"><span data-stu-id="dab28-129">**MDM\_EnterpriseModernAppManagement\_AppManagement01**</span></span>](mdm-enterprisemodernappmanagement-appmanagement01.md)
</dt> <dt>

[<span data-ttu-id="dab28-130">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="dab28-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

