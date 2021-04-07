---
title: Método SetVirtualIPActive da classe Win32_TSVirtualIP
description: Define o valor da propriedade VirtualIPActive.
ms.assetid: e485aeb1-afdf-4572-bac7-daa80d903edc
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualIPActive
- Método SetVirtualIPActive Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SetVirtualIPActive
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPActive
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06534c967c5d86a7a19c060254b3b988ff98b17e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918645"
---
# <a name="setvirtualipactive-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="ec3cd-106">Método SetVirtualIPActive da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="ec3cd-106">SetVirtualIPActive method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="ec3cd-107">Define o valor da propriedade **VirtualIPActive** .</span><span class="sxs-lookup"><span data-stu-id="ec3cd-107">Sets the **VirtualIPActive** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec3cd-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ec3cd-108">Syntax</span></span>


```mof
uint32 SetVirtualIPActive(
  [in] uint32 VirtualIPActive
);
```



## <a name="parameters"></a><span data-ttu-id="ec3cd-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ec3cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec3cd-110">*VirtualIPActive* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ec3cd-110">*VirtualIPActive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec3cd-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec3cd-111">Type: **uint32**</span></span>

<span data-ttu-id="ec3cd-112">Especifica se a virtualização de IP está ativa no servidor.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-112">Specifies if IP virtualization is active on the server.</span></span> <span data-ttu-id="ec3cd-113">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="ec3cd-114">zero</span><span class="sxs-lookup"><span data-stu-id="ec3cd-114">zero</span></span>
</dt> <dd>

<span data-ttu-id="ec3cd-115">A virtualização de IP não está ativa.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-115">IP virtualization is not active.</span></span>

</dd> <dt>

<span data-ttu-id="ec3cd-116">diferente</span><span class="sxs-lookup"><span data-stu-id="ec3cd-116">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="ec3cd-117">A virtualização de IP está ativa.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-117">IP virtualization is active.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec3cd-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ec3cd-118">Return value</span></span>

<span data-ttu-id="ec3cd-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ec3cd-119">Type: **uint32**</span></span>

<span data-ttu-id="ec3cd-120">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ec3cd-121">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="ec3cd-122">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="ec3cd-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec3cd-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ec3cd-123">Requirements</span></span>



| <span data-ttu-id="ec3cd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ec3cd-124">Requirement</span></span> | <span data-ttu-id="ec3cd-125">Valor</span><span class="sxs-lookup"><span data-stu-id="ec3cd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec3cd-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec3cd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ec3cd-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ec3cd-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ec3cd-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ec3cd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ec3cd-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ec3cd-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ec3cd-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="ec3cd-130">Namespace</span></span><br/>                | <span data-ttu-id="ec3cd-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="ec3cd-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ec3cd-132">MOF</span><span class="sxs-lookup"><span data-stu-id="ec3cd-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec3cd-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec3cd-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec3cd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ec3cd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec3cd-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec3cd-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec3cd-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="ec3cd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec3cd-137">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="ec3cd-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





