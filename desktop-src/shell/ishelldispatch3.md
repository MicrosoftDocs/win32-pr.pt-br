---
description: Estende o objeto IShellDispatch2.
ms.assetid: 89d0aa4d-844d-497d-82bb-bcc2bcf9c78b
title: Objeto IShellDispatch3 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch3
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 501b1396bd08ad8fd06f25da9b7030d4ce28d1e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967514"
---
# <a name="ishelldispatch3-object"></a><span data-ttu-id="33518-103">Objeto IShellDispatch3</span><span class="sxs-lookup"><span data-stu-id="33518-103">IShellDispatch3 object</span></span>

<span data-ttu-id="33518-104">Estende o objeto [**IShellDispatch2**](ishelldispatch2-object.md) .</span><span class="sxs-lookup"><span data-stu-id="33518-104">Extends the [**IShellDispatch2**](ishelldispatch2-object.md) object.</span></span> <span data-ttu-id="33518-105">O **IShellDispatch3** dá suporte a um novo método além das propriedades e métodos com suporte do **IShellDispatch2**.</span><span class="sxs-lookup"><span data-stu-id="33518-105">**IShellDispatch3** supports one new method in addition to the properties and methods supported by **IShellDispatch2**.</span></span>

> [!Note]  
> <span data-ttu-id="33518-106">**IShellDispatch3** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="33518-106">**IShellDispatch3** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="33518-107">Membros</span><span class="sxs-lookup"><span data-stu-id="33518-107">Members</span></span>

<span data-ttu-id="33518-108">O objeto **IShellDispatch3** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="33518-108">The **IShellDispatch3** object has these types of members:</span></span>

-   [<span data-ttu-id="33518-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="33518-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="33518-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="33518-110">Methods</span></span>

<span data-ttu-id="33518-111">O objeto **IShellDispatch3** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="33518-111">The **IShellDispatch3** object has these methods.</span></span>



| <span data-ttu-id="33518-112">Método</span><span class="sxs-lookup"><span data-stu-id="33518-112">Method</span></span>                                             | <span data-ttu-id="33518-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="33518-113">Description</span></span>                                                  |
|:---------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="33518-114">**AddToRecent**</span><span class="sxs-lookup"><span data-stu-id="33518-114">**AddToRecent**</span></span>](ishelldispatch3-addtorecent.md) | <span data-ttu-id="33518-115">Adiciona um arquivo à lista MRU (usada mais recentemente).</span><span class="sxs-lookup"><span data-stu-id="33518-115">Adds a file to the most recently used (MRU) list.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33518-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="33518-116">Remarks</span></span>

<span data-ttu-id="33518-117">Para obter uma discussão sobre os serviços do Windows, consulte a documentação de [Serviços](../services/services.md) .</span><span class="sxs-lookup"><span data-stu-id="33518-117">For a discussion of Windows services, see the [Services](../services/services.md) documentation.</span></span>

## <a name="requirements"></a><span data-ttu-id="33518-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33518-118">Requirements</span></span>



| <span data-ttu-id="33518-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="33518-119">Requirement</span></span> | <span data-ttu-id="33518-120">Valor</span><span class="sxs-lookup"><span data-stu-id="33518-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33518-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33518-121">Minimum supported client</span></span><br/> | <span data-ttu-id="33518-122">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="33518-122">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="33518-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="33518-123">Minimum supported server</span></span><br/> | <span data-ttu-id="33518-124">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="33518-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="33518-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33518-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="33518-126"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="33518-126"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="33518-127">INSERI</span><span class="sxs-lookup"><span data-stu-id="33518-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="33518-128"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="33518-128"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="33518-129">DLL</span><span class="sxs-lookup"><span data-stu-id="33518-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33518-130"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="33518-130"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33518-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="33518-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33518-132">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="33518-132">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="33518-133">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="33518-133">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="33518-134">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="33518-134">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="33518-135">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="33518-135">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> </dl>

 

 
