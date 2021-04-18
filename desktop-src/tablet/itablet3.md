---
description: A interface ITablet3 permite a consulta multitoque para entrada.
ms.assetid: 949f2d83-7761-4d60-b8fe-5a9ac7567238
title: Interface ITablet3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet3
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f37d70888ccedf0fe941f0387c064aba37dc287e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766503"
---
# <a name="itablet3-interface"></a><span data-ttu-id="f273a-103">Interface ITablet3</span><span class="sxs-lookup"><span data-stu-id="f273a-103">ITablet3 interface</span></span>

<span data-ttu-id="f273a-104">A interface ITablet3 permite a consulta multitoque para entrada.</span><span class="sxs-lookup"><span data-stu-id="f273a-104">The ITablet3 interface enables multitouch querying for input.</span></span>

## <a name="members"></a><span data-ttu-id="f273a-105">Membros</span><span class="sxs-lookup"><span data-stu-id="f273a-105">Members</span></span>

<span data-ttu-id="f273a-106">A interface **ITablet3** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="f273a-106">The **ITablet3** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="f273a-107">**ITablet3** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f273a-107">**ITablet3** also has these types of members:</span></span>

-   [<span data-ttu-id="f273a-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="f273a-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="f273a-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="f273a-109">Methods</span></span>

<span data-ttu-id="f273a-110">A interface **ITablet3** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f273a-110">The **ITablet3** interface has these methods.</span></span>



| <span data-ttu-id="f273a-111">Método</span><span class="sxs-lookup"><span data-stu-id="f273a-111">Method</span></span>                                                  | <span data-ttu-id="f273a-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f273a-112">Description</span></span>                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [<span data-ttu-id="f273a-113">**GetMaximumCursors**</span><span class="sxs-lookup"><span data-stu-id="f273a-113">**GetMaximumCursors**</span></span>](itablet3-getmaximumcursors.md) | <span data-ttu-id="f273a-114">Recupera o número máximo de entradas com suporte.</span><span class="sxs-lookup"><span data-stu-id="f273a-114">Retrieves the maximum number of inputs supported.</span></span><br/>        |
| [<span data-ttu-id="f273a-115">**isMultiTouch**</span><span class="sxs-lookup"><span data-stu-id="f273a-115">**isMultiTouch**</span></span>](itablet3-ismultitouch.md)           | <span data-ttu-id="f273a-116">Indica se o multitoque está habilitado para este objeto.</span><span class="sxs-lookup"><span data-stu-id="f273a-116">Indicates whether multitouch is enabled for this object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f273a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="f273a-117">Remarks</span></span>

<span data-ttu-id="f273a-118">Os desenvolvedores não devem usar essa interface</span><span class="sxs-lookup"><span data-stu-id="f273a-118">Developers should not use this interface</span></span>

<span data-ttu-id="f273a-119">O código a seguir descreve como a interface **ITablet3** é definida.</span><span class="sxs-lookup"><span data-stu-id="f273a-119">The following code describes how the **ITablet3** interface is defined.</span></span>

``` syntax
[
  object,
  uuid(AC0E3951-0A2F-448E-88D0-49DA0C453460)
  pointer_default(unique)
]
interface ITablet3 : IUnknown
{
    HRESULT IsMultiTouch([out] BOOL *pIsMultiTouch);

    HRESULT GetMaximumCursors([out] ULONG *pMaximumCursors);
};
  
```

## <a name="requirements"></a><span data-ttu-id="f273a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f273a-120">Requirements</span></span>



| <span data-ttu-id="f273a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f273a-121">Requirement</span></span> | <span data-ttu-id="f273a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f273a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f273a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f273a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f273a-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="f273a-124">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="f273a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f273a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f273a-126">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="f273a-126">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f273a-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f273a-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="f273a-128"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f273a-128"><dt>Wisptis.exe</dt></span></span> </dl> |



 

