---
title: função glFlush (GL. h)
description: A função glFlush força a execução de funções OpenGL em tempo finito.
ms.assetid: 7544b724-472f-4055-8f1c-64ddb58caaf3
keywords:
- função glFlush OpenGL
topic_type:
- apiref
api_name:
- glFlush
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8366fd5c42f68c495d544c20c3382b4e9fd37665
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645243"
---
# <a name="glflush-function"></a><span data-ttu-id="cf6ed-104">função glFlush</span><span class="sxs-lookup"><span data-stu-id="cf6ed-104">glFlush function</span></span>

<span data-ttu-id="cf6ed-105">A função **glFlush** força a execução de funções OpenGL em tempo finito.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-105">The **glFlush** function forces execution of OpenGL functions in finite time.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf6ed-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cf6ed-106">Syntax</span></span>


```C++
void WINAPI glFlush(void);
```



## <a name="parameters"></a><span data-ttu-id="cf6ed-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cf6ed-107">Parameters</span></span>

<span data-ttu-id="cf6ed-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cf6ed-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cf6ed-109">Return value</span></span>

<span data-ttu-id="cf6ed-110">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-110">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="cf6ed-111">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="cf6ed-111">Error codes</span></span>

<span data-ttu-id="cf6ed-112">O código de erro a seguir pode ser recuperado pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="cf6ed-112">The following error code can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="cf6ed-113">Nome</span><span class="sxs-lookup"><span data-stu-id="cf6ed-113">Name</span></span>                                                                                                  | <span data-ttu-id="cf6ed-114">Significado</span><span class="sxs-lookup"><span data-stu-id="cf6ed-114">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cf6ed-115"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ed-115"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="cf6ed-116">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="cf6ed-116">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cf6ed-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf6ed-117">Remarks</span></span>

<span data-ttu-id="cf6ed-118">Diferentes implementações do OpenGL armazenam comandos de buffer em vários locais diferentes, incluindo buffers de rede e o acelerador de gráficos em si.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-118">Different OpenGL implementations buffer commands in several different locations, including network buffers and the graphics accelerator itself.</span></span> <span data-ttu-id="cf6ed-119">A função **glFlush** esvazia todos esses buffers, fazendo com que todos os comandos emitidos sejam executados tão rapidamente quanto são aceitos pelo mecanismo de renderização real.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-119">The **glFlush** function empties all these buffers, causing all issued commands to be executed as quickly as they are accepted by the actual rendering engine.</span></span> <span data-ttu-id="cf6ed-120">Embora essa execução não possa ser concluída em nenhum período de tempo específico, ela é concluída em uma quantidade finita de tempo.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-120">Though this execution may not be completed in any particular time period, it does complete in a finite amount of time.</span></span>

<span data-ttu-id="cf6ed-121">Como qualquer programa OpenGL pode ser executado em uma rede ou em um acelerador que armazena em buffer os comandos, certifique-se de chamar **glFlush** em todos os programas que exigem que todos os comandos emitidos anteriormente tenham sido concluídos.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-121">Because any OpenGL program might be executed over a network, or on an accelerator that buffers commands, be sure to call **glFlush** in any programs requiring that all of their previously issued commands have been completed.</span></span> <span data-ttu-id="cf6ed-122">Por exemplo, chame **glFlush** antes de aguardar a entrada do usuário que depende da imagem gerada.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-122">For example, call **glFlush** before waiting for user input that depends on the generated image.</span></span>

<span data-ttu-id="cf6ed-123">A função **glFlush** pode retornar a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-123">The **glFlush** function can return at any time.</span></span> <span data-ttu-id="cf6ed-124">Ele não aguarda até que a execução de todas as funções OpenGL emitidas anteriormente seja concluída.</span><span class="sxs-lookup"><span data-stu-id="cf6ed-124">It does not wait until the execution of all previously issued OpenGL functions is complete.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf6ed-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf6ed-125">Requirements</span></span>



| <span data-ttu-id="cf6ed-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf6ed-126">Requirement</span></span> | <span data-ttu-id="cf6ed-127">Valor</span><span class="sxs-lookup"><span data-stu-id="cf6ed-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf6ed-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf6ed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cf6ed-129">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf6ed-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="cf6ed-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf6ed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cf6ed-131">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf6ed-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cf6ed-132">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf6ed-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf6ed-133"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ed-133"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="cf6ed-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cf6ed-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="cf6ed-135"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ed-135"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="cf6ed-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cf6ed-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf6ed-137"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf6ed-137"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf6ed-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf6ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf6ed-139">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="cf6ed-139">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="cf6ed-140">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="cf6ed-140">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="cf6ed-141">**glFinish**</span><span class="sxs-lookup"><span data-stu-id="cf6ed-141">**glFinish**</span></span>](glfinish.md)
</dt> </dl>

 

 





