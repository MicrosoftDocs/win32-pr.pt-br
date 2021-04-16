---
title: Função de fábrica D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Cria um objeto de fábrica que pode ser usado para criar recursos de Direct2D. | Função de fábrica D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754074"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a><span data-ttu-id="60def-105">D2D1CreateFactory <Factory> ( \_ \_ tipo de fábrica d2d1, \_ D2D1 \_ Opções de fábrica&, fábrica \* \* ) função</span><span class="sxs-lookup"><span data-stu-id="60def-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,D2D1\_FACTORY\_OPTIONS&,Factory\*\*) Function</span></span>

<span data-ttu-id="60def-106">Cria um objeto de fábrica que pode ser usado para criar recursos de Direct2D.</span><span class="sxs-lookup"><span data-stu-id="60def-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="60def-107">Parâmetros de modelo</span><span class="sxs-lookup"><span data-stu-id="60def-107">Template Parameters</span></span>



| <span data-ttu-id="60def-108">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="60def-108">Parameter</span></span> | <span data-ttu-id="60def-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="60def-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="60def-110">*Padrões*</span><span class="sxs-lookup"><span data-stu-id="60def-110">*Factory*</span></span> | <span data-ttu-id="60def-111">O tipo de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) a ser criado.</span><span class="sxs-lookup"><span data-stu-id="60def-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="60def-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="60def-112">Parameters</span></span>



| <span data-ttu-id="60def-113">Parâmetro</span><span class="sxs-lookup"><span data-stu-id="60def-113">Parameter</span></span>        | <span data-ttu-id="60def-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="60def-114">Description</span></span>                                                                     |
|------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="60def-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="60def-115">*factoryType*</span></span>    | <span data-ttu-id="60def-116">O modelo de Threading da fábrica e os recursos que ele cria.</span><span class="sxs-lookup"><span data-stu-id="60def-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="60def-117">*factoryoptions*</span><span class="sxs-lookup"><span data-stu-id="60def-117">*factoryOptions*</span></span> | <span data-ttu-id="60def-118">O nível de detalhe fornecido à camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="60def-118">The level of detail provided to the debugging layer.</span></span>                            |
| <span data-ttu-id="60def-119">*fábrica*</span><span class="sxs-lookup"><span data-stu-id="60def-119">*factory*</span></span>        | <span data-ttu-id="60def-120">Quando esse método retorna, contém o endereço de um ponteiro para a nova fábrica.</span><span class="sxs-lookup"><span data-stu-id="60def-120">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="60def-121">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="60def-121">Return Value</span></span>

<span data-ttu-id="60def-122">Se o método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="60def-122">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="60def-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="60def-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="60def-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60def-124">Requirements</span></span>



| <span data-ttu-id="60def-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="60def-125">Requirement</span></span> | <span data-ttu-id="60def-126">Valor</span><span class="sxs-lookup"><span data-stu-id="60def-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60def-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60def-127">Minimum supported client</span></span><br/> | <span data-ttu-id="60def-128">Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]</span><span class="sxs-lookup"><span data-stu-id="60def-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="60def-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="60def-129">Minimum supported server</span></span><br/> | <span data-ttu-id="60def-130">Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="60def-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="60def-131">Número mínimo de telefone com suporte</span><span class="sxs-lookup"><span data-stu-id="60def-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="60def-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="60def-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="60def-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="60def-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="60def-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="60def-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="60def-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="60def-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="60def-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60def-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="60def-137">DLL</span><span class="sxs-lookup"><span data-stu-id="60def-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60def-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60def-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

