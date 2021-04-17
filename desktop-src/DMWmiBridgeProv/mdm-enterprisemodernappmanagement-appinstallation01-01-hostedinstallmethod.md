---
title: Método HostedInstallMethod da classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
description: Método para executar uma instalação de um pacote de aplicativo de um local hospedado, como uma unidade local, uma UNC ou uma fonte de dados HTTPS. Consulte também HostedInstall.
ms.assetid: 1ec16315-75ce-4613-804e-6b587c4071d6
keywords:
- Método HostedInstallMethod
- Método HostedInstallMethod, classe MDM_EnterpriseModernAppManagement_AppInstallation01_01
- Classe MDM_EnterpriseModernAppManagement_AppInstallation01_01, método HostedInstallMethod
topic_type:
- apiref
api_name:
- MDM_EnterpriseModernAppManagement_AppInstallation01_01.HostedInstallMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9597f748a2b5695fd2703f187cfe50db7ad0aa85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753559"
---
# <a name="hostedinstallmethod-method-of-the-mdm_enterprisemodernappmanagement_appinstallation01_01-class"></a><span data-ttu-id="2102f-107">Método HostedInstallMethod da classe MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01</span><span class="sxs-lookup"><span data-stu-id="2102f-107">HostedInstallMethod method of the MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01 class</span></span>

<span data-ttu-id="2102f-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2102f-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2102f-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2102f-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2102f-110">Método para executar uma instalação de um pacote de aplicativo de um local hospedado, como uma unidade local, uma UNC ou uma fonte de dados HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2102f-110">Method to perform an install of an app package from a hosted location, such as a local drive, a UNC, or HTTPS data source.</span></span> <span data-ttu-id="2102f-111">Consulte também [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span><span class="sxs-lookup"><span data-stu-id="2102f-111">See also, [HostedInstall](/windows/client-management/mdm/enterprisemodernappmanagement-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="2102f-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2102f-112">Syntax</span></span>


```mof
uint32 HostedInstallMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="2102f-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2102f-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2102f-114">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2102f-114">*param* \[in\]</span></span>
<span data-ttu-id="2102f-115"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2102f-115"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2102f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2102f-116">Requirements</span></span>



| <span data-ttu-id="2102f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="2102f-117">Requirement</span></span> | <span data-ttu-id="2102f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="2102f-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2102f-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2102f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2102f-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2102f-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2102f-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2102f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2102f-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2102f-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2102f-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="2102f-123">Namespace</span></span><br/>                | <span data-ttu-id="2102f-124">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2102f-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="2102f-125">MOF</span><span class="sxs-lookup"><span data-stu-id="2102f-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2102f-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2102f-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2102f-127">DLL</span><span class="sxs-lookup"><span data-stu-id="2102f-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2102f-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2102f-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2102f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="2102f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2102f-130">**MDM \_ EnterpriseModernAppManagement \_ AppInstallation01 \_ 01**</span><span class="sxs-lookup"><span data-stu-id="2102f-130">**MDM\_EnterpriseModernAppManagement\_AppInstallation01\_01**</span></span>](mdm-enterprisemodernappmanagement-appinstallation01-01.md)
</dt> <dt>

[<span data-ttu-id="2102f-131">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="2102f-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

