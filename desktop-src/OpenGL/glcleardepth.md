---
title: função glClearDepth (GL. h)
description: A função glClearDepth especifica o valor claro para o buffer de profundidade.
ms.assetid: 8e26ae78-edc1-4201-a0db-d5bc8ae6dc82
keywords:
- função glClearDepth OpenGL
topic_type:
- apiref
api_name:
- glClearDepth
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cf968c7ae172bf4ce354c84b2071d62304327ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295804"
---
# <a name="glcleardepth-function"></a><span data-ttu-id="e082d-104">função glClearDepth</span><span class="sxs-lookup"><span data-stu-id="e082d-104">glClearDepth function</span></span>

<span data-ttu-id="e082d-105">A função **glClearDepth** especifica o valor claro para o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e082d-105">The **glClearDepth** function specifies the clear value for the depth buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="e082d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e082d-106">Syntax</span></span>


```C++
void WINAPI glClearDepth(
   GLclampd depth
);
```



## <a name="parameters"></a><span data-ttu-id="e082d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e082d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e082d-108">*Detalhado*</span><span class="sxs-lookup"><span data-stu-id="e082d-108">*depth*</span></span> 
</dt> <dd>

<span data-ttu-id="e082d-109">O valor de profundidade usado quando o buffer de profundidade é limpo.</span><span class="sxs-lookup"><span data-stu-id="e082d-109">The depth value used when the depth buffer is cleared.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e082d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e082d-110">Return value</span></span>

<span data-ttu-id="e082d-111">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e082d-111">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e082d-112">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e082d-112">Error codes</span></span>

<span data-ttu-id="e082d-113">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e082d-113">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e082d-114">Nome</span><span class="sxs-lookup"><span data-stu-id="e082d-114">Name</span></span>                                                                                                  | <span data-ttu-id="e082d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="e082d-115">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e082d-116"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e082d-116"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e082d-117">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e082d-117">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="e082d-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="e082d-118">Remarks</span></span>

<span data-ttu-id="e082d-119">A função **glClearDepth** especifica o valor de profundidade usado pelo [**glClear**](glclear.md) para limpar o buffer de profundidade.</span><span class="sxs-lookup"><span data-stu-id="e082d-119">The **glClearDepth** function specifies the depth value used by [**glClear**](glclear.md) to clear the depth buffer.</span></span> <span data-ttu-id="e082d-120">Os valores especificados por **glClearDepth** são clamped para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="e082d-120">Values specified by **glClearDepth** are clamped to the range \[0,1\].</span></span>

<span data-ttu-id="e082d-121">A função a seguir recupera informações relacionadas à função **glClearDepth** :</span><span class="sxs-lookup"><span data-stu-id="e082d-121">The following function retrieves information related to the **glClearDepth** function:</span></span>

<span data-ttu-id="e082d-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com \_ \_ valor claro de profundidade do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="e082d-122">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_DEPTH\_CLEAR\_VALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="e082d-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e082d-123">Requirements</span></span>



| <span data-ttu-id="e082d-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="e082d-124">Requirement</span></span> | <span data-ttu-id="e082d-125">Valor</span><span class="sxs-lookup"><span data-stu-id="e082d-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e082d-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e082d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="e082d-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e082d-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e082d-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e082d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="e082d-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e082d-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e082d-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e082d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="e082d-131"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e082d-131"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e082d-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e082d-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="e082d-133"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e082d-133"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e082d-134">DLL</span><span class="sxs-lookup"><span data-stu-id="e082d-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e082d-135"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e082d-135"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e082d-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="e082d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e082d-137">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e082d-137">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e082d-138">**glClear**</span><span class="sxs-lookup"><span data-stu-id="e082d-138">**glClear**</span></span>](glclear.md)
</dt> <dt>

[<span data-ttu-id="e082d-139">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e082d-139">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e082d-140">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e082d-140">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> </dl>

 

 





