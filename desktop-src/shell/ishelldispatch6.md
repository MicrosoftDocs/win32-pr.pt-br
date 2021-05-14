---
description: Estende o objeto IShellDispatch5.
title: Objeto IShellDispatch6 (Shldisp.h)
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
ms.openlocfilehash: de27322324dc8a25bdc679374e625f94a1d1a2ae
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843027"
---
# <a name="ishelldispatch6-object"></a><span data-ttu-id="de3dd-103">Objeto IShellDispatch6</span><span class="sxs-lookup"><span data-stu-id="de3dd-103">IShellDispatch6 object</span></span>

<span data-ttu-id="de3dd-104">Estende o [**objeto IShellDispatch5.**](ishelldispatch5.md)</span><span class="sxs-lookup"><span data-stu-id="de3dd-104">Extends the [**IShellDispatch5**](ishelldispatch5.md) object.</span></span> <span data-ttu-id="de3dd-105">Além das propriedades e métodos com suporte de **IShellDispatch5,** **IShellDispatch6** adiciona um método que exibe o painel Pesquisa de Aplicativos.</span><span class="sxs-lookup"><span data-stu-id="de3dd-105">In addition to the properties and methods supported by **IShellDispatch5**, **IShellDispatch6** adds a method that displays the Apps Search pane.</span></span>

> [!Note]  
> <span data-ttu-id="de3dd-106">**IShellDispatch6** é implementado e acessado por meio do [**objeto Shell.**](shell.md)</span><span class="sxs-lookup"><span data-stu-id="de3dd-106">**IShellDispatch6** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="de3dd-107">Membros</span><span class="sxs-lookup"><span data-stu-id="de3dd-107">Members</span></span>

<span data-ttu-id="de3dd-108">O **objeto IShellDispatch6** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="de3dd-108">The **IShellDispatch6** object has these types of members:</span></span>

-   [<span data-ttu-id="de3dd-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="de3dd-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="de3dd-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="de3dd-110">Methods</span></span>

<span data-ttu-id="de3dd-111">O **objeto IShellDispatch6** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="de3dd-111">The **IShellDispatch6** object has these methods.</span></span>



| <span data-ttu-id="de3dd-112">Método</span><span class="sxs-lookup"><span data-stu-id="de3dd-112">Method</span></span>                                                 | <span data-ttu-id="de3dd-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="de3dd-113">Description</span></span>                                                                                                                  |
|:-------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="de3dd-114">**SearchCommand**</span><span class="sxs-lookup"><span data-stu-id="de3dd-114">**SearchCommand**</span></span>](ishelldispatch6-searchcommand.md) | <span data-ttu-id="de3dd-115">Exibe o painel Pesquisa de Aplicativos, que normalmente aparece quando você começa a digitar um termo de pesquisa do tela inicial.</span><span class="sxs-lookup"><span data-stu-id="de3dd-115">Displays the Apps Search pane, which normally appears when you begin to type a search term from the Start screen.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="de3dd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de3dd-116">Requirements</span></span>



| <span data-ttu-id="de3dd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="de3dd-117">Requirement</span></span> | <span data-ttu-id="de3dd-118">Valor</span><span class="sxs-lookup"><span data-stu-id="de3dd-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="de3dd-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de3dd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="de3dd-120">Windows 8 \[ aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de3dd-120">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="de3dd-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de3dd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="de3dd-122">Somente aplicativos da área de trabalho do Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="de3dd-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="de3dd-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="de3dd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="de3dd-124"><dt>Shldisp.h</dt></span><span class="sxs-lookup"><span data-stu-id="de3dd-124"><dt>Shldisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="de3dd-125">Idl</span><span class="sxs-lookup"><span data-stu-id="de3dd-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="de3dd-126"><dt>Shldisp.idl</dt></span><span class="sxs-lookup"><span data-stu-id="de3dd-126"><dt>Shldisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="de3dd-127">DLL</span><span class="sxs-lookup"><span data-stu-id="de3dd-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="de3dd-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="de3dd-128"><dt>Shell32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de3dd-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="de3dd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de3dd-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="de3dd-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="de3dd-131">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="de3dd-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="de3dd-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="de3dd-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="de3dd-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="de3dd-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="de3dd-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="de3dd-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="de3dd-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="de3dd-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> <dt>

[<span data-ttu-id="de3dd-136">**IShellDispatch5**</span><span class="sxs-lookup"><span data-stu-id="de3dd-136">**IShellDispatch5**</span></span>](ishelldispatch5.md)
</dt> </dl>

 

 
