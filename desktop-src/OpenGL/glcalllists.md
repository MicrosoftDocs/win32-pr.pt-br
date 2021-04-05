---
title: função glCallLists (GL. h)
description: A função glCallLists executa uma lista de listas de exibição.
ms.assetid: 7c0a00df-91ee-44ad-9e02-97c1b078e87f
keywords:
- função glCallLists OpenGL
topic_type:
- apiref
api_name:
- glCallLists
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a119f3a63b0f04140a72cc5ca818833ae9ea8b20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918587"
---
# <a name="glcalllists-function"></a><span data-ttu-id="4a6f8-104">função glCallLists</span><span class="sxs-lookup"><span data-stu-id="4a6f8-104">glCallLists function</span></span>

<span data-ttu-id="4a6f8-105">A função **glCallLists** executa uma lista de listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-105">The **glCallLists** function executes a list of display lists.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a6f8-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4a6f8-106">Syntax</span></span>


```C++
void WINAPI glCallLists(
         GLsizei n,
         GLenum  type,
   const GLvoid  *lists
);
```



## <a name="parameters"></a><span data-ttu-id="4a6f8-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4a6f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a6f8-108">*n*</span><span class="sxs-lookup"><span data-stu-id="4a6f8-108">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6f8-109">O número de listas de exibição a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-109">The number of display lists to be executed.</span></span>

</dd> <dt>

<span data-ttu-id="4a6f8-110">*tipo*</span><span class="sxs-lookup"><span data-stu-id="4a6f8-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6f8-111">O tipo de valores em *listas*.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-111">The type of values in *lists*.</span></span> <span data-ttu-id="4a6f8-112">As constantes simbólicas a seguir são aceitas.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-112">The following symbolic constants are accepted.</span></span>



