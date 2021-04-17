---
title: Método SetVirtualIPMode da classe Win32_TSVirtualIP
description: Define o valor da propriedade VirtualIPMode.
ms.assetid: d4b39566-ad2a-493b-8022-c006a857043d
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota do método SetVirtualIPMode
- Método SetVirtualIPMode Serviços de Área de Trabalho Remota, classe Win32_TSVirtualIP
- Classe Win32_TSVirtualIP Serviços de Área de Trabalho Remota, método SetVirtualIPMode
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.SetVirtualIPMode
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 250633f5d41f5a4a7cb06a17ba9ae45bb444a018
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105780097"
---
# <a name="setvirtualipmode-method-of-the-win32_tsvirtualip-class"></a><span data-ttu-id="1c652-106">Método SetVirtualIPMode da classe Win32 \_ TSVirtualIP</span><span class="sxs-lookup"><span data-stu-id="1c652-106">SetVirtualIPMode method of the Win32\_TSVirtualIP class</span></span>

<span data-ttu-id="1c652-107">Define o valor da propriedade **VirtualIPMode** .</span><span class="sxs-lookup"><span data-stu-id="1c652-107">Sets the **VirtualIPMode** property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c652-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c652-108">Syntax</span></span>


```mof
uint32 SetVirtualIPMode(
  [in] uint32 VirtualIPMode
);
```



## <a name="parameters"></a><span data-ttu-id="1c652-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c652-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c652-110">*VirtualIPMode* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1c652-110">*VirtualIPMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c652-111">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c652-111">Type: **uint32**</span></span>

<span data-ttu-id="1c652-112">Especifica qual modo de virtualização de IP está sendo usado no servidor.</span><span class="sxs-lookup"><span data-stu-id="1c652-112">Specifies which IP virtualization mode is being used on the server.</span></span> <span data-ttu-id="1c652-113">Isso pode ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="1c652-113">This can be one of the following values.</span></span>

<dt>

<span data-ttu-id="1c652-114">0</span><span class="sxs-lookup"><span data-stu-id="1c652-114">0</span></span>
</dt> <dd>

<span data-ttu-id="1c652-115">O modo de virtualização de IP é por sessão.</span><span class="sxs-lookup"><span data-stu-id="1c652-115">The IP virtualization mode is per-session.</span></span>

</dd> <dt>

<span data-ttu-id="1c652-116">1</span><span class="sxs-lookup"><span data-stu-id="1c652-116">1</span></span>
</dt> <dd>

<span data-ttu-id="1c652-117">O modo de virtualização de IP é por usuário.</span><span class="sxs-lookup"><span data-stu-id="1c652-117">The IP virtualization mode is per-user.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c652-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1c652-118">Return value</span></span>

<span data-ttu-id="1c652-119">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1c652-119">Type: **uint32**</span></span>

<span data-ttu-id="1c652-120">Retorna 0 em caso de êxito; caso contrário, retorna um código de erro WMI.</span><span class="sxs-lookup"><span data-stu-id="1c652-120">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="1c652-121">Consulte [serviços de área de trabalho remota códigos de erro do provedor WMI](terminal-services-wmi-provider-error-codes.md) para obter uma lista desses valores.</span><span class="sxs-lookup"><span data-stu-id="1c652-121">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="1c652-122">O método retornará um erro se a configuração estiver sob controle de diretiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="1c652-122">The method returns an error if the setting is under group policy control.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c652-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c652-123">Requirements</span></span>



| <span data-ttu-id="1c652-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c652-124">Requirement</span></span> | <span data-ttu-id="1c652-125">Valor</span><span class="sxs-lookup"><span data-stu-id="1c652-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c652-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c652-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1c652-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="1c652-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1c652-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1c652-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1c652-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="1c652-129">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="1c652-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c652-130">Namespace</span></span><br/>                | <span data-ttu-id="1c652-131">\\TerminalServices da CIMv2 raiz \\</span><span class="sxs-lookup"><span data-stu-id="1c652-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1c652-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1c652-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1c652-133"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1c652-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1c652-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1c652-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c652-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c652-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c652-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c652-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c652-137">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="1c652-137">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

 





