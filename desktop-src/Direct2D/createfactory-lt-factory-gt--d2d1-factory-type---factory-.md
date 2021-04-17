---
title: Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
description: Cria um objeto de fábrica que pode ser usado para criar recursos de Direct2D. | Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105748076"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><span data-ttu-id="31682-105"><Factory>Função D2D1CreateFactory ( \_ \_ tipo de fábrica d2d1, fábrica \* \* )</span><span class="sxs-lookup"><span data-stu-id="31682-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,Factory\*\*) Function</span></span>

<span data-ttu-id="31682-106">Cria um objeto de fábrica que pode ser usado para criar recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="31682-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="31682-107">Parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="31682-107">Template Parameters</span></span>



| <span data-ttu-id="31682-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="31682-108">Parameter</span></span> | <span data-ttu-id="31682-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="31682-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="31682-110">*Padrões*</span><span class="sxs-lookup"><span data-stu-id="31682-110">*Factory*</span></span> | <span data-ttu-id="31682-111">O tipo de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="31682-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="31682-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31682-112">Parameters</span></span>



| <span data-ttu-id="31682-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="31682-113">Parameter</span></span>     | <span data-ttu-id="31682-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="31682-114">Description</span></span>                                                                     |
|---------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="31682-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="31682-115">*factoryType*</span></span> | <span data-ttu-id="31682-116">O modelo de Threading da fábrica e os recursos que ele cria.</span><span class="sxs-lookup"><span data-stu-id="31682-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="31682-117">*fábrica*</span><span class="sxs-lookup"><span data-stu-id="31682-117">*factory*</span></span>     | <span data-ttu-id="31682-118">Quando esse método retorna, contém o endereço de um ponteiro para a nova fábrica.</span><span class="sxs-lookup"><span data-stu-id="31682-118">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="31682-119">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="31682-119">Return Value</span></span>

<span data-ttu-id="31682-120">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="31682-120">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="31682-121">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="31682-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="examples"></a><span data-ttu-id="31682-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="31682-122">Examples</span></span>

<span data-ttu-id="31682-123">O exemplo a seguir cria uma fábrica.</span><span class="sxs-lookup"><span data-stu-id="31682-123">The following example creates a factory.</span></span>


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="31682-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31682-124">Requirements</span></span>



| <span data-ttu-id="31682-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="31682-125">Requirement</span></span> | <span data-ttu-id="31682-126">Valor</span><span class="sxs-lookup"><span data-stu-id="31682-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31682-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31682-127">Minimum supported client</span></span><br/> | <span data-ttu-id="31682-128">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="31682-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="31682-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31682-129">Minimum supported server</span></span><br/> | <span data-ttu-id="31682-130">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="31682-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="31682-131">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="31682-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="31682-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="31682-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="31682-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31682-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="31682-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="31682-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="31682-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31682-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="31682-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31682-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="31682-137">DLL</span><span class="sxs-lookup"><span data-stu-id="31682-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31682-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31682-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

