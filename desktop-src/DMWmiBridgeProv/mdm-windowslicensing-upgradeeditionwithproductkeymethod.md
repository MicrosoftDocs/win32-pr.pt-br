---
title: Método UpgradeEditionWithProductKeyMethod da classe MDM_WindowsLicensing
description: Insere uma chave do produto (Product Key) para uma atualização de edição de dispositivos Windows 10 desktop. Consulte também UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Método UpgradeEditionWithProductKeyMethod
- Método UpgradeEditionWithProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, método UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85824fc6fac9e5a15bf2bc890215afcbd0958680
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455588"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="15ee6-107">Método UpgradeEditionWithProductKeyMethod da classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="15ee6-107">UpgradeEditionWithProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="15ee6-108">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="15ee6-108">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="15ee6-109">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="15ee6-109">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="15ee6-110">Insere uma chave do produto (Product Key) para uma atualização de edição de dispositivos Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="15ee6-110">Enters a product key for an edition upgrade of Windows 10 desktop devices.</span></span> <span data-ttu-id="15ee6-111">Consulte também [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span><span class="sxs-lookup"><span data-stu-id="15ee6-111">See also, [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="15ee6-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15ee6-112">Syntax</span></span>


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="15ee6-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15ee6-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15ee6-114">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="15ee6-114">*param* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15ee6-115">A chave do produto.</span><span class="sxs-lookup"><span data-stu-id="15ee6-115">The product key.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="15ee6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15ee6-116">Requirements</span></span>



| <span data-ttu-id="15ee6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="15ee6-117">Requirement</span></span> | <span data-ttu-id="15ee6-118">Valor</span><span class="sxs-lookup"><span data-stu-id="15ee6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15ee6-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15ee6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="15ee6-120">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="15ee6-120">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="15ee6-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15ee6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="15ee6-122">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="15ee6-122">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="15ee6-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="15ee6-123">Namespace</span></span><br/>                | <span data-ttu-id="15ee6-124">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="15ee6-124">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="15ee6-125">MOF</span><span class="sxs-lookup"><span data-stu-id="15ee6-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15ee6-126"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="15ee6-126"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="15ee6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="15ee6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15ee6-128"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15ee6-128"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15ee6-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="15ee6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15ee6-130">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="15ee6-130">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> <dt>

[<span data-ttu-id="15ee6-131">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="15ee6-131">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

