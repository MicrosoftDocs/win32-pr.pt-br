---
description: O novo método inicializa um comando a ser executado e retorna um novo objeto CDeferredCommand.
ms.assetid: bdd80747-a15b-422a-b742-ebfa4076bdf7
title: Método CCmdQueue. New (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.New
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 58c3aee63005010b9ed7366cfb63a69fcc7348b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757706"
---
# <a name="ccmdqueuenew-method"></a><span data-ttu-id="d913b-103">Método CCmdQueue. New</span><span class="sxs-lookup"><span data-stu-id="d913b-103">CCmdQueue.New method</span></span>

<span data-ttu-id="d913b-104">O `New` método inicializa um comando a ser executado e retorna um novo objeto [**CDeferredCommand**](cdeferredcommand.md) .</span><span class="sxs-lookup"><span data-stu-id="d913b-104">The `New` method initializes a command to be run and returns a new [**CDeferredCommand**](cdeferredcommand.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d913b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d913b-105">Syntax</span></span>


```C++
virtual HRESULT New(
   CDeferredCommand **ppCmd,
   LPUNKNOWN        pUnk,
   REFTIME          time,
   GUID             *iid,
   long             dispidMethod,
   short            wFlags,
   long             cArgs,
   VARIANT          *pDispParams,
   VARIANT          *pvarResult,
   short            *puArgErr,
   BOOL             bStream
);
```



## <a name="parameters"></a><span data-ttu-id="d913b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d913b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d913b-107">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="d913b-107">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-108">Endereço de um ponteiro para um objeto [**CDeferredCommand**](cdeferredcommand.md) pelo qual um aplicativo pode cancelar o comando, definir um novo horário de apresentação para ele ou recuperar informações de estimativa.</span><span class="sxs-lookup"><span data-stu-id="d913b-108">Address of a pointer to a [**CDeferredCommand**](cdeferredcommand.md) object by which an application can cancel the command, set a new presentation time for it, or retrieve estimate information.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="d913b-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-110">Ponteiro para o objeto que executará o comando.</span><span class="sxs-lookup"><span data-stu-id="d913b-110">Pointer to the object that will run the command.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-111">*time*</span><span class="sxs-lookup"><span data-stu-id="d913b-111">*time*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-112">Hora em que o comando ou comandos enfileirados são executados.</span><span class="sxs-lookup"><span data-stu-id="d913b-112">Time at which to run the queued command or commands.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-113">*IID*</span><span class="sxs-lookup"><span data-stu-id="d913b-113">*iid*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-114">Ponteiro para o identificador global exclusivo (**GUID**) da interface a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="d913b-114">Pointer to the globally unique identifier (**GUID**) of the interface to call.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-115">*dispidMethod*</span><span class="sxs-lookup"><span data-stu-id="d913b-115">*dispidMethod*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-116">Método na interface a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="d913b-116">Method on the interface to be called.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-117">*wFlags*</span><span class="sxs-lookup"><span data-stu-id="d913b-117">*wFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-118">Sinalizadores que descrevem o contexto da chamada.</span><span class="sxs-lookup"><span data-stu-id="d913b-118">Flags describing the context of the call.</span></span> <span data-ttu-id="d913b-119">Esse parâmetro oferece suporte aos mesmos sinalizadores que o método **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="d913b-119">This parameter supports the same flags as the **IDispatch::Invoke** method.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-120">*cArgs*</span><span class="sxs-lookup"><span data-stu-id="d913b-120">*cArgs*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-121">Número de argumentos passados.</span><span class="sxs-lookup"><span data-stu-id="d913b-121">Number of arguments passed.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-122">*pDispParams*</span><span class="sxs-lookup"><span data-stu-id="d913b-122">*pDispParams*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-123">Ponteiro para a lista de tipos variantes associados aos parâmetros de expedição.</span><span class="sxs-lookup"><span data-stu-id="d913b-123">Pointer to the list of variant types associated with the dispatch parameters.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-124">*pvarResult*</span><span class="sxs-lookup"><span data-stu-id="d913b-124">*pvarResult*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-125">Ponteiro para a lista em que os resultados, se houver, devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="d913b-125">Pointer to the list where results, if any, are to be returned.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-126">*puArgErr*</span><span class="sxs-lookup"><span data-stu-id="d913b-126">*puArgErr*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-127">Ponteiro para o índice na lista de parâmetros *pDispParams* em que ocorreu o último erro.</span><span class="sxs-lookup"><span data-stu-id="d913b-127">Pointer to the index within the *pDispParams* parameter list where the last error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d913b-128">*bStream*</span><span class="sxs-lookup"><span data-stu-id="d913b-128">*bStream*</span></span> 
</dt> <dd>

<span data-ttu-id="d913b-129">Valor que indica se o parâmetro de *tempo* é um valor de tempo de transmissão (**true**) ou um valor de tempo de apresentação (**false**).</span><span class="sxs-lookup"><span data-stu-id="d913b-129">Value indicating whether the *time* parameter is a stream-time value (**TRUE**) or a presentation-time value (**FALSE**).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d913b-130">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d913b-130">Return value</span></span>

<span data-ttu-id="d913b-131">Retornará S \_ OK se for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="d913b-131">Returns S\_OK if successful.</span></span> <span data-ttu-id="d913b-132">Retorna E \_ OUTOFMEMORY se *ppCmd* retornar da criação do novo objeto [**CDeferredCommand**](cdeferredcommand.md) com um valor de **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d913b-132">Returns E\_OUTOFMEMORY if *ppCmd* returns from creating the new [**CDeferredCommand**](cdeferredcommand.md) object with a value of **NULL**.</span></span> <span data-ttu-id="d913b-133">Caso contrário, retorna um **HRESULT** que indica um erro ao tentar criar um novo objeto **CDeferredCommand** .</span><span class="sxs-lookup"><span data-stu-id="d913b-133">Otherwise, returns an **HRESULT** that indicates an error from attempting to create a new **CDeferredCommand** object.</span></span> <span data-ttu-id="d913b-134">Se houver um erro, nenhum objeto será colocado na fila.</span><span class="sxs-lookup"><span data-stu-id="d913b-134">If there is an error, no object has been queued.</span></span>

## <a name="remarks"></a><span data-ttu-id="d913b-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="d913b-135">Remarks</span></span>

<span data-ttu-id="d913b-136">O novo objeto [**CDeferredCommand**](cdeferredcommand.md) será inicializado com os parâmetros e será adicionado à fila durante a construção.</span><span class="sxs-lookup"><span data-stu-id="d913b-136">The new [**CDeferredCommand**](cdeferredcommand.md) object will be initialized with the parameters and will be added to the queue during construction.</span></span> <span data-ttu-id="d913b-137">Esse método é semelhante ao método **IDispatch:: Invoke** .</span><span class="sxs-lookup"><span data-stu-id="d913b-137">This method is similar to the **IDispatch::Invoke** method.</span></span>

<span data-ttu-id="d913b-138">Os valores para o parâmetro *wFlags* incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d913b-138">Values for the *wFlags* parameter include the following:</span></span>



| <span data-ttu-id="d913b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="d913b-139">Value</span></span>                    | <span data-ttu-id="d913b-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="d913b-140">Description</span></span>                                                                                                                                                          |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d913b-141">método de expedição \_</span><span class="sxs-lookup"><span data-stu-id="d913b-141">DISPATCH\_METHOD</span></span>         | <span data-ttu-id="d913b-142">O membro está sendo executado como um método.</span><span class="sxs-lookup"><span data-stu-id="d913b-142">The member is being run as a method.</span></span> <span data-ttu-id="d913b-143">Se uma propriedade tiver o mesmo nome, isso e o \_ sinalizador PROPERTYGET de expedição poderão ser definidos.</span><span class="sxs-lookup"><span data-stu-id="d913b-143">If a property has the same name, both this and the DISPATCH\_PROPERTYGET flag can be set.</span></span>                                       |
| <span data-ttu-id="d913b-144">PROPERTYGET de expedição \_</span><span class="sxs-lookup"><span data-stu-id="d913b-144">DISPATCH\_PROPERTYGET</span></span>    | <span data-ttu-id="d913b-145">O membro está sendo recuperado como uma propriedade ou um membro de dados.</span><span class="sxs-lookup"><span data-stu-id="d913b-145">The member is being retrieved as a property or data member.</span></span>                                                                                                          |
| <span data-ttu-id="d913b-146">PROPERTYPUT de expedição \_</span><span class="sxs-lookup"><span data-stu-id="d913b-146">DISPATCH\_PROPERTYPUT</span></span>    | <span data-ttu-id="d913b-147">O membro está sendo alterado como um membro de propriedade ou de dados.</span><span class="sxs-lookup"><span data-stu-id="d913b-147">The member is being changed as a property or data member.</span></span>                                                                                                            |
| <span data-ttu-id="d913b-148">PROPERTYPUTREF de expedição \_</span><span class="sxs-lookup"><span data-stu-id="d913b-148">DISPATCH\_PROPERTYPUTREF</span></span> | <span data-ttu-id="d913b-149">O membro está sendo alterado por meio de uma atribuição de referência, em vez de uma atribuição de valor.</span><span class="sxs-lookup"><span data-stu-id="d913b-149">The member is being changed via a reference assignment, rather than a value assignment.</span></span> <span data-ttu-id="d913b-150">Esse valor é válido somente quando a propriedade aceita uma referência a um objeto.</span><span class="sxs-lookup"><span data-stu-id="d913b-150">This value is valid only when the property accepts a reference to an object.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="d913b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d913b-151">Requirements</span></span>



| <span data-ttu-id="d913b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d913b-152">Requirement</span></span> | <span data-ttu-id="d913b-153">Valor</span><span class="sxs-lookup"><span data-stu-id="d913b-153">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d913b-154">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d913b-154">Header</span></span><br/>  | <dl> <span data-ttu-id="d913b-155"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d913b-155"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d913b-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d913b-156">Library</span></span><br/> | <dl> <span data-ttu-id="d913b-157"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d913b-157"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d913b-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="d913b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d913b-159">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="d913b-159">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




