---
title: função glGetError (GL. h)
description: A função glGetError retorna informações de erro.
ms.assetid: 18f0368f-054f-4b84-8397-3f9ee4aa07fa
keywords:
- função glGetError OpenGL
topic_type:
- apiref
api_name:
- glGetError
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c0abf6ec03ca0c29ede3b7d396db375fd06ac6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919004"
---
# <a name="glgeterror-function"></a><span data-ttu-id="6d676-104">função glGetError</span><span class="sxs-lookup"><span data-stu-id="6d676-104">glGetError function</span></span>

<span data-ttu-id="6d676-105">A função **glGetError** retorna informações de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-105">The **glGetError** function returns error information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d676-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d676-106">Syntax</span></span>


```C++
GLenum WINAPI glGetError(void);
```



## <a name="parameters"></a><span data-ttu-id="6d676-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6d676-107">Parameters</span></span>

<span data-ttu-id="6d676-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6d676-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6d676-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6d676-109">Return value</span></span>

<span data-ttu-id="6d676-110">A função **glGetError** retorna um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-110">The **glGetError** function returns one of the following error codes.</span></span>



| <span data-ttu-id="6d676-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6d676-111">Return code</span></span>                                                                                           | <span data-ttu-id="6d676-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d676-112">Description</span></span>                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6d676-113"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-113"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="6d676-114">Um valor inaceitável é especificado para um argumento enumerado.</span><span class="sxs-lookup"><span data-stu-id="6d676-114">An unacceptable value is specified for an enumerated argument.</span></span> <span data-ttu-id="6d676-115">A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-115">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>         |
| <dl> <span data-ttu-id="6d676-116"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-116"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="6d676-117">Um argumento numérico está fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="6d676-117">A numeric argument is out of range.</span></span> <span data-ttu-id="6d676-118">A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-118">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6d676-119"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="6d676-120">A operação especificada não é permitida no estado atual.</span><span class="sxs-lookup"><span data-stu-id="6d676-120">The specified operation is not allowed in the current state.</span></span> <span data-ttu-id="6d676-121">A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-121">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>           |
| <dl> <span data-ttu-id="6d676-122"><dt>**GL \_ sem \_ erro**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-122"><dt>**GL\_NO\_ERROR**</dt></span></span> </dl>          | <span data-ttu-id="6d676-123">Nenhum erro foi registrado.</span><span class="sxs-lookup"><span data-stu-id="6d676-123">No error has been recorded.</span></span> <span data-ttu-id="6d676-124">O valor dessa constante simbólica é garantido como zero.</span><span class="sxs-lookup"><span data-stu-id="6d676-124">The value of this symbolic constant is guaranteed to be zero.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="6d676-125"><dt>**\_estouro de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-125"><dt>**GL\_STACK\_OVERFLOW**</dt></span></span> </dl>    | <span data-ttu-id="6d676-126">Essa função causaria um estouro de pilha.</span><span class="sxs-lookup"><span data-stu-id="6d676-126">This function would cause a stack overflow.</span></span> <span data-ttu-id="6d676-127">A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-127">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                            |
| <dl> <span data-ttu-id="6d676-128"><dt>**\_estouro negativo de pilha GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-128"><dt>**GL\_STACK\_UNDERFLOW**</dt></span></span> </dl>   | <span data-ttu-id="6d676-129">Essa função causaria um estouro negativo de pilha.</span><span class="sxs-lookup"><span data-stu-id="6d676-129">This function would cause a stack underflow.</span></span> <span data-ttu-id="6d676-130">A função transgressor é ignorada, não tendo nenhum efeito colateral além de definir o sinalizador de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-130">The offending function is ignored, having no side effect other than to set the error flag.</span></span><br/>                           |
| <dl> <span data-ttu-id="6d676-131"><dt>**GL \_ sem \_ \_ memória**</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-131"><dt>**GL\_OUT\_OF\_MEMORY**</dt></span></span> </dl>    | <span data-ttu-id="6d676-132">Não há memória suficiente restante para executar a função.</span><span class="sxs-lookup"><span data-stu-id="6d676-132">There is not enough memory left to execute the function.</span></span> <span data-ttu-id="6d676-133">O estado do OpenGL é indefinido, exceto pelo Estado dos sinalizadores de erro, depois que esse erro é registrado.</span><span class="sxs-lookup"><span data-stu-id="6d676-133">The state of OpenGL is undefined, except for the state of the error flags, after this error is recorded.</span></span><br/> |



 