| <span data-ttu-id="4a6f8-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4a6f8-113">Value</span></span>                                                                                                                                                                      | <span data-ttu-id="4a6f8-114">Significado</span><span class="sxs-lookup"><span data-stu-id="4a6f8-114">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_BYTE"></span><span id="gl_byte"></span><dl> <span data-ttu-id="4a6f8-115"><dt>**\_byte GL**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-115"><dt>**GL\_BYTE**</dt></span></span> </dl>                                | <span data-ttu-id="4a6f8-116">O parâmetro *Lists* é tratado como uma matriz de bytes assinados, cada um no intervalo de-128 a 127.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-116">The *lists* parameter is treated as an array of signed bytes, each in the range -128 through 127.</span></span><br/>                                                                                                                                                                                                                                                                                       |
| <span id="GL_UNSIGNED_BYTE"></span><span id="gl_unsigned_byte"></span><dl> <span data-ttu-id="4a6f8-117"><dt>**\_byte não assinado GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-117"><dt>**GL\_UNSIGNED\_BYTE**</dt></span></span> </dl>    | <span data-ttu-id="4a6f8-118">O parâmetro *Lists* é tratado como uma matriz de bytes não assinados, cada um no intervalo de 0 a 255.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-118">The *lists* parameter is treated as an array of unsigned bytes, each in the range 0 through 255.</span></span><br/>                                                                                                                                                                                                                                                                                        |
| <span id="GL_SHORT"></span><span id="gl_short"></span><dl> <span data-ttu-id="4a6f8-119"><dt>**GL \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-119"><dt>**GL\_SHORT**</dt></span></span> </dl>                             | <span data-ttu-id="4a6f8-120">O parâmetro *Lists* é tratado como uma matriz de inteiros de 2 bytes assinados, cada um no intervalo de-32768 a 32767.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-120">The *lists* parameter is treated as an array of signed 2-byte integers, each in the range -32768 through 32767.</span></span><br/>                                                                                                                                                                                                                                                                         |
| <span id="GL_UNSIGNED_SHORT"></span><span id="gl_unsigned_short"></span><dl> <span data-ttu-id="4a6f8-121"><dt>**GL \_ não assinado \_ curto**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-121"><dt>**GL\_UNSIGNED\_SHORT**</dt></span></span> </dl> | <span data-ttu-id="4a6f8-122">O parâmetro *Lists* é tratado como uma matriz de inteiros de 2 bytes não assinados, cada um no intervalo de 0 a 65535.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-122">The *lists* parameter is treated as an array of unsigned 2-byte integers, each in the range 0 through 65535.</span></span><br/>                                                                                                                                                                                                                                                                            |
| <span id="GL_INT"></span><span id="gl_int"></span><dl> <span data-ttu-id="4a6f8-123"><dt>**RAZÃO \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-123"><dt>**GL\_INT**</dt></span></span> </dl>                                   | <span data-ttu-id="4a6f8-124">O parâmetro *Lists* é tratado como uma matriz de inteiros de 4 bytes assinados.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-124">The *lists* parameter is treated as an array of signed 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_UNSIGNED_INT"></span><span id="gl_unsigned_int"></span><dl> <span data-ttu-id="4a6f8-125"><dt>**GL \_ não assinado \_ int**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-125"><dt>**GL\_UNSIGNED\_INT**</dt></span></span> </dl>       | <span data-ttu-id="4a6f8-126">O parâmetro *Lists* é tratado como uma matriz de inteiros de 4 bytes sem sinal.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-126">The *lists* parameter is treated as an array of unsigned 4-byte integers.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="GL_FLOAT"></span><span id="gl_float"></span><dl> <span data-ttu-id="4a6f8-127"><dt>**GL \_ float**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-127"><dt>**GL\_FLOAT**</dt></span></span> </dl>                             | <span data-ttu-id="4a6f8-128">O parâmetro *Lists* é tratado como uma matriz de valores de ponto flutuante de 4 bytes.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-128">The *lists* parameter is treated as an array of 4-byte, floating-point values.</span></span><br/>                                                                                                                                                                                                                                                                                                          |
| <span id="GL_2_BYTES"></span><span id="gl_2_bytes"></span><dl> <span data-ttu-id="4a6f8-129"><dt>**GL \_ 2 \_ bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-129"><dt>**GL\_2\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="4a6f8-130">O parâmetro *Lists* é tratado como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-130">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="4a6f8-131">Cada par de bytes especifica um único nome de lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-131">Each pair of bytes specifies a single display-list name.</span></span> <span data-ttu-id="4a6f8-132">O valor do par é calculado como 256 vezes o valor não assinado do primeiro byte mais o valor não assinado do segundo byte.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-132">The value of the pair is computed as 256 times the unsigned value of the first byte plus the unsigned value of the second byte.</span></span><br/>                                                                                                                                |
| <span id="GL_3_BYTES"></span><span id="gl_3_bytes"></span><dl> <span data-ttu-id="4a6f8-133"><dt>**GL \_ 3 \_ bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-133"><dt>**GL\_3\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="4a6f8-134">O parâmetro *Lists* é tratado como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-134">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="4a6f8-135">Cada terceto de bytes especifica um único nome de lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-135">Each triplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="4a6f8-136">O valor de terceto é calculado como 65536 vezes o valor não assinado do primeiro byte, além de 256 vezes o valor não assinado do segundo byte, mais o valor não assinado do terceiro byte.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-136">The value of the triplet is computed as 65536 times the unsigned value of the first byte, plus 256 times the unsigned value of the second byte, plus the unsigned value of the third byte.</span></span><br/>                                                                  |
| <span id="GL_4_BYTES"></span><span id="gl_4_bytes"></span><dl> <span data-ttu-id="4a6f8-137"><dt>**GL \_ 4 \_ bytes**</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-137"><dt>**GL\_4\_BYTES**</dt></span></span> </dl>                      | <span data-ttu-id="4a6f8-138">O parâmetro *Lists* é tratado como uma matriz de bytes não assinados.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-138">The *lists* parameter is treated as an array of unsigned bytes.</span></span> <span data-ttu-id="4a6f8-139">Cada quadruplet de bytes especifica um único nome de lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-139">Each quadruplet of bytes specifies a single display list name.</span></span> <span data-ttu-id="4a6f8-140">O valor de quadruplet é computado como 16777216 vezes o valor não assinado do primeiro byte, além de 65536 vezes o valor não assinado do segundo byte, além de 256 vezes o valor não assinado do terceiro byte, mais o valor não assinado do quarto byte.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-140">The value of the quadruplet is computed as 16777216 times the unsigned value of the first byte, plus 65536 times the unsigned value of the second byte, plus 256 times the unsigned value of the third byte, plus the unsigned value of the fourth byte.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4a6f8-141">*lista*</span><span class="sxs-lookup"><span data-stu-id="4a6f8-141">*lists*</span></span> 
</dt> <dd>

