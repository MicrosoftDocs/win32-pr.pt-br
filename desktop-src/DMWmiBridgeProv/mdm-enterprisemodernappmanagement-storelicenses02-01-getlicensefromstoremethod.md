---
title: Método GetLicenseFromStoreMethod da classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
description: Método para obter uma licença da loja. Consulte também GetLicenseFromStore.
ms.assetid: 4cf8a979-60c1-4ec1-968e-5a90cc671ebf
keywords:
- Método GetLicenseFromStoreMethod
- Método GetLicenseFromStoreMethod, classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01
- Classe MDM_EnterpriseModernAppManagement_StoreLicenses02_01, método GetLicenseFromStoreMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_StoreLicenses02_01.GetLicenseFromStoreMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8751546bfb57e5c9bf34db97ee6b59dd7e1f580
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085987"
---
# <a name="getlicensefromstoremethod-method-of-the-mdm_enterprisemodernappmanagement_storelicenses02_01-class"></a><span data-ttu-id="7bd38-107">Método GetLicenseFromStoreMethod da classe MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01</span><span class="sxs-lookup"><span data-stu-id="7bd38-107">GetLicenseFromStoreMethod method of the MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01 class</span></span>

<span data-ttu-id="7bd38-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="7bd38-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7bd38-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="7bd38-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7bd38-110">Método para obter uma licença da loja.</span><span class="sxs-lookup"><span data-stu-id="7bd38-110">Method for getting a license from the store.</span></span> <span data-ttu-id="7bd38-111">Consulte também [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="7bd38-111">See also, [GetLicenseFromStore](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bd38-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7bd38-112">Syntax</span></span>


```mof
uint32 GetLicenseFromStoreMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="7bd38-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7bd38-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bd38-114">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7bd38-114">*param* \[in\]</span></span>
<span data-ttu-id="7bd38-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7bd38-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="7bd38-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bd38-116">Requirements</span></span>



| <span data-ttu-id="7bd38-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bd38-117">Requirement</span></span> | <span data-ttu-id="7bd38-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7bd38-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bd38-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bd38-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7bd38-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="7bd38-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7bd38-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7bd38-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7bd38-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7bd38-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7bd38-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7bd38-123">Namespace</span></span><br/>                | <span data-ttu-id="7bd38-124">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="7bd38-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7bd38-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7bd38-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bd38-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bd38-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bd38-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7bd38-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bd38-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bd38-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bd38-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="7bd38-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd38-130">**MDM \_ EnterpriseModernAppManagement \_ StoreLicenses02 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="7bd38-130">**MDM\_EnterpriseModernAppManagement\_StoreLicenses02\_01**</span></span>](mdm-enterprisemodernappmanagement-storelicenses02-01.md)
</dt> <dt>

[<span data-ttu-id="7bd38-131">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="7bd38-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

