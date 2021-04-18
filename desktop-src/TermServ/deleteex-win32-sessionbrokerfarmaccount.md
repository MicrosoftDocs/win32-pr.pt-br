---
title: Método DeleteEx da classe Win32_SessionBrokerFarmAccount
description: A \_ classe Win32 SessionBrokerFarmAccount não está mais disponível para uso a partir do Windows Server 2012. | Método DeleteEx da classe Win32_SessionBrokerFarmAccount
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método DeleteEx
- Método DeleteEx Serviços de Área de Trabalho Remota, classe Win32_SessionBrokerFarmAccount
- Classe Win32_SessionBrokerFarmAccount Serviços de Área de Trabalho Remota, método DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105810445"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a><span data-ttu-id="a7c0a-107">Método DeleteEx da classe Win32 \_ SessionBrokerFarmAccount</span><span class="sxs-lookup"><span data-stu-id="a7c0a-107">DeleteEx method of the Win32\_SessionBrokerFarmAccount class</span></span>

<span data-ttu-id="a7c0a-108">\[A classe [**Win32 \_ SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) não está mais disponível para uso a partir do Windows Server 2012.\]</span><span class="sxs-lookup"><span data-stu-id="a7c0a-108">\[The [**Win32\_SessionBrokerFarmAccount**](win32-sessionbrokerfarmaccount.md) class is no longer available for use as of Windows Server 2012.\]</span></span>

<span data-ttu-id="a7c0a-109">Exclui a conta do farm.</span><span class="sxs-lookup"><span data-stu-id="a7c0a-109">Deletes the farm account.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7c0a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7c0a-110">Syntax</span></span>


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a><span data-ttu-id="a7c0a-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7c0a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7c0a-112">*DeleteComputerObject* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a7c0a-112">*DeleteComputerObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7c0a-113">Indica se o objeto de computador associado ao farm deve ser removido da Active Directory.</span><span class="sxs-lookup"><span data-stu-id="a7c0a-113">Indicates whether the computer object associated with the farm is to be removed from Active Directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7c0a-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a7c0a-114">Return value</span></span>

<span data-ttu-id="a7c0a-115">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="a7c0a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a7c0a-116">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="a7c0a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7c0a-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7c0a-117">Requirements</span></span>



| <span data-ttu-id="a7c0a-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7c0a-118">Requirement</span></span> | <span data-ttu-id="a7c0a-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a7c0a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7c0a-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7c0a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a7c0a-121">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a7c0a-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a7c0a-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a7c0a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a7c0a-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7c0a-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="a7c0a-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a7c0a-124">End of client support</span></span><br/>    | <span data-ttu-id="a7c0a-125">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a7c0a-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a7c0a-126">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="a7c0a-126">End of server support</span></span><br/>    | <span data-ttu-id="a7c0a-127">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a7c0a-127">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="a7c0a-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="a7c0a-128">Namespace</span></span><br/>                | <span data-ttu-id="a7c0a-129">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="a7c0a-129">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="a7c0a-130">MOF</span><span class="sxs-lookup"><span data-stu-id="a7c0a-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a7c0a-131"><dt>TssdWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a7c0a-131"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a7c0a-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a7c0a-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7c0a-133"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7c0a-133"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7c0a-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7c0a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7c0a-135">**\_SessionBrokerFarmAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="a7c0a-135">**Win32\_SessionBrokerFarmAccount**</span></span>](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