<span data-ttu-id="4a6f8-142">O endereço de uma matriz de deslocamentos de nome na lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-142">The address of an array of name offsets in the display list.</span></span> <span data-ttu-id="4a6f8-143">O tipo de ponteiro é void porque os deslocamentos podem ser bytes, short, ints ou floats, dependendo do valor do *tipo*.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-143">The pointer type is void because the offsets can be bytes, shorts, ints, or floats, depending on the value of *type*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a6f8-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4a6f8-144">Return value</span></span>

<span data-ttu-id="4a6f8-145">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-145">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a6f8-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="4a6f8-146">Remarks</span></span>

<span data-ttu-id="4a6f8-147">A função **glCallLists** faz com que cada lista de exibição na lista de nomes seja passada como *listas* a serem executadas.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-147">The **glCallLists** function causes each display list in the list of names passed as *lists* to be executed.</span></span> <span data-ttu-id="4a6f8-148">Como resultado, as funções salvas em cada lista de exibição são executadas em ordem, assim como se elas fossem chamadas sem usar uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-148">As a result, the functions saved in each display list are executed in order, just as if they were called without using a display list.</span></span> <span data-ttu-id="4a6f8-149">Os nomes das listas de exibição que não foram definidas são ignorados.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-149">Names of display lists that have not been defined are ignored.</span></span>

<span data-ttu-id="4a6f8-150">A função **glCallLists** fornece um meio eficiente para executar listas de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-150">The **glCallLists** function provides an efficient means for executing display lists.</span></span> <span data-ttu-id="4a6f8-151">O parâmetro *n* especifica o número de listas com vários formatos de nome (especificados pelo parâmetro de *tipo* ) **glCallLists** executado.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-151">The *n* parameter specifies the number of lists with various name formats (specified by the *type* parameter) **glCallLists** executes.</span></span>

<span data-ttu-id="4a6f8-152">A lista de nomes de listas de exibição não é terminada em nulo.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-152">The list of display list names is not null-terminated.</span></span> <span data-ttu-id="4a6f8-153">Em vez disso, *n* especifica quantos nomes devem ser obtidos de *listas*.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-153">Rather, *n* specifies how many names are to be taken from *lists*.</span></span>

<span data-ttu-id="4a6f8-154">A função [**glListBase**](gllistbase.md) torna um nível adicional de indireção disponível.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-154">The [**glListBase**](gllistbase.md) function makes an additional level of indirection available.</span></span> <span data-ttu-id="4a6f8-155">A função **glListBase** especifica um deslocamento não assinado que é adicionado a cada nome de lista de exibição especificado em *listas* antes que a lista de exibição seja executada.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-155">The **glListBase** function specifies an unsigned offset that is added to each display list name specified in *lists* before that display list is executed.</span></span>

<span data-ttu-id="4a6f8-156">A função **glCallLists** pode aparecer dentro de uma lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-156">The **glCallLists** function can appear inside a display list.</span></span> <span data-ttu-id="4a6f8-157">Para evitar a possibilidade de recursão infinita resultante de listas de exibição chamando uma outra, um limite é colocado no nível de aninhamento das listas de exibição durante a execução da lista de exibição.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-157">To avoid the possibility of infinite recursion resulting from display lists calling one another, a limit is placed on the nesting level of display lists during display list execution.</span></span> <span data-ttu-id="4a6f8-158">Esse limite deve ser pelo menos 64 e depende da implementação.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-158">This limit must be at least 64, and it depends on the implementation.</span></span>

