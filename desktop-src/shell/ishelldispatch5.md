---
description: Estende o objeto IShellDispatch4.
title: Objeto IShellDispatch5 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch5
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9170340a-0f11-4ec9-877d-fb7fef9888b2
ms.openlocfilehash: 26c3112faa748aa443526fbe9cb493af67502cd7
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842997"
---
# <a name="ishelldispatch5-object"></a><span data-ttu-id="c6ff5-103">Objeto IShellDispatch5</span><span class="sxs-lookup"><span data-stu-id="c6ff5-103">IShellDispatch5 object</span></span>

<span data-ttu-id="c6ff5-104">Estende o objeto [**IShellDispatch4**](ishelldispatch4.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ff5-104">Extends the [**IShellDispatch4**](ishelldispatch4.md) object.</span></span> <span data-ttu-id="c6ff5-105">Além das propriedades e métodos com suporte do **IShellDispatch4**, o **IShellDispatch5** adiciona um método que exibe janelas abertas em uma pilha 3D.</span><span class="sxs-lookup"><span data-stu-id="c6ff5-105">In addition to the properties and methods supported by **IShellDispatch4**, **IShellDispatch5** adds a method that displays open windows in a 3D stack.</span></span>

> [!Note]  
> <span data-ttu-id="c6ff5-106">**IShellDispatch5** é implementado e acessado por meio do objeto [**shell**](shell.md) .</span><span class="sxs-lookup"><span data-stu-id="c6ff5-106">**IShellDispatch5** is implemented and accessed through the [**Shell**](shell.md) object.</span></span>

 

## <a name="members"></a><span data-ttu-id="c6ff5-107">Membros</span><span class="sxs-lookup"><span data-stu-id="c6ff5-107">Members</span></span>

<span data-ttu-id="c6ff5-108">O objeto **IShellDispatch5** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c6ff5-108">The **IShellDispatch5** object has these types of members:</span></span>

-   [<span data-ttu-id="c6ff5-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6ff5-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c6ff5-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="c6ff5-110">Methods</span></span>

<span data-ttu-id="c6ff5-111">O objeto **IShellDispatch5** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c6ff5-111">The **IShellDispatch5** object has these methods.</span></span>



| <span data-ttu-id="c6ff5-112">Método</span><span class="sxs-lookup"><span data-stu-id="c6ff5-112">Method</span></span>                                                   | <span data-ttu-id="c6ff5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="c6ff5-113">Description</span></span>                                                                    |
|:---------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="c6ff5-114">**WindowSwitcher**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-114">**WindowSwitcher**</span></span>](ishelldispatch5-windowswitcher.md) | <span data-ttu-id="c6ff5-115">Exibe as janelas abertas em uma pilha 3D que você pode percorrer.</span><span class="sxs-lookup"><span data-stu-id="c6ff5-115">Displays your open windows in a 3D stack that you can flip through.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c6ff5-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6ff5-116">Requirements</span></span>



| <span data-ttu-id="c6ff5-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6ff5-117">Requirement</span></span> | <span data-ttu-id="c6ff5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c6ff5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6ff5-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6ff5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c6ff5-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c6ff5-120">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="c6ff5-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c6ff5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c6ff5-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c6ff5-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c6ff5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6ff5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6ff5-124"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c6ff5-124"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="c6ff5-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="c6ff5-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c6ff5-126"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c6ff5-126"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="c6ff5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="c6ff5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c6ff5-128"><dt>Shell32.dll (versão 6,0 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="c6ff5-128"><dt>Shell32.dll (version 6.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6ff5-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6ff5-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6ff5-130">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-130">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="c6ff5-131">**Objeto Shell**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-131">**Shell Object**</span></span>](shell.md)
</dt> <dt>

[<span data-ttu-id="c6ff5-132">**IShellDispatch**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-132">**IShellDispatch**</span></span>](ishelldispatch.md)
</dt> <dt>

[<span data-ttu-id="c6ff5-133">**IShellDispatch2**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-133">**IShellDispatch2**</span></span>](ishelldispatch2-object.md)
</dt> <dt>

[<span data-ttu-id="c6ff5-134">**IShellDispatch3**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-134">**IShellDispatch3**</span></span>](ishelldispatch3.md)
</dt> <dt>

[<span data-ttu-id="c6ff5-135">**IShellDispatch4**</span><span class="sxs-lookup"><span data-stu-id="c6ff5-135">**IShellDispatch4**</span></span>](ishelldispatch4.md)
</dt> </dl>

 

 
