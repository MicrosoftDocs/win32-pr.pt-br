---
title: função glReadBuffer (GL. h)
description: A função glReadBuffer seleciona uma fonte de buffer de cores para pixels.
ms.assetid: 734153fa-e809-4b70-867e-55e46ab95712
keywords:
- função glReadBuffer OpenGL
topic_type:
- apiref
api_name:
- glReadBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59f0e88cdcb2b1b3257b23606f8160e0986584db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758032"
---
# <a name="glreadbuffer-function"></a><span data-ttu-id="f46b0-104">função glReadBuffer</span><span class="sxs-lookup"><span data-stu-id="f46b0-104">glReadBuffer function</span></span>

<span data-ttu-id="f46b0-105">A função **glReadBuffer** seleciona uma fonte de buffer de cores para pixels.</span><span class="sxs-lookup"><span data-stu-id="f46b0-105">The **glReadBuffer** function selects a color buffer source for pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="f46b0-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f46b0-106">Syntax</span></span>


```C++
void WINAPI glReadBuffer(
   GLenum mode
);
```



## <a name="parameters"></a><span data-ttu-id="f46b0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f46b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f46b0-108">*mode*</span><span class="sxs-lookup"><span data-stu-id="f46b0-108">*mode*</span></span> 
</dt> <dd>

<span data-ttu-id="f46b0-109">Um buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="f46b0-109">A color buffer.</span></span> <span data-ttu-id="f46b0-110">Os valores aceitos são GL \_ frontal \_ esquerdo, GL \_ frontal \_ direito, GL \_ traseiro \_ esquerdo, GL \_ traseiro \_ direito, GL \_ frontal, GL \_ voltar, GL \_ Left, GL \_ direito e GL \_ aux *i*, onde *estou* entre 0 e GL \_ \_ buffers Aux 1.</span><span class="sxs-lookup"><span data-stu-id="f46b0-110">Accepted values are GL\_FRONT\_LEFT, GL\_FRONT\_RIGHT, GL\_BACK\_LEFT, GL\_BACK\_RIGHT, GL\_FRONT, GL\_BACK, GL\_LEFT, GL\_RIGHT, and GL\_AUX *i*, where *i* is between 0 and GL\_AUX\_BUFFERS 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f46b0-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f46b0-111">Return value</span></span>

<span data-ttu-id="f46b0-112">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="f46b0-112">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f46b0-113">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="f46b0-113">Error codes</span></span>

<span data-ttu-id="f46b0-114">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="f46b0-114">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="f46b0-115">Nome</span><span class="sxs-lookup"><span data-stu-id="f46b0-115">Name</span></span>                                                                                                  | <span data-ttu-id="f46b0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="f46b0-116">Meaning</span></span>                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f46b0-117"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="f46b0-117"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="f46b0-118">o *modo* não era um dos doze (ou mais) valores aceitos.</span><span class="sxs-lookup"><span data-stu-id="f46b0-118">*mode* was not an one of the twelve (or more) accepted values.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="f46b0-119"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f46b0-119"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f46b0-120">o *modo* especificou um buffer que não existe.</span><span class="sxs-lookup"><span data-stu-id="f46b0-120">*mode* specified a buffer that does not exist.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="f46b0-121"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f46b0-121"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="f46b0-122">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="f46b0-122">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f46b0-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="f46b0-123">Remarks</span></span>

