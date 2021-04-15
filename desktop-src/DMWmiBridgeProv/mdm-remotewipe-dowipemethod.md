---
title: método doWipeMethod da classe MDM_RemoteWipe
description: Dispara o dispositivo para iniciar o apagamento remoto.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- método doWipeMethod
- método doWipeMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, método doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454669"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a><span data-ttu-id="2ebdc-106">método doWipeMethod da classe MDM \_ RemoteWipe</span><span class="sxs-lookup"><span data-stu-id="2ebdc-106">doWipeMethod method of the MDM\_RemoteWipe class</span></span>

<span data-ttu-id="2ebdc-107">\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente.</span><span class="sxs-lookup"><span data-stu-id="2ebdc-107">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2ebdc-108">A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]</span><span class="sxs-lookup"><span data-stu-id="2ebdc-108">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2ebdc-109">Dispara o dispositivo para iniciar o apagamento remoto.</span><span class="sxs-lookup"><span data-stu-id="2ebdc-109">Triggers the device to start the remote wipe.</span></span> <span data-ttu-id="2ebdc-110">Consulte também, [doborracha](/windows/client-management/mdm/remotewipe-csp).</span><span class="sxs-lookup"><span data-stu-id="2ebdc-110">See also, [doWipe](/windows/client-management/mdm/remotewipe-csp).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ebdc-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ebdc-111">Syntax</span></span>


```mof
uint32 doWipeMethod(
  [in] string param
);
```



## <a name="parameters"></a><span data-ttu-id="2ebdc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ebdc-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ebdc-113">*parâmetro* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ebdc-113">*param* \[in\]</span></span>
<span data-ttu-id="2ebdc-114"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="2ebdc-114"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="2ebdc-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ebdc-115">Requirements</span></span>



| <span data-ttu-id="2ebdc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ebdc-116">Requirement</span></span> | <span data-ttu-id="2ebdc-117">Valor</span><span class="sxs-lookup"><span data-stu-id="2ebdc-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ebdc-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ebdc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2ebdc-119">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="2ebdc-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ebdc-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ebdc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2ebdc-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="2ebdc-121">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="2ebdc-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ebdc-122">Namespace</span></span><br/>                | <span data-ttu-id="2ebdc-123">\\DMMap de \\ MDM \\ CIMv2 raiz</span><span class="sxs-lookup"><span data-stu-id="2ebdc-123">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="2ebdc-124">MOF</span><span class="sxs-lookup"><span data-stu-id="2ebdc-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ebdc-125"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ebdc-125"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ebdc-126">DLL</span><span class="sxs-lookup"><span data-stu-id="2ebdc-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ebdc-127"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ebdc-127"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ebdc-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ebdc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ebdc-129">**\_REMOTEWIPE MDM**</span><span class="sxs-lookup"><span data-stu-id="2ebdc-129">**MDM\_RemoteWipe**</span></span>](mdm-remotewipe.md)
</dt> <dt>

[<span data-ttu-id="2ebdc-130">Como usar os scripts do PowerShell com o provedor de ponte WMI</span><span class="sxs-lookup"><span data-stu-id="2ebdc-130">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

