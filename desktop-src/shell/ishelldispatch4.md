---
description: Estende o objeto IShellDispatch3.
title: Objeto IShellDispatch4 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch4
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4fe37e38-ee71-41f0-b620-35fdc18f9dbb
ms.openlocfilehash: daec9c922a0bac05154c1108f236ddf336a2e380
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843057"
---
# <a name="ishelldispatch4-object"></a><span data-ttu-id="116d3-103">Objeto IShellDispatch4</span><span class="sxs-lookup"><span data-stu-id="116d3-103">IShellDispatch4 object</span></span>

<span data-ttu-id="116d3-104">Estende o objeto [**IShellDispatch3**](ishelldispatch3.md) .</span><span class="sxs-lookup"><span data-stu-id="116d3-104">Extends the [**IShellDispatch3**](ishelldispatch3.md) object.</span></span> <span data-ttu-id="116d3-105">Além das propriedades e métodos com suporte do **IShellDispatch3**, o **IShellDispatch4** dá suporte a quatro métodos adicionais.</span><span class="sxs-lookup"><span data-stu-id="116d3-105">In addition to the properties and methods supported by **IShellDispatch3**, **IShellDispatch4** supports four additional methods.</span></span>

> [!Note]  
> <span data-ttu-id="116d3-106">**IShellDispatch4** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="116d3-106">**IShellDispatch4** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="116d3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="116d3-107">Members</span></span>

<span data-ttu-id="116d3-108">O objeto **IShellDispatch4** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="116d3-108">The **IShellDispatch4** object has these types of members:</span></span>

-   [<span data-ttu-id="116d3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="116d3-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="116d3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="116d3-110">Methods</span></span>

<span data-ttu-id="116d3-111">O objeto **IShellDispatch4** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="116d3-111">The **IShellDispatch4** object has these methods.</span></span>



| <span data-ttu-id="116d3-112">Método</span><span class="sxs-lookup"><span data-stu-id="116d3-112">Method</span></span>                                                     | <span data-ttu-id="116d3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="116d3-113">Description</span></span>                                                         |
|:-----------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="116d3-114">**ExplorerPolicy**</span><span class="sxs-lookup"><span data-stu-id="116d3-114">**ExplorerPolicy**</span></span>](ishelldispatch4-explorerpolicy.md)   | <span data-ttu-id="116d3-115">Obtém o valor de uma política especificada do Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="116d3-115">Gets the value for a specified Internet Explorer policy.</span></span><br/> |
| [<span data-ttu-id="116d3-116">**GetDefinition**</span><span class="sxs-lookup"><span data-stu-id="116d3-116">**GetSetting**</span></span>](ishelldispatch4-getsetting.md)           | <span data-ttu-id="116d3-117">Recupera uma configuração de shell global.</span><span class="sxs-lookup"><span data-stu-id="116d3-117">Retrieves a global Shell setting.</span></span><br/>                        |
| [<span data-ttu-id="116d3-118">**ToggleDesktop**</span><span class="sxs-lookup"><span data-stu-id="116d3-118">**ToggleDesktop**</span></span>](ishelldispatch4-toggledesktop.md)     | <span data-ttu-id="116d3-119">Exibe ou oculta a área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="116d3-119">Displays or hides the desktop.</span></span><br/>                           |
| [<span data-ttu-id="116d3-120">**WindowsSecurity**</span><span class="sxs-lookup"><span data-stu-id="116d3-120">**WindowsSecurity**</span></span>](ishelldispatch4-windowssecurity.md) | <span data-ttu-id="116d3-121">Exibe a caixa de diálogo **segurança do Windows** .</span><span class="sxs-lookup"><span data-stu-id="116d3-121">Displays the **Windows Security** dialog box.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="116d3-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="116d3-122">Remarks</span></span>

<span data-ttu-id="116d3-123">Para obter uma discussão sobre os serviços do Windows, consulte a documentação de [Serviços](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="116d3-123">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="116d3-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="116d3-124">Requirements</span></span>



| <span data-ttu-id="116d3-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="116d3-125">Requirement</span></span> | <span data-ttu-id="116d3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="116d3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="116d3-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="116d3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="116d3-128">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="116d3-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="116d3-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="116d3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="116d3-130">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="116d3-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="116d3-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="116d3-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="116d3-132"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="116d3-132"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="116d3-133">Idl</span><span class="sxs-lookup"><span data-stu-id="116d3-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="116d3-134"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="116d3-134"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="116d3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="116d3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="116d3-136"><dt>Shell32.dll (versão 6.0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="116d3-136"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="116d3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="116d3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116d3-138">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="116d3-138">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="116d3-139">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="116d3-139">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="116d3-140">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="116d3-140">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="116d3-141">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="116d3-141">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="116d3-142">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="116d3-142">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> </dl>

 

 
