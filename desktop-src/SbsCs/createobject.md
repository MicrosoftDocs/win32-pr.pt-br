---
description: O método CreateObject do objeto Microsoft. Windows. ActCtx cria um objeto no contexto do manifesto atual.
ms.assetid: 531e6501-bb68-472b-b483-1f52815ba9d7
title: Método ActCtx. CreateObject
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.CreateObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: 2b4c4393d59ea5ab711dbf4bb1f4c88d906b6582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170033"
---
# <a name="actctxcreateobject-method"></a><span data-ttu-id="c81ed-103">Método ActCtx. CreateObject</span><span class="sxs-lookup"><span data-stu-id="c81ed-103">ActCtx.CreateObject method</span></span>

<span data-ttu-id="c81ed-104">O método **CreateObject** do objeto [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) cria um objeto no contexto do manifesto atual.</span><span class="sxs-lookup"><span data-stu-id="c81ed-104">The **CreateObject** method of the [**Microsoft.Windows.ActCtx**](microsoft-windows-actctx-object.md) object creates an object in the context of the current manifest.</span></span>

## <a name="syntax"></a><span data-ttu-id="c81ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c81ed-105">Syntax</span></span>


```JScript
ActCtx.CreateObject(
  objectId
)
```



## <a name="parameters"></a><span data-ttu-id="c81ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c81ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c81ed-107">*objectId*</span><span class="sxs-lookup"><span data-stu-id="c81ed-107">*objectId*</span></span> 
</dt> <dd>

<span data-ttu-id="c81ed-108">Uma cadeia de caracteres que especifica o tipo de objeto a ser criado.</span><span class="sxs-lookup"><span data-stu-id="c81ed-108">A string that specifies the type of object to create.</span></span> <span data-ttu-id="c81ed-109">Por exemplo, uma ProgID COM.</span><span class="sxs-lookup"><span data-stu-id="c81ed-109">For example, a COM ProgID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c81ed-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c81ed-110">Return value</span></span>

<span data-ttu-id="c81ed-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c81ed-111">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c81ed-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c81ed-112">Requirements</span></span>



| <span data-ttu-id="c81ed-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c81ed-113">Requirement</span></span> | <span data-ttu-id="c81ed-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c81ed-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c81ed-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c81ed-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c81ed-116">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c81ed-116">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c81ed-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c81ed-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c81ed-118">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c81ed-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c81ed-119">DLL</span><span class="sxs-lookup"><span data-stu-id="c81ed-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c81ed-120"><dt>Sxsoa.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c81ed-120"><dt>Sxsoa.dll</dt></span></span> </dl> |
| <span data-ttu-id="c81ed-121">IID</span><span class="sxs-lookup"><span data-stu-id="c81ed-121">IID</span></span><br/>                      | <span data-ttu-id="c81ed-122">IID \_ IActCtx é definido como 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span><span class="sxs-lookup"><span data-stu-id="c81ed-122">IID\_IActCtx is defined as 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="c81ed-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c81ed-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c81ed-124">**Método GetObject**</span><span class="sxs-lookup"><span data-stu-id="c81ed-124">**GetObject Method**</span></span>](getobject.md)
</dt> </dl>

 

 




