---
title: Interface INapComponentConfig (NapCommon. h)
description: Fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema).
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- INapComponentConfig da interface NAP
- INapComponentConfig interface NAP, descrita
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369482"
---
# <a name="inapcomponentconfig-interface"></a><span data-ttu-id="ff69b-105">Interface INapComponentConfig</span><span class="sxs-lookup"><span data-stu-id="ff69b-105">INapComponentConfig interface</span></span>

> [!Note]  
> <span data-ttu-id="ff69b-106">A plataforma de proteção de acesso à rede não está disponível a partir do Windows 10</span><span class="sxs-lookup"><span data-stu-id="ff69b-106">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ff69b-107">A interface **INapComponentConfig** fornece métodos de configuração do sistema NAP para SHVs (validadores da integridade do sistema).</span><span class="sxs-lookup"><span data-stu-id="ff69b-107">The **INapComponentConfig** interface provides NAP system configuration methods for system health validators (SHVs).</span></span>

> [!Note]  
> <span data-ttu-id="ff69b-108">[**INapComponentConfig2**](inapcomponentconfig2.md) e [**INapComponentConfig3**](inapcomponentconfig3.md) herdam todos os métodos dessa interface e devem ser usados em seu lugar.</span><span class="sxs-lookup"><span data-stu-id="ff69b-108">[**INapComponentConfig2**](inapcomponentconfig2.md) and [**INapComponentConfig3**](inapcomponentconfig3.md) inherit all the methods of this interface and should be used instead.</span></span>

 

## <a name="members"></a><span data-ttu-id="ff69b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ff69b-109">Members</span></span>

<span data-ttu-id="ff69b-110">A interface **INapComponentConfig** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ff69b-110">The **INapComponentConfig** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ff69b-111">**INapComponentConfig** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ff69b-111">**INapComponentConfig** also has these types of members:</span></span>

-   [<span data-ttu-id="ff69b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff69b-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ff69b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ff69b-113">Methods</span></span>

<span data-ttu-id="ff69b-114">A interface **INapComponentConfig** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ff69b-114">The **INapComponentConfig** interface has these methods.</span></span>



| <span data-ttu-id="ff69b-115">Método</span><span class="sxs-lookup"><span data-stu-id="ff69b-115">Method</span></span>                                                                          | <span data-ttu-id="ff69b-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="ff69b-116">Description</span></span>                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff69b-117">**INapComponentConfig:: GetConfig**</span><span class="sxs-lookup"><span data-stu-id="ff69b-117">**INapComponentConfig::GetConfig**</span></span>](inapcomponentconfig-getconfig.md)         | <span data-ttu-id="ff69b-118">Recupera a configuração do componente SHV.</span><span class="sxs-lookup"><span data-stu-id="ff69b-118">Retrieves the SHV component configuration.</span></span><br/>                                |
| [<span data-ttu-id="ff69b-119">**INapComponentConfig::InvokeUI**</span><span class="sxs-lookup"><span data-stu-id="ff69b-119">**INapComponentConfig::InvokeUI**</span></span>](inapcomponentconfig-invokeui.md)           | <span data-ttu-id="ff69b-120">Inicia a interface do usuário personalizada para um componente SHV.</span><span class="sxs-lookup"><span data-stu-id="ff69b-120">Launches the customized user interface for an SHV component.</span></span><br/>              |
| [<span data-ttu-id="ff69b-121">**INapComponentConfig::IsUISupported**</span><span class="sxs-lookup"><span data-stu-id="ff69b-121">**INapComponentConfig::IsUISupported**</span></span>](inapcomponentconfig-isuisupported.md) | <span data-ttu-id="ff69b-122">Especifica se o componente SHV dá suporte a uma interface do usuário personalizada.</span><span class="sxs-lookup"><span data-stu-id="ff69b-122">Specifies whether the SHV component supports a customized user interface.</span></span><br/> |
| [<span data-ttu-id="ff69b-123">**INapComponentConfig:: setconfig**</span><span class="sxs-lookup"><span data-stu-id="ff69b-123">**INapComponentConfig::SetConfig**</span></span>](inapcomponentconfig-setconfig.md)         | <span data-ttu-id="ff69b-124">Define a configuração do componente SHV.</span><span class="sxs-lookup"><span data-stu-id="ff69b-124">Sets the SHV component configuration.</span></span><br/>                                     |



 

## <a name="remarks"></a><span data-ttu-id="ff69b-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff69b-125">Remarks</span></span>

<span data-ttu-id="ff69b-126">Essa interface não deve ser implementada por agentes de integridade do sistema (SHAs) ou clientes de imposição de quarentena (QECs).</span><span class="sxs-lookup"><span data-stu-id="ff69b-126">This interface should not be implemented by system health agents (SHAs) or quarantine enforcement clients (QECs).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff69b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff69b-127">Requirements</span></span>



| <span data-ttu-id="ff69b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff69b-128">Requirement</span></span> | <span data-ttu-id="ff69b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ff69b-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff69b-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff69b-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff69b-131">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ff69b-131">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ff69b-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ff69b-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff69b-133">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ff69b-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ff69b-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ff69b-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff69b-135"><dt>NapCommon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ff69b-135"><dt>NapCommon.h</dt></span></span> </dl>   |
| <span data-ttu-id="ff69b-136">INSERI</span><span class="sxs-lookup"><span data-stu-id="ff69b-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ff69b-137"><dt>NapCommon. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ff69b-137"><dt>NapCommon.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff69b-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff69b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff69b-139">Interfaces NAP</span><span class="sxs-lookup"><span data-stu-id="ff69b-139">NAP Interfaces</span></span>](nap-interfaces.md)
</dt> <dt>

[<span data-ttu-id="ff69b-140">Referência de NAP</span><span class="sxs-lookup"><span data-stu-id="ff69b-140">NAP Reference</span></span>](nap-reference.md)
</dt> </dl>

 

