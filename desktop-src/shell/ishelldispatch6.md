---
description: Estende o objeto IShellDispatch5.
title: Objeto IShellDispatch6 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch6
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 540A5CFD-1520-4B61-B461-E893EFA27115
ms.openlocfilehash: 42e9690ec5b2f5995b184e4e686b27037aab891d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090840"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="778f3-103">Objeto IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="778f3-103">IShellDispatch6 object</span></span>

<span data-ttu-id="778f3-104">Estende o objeto [**IShellDispatch5**](ishelldispatch5.md) .</span><span class="sxs-lookup"><span data-stu-id="778f3-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="778f3-105">Além das propriedades e métodos com suporte do **IShellDispatch5**, o **IShellDispatch6** adiciona um método que exibe o painel de pesquisa de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="778f3-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="778f3-106">**IShellDispatch6** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="778f3-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="778f3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="778f3-107">Members</span></span>

<span data-ttu-id="778f3-108">O objeto **IShellDispatch6** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="778f3-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="778f3-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="778f3-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="778f3-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="778f3-110">Methods</span></span>

<span data-ttu-id="778f3-111">O objeto **IShellDispatch6** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="778f3-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="778f3-112">Método</span><span class="sxs-lookup"><span data-stu-id="778f3-112">Method</span></span>                                                 | <span data-ttu-id="778f3-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="778f3-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="778f3-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="778f3-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="778f3-115">Exibe o painel de pesquisa de aplicativos, que normalmente aparece quando você começa a digitar um termo de pesquisa na tela inicial.</span><span class="sxs-lookup"><span data-stu-id="778f3-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="778f3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="778f3-116">Requirements</span></span>



| <span data-ttu-id="778f3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="778f3-117">Requirement</span></span> | <span data-ttu-id="778f3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="778f3-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="778f3-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="778f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="778f3-120">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="778f3-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="778f3-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="778f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="778f3-122">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="778f3-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="778f3-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="778f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="778f3-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="778f3-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="778f3-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="778f3-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="778f3-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="778f3-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="778f3-127">DLL</span><span class="sxs-lookup"><span data-stu-id="778f3-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="778f3-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="778f3-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="778f3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="778f3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="778f3-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="778f3-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="778f3-131">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="778f3-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="778f3-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="778f3-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="778f3-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="778f3-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="778f3-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="778f3-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="778f3-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="778f3-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="778f3-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="778f3-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
