---
description: Use o \_ método SpawnDerivedClass do objeto SWbemObject para criar um objeto de classe derivada do objeto atual. O objeto deve ser uma definição de classe que se torna a classe pai do objeto gerado.
ms.assetid: 1b5aaea7-50f4-40bd-ab2a-f4ff55cc22fc
ms.tgt_platform: multiple
title: Método de SWbemObject.SpawnDerivedClass_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
- ISWbemObject.SpawnDerivedClass_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b26e1d894e5ccc0d0fcec9d7ac9ad0101d18c7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165197"
---
# <a name="swbemobjectspawnderivedclass_-method"></a><span data-ttu-id="d970a-104">Método SWbemObject. SpawnDerivedClass \_</span><span class="sxs-lookup"><span data-stu-id="d970a-104">SWbemObject.SpawnDerivedClass\_ method</span></span>

<span data-ttu-id="d970a-105">Use o **método \_ SpawnDerivedClass** do objeto [**SWbemObject**](swbemobject.md) para criar um objeto de classe derivada do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="d970a-105">Use the **SpawnDerivedClass\_** method of the [**SWbemObject**](swbemobject.md) object to create a derived class object from the current object.</span></span> <span data-ttu-id="d970a-106">O objeto deve ser uma definição de classe que se torna a classe pai do objeto gerado.</span><span class="sxs-lookup"><span data-stu-id="d970a-106">The object must be a class definition that becomes the parent class of the spawned object.</span></span>

<span data-ttu-id="d970a-107">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d970a-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d970a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d970a-108">Syntax</span></span>


```VB
objNewClass = .SpawnDerivedClass_( _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d970a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d970a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d970a-110">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="d970a-110">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d970a-111">Reservado e deve ser 0 (zero) se especificado.</span><span class="sxs-lookup"><span data-stu-id="d970a-111">Reserved and must be 0 (zero) if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d970a-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d970a-112">Return value</span></span>

<span data-ttu-id="d970a-113">Se a chamada for bem-sucedida, o objeto [**SWbemObject**](swbemobject.md) conterá o novo objeto de definição de classe.</span><span class="sxs-lookup"><span data-stu-id="d970a-113">If the call is successful, the [**SWbemObject**](swbemobject.md) object contains the new class definition object.</span></span> <span data-ttu-id="d970a-114">Nenhum objeto retorna quando há um erro.</span><span class="sxs-lookup"><span data-stu-id="d970a-114">No object returns when there is an error.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d970a-115">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d970a-115">Error codes</span></span>

<span data-ttu-id="d970a-116">Após a conclusão do método **SpawnDerivedClass \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="d970a-116">After the completion of the **SpawnDerivedClass\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d970a-117">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d970a-117">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d970a-118">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="d970a-118">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d970a-119">**wbemErrIllegalOperation** -2147749918 (0x8004101E)</span><span class="sxs-lookup"><span data-stu-id="d970a-119">**wbemErrIllegalOperation** - 2147749918 (0x8004101E)</span></span>
</dt> <dd>

<span data-ttu-id="d970a-120">O usuário solicitou uma operação ilegal, como a geração de uma classe de uma instância.</span><span class="sxs-lookup"><span data-stu-id="d970a-120">User requested an illegal operation, such as spawning a class from an instance.</span></span>

</dd> <dt>

<span data-ttu-id="d970a-121">**wbemErrIncompleteClass** -2147749920 (0x80041020)</span><span class="sxs-lookup"><span data-stu-id="d970a-121">**wbemErrIncompleteClass** - 2147749920 (0x80041020)</span></span>
</dt> <dd>

<span data-ttu-id="d970a-122">A classe de origem não foi totalmente definida ou registrada com WMI, portanto, uma nova classe derivada não é permitida.</span><span class="sxs-lookup"><span data-stu-id="d970a-122">Source class was not completely defined or registered with WMI, so a new derived class is not permitted.</span></span>

</dd> <dt>

<span data-ttu-id="d970a-123">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d970a-123">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d970a-124">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="d970a-124">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d970a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d970a-125">Remarks</span></span>

<span data-ttu-id="d970a-126">O objeto retornado automaticamente se torna uma subclasse do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="d970a-126">The object that is returned automatically becomes a subclass of the current object.</span></span> <span data-ttu-id="d970a-127">Esse comportamento não pode ser substituído.</span><span class="sxs-lookup"><span data-stu-id="d970a-127">This behavior cannot be overridden.</span></span> <span data-ttu-id="d970a-128">Não há nenhum outro método pelo qual você possa criar classes derivadas.</span><span class="sxs-lookup"><span data-stu-id="d970a-128">There is no other method by which you can create derived classes.</span></span>

<span data-ttu-id="d970a-129">Você não pode criar uma classe derivada de uma classe que seja local para seu próprio processo de cliente.</span><span class="sxs-lookup"><span data-stu-id="d970a-129">You cannot create a derived class from a class that is local to your own client process.</span></span> <span data-ttu-id="d970a-130">Antes de usar esse método para criar uma classe derivada, você deve criar a classe base.</span><span class="sxs-lookup"><span data-stu-id="d970a-130">Before use this method to create a derived class, you must create the base class.</span></span> <span data-ttu-id="d970a-131">Para criar a classe base, chame [**SWbemObject. put \_**](swbemobject-put-.md)e recupere a classe base usando [**SWbemServices. Get**](swbemservices-get.md).</span><span class="sxs-lookup"><span data-stu-id="d970a-131">To create the base class, call [**SWbemObject.Put\_**](swbemobject-put-.md), and retrieve the base class using [**SWbemServices.Get**](swbemservices-get.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d970a-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d970a-132">Requirements</span></span>



| <span data-ttu-id="d970a-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="d970a-133">Requirement</span></span> | <span data-ttu-id="d970a-134">Valor</span><span class="sxs-lookup"><span data-stu-id="d970a-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d970a-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d970a-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d970a-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d970a-136">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d970a-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d970a-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d970a-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d970a-138">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d970a-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d970a-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d970a-140"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d970a-140"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d970a-141">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d970a-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="d970a-142"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d970a-142"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d970a-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d970a-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d970a-144"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d970a-144"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d970a-145">CLSID</span><span class="sxs-lookup"><span data-stu-id="d970a-145">CLSID</span></span><br/>                    | <span data-ttu-id="d970a-146">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="d970a-146">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="d970a-147">IID</span><span class="sxs-lookup"><span data-stu-id="d970a-147">IID</span></span><br/>                      | <span data-ttu-id="d970a-148">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="d970a-148">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




