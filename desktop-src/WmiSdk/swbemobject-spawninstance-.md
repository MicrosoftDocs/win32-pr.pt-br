---
description: Use o \_ método SpawnInstance do objeto SWbemObject para criar uma nova instância de uma classe.
ms.assetid: 4761bdb2-455a-48c4-9e22-bfba6a1036ec
ms.tgt_platform: multiple
title: Método de SWbemObject.SpawnInstance_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
- ISWbemObject.SpawnInstance_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 804c7d2828723ee8da5dae28321faab62a32a0f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171788"
---
# <a name="swbemobjectspawninstance_-method"></a><span data-ttu-id="b12f9-103">Método SWbemObject. SpawnInstance \_</span><span class="sxs-lookup"><span data-stu-id="b12f9-103">SWbemObject.SpawnInstance\_ method</span></span>

<span data-ttu-id="b12f9-104">Use o **método \_ SpawnInstance** do objeto [**SWbemObject**](swbemobject.md) para criar uma nova instância de uma classe.</span><span class="sxs-lookup"><span data-stu-id="b12f9-104">Use the **SpawnInstance\_** method of the [**SWbemObject**](swbemobject.md) object to create a new instance of a class.</span></span> <span data-ttu-id="b12f9-105">O objeto atual deve ser uma definição de classe obtida do WMI por meio de um método como [**SWbemServices. Get**](swbemservices-get.md) ou [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="b12f9-105">The current object must be a class definition obtained from WMI via a method such as [**SWbemServices.Get**](swbemservices-get.md) or [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span> <span data-ttu-id="b12f9-106">Em seguida, use essa definição de classe para criar novas instâncias.</span><span class="sxs-lookup"><span data-stu-id="b12f9-106">Then, use this class definition to create new instances.</span></span> <span data-ttu-id="b12f9-107">Crie cada nova instância localmente no processo e chame [**SWbemObject. put \_**](swbemobject-put-.md) para realmente criar a instância no WMI.</span><span class="sxs-lookup"><span data-stu-id="b12f9-107">Create each new instance locally within the process, and then call [**SWbemObject.Put\_**](swbemobject-put-.md) to actually create the instance within WMI.</span></span>

> [!Note]  
> <span data-ttu-id="b12f9-108">Há suporte para a geração de uma instância de uma instância, mas a instância retornada está vazia.</span><span class="sxs-lookup"><span data-stu-id="b12f9-108">Spawning an instance from an instance is supported, but the returned instance is empty.</span></span>

 

<span data-ttu-id="b12f9-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b12f9-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b12f9-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b12f9-110">Syntax</span></span>


```VB
objNewInstance = .SpawnInstance_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b12f9-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b12f9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b12f9-112">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b12f9-112">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b12f9-113">Reservado e deve ser zero se especificado.</span><span class="sxs-lookup"><span data-stu-id="b12f9-113">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b12f9-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b12f9-114">Return value</span></span>

<span data-ttu-id="b12f9-115">Se for bem-sucedida, essa chamada retornará um objeto [**SWbemObject**](swbemobject.md) que contém uma nova instância da classe.</span><span class="sxs-lookup"><span data-stu-id="b12f9-115">If successful, this call returns an [**SWbemObject**](swbemobject.md) object that contains a new instance of the class.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b12f9-116">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="b12f9-116">Error codes</span></span>

<span data-ttu-id="b12f9-117">Após a conclusão do método **SpawnInstance \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="b12f9-117">After the completion of the **SpawnInstance\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="b12f9-118">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="b12f9-118">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="b12f9-119">O objeto atual não é uma definição de classe válida e não pode gerar novas instâncias.</span><span class="sxs-lookup"><span data-stu-id="b12f9-119">Current object is not a valid class definition, and it cannot spawn new instances.</span></span> <span data-ttu-id="b12f9-120">Ele está incompleto ou não foi registrado com o WMI usando [**SWbemObject. put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="b12f9-120">Either it is incomplete, or it has not been registered with WMI using [**SWbemObject.Put\_**](swbemobject-put-.md).</span></span>

</dd> <dt>

<span data-ttu-id="b12f9-121">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="b12f9-121">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="b12f9-122">Retornado se esse método for usado em uma instância em vez de uma classe.</span><span class="sxs-lookup"><span data-stu-id="b12f9-122">Returned if this method is used on an instance instead of a class.</span></span>

</dd> <dt>

<span data-ttu-id="b12f9-123">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="b12f9-123">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="b12f9-124">Foi especificado um parâmetro inválido.</span><span class="sxs-lookup"><span data-stu-id="b12f9-124">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="b12f9-125">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="b12f9-125">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="b12f9-126">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="b12f9-126">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b12f9-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b12f9-127">Requirements</span></span>



| <span data-ttu-id="b12f9-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b12f9-128">Requirement</span></span> | <span data-ttu-id="b12f9-129">Valor</span><span class="sxs-lookup"><span data-stu-id="b12f9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b12f9-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b12f9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b12f9-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b12f9-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b12f9-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b12f9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b12f9-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b12f9-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b12f9-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b12f9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b12f9-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b12f9-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b12f9-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b12f9-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="b12f9-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b12f9-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b12f9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b12f9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b12f9-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b12f9-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b12f9-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="b12f9-140">CLSID</span></span><br/>                    | <span data-ttu-id="b12f9-141">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="b12f9-141">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="b12f9-142">IID</span><span class="sxs-lookup"><span data-stu-id="b12f9-142">IID</span></span><br/>                      | <span data-ttu-id="b12f9-143">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="b12f9-143">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="b12f9-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="b12f9-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b12f9-145">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="b12f9-145">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="b12f9-146">**SWbemObject. put\_**</span><span class="sxs-lookup"><span data-stu-id="b12f9-146">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)
</dt> <dt>

[<span data-ttu-id="b12f9-147">**SWbemServices. Get**</span><span class="sxs-lookup"><span data-stu-id="b12f9-147">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> </dl>

 

 




