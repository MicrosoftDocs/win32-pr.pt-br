---
title: Método SetVirtualizeLoopbackAddressesEnabled da classe Win32_TSVirtualIP
description: Define o valor da propriedade VirtualizeLoopbackAddressesEnabled.
ms.assetid: 84A4FF36-82B3-462A-9D2E-C15DD99524E4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualizeLoopbackAddressesEnabled
- Método SetVirtualizeLoopbackAddressesEnabled Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SetVirtualizeLoopbackAddressesEnabled
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualizeLoopbackAddressesEnabled
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed74e74a9f0fcbcd070a50743e6182649c2dca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753516"
---
# <a name="setvirtualizeloopbackaddressesenabled-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="7d52d-106">Método SetVirtualizeLoopbackAddressesEnabled da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="7d52d-106">SetVirtualizeLoopbackAddressesEnabled method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="7d52d-107">Define o valor da propriedade **VirtualizeLoopbackAddressesEnabled** .</span><span class="sxs-lookup"><span data-stu-id="7d52d-107">Sets the **VirtualizeLoopbackAddressesEnabled** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d52d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7d52d-108">Syntax</span></span>


```mof
uint32 SetVirtualizeLoopbackAddressesEnabled(
  [in] uint32 VirtualizeLoopbackAddressesEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="7d52d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7d52d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d52d-110">*VirtualizeLoopbackAddressesEnabled* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7d52d-110">*VirtualizeLoopbackAddressesEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7d52d-111">Especifica se a virtualização de endereço de loopback deve ser habilitada.</span><span class="sxs-lookup"><span data-stu-id="7d52d-111">Specifies whether to enable loopback address virtualization.</span></span> <span data-ttu-id="7d52d-112">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="7d52d-112">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="7d52d-113">0</span><span class="sxs-lookup"><span data-stu-id="7d52d-113">0</span></span>
</dt> <dd>

<span data-ttu-id="7d52d-114">Não habilite a virtualização de endereço de loopback.</span><span class="sxs-lookup"><span data-stu-id="7d52d-114">Do not enable loopback address virtualization.</span></span>

</dd> <dt>

<span data-ttu-id="7d52d-115">1</span><span class="sxs-lookup"><span data-stu-id="7d52d-115">1</span></span>
</dt> <dd>

<span data-ttu-id="7d52d-116">Habilite a virtualização de endereço de loopback.</span><span class="sxs-lookup"><span data-stu-id="7d52d-116">Enable loopback address virtualization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7d52d-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7d52d-117">Return value</span></span>

<span data-ttu-id="7d52d-118">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="7d52d-118">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7d52d-119">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="7d52d-119">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="7d52d-120">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="7d52d-120">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d52d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7d52d-121">Requirements</span></span>



| <span data-ttu-id="7d52d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="7d52d-122">Requirement</span></span> | <span data-ttu-id="7d52d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="7d52d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7d52d-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d52d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7d52d-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7d52d-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7d52d-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7d52d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7d52d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="7d52d-127">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="7d52d-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="7d52d-128">Namespace</span></span><br/>                | <span data-ttu-id="7d52d-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="7d52d-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="7d52d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="7d52d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7d52d-131"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7d52d-131"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7d52d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7d52d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7d52d-133"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7d52d-133"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d52d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7d52d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d52d-135">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="7d52d-135">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