<span data-ttu-id="6d676-134">Observe que **glGetError** retorna GL \_ Operation inválida \_ se for chamado entre uma chamada para [**glBegin**](glbegin.md) e sua chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="6d676-134">Note that **glGetError** returns GL\_INVALID\_OPERATION if it is called between a call to [**glBegin**](glbegin.md) and its corresponding call to [**glEnd**](glend.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6d676-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="6d676-135">Remarks</span></span>

<span data-ttu-id="6d676-136">Cada erro detectável é atribuído a um código numérico e a um nome simbólico.</span><span class="sxs-lookup"><span data-stu-id="6d676-136">Each detectable error is assigned a numeric code and symbolic name.</span></span> <span data-ttu-id="6d676-137">Quando ocorre um erro, o sinalizador de erro é definido como o valor do código de erro apropriado.</span><span class="sxs-lookup"><span data-stu-id="6d676-137">When an error occurs, the error flag is set to the appropriate error code value.</span></span> <span data-ttu-id="6d676-138">Nenhum outro erro é registrado até que **glGetError** seja chamado, o código de erro é retornado e o sinalizador é redefinido para GL \_ sem \_ erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-138">No other errors are recorded until **glGetError** is called, the error code is returned, and the flag is reset to GL\_NO\_ERROR.</span></span> <span data-ttu-id="6d676-139">Se uma chamada para **glGetError** retornar GL \_ sem \_ erro, não haverá erro detectável desde a última chamada para **GlGetError** ou desde que o OpenGL foi inicializado.</span><span class="sxs-lookup"><span data-stu-id="6d676-139">If a call to **glGetError** returns GL\_NO\_ERROR, there has been no detectable error since the last call to **glGetError**, or since OpenGL was initialized.</span></span>

<span data-ttu-id="6d676-140">Para permitir implementações distribuídas, pode haver vários sinalizadores de erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-140">To allow for distributed implementations, there may be several error flags.</span></span> <span data-ttu-id="6d676-141">Se qualquer sinalizador de erro único gravou um erro, o valor desse sinalizador será retornado e esse sinalizador será redefinido como GL \_ sem \_ erro quando **glGetError** for chamado.</span><span class="sxs-lookup"><span data-stu-id="6d676-141">If any single error flag has recorded an error, the value of that flag is returned and that flag is reset to GL\_NO\_ERROR when **glGetError** is called.</span></span> <span data-ttu-id="6d676-142">Se mais de um sinalizador tiver registrado um erro, **glGetError** retornará e limpará um valor de sinalizador de erro arbitrário.</span><span class="sxs-lookup"><span data-stu-id="6d676-142">If more than one flag has recorded an error, **glGetError** returns and clears an arbitrary error flag value.</span></span> <span data-ttu-id="6d676-143">Se todos os sinalizadores de erro forem redefinidos, você sempre deverá chamar **glGetError** em um loop até que ele retorne o GL \_ sem \_ erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-143">If all error flags are to be reset, you should always call **glGetError** in a loop until it returns GL\_NO\_ERROR.</span></span>

<span data-ttu-id="6d676-144">Inicialmente, todos os sinalizadores de erro são definidos como GL \_ sem \_ erro.</span><span class="sxs-lookup"><span data-stu-id="6d676-144">Initially, all error flags are set to GL\_NO\_ERROR.</span></span>

<span data-ttu-id="6d676-145">Quando um sinalizador de erro é definido, os resultados de uma operação OpenGL são indefinidos somente se o GL \_ \_ \_ tiver ocorrido memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="6d676-145">When an error flag is set, results of an OpenGL operation are undefined only if GL\_OUT\_OF\_MEMORY has occurred.</span></span> <span data-ttu-id="6d676-146">Em todos os outros casos, a função que gera o erro é ignorada e não tem efeito sobre o estado do OpenGL ou o conteúdo do framebuffer.</span><span class="sxs-lookup"><span data-stu-id="6d676-146">In all other cases, the function generating the error is ignored and has no effect on the OpenGL state or framebuffer contents.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d676-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d676-147">Requirements</span></span>



| <span data-ttu-id="6d676-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d676-148">Requirement</span></span> | <span data-ttu-id="6d676-149">Valor</span><span class="sxs-lookup"><span data-stu-id="6d676-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6d676-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d676-150">Minimum supported client</span></span><br/> | <span data-ttu-id="6d676-151">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d676-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6d676-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d676-152">Minimum supported server</span></span><br/> | <span data-ttu-id="6d676-153">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="6d676-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6d676-154">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="6d676-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d676-155"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-155"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="6d676-156">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d676-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="6d676-157"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-157"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="6d676-158">DLL</span><span class="sxs-lookup"><span data-stu-id="6d676-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d676-159"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d676-159"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d676-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d676-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d676-161">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="6d676-161">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="6d676-162">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="6d676-162">**glEnd**</span></span>](glend.md)
</dt> </dl>

 

 





