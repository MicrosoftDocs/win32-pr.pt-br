---
title: função gluQuadricCallback (Glu. h)
description: A função gluQuadricCallback define um retorno de chamada para um objeto Quadric.
ms.assetid: 1f1e9fe9-7239-419c-92b6-af2534850ac5
keywords:
- função gluQuadricCallback OpenGL
topic_type:
- apiref
api_name:
- gluQuadricCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c0c92e3cd4e723b59ee9060c5e2f33b710e7f69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499586"
---
# <a name="gluquadriccallback-function"></a><span data-ttu-id="ed643-104">função gluQuadricCallback</span><span class="sxs-lookup"><span data-stu-id="ed643-104">gluQuadricCallback function</span></span>

<span data-ttu-id="ed643-105">A função **gluQuadricCallback** define um retorno de chamada para um objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="ed643-105">The **gluQuadricCallback** function defines a callback for a quadric object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed643-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed643-106">Syntax</span></span>


```C++
void WINAPI gluQuadricCallback(
   GLUquadric *qobj,
   GLenum     which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="ed643-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed643-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed643-108">*qobj*</span><span class="sxs-lookup"><span data-stu-id="ed643-108">*qobj*</span></span> 
</dt> <dd>

<span data-ttu-id="ed643-109">O objeto Quadric (criado com [**gluNewQuadric**](glunewquadric.md)).</span><span class="sxs-lookup"><span data-stu-id="ed643-109">The quadric object (created with [**gluNewQuadric**](glunewquadric.md)).</span></span>

</dd> <dt>

<span data-ttu-id="ed643-110">*Onde*</span><span class="sxs-lookup"><span data-stu-id="ed643-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="ed643-111">O retorno de chamada que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="ed643-111">The callback being defined.</span></span> <span data-ttu-id="ed643-112">O único valor válido é GLU \_ Error.</span><span class="sxs-lookup"><span data-stu-id="ed643-112">The only valid value is GLU\_ERROR.</span></span>



| <span data-ttu-id="ed643-113">Valor</span><span class="sxs-lookup"><span data-stu-id="ed643-113">Value</span></span>                                                                                                                                             | <span data-ttu-id="ed643-114">Significado</span><span class="sxs-lookup"><span data-stu-id="ed643-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GLU_ERROR"></span><span id="glu_error"></span><dl> <span data-ttu-id="ed643-115"><dt>**erro de GLU \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ed643-115"><dt>**GLU\_ERROR**</dt></span></span> </dl> | <span data-ttu-id="ed643-116">A função **gluQuadricCallback** é chamada quando um erro é encontrado.</span><span class="sxs-lookup"><span data-stu-id="ed643-116">The **gluQuadricCallback** function is called when an error is encountered.</span></span> <span data-ttu-id="ed643-117">Seu único argumento é do tipo **GLenum** e indica o erro específico que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="ed643-117">Its single argument is of type **GLenum**, and it indicates the specific error that occurred.</span></span> <span data-ttu-id="ed643-118">As cadeias de caracteres que descrevem esses erros podem ser recuperadas com a chamada [**gluErrorString**](gluerrorstring.md) .</span><span class="sxs-lookup"><span data-stu-id="ed643-118">Character strings describing these errors can be retrieved with the [**gluErrorString**](gluerrorstring.md) call.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ed643-119">*fn*</span><span class="sxs-lookup"><span data-stu-id="ed643-119">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="ed643-120">A função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="ed643-120">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed643-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed643-121">Return value</span></span>

<span data-ttu-id="ed643-122">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ed643-122">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed643-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed643-123">Remarks</span></span>

<span data-ttu-id="ed643-124">Use **gluQuadricCallback** para definir um novo retorno de chamada a ser usado por um objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="ed643-124">Use **gluQuadricCallback** to define a new callback to be used by a quadric object.</span></span> <span data-ttu-id="ed643-125">Se o retorno de chamada especificado já estiver definido, ele será substituído.</span><span class="sxs-lookup"><span data-stu-id="ed643-125">If the specified callback is already defined, it is replaced.</span></span> <span data-ttu-id="ed643-126">Se *FN* for **NULL**, qualquer retorno de chamada existente será apagado.</span><span class="sxs-lookup"><span data-stu-id="ed643-126">If *fn* is **NULL**, any existing callback is erased.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed643-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed643-127">Requirements</span></span>



| <span data-ttu-id="ed643-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed643-128">Requirement</span></span> | <span data-ttu-id="ed643-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ed643-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ed643-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed643-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ed643-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed643-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ed643-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ed643-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ed643-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ed643-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ed643-134">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ed643-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="ed643-135"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="ed643-135"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="ed643-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed643-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="ed643-137"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ed643-137"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="ed643-138">DLL</span><span class="sxs-lookup"><span data-stu-id="ed643-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed643-139"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed643-139"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed643-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed643-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed643-141">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="ed643-141">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="ed643-142">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="ed643-142">**gluNewQuadric**</span></span>](glunewquadric.md)
</dt> </dl>

 

 





