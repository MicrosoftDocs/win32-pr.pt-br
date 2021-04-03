---
title: Método UpgradeEditionWithLicenseMethod da classe MDM_WindowsLicensing
description: Método para fornecer uma licença para uma atualização de edição de dispositivos Windows 10 Mobile. Consulte também UpgradeEditionWithLicense.
ms.assetid: 1a57fb71-eea6-41bf-bc44-6d3a816096a4
keywords:
- Método UpgradeEditionWithLicenseMethod
- Método UpgradeEditionWithLicenseMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, método UpgradeEditionWithLicenseMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithLicenseMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b336ee4128aa520ecd463c3607254526c7c3dc7d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918836"
---
# <a name="upgradeeditionwithlicensemethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="fc005-107">Método UpgradeEditionWithLicenseMethod da classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="fc005-107">UpgradeEditionWithLicenseMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="fc005-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="fc005-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="fc005-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="fc005-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="fc005-110">Método para fornecer uma licença para uma atualização de edição de dispositivos Windows 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="fc005-110">Method for providing a license for an edition upgrade of Windows 10 mobile devices.</span></span> <span data-ttu-id="fc005-111">Consulte também [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="fc005-111">See also, [UpgradeEditionWithLicense](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc005-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fc005-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithLicenseMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="fc005-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fc005-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc005-114">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fc005-114">*param* \[in\]</span></span>
<span data-ttu-id="fc005-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="fc005-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="fc005-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc005-116">Requirements</span></span>



| <span data-ttu-id="fc005-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc005-117">Requirement</span></span> | <span data-ttu-id="fc005-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fc005-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc005-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc005-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fc005-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="fc005-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fc005-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fc005-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fc005-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="fc005-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="fc005-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc005-123">Namespace</span></span><br/>                | <span data-ttu-id="fc005-124">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="fc005-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="fc005-125">MOF</span><span class="sxs-lookup"><span data-stu-id="fc005-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc005-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc005-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc005-127">DLL</span><span class="sxs-lookup"><span data-stu-id="fc005-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc005-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc005-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc005-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="fc005-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc005-130">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="fc005-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="fc005-131">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="fc005-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