<span data-ttu-id="4a6f8-159">O estado OpenGL não é salvo e restaurado em uma chamada para **glCallLists**.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-159">The OpenGL state is not saved and restored across a call to **glCallLists**.</span></span> <span data-ttu-id="4a6f8-160">Assim, as alterações feitas no estado OpenGL durante a execução das listas de exibição permanecem após a conclusão da execução.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-160">Thus, changes made to the OpenGL state during the execution of the display lists remain after execution is completed.</span></span> <span data-ttu-id="4a6f8-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md)e [**glPopMatrix**](glpopmatrix.md) para preservar o estado do OpenGL entre chamadas de **glCallLists** .</span><span class="sxs-lookup"><span data-stu-id="4a6f8-161">Use [**glPushAttrib**](glpushattrib.md), [**glPopAttrib**](glpopattrib.md), [**glPushMatrix**](glpushmatrix.md), and [**glPopMatrix**](glpopmatrix.md) to preserve the OpenGL state across **glCallLists** calls.</span></span>

<span data-ttu-id="4a6f8-162">Você pode executar listas de exibição entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md), desde que a lista de exibição inclua apenas funções que são permitidas nesse intervalo.</span><span class="sxs-lookup"><span data-stu-id="4a6f8-162">You can execute display lists between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md), as long as the display list includes only functions that are allowed in this interval.</span></span>

<span data-ttu-id="4a6f8-163">As funções a seguir recuperam informações relacionadas à função **glCallLists** :</span><span class="sxs-lookup"><span data-stu-id="4a6f8-163">The following functions retrieve information related to the **glCallLists** function:</span></span>

<span data-ttu-id="4a6f8-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com base de lista de argumentos GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="4a6f8-164">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_LIST\_BASE</span></span>

<span data-ttu-id="4a6f8-165"> \_ \_ aninhamento de lista de glGet com Argument GL Max \_</span><span class="sxs-lookup"><span data-stu-id="4a6f8-165">**glGet** with argument GL\_MAX\_LIST\_NESTING</span></span>

[<span data-ttu-id="4a6f8-166">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-166">**glIsList**</span></span>](glislist.md)

## <a name="requirements"></a><span data-ttu-id="4a6f8-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4a6f8-167">Requirements</span></span>



| <span data-ttu-id="4a6f8-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="4a6f8-168">Requirement</span></span> | <span data-ttu-id="4a6f8-169">Valor</span><span class="sxs-lookup"><span data-stu-id="4a6f8-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4a6f8-170">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a6f8-170">Minimum supported client</span></span><br/> | <span data-ttu-id="4a6f8-171">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a6f8-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="4a6f8-172">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4a6f8-172">Minimum supported server</span></span><br/> | <span data-ttu-id="4a6f8-173">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="4a6f8-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4a6f8-174">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="4a6f8-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a6f8-175"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-175"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="4a6f8-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4a6f8-176">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a6f8-177"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-177"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="4a6f8-178">DLL</span><span class="sxs-lookup"><span data-stu-id="4a6f8-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a6f8-179"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a6f8-179"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a6f8-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="4a6f8-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a6f8-181">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-181">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-182">**glCallList**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-182">**glCallList**</span></span>](glcalllist.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-183">**glDeleteLists**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-183">**glDeleteLists**</span></span>](gldeletelists.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-184">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-184">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-185">**glGenLists**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-185">**glGenLists**</span></span>](glgenlists.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-186">**glGet**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-186">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-187">**glIsList**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-187">**glIsList**</span></span>](glislist.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-188">**glListBase**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-188">**glListBase**</span></span>](gllistbase.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-189">**glNewList**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-189">**glNewList**</span></span>](glnewlist.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-190">**glPopAttrib**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-190">**glPopAttrib**</span></span>](glpopattrib.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-191">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-191">**glPopMatrix**</span></span>](glpopmatrix.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-192">**glPushAttrib**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-192">**glPushAttrib**</span></span>](glpushattrib.md)
</dt> <dt>

[<span data-ttu-id="4a6f8-193">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="4a6f8-193">**glPushMatrix**</span></span>](glpushmatrix.md)
</dt> </dl>

 

 