<span data-ttu-id="f46b0-124">A função **glReadBuffer** especifica um buffer de cores como a origem para os comandos [**glReadPixels**](glreadpixels.md) e [**glCopyPixels**](glcopypixels.md) subsequentes.</span><span class="sxs-lookup"><span data-stu-id="f46b0-124">The **glReadBuffer** function specifies a color buffer as the source for subsequent [**glReadPixels**](glreadpixels.md) and [**glCopyPixels**](glcopypixels.md) commands.</span></span> <span data-ttu-id="f46b0-125">O parâmetro *Mode* aceita um de doze ou mais valores predefinidos.</span><span class="sxs-lookup"><span data-stu-id="f46b0-125">The *mode* parameter accepts one of twelve or more predefined values.</span></span> <span data-ttu-id="f46b0-126">(GL \_ AUX0 por meio do GL \_ AUX3 são sempre definidos.) Em um sistema totalmente configurado, \_ o GL frontal, GL \_ Left e GL \_ front \_ Left, todos os nomes o buffer frontal esquerdo, o GL \_ front \_ Right e GL \_ Right Name o buffer frontal direito, e GL \_ back \_ Left e GL \_ back name The Back-Left buffer.</span><span class="sxs-lookup"><span data-stu-id="f46b0-126">(GL\_AUX0 through GL\_AUX3 are always defined.) In a fully configured system, GL\_FRONT, GL\_LEFT, and GL\_FRONT\_LEFT all name the front-left buffer, GL\_FRONT\_RIGHT and GL\_RIGHT name the front-right buffer, and GL\_BACK\_LEFT and GL\_BACK name the back-left buffer.</span></span>

<span data-ttu-id="f46b0-127">As configurações de buffer duplo não estéreo têm apenas um buffer frontal esquerdo e um back-Left.</span><span class="sxs-lookup"><span data-stu-id="f46b0-127">Nonstereo double-buffered configurations have only a front-left and a back-left buffer.</span></span> <span data-ttu-id="f46b0-128">Configurações de buffer único têm um buffer front-Left e um front-Right se estéreo e apenas um buffer de front-Left se não estéreo.</span><span class="sxs-lookup"><span data-stu-id="f46b0-128">Single-buffered configurations have a front-left and a front-right buffer if stereo, and only a front-left buffer if nonstereo.</span></span> <span data-ttu-id="f46b0-129">É um erro especificar um buffer inexistente para **glReadBuffer**.</span><span class="sxs-lookup"><span data-stu-id="f46b0-129">It is an error to specify a nonexistent buffer to **glReadBuffer**.</span></span>

<span data-ttu-id="f46b0-130">Por padrão, o *modo* é GL \_ frontal em configurações de buffer único e o GL \_ volta em configurações de buffer duplo.</span><span class="sxs-lookup"><span data-stu-id="f46b0-130">By default, *mode* is GL\_FRONT in single-buffered configurations, and GL\_BACK in double-buffered configurations.</span></span>

<span data-ttu-id="f46b0-131">A função a seguir recupera informações relacionadas a **glReadBuffer**:</span><span class="sxs-lookup"><span data-stu-id="f46b0-131">The following function retrieves information related to **glReadBuffer**:</span></span>

<span data-ttu-id="f46b0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ buffer de leitura do argumento GL \_</span><span class="sxs-lookup"><span data-stu-id="f46b0-132">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_READ\_BUFFER</span></span>

## <a name="requirements"></a><span data-ttu-id="f46b0-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f46b0-133">Requirements</span></span>



| <span data-ttu-id="f46b0-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f46b0-134">Requirement</span></span> | <span data-ttu-id="f46b0-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f46b0-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f46b0-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f46b0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f46b0-137">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f46b0-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f46b0-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f46b0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f46b0-139">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f46b0-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f46b0-140">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="f46b0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f46b0-141"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="f46b0-141"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="f46b0-142">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f46b0-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="f46b0-143"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f46b0-143"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="f46b0-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f46b0-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f46b0-145"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f46b0-145"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f46b0-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="f46b0-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f46b0-147">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="f46b0-147">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="f46b0-148">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="f46b0-148">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="f46b0-149">**glDrawBuffer**</span><span class="sxs-lookup"><span data-stu-id="f46b0-149">**glDrawBuffer**</span></span>](gldrawbuffer.md)
</dt> <dt>

[<span data-ttu-id="f46b0-150">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="f46b0-150">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="f46b0-151">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="f46b0-151">**glReadPixels**</span></span>](glreadpixels.md)
</dt> </dl>

 

 





