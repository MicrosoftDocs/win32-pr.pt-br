---
title: função glFinish (GL. h)
description: A função glFinish é bloqueada até que toda a execução de OpenGL seja concluída.
ms.assetid: 1dcb4767-02ea-41d8-bf1f-d61d20873d4f
keywords:
- função glFinish OpenGL
topic_type:
- apiref
api_name:
- glFinish
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4731ffc91dbb8d31137a792b59d3ebc36bb4d5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499825"
---
# <a name="glfinish-function"></a><span data-ttu-id="630e4-104">função glFinish</span><span class="sxs-lookup"><span data-stu-id="630e4-104">glFinish function</span></span>

<span data-ttu-id="630e4-105">A função **glFinish** é bloqueada até que toda a execução de OpenGL seja concluída.</span><span class="sxs-lookup"><span data-stu-id="630e4-105">The **glFinish** function blocks until all OpenGL execution is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="630e4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="630e4-106">Syntax</span></span>


```C++
void WINAPI glFinish(void);
```



## <a name="parameters"></a><span data-ttu-id="630e4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="630e4-107">Parameters</span></span>

<span data-ttu-id="630e4-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="630e4-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="630e4-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="630e4-109">Return value</span></span>

<span data-ttu-id="630e4-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="630e4-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="630e4-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="630e4-111">Error codes</span></span>

<span data-ttu-id="630e4-112">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="630e4-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="630e4-113">Nome</span><span class="sxs-lookup"><span data-stu-id="630e4-113">Name</span></span>                                                                                                  | <span data-ttu-id="630e4-114">Significado</span><span class="sxs-lookup"><span data-stu-id="630e4-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="630e4-115"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="630e4-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="630e4-116">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="630e4-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="630e4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="630e4-117">Remarks</span></span>

<span data-ttu-id="630e4-118">A função **glFinish** não retorna até que os efeitos de todas as funções OpenGL previamente chamadas sejam concluídos.</span><span class="sxs-lookup"><span data-stu-id="630e4-118">The **glFinish** function does not return until the effects of all previously called OpenGL functions are complete.</span></span> <span data-ttu-id="630e4-119">Esses efeitos incluem todas as alterações no estado OpenGL, todas as alterações no estado da conexão e todas as alterações no conteúdo do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="630e4-119">Such effects include all changes to the OpenGL state, all changes to the connection state, and all changes to the framebuffer contents.</span></span>

<span data-ttu-id="630e4-120">A função **glFinish** requer uma viagem de ida e volta ao servidor.</span><span class="sxs-lookup"><span data-stu-id="630e4-120">The **glFinish** function requires a round trip to the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="630e4-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="630e4-121">Requirements</span></span>



| <span data-ttu-id="630e4-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="630e4-122">Requirement</span></span> | <span data-ttu-id="630e4-123">Valor</span><span class="sxs-lookup"><span data-stu-id="630e4-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="630e4-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="630e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="630e4-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="630e4-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="630e4-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="630e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="630e4-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="630e4-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="630e4-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="630e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="630e4-129"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="630e4-129"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="630e4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="630e4-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="630e4-131"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="630e4-131"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="630e4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="630e4-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="630e4-133"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="630e4-133"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="630e4-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="630e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="630e4-135">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="630e4-135">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="630e4-136">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="630e4-136">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="630e4-137">**glFlush**</span><span class="sxs-lookup"><span data-stu-id="630e4-137">**glFlush**</span></span>](glflush.md)
</dt> </dl>

 

 





