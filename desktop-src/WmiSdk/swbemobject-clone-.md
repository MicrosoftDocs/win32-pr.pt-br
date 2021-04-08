---
description: O \_ método clone do objeto SWbemObject retorna um novo objeto que é um clone do objeto atual.
ms.assetid: d0773c94-30b5-4217-8a9a-0bceb9e75f02
ms.tgt_platform: multiple
title: Método de SWbemObject.Clone_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Clone_
- ISWbemObject.Clone_
- ISWbemObject.Clone_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 84ca02bf749fd69db01ca7925b554c4eb0d95c35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011584"
---
# <a name="swbemobjectclone_-method"></a><span data-ttu-id="15871-103">Método SWbemObject. Clone \_</span><span class="sxs-lookup"><span data-stu-id="15871-103">SWbemObject.Clone\_ method</span></span>

<span data-ttu-id="15871-104">O **método \_ clone** do objeto [**SWbemObject**](swbemobject.md) retorna um novo objeto que é um clone do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="15871-104">The **Clone\_** method of the [**SWbemObject**](swbemobject.md) object returns a new object that is a clone of the current object.</span></span>

<span data-ttu-id="15871-105">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="15871-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="15871-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="15871-106">Syntax</span></span>


```VB
objWbemObject = .Clone_( _
)
```



## <a name="parameters"></a><span data-ttu-id="15871-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15871-107">Parameters</span></span>

<span data-ttu-id="15871-108">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="15871-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15871-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="15871-109">Return value</span></span>

<span data-ttu-id="15871-110">Se for bem-sucedido, esse método retornará um novo objeto [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="15871-110">If successful, this method returns a new [**SWbemObject**](swbemobject.md) object.</span></span>

## <a name="error-codes"></a><span data-ttu-id="15871-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="15871-111">Error codes</span></span>

<span data-ttu-id="15871-112">Após a conclusão do **método \_ clone** , o objeto **Err** pode conter um dos códigos de erro abaixo.</span><span class="sxs-lookup"><span data-stu-id="15871-112">After completion of the **Clone\_** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="15871-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="15871-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="15871-114">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="15871-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="15871-115">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="15871-115">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="15871-116">**Nada** foi especificado como parâmetro e não é aceitável nesse uso.</span><span class="sxs-lookup"><span data-stu-id="15871-116">**Nothing** was specified as a parameter, and it is not acceptable in this usage.</span></span>

</dd> <dt>

<span data-ttu-id="15871-117">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="15871-117">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="15871-118">Não há memória suficiente para clonar o objeto.</span><span class="sxs-lookup"><span data-stu-id="15871-118">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15871-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="15871-119">Remarks</span></span>

<span data-ttu-id="15871-120">Use o **método \_ clone** para duplicar uma definição de classe ou uma instância.</span><span class="sxs-lookup"><span data-stu-id="15871-120">Use the **Clone\_** method to duplicate a class definition or an instance.</span></span> <span data-ttu-id="15871-121">Isso é útil quando você precisa da cópia original do objeto para fins de backup enquanto você está modificando uma nova cópia.</span><span class="sxs-lookup"><span data-stu-id="15871-121">This is useful when you need the original copy of the object for backup purposes while you are modifying a new copy.</span></span> <span data-ttu-id="15871-122">Da mesma forma, use esse método para criar várias instâncias novas de uma única instância de origem.</span><span class="sxs-lookup"><span data-stu-id="15871-122">Likewise, use this method to create many new instances from a single source instance.</span></span> <span data-ttu-id="15871-123">Por exemplo, use [**SWbemObject. SpawnInstance \_**](swbemobject-spawninstance-.md) para criar uma única instância inicial e use **SWbemObject. Clone \_** para produzir rapidamente 100 cópias da instância.</span><span class="sxs-lookup"><span data-stu-id="15871-123">For example, use [**SWbemObject.SpawnInstance\_**](swbemobject-spawninstance-.md) to create a single starting instance, and use **SWbemObject.Clone\_** to produce 100 copies of the instance quickly.</span></span> <span data-ttu-id="15871-124">Subsequentemente, você pode modificar os objetos, dando a cada um valores específicos.</span><span class="sxs-lookup"><span data-stu-id="15871-124">Subsequently, you can modify the objects, giving each one specific values.</span></span>

<span data-ttu-id="15871-125">Não é possível usar esse método para converter uma definição de classe em uma instância ou para converter uma instância em uma definição de classe.</span><span class="sxs-lookup"><span data-stu-id="15871-125">It is not possible to use this method to convert a class definition to an instance, or to convert an instance to a class definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="15871-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="15871-126">Requirements</span></span>



| <span data-ttu-id="15871-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="15871-127">Requirement</span></span> | <span data-ttu-id="15871-128">Valor</span><span class="sxs-lookup"><span data-stu-id="15871-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15871-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15871-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15871-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="15871-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="15871-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="15871-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15871-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="15871-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="15871-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="15871-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="15871-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="15871-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="15871-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="15871-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="15871-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="15871-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="15871-137">DLL</span><span class="sxs-lookup"><span data-stu-id="15871-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15871-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15871-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="15871-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="15871-139">CLSID</span></span><br/>                    | <span data-ttu-id="15871-140">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="15871-140">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="15871-141">IID</span><span class="sxs-lookup"><span data-stu-id="15871-141">IID</span></span><br/>                      | <span data-ttu-id="15871-142">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="15871-142">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




