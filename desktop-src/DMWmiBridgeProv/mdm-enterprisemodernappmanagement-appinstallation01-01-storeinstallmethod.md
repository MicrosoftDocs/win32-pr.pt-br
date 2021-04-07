---
title: Método StoreInstallMethod da classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Método para executar uma instalação de um aplicativo e uma licença da Windows Store. Consulte também StoreInstall.
ms.assetid: 4f8aff47-ad16-4fe5-85be-7ddb55ddff24
keywords:
- Método StoreInstallMethod
- Método StoreInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, método StoreInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.StoreInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4ae34e8502b7d408a7fb4d96fb9c2c4fadb509
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918846"
---
# <a name="storeinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="0260c-107">Método StoreInstallMethod da classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="0260c-107">StoreInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="0260c-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="0260c-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0260c-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="0260c-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0260c-110">Método para executar uma instalação de um aplicativo e uma licença da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0260c-110">Method to perform an install of an app and a license from the Windows Store.</span></span> <span data-ttu-id="0260c-111">Consulte também [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="0260c-111">See also, [StoreInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="0260c-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0260c-112">Syntax</span></span>


```mof
uint32 StoreInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="0260c-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0260c-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0260c-114">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0260c-114">*param* \[in\]</span></span>
<span data-ttu-id="0260c-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0260c-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0260c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0260c-116">Requirements</span></span>



| <span data-ttu-id="0260c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0260c-117">Requirement</span></span> | <span data-ttu-id="0260c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0260c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0260c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0260c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0260c-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="0260c-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0260c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0260c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0260c-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="0260c-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0260c-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="0260c-123">Namespace</span></span><br/>                | <span data-ttu-id="0260c-124">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="0260c-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0260c-125">MOF</span><span class="sxs-lookup"><span data-stu-id="0260c-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0260c-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0260c-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0260c-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0260c-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0260c-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0260c-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0260c-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0260c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0260c-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="0260c-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="0260c-131">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="0260c-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

