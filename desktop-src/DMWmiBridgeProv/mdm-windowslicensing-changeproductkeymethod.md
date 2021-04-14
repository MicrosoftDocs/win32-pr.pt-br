---
title: Método ChangeProductKeyMethod da classe MDM_WindowsLicensing
description: Esse método instala uma chave do produto para dispositivos Windows 10 desktop. Ponto não reinicializado. Consulte também ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Método ChangeProductKeyMethod
- Método ChangeProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, método ChangeProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455589"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a><span data-ttu-id="11872-108">Método ChangeProductKeyMethod da classe MDM \_ WindowsLicensing</span><span class="sxs-lookup"><span data-stu-id="11872-108">ChangeProductKeyMethod method of the MDM\_WindowsLicensing class</span></span>

<span data-ttu-id="11872-109">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="11872-109">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="11872-110">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="11872-110">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="11872-111">Esse método instala uma chave do produto para dispositivos Windows 10 desktop.</span><span class="sxs-lookup"><span data-stu-id="11872-111">This method installs a product key for Windows 10 desktop devices.</span></span> <span data-ttu-id="11872-112">Ponto não reinicializado.</span><span class="sxs-lookup"><span data-stu-id="11872-112">Dot not reboot.</span></span> <span data-ttu-id="11872-113">Confira também [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span><span class="sxs-lookup"><span data-stu-id="11872-113">See also [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)</span></span>

## <a name="syntax"></a><span data-ttu-id="11872-114">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="11872-114">Syntax</span></span>


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="11872-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="11872-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11872-116">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="11872-116">*param* \[in\]</span></span>
<span data-ttu-id="11872-117"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="11872-117"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="11872-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11872-118">Requirements</span></span>



| <span data-ttu-id="11872-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="11872-119">Requirement</span></span> | <span data-ttu-id="11872-120">Valor</span><span class="sxs-lookup"><span data-stu-id="11872-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11872-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11872-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11872-122">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="11872-122">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="11872-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="11872-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11872-124">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="11872-124">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="11872-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="11872-125">Namespace</span></span><br/>                | <span data-ttu-id="11872-126">\\Dmmap de \\ MDM \\ cimv2 raiz</span><span class="sxs-lookup"><span data-stu-id="11872-126">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="11872-127">MOF</span><span class="sxs-lookup"><span data-stu-id="11872-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="11872-128"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="11872-128"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="11872-129">DLL</span><span class="sxs-lookup"><span data-stu-id="11872-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11872-130"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11872-130"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11872-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="11872-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11872-132">**\_WINDOWSLICENSING MDM**</span><span class="sxs-lookup"><span data-stu-id="11872-132">**MDM\_WindowsLicensing**</span></span>](mdm-windowslicensing.md)
</dt> </dl>

 

