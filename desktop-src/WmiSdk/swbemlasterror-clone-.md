---
description: O \_ método clone do objeto SWbemLastError retorna um novo objeto que é um clone do objeto SWbemLastError atual.
ms.assetid: 577be060-309f-40a2-a4db-c0a477c21f11
ms.tgt_platform: multiple
title: Método de SWbemLastError.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Clone_
- ISWbemLastError.Clone_
- ISWbemLastError.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7d4d43f73ab42021235db39adba0a77bc783b97a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763535"
---
# <a name="swbemlasterrorclone_-method"></a><span data-ttu-id="fde37-103">Método SWbemLastError. Clone \_</span><span class="sxs-lookup"><span data-stu-id="fde37-103">SWbemLastError.Clone\_ method</span></span>

<span data-ttu-id="fde37-104">O **método \_ clone** do objeto [**SWbemLastError**](swbemlasterror.md) retorna um novo objeto que é um clone do objeto **SWbemLastError** atual.</span><span class="sxs-lookup"><span data-stu-id="fde37-104">The **Clone\_** method of the [**SWbemLastError**](swbemlasterror.md) object returns a new object that is a clone of the current **SWbemLastError** object.</span></span>

<span data-ttu-id="fde37-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fde37-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fde37-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fde37-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="fde37-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fde37-107">Parameters</span></span>

<span data-ttu-id="fde37-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fde37-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fde37-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fde37-109">Return value</span></span>

<span data-ttu-id="fde37-110">Se o **método \_ clone** for bem-sucedido, ele retornará um novo objeto [**SWbemLastError**](swbemlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="fde37-110">If the **Clone\_** method is successful, it returns a new [**SWbemLastError**](swbemlasterror.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="fde37-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="fde37-111">Error codes</span></span>

<span data-ttu-id="fde37-112">Após a conclusão do método **clone \_** , o objeto **Err** pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="fde37-112">Upon the completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="fde37-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="fde37-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="fde37-114">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="fde37-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="fde37-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="fde37-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="fde37-116">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="fde37-116">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="fde37-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="fde37-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="fde37-118">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="fde37-118">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fde37-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fde37-119">Remarks</span></span>

<span data-ttu-id="fde37-120">Use o **método \_ clone** para duplicar uma definição ou instância de classe.</span><span class="sxs-lookup"><span data-stu-id="fde37-120">Use the **Clone\_** method to duplicate a class definition or instance.</span></span> <span data-ttu-id="fde37-121">Esse método é útil quando você precisa fazer backup da cópia original do objeto enquanto modifica uma nova cópia.</span><span class="sxs-lookup"><span data-stu-id="fde37-121">This method is useful when you need to back up the original copy of the object while you modify a new copy.</span></span> <span data-ttu-id="fde37-122">Além disso, use esse método para criar várias instâncias novas de uma única instância de origem.</span><span class="sxs-lookup"><span data-stu-id="fde37-122">Also, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="fde37-123">Por exemplo, use [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) para criar uma única instância inicial e use **SWbemLastError. Clone \_** para produzir rapidamente 100 cópias da instância.</span><span class="sxs-lookup"><span data-stu-id="fde37-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance and use **SWbemLastError.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="fde37-124">Subsequentemente, você pode modificar os objetos, fornecendo valores específicos para cada objeto.</span><span class="sxs-lookup"><span data-stu-id="fde37-124">Subsequently, you can modify the objects, giving specific values to each object.</span></span>

<span data-ttu-id="fde37-125">Não é possível usar esse método para converter uma definição de classe em uma instância ou para converter uma instância em uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="fde37-125">It is not possible to use this method to convert a class definition to an instance or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde37-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde37-126">Requirements</span></span>



| <span data-ttu-id="fde37-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde37-127">Requirement</span></span> | <span data-ttu-id="fde37-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fde37-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fde37-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fde37-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fde37-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fde37-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fde37-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fde37-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fde37-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fde37-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fde37-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fde37-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde37-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde37-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fde37-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fde37-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="fde37-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fde37-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fde37-137">DLL</span><span class="sxs-lookup"><span data-stu-id="fde37-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fde37-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fde37-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fde37-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="fde37-139">CLSID</span></span><br/>                    | <span data-ttu-id="fde37-140">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="fde37-140">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="fde37-141">IID</span><span class="sxs-lookup"><span data-stu-id="fde37-141">IID</span></span><br/>                      | <span data-ttu-id="fde37-142">ISWbemLastError de IID \_</span><span class="sxs-lookup"><span data-stu-id="fde37-142">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




