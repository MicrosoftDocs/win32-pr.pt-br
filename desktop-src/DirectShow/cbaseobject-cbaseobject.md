---
description: Método de construtor.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Construtor CBaseObject. CBaseObject (combase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756643"
---
# <a name="cbaseobjectcbaseobject-constructor"></a><span data-ttu-id="e9ac8-103">Construtor CBaseObject. CBaseObject</span><span class="sxs-lookup"><span data-stu-id="e9ac8-103">CBaseObject.CBaseObject constructor</span></span>

<span data-ttu-id="e9ac8-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e9ac8-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9ac8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e9ac8-105">Syntax</span></span>


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a><span data-ttu-id="e9ac8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e9ac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9ac8-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e9ac8-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e9ac8-108">Cadeia de caracteres que contém o nome do objeto, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="e9ac8-108">String that contains the name of the object, for debugging purposes.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e9ac8-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9ac8-109">Remarks</span></span>

<span data-ttu-id="e9ac8-110">Esse método incrementa a contagem de objetos ativos.</span><span class="sxs-lookup"><span data-stu-id="e9ac8-110">This method increments the active-object count.</span></span> <span data-ttu-id="e9ac8-111">(Consulte [**CBaseObject:: ObjectsActive**](cbaseobject-objectsactive.md).)</span><span class="sxs-lookup"><span data-stu-id="e9ac8-111">(See [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)</span></span>

<span data-ttu-id="e9ac8-112">Aloque o parâmetro *pname* na memória estática:</span><span class="sxs-lookup"><span data-stu-id="e9ac8-112">Allocate the *pName* parameter in static memory:</span></span>


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



<span data-ttu-id="e9ac8-113">A macro de [**nome**](name.md) compila como **NULL** em compilações de varejo, para que as cadeias de caracteres estáticas apareçam somente em compilações de depuração.</span><span class="sxs-lookup"><span data-stu-id="e9ac8-113">The [**NAME**](name.md) macro compiles to **NULL** in retail builds, so that static strings appear only in debug builds.</span></span> <span data-ttu-id="e9ac8-114">Para obter mais informações, consulte [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span><span class="sxs-lookup"><span data-stu-id="e9ac8-114">For more information, see [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e9ac8-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9ac8-115">Requirements</span></span>



| <span data-ttu-id="e9ac8-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9ac8-116">Requirement</span></span> | <span data-ttu-id="e9ac8-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e9ac8-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9ac8-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9ac8-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e9ac8-119"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ac8-119"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e9ac8-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9ac8-120">Library</span></span><br/> | <dl> <span data-ttu-id="e9ac8-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e9ac8-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9ac8-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9ac8-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9ac8-123">**Classe CBaseObject**</span><span class="sxs-lookup"><span data-stu-id="e9ac8-123">**CBaseObject Class**</span></span>](cbaseobject.md)
</dt> </dl>

 

 




