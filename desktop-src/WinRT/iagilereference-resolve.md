---
description: Obtém a ID da interface de uma referência ágil a um objeto.
ms.assetid: 627A7EE4-CFEF-47F6-BA99-51BEB78C5D55
title: 'Método IAgileReference:: resolve'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAgileReference.Resolve
api_type:
- COM
api_location:
- objidl.h
ms.openlocfilehash: 1c3ac95802a44f4305abb24566744ad98c67b174
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765779"
---
# <a name="iagilereferenceresolve-method"></a><span data-ttu-id="c31f2-103">Método IAgileReference:: resolve</span><span class="sxs-lookup"><span data-stu-id="c31f2-103">IAgileReference::Resolve method</span></span>

<span data-ttu-id="c31f2-104">Obtém a ID da interface de uma referência ágil a um objeto.</span><span class="sxs-lookup"><span data-stu-id="c31f2-104">Gets the interface ID of an agile reference to an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="c31f2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c31f2-105">Syntax</span></span>


```C++
HRESULT Resolve(
  [in]          REFIID riid,
  [out, retval] void   **ppvObjectReference
);
```



## <a name="parameters"></a><span data-ttu-id="c31f2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c31f2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c31f2-107">*riid* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c31f2-107">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c31f2-108">A ID da interface a ser recuperada da referência ágil.</span><span class="sxs-lookup"><span data-stu-id="c31f2-108">The interface ID of the interface to be retrieved from the agile reference.</span></span> <span data-ttu-id="c31f2-109">Não é necessário ser o mesmo que a interface registrada.</span><span class="sxs-lookup"><span data-stu-id="c31f2-109">It is not required to be the same as the registered interface.</span></span>

</dd> <dt>

<span data-ttu-id="c31f2-110">*ppvObjectReference* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="c31f2-110">*ppvObjectReference* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="c31f2-111">Após a conclusão bem-sucedida, \* *ppvObjectReference* é um ponteiro para a interface especificada por *riid*.</span><span class="sxs-lookup"><span data-stu-id="c31f2-111">On successful completion, \**ppvObjectReference* is a pointer to the interface specified by *riid*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c31f2-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c31f2-112">Return value</span></span>

<span data-ttu-id="c31f2-113">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="c31f2-113">This method can return one of these values.</span></span>



| <span data-ttu-id="c31f2-114">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c31f2-114">Return value</span></span>                                                                              | <span data-ttu-id="c31f2-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="c31f2-115">Description</span></span>                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c31f2-116"><dt>S \_ OK</dt></span><span class="sxs-lookup"><span data-stu-id="c31f2-116"><dt>S\_OK</dt></span></span> </dl>          | <span data-ttu-id="c31f2-117">O método foi concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="c31f2-117">The method completed successfully.</span></span><br/>                                  |
| <dl> <span data-ttu-id="c31f2-118"><dt>E \_ NOinterface</dt></span><span class="sxs-lookup"><span data-stu-id="c31f2-118"><dt>E\_NOINTERFACE</dt></span></span> </dl> | <span data-ttu-id="c31f2-119">A interface solicitada não está implementada no objeto registrado.</span><span class="sxs-lookup"><span data-stu-id="c31f2-119">The requested interface isn't implemented on the registered object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c31f2-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="c31f2-120">Remarks</span></span>

<span data-ttu-id="c31f2-121">Chame a função [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) para criar uma referência ágil a um objeto.</span><span class="sxs-lookup"><span data-stu-id="c31f2-121">Call the [**RoGetAgileReference**](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference) function to create an agile reference to an object.</span></span> <span data-ttu-id="c31f2-122">Chame o método **resolve** para localizar o objeto no apartamento no qual **resolve** é chamado.</span><span class="sxs-lookup"><span data-stu-id="c31f2-122">Call the **Resolve** method to localize the object into the apartment in which **Resolve** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="c31f2-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c31f2-123">Requirements</span></span>



| <span data-ttu-id="c31f2-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c31f2-124">Requirement</span></span> | <span data-ttu-id="c31f2-125">Valor</span><span class="sxs-lookup"><span data-stu-id="c31f2-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="c31f2-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c31f2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c31f2-127">Aplicativos Windows 8.1 aplicativos de \[ área de trabalho \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c31f2-127">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>            |
| <span data-ttu-id="c31f2-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c31f2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c31f2-129">\[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2012 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="c31f2-129">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c31f2-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="c31f2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c31f2-131">**IAgileReference**</span><span class="sxs-lookup"><span data-stu-id="c31f2-131">**IAgileReference**</span></span>](/windows/desktop/api/objidl/nn-objidl-iagilereference)
</dt> <dt>

[<span data-ttu-id="c31f2-132">**RoGetAgileReference**</span><span class="sxs-lookup"><span data-stu-id="c31f2-132">**RoGetAgileReference**</span></span>](/windows/desktop/api/ComBaseApi/nf-combaseapi-rogetagilereference)
</dt> </dl>

 

 




