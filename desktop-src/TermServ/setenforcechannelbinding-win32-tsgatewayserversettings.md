---
title: Método SetEnforceChannelBinding da classe Win32_TSGatewayServerSettings
description: Define a propriedade EnforceChannelBinding.
ms.assetid: 8bd64fe7-bad5-44e6-a309-10802d9a8bd4
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetEnforceChannelBinding
- Método SetEnforceChannelBinding Serviços de Área de Trabalho Remota, classe Win32_TSGatewayServerSettings
- Classe Win32_TSGatewayServerSettings Serviços de Área de Trabalho Remota, método SetEnforceChannelBinding
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.SetEnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b236341f0fdac31f80f7e7d77aa12a4b22eb9731
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499457"
---
# <a name="setenforcechannelbinding-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="923be-106">Método SetEnforceChannelBinding da classe Win32 \_ TSGatewayServerSettings</span><span class="sxs-lookup"><span data-stu-id="923be-106">SetEnforceChannelBinding method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="923be-107">Define a propriedade **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="923be-107">Sets the **EnforceChannelBinding** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="923be-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="923be-108">Syntax</span></span>


```mof
uint32 SetEnforceChannelBinding(
  [in] boolean EnforceChannelBinding
);
```



## <a name="parameters"></a><span data-ttu-id="923be-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="923be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="923be-110">*EnforceChannelBinding* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="923be-110">*EnforceChannelBinding* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="923be-111">Especifica o novo valor da propriedade **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="923be-111">Specifies the new **EnforceChannelBinding** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="923be-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="923be-112">Return value</span></span>

<span data-ttu-id="923be-113">Se o método tiver sucesso, ele retornará zero.</span><span class="sxs-lookup"><span data-stu-id="923be-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="923be-114">Se o método não for bem-sucedido, ele retornará um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="923be-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="923be-115">Para obter uma lista de códigos de erro, consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="923be-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="923be-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="923be-116">Requirements</span></span>



| <span data-ttu-id="923be-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="923be-117">Requirement</span></span> | <span data-ttu-id="923be-118">Valor</span><span class="sxs-lookup"><span data-stu-id="923be-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="923be-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="923be-119">Minimum supported client</span></span><br/> | <span data-ttu-id="923be-120">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="923be-120">None supported</span></span><br/>                                                                |
| <span data-ttu-id="923be-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="923be-121">Minimum supported server</span></span><br/> | <span data-ttu-id="923be-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="923be-122">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="923be-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="923be-123">Namespace</span></span><br/>                | <span data-ttu-id="923be-124">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="923be-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="923be-125">MOF</span><span class="sxs-lookup"><span data-stu-id="923be-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="923be-126"><dt>TS. mof</dt></span><span class="sxs-lookup"><span data-stu-id="923be-126"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="923be-127">DLL</span><span class="sxs-lookup"><span data-stu-id="923be-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="923be-128"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="923be-128"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="923be-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="923be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="923be-130">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="923be-130">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

 





