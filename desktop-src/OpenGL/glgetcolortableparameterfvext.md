---
title: função glGetColorTableParameterfvEXT (GL. h)
description: As funções glGetColorTableParameterfvEXT e glGetColorTableParameterivEXT obtêm parâmetros de paleta de tabelas de cores. | função glGetColorTableParameterfvEXT (GL. h)
ms.assetid: e78051aa-4233-413c-8838-0741b54eab0e
keywords:
- função glGetColorTableParameterfvEXT OpenGL
topic_type:
- apiref
api_name:
- glGetColorTableParameterfvEXT
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 533ca0c847548fa1de4518079ca6e49d15b6830f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370884"
---
# <a name="glgetcolortableparameterfvext-function"></a><span data-ttu-id="de0da-105">função glGetColorTableParameterfvEXT</span><span class="sxs-lookup"><span data-stu-id="de0da-105">glGetColorTableParameterfvEXT function</span></span>

<span data-ttu-id="de0da-106">As funções **glGetColorTableParameterfvEXT** e [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) obtêm parâmetros de paleta de tabelas de cores.</span><span class="sxs-lookup"><span data-stu-id="de0da-106">The **glGetColorTableParameterfvEXT** and [**glGetColorTableParameterivEXT**](glgetcolortableparameterivext.md) functions get palette parameters from color tables.</span></span>

## <a name="syntax"></a><span data-ttu-id="de0da-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="de0da-107">Syntax</span></span>


```C++
void WINAPI glGetColorTableParameterfvEXT(
   GLenum  target,
   GLenum  pname,
   GLfloat *params
);
```



## <a name="parameters"></a><span data-ttu-id="de0da-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="de0da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de0da-109">*destino*</span><span class="sxs-lookup"><span data-stu-id="de0da-109">*target*</span></span> 
</dt> <dd>

<span data-ttu-id="de0da-110">A textura de destino da paleta para a qual você deseja dados de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="de0da-110">The target texture of the palette for which you want parameter data.</span></span> <span data-ttu-id="de0da-111">Deve ser a textura \_ 1D, a textura \_ 2D, a \_ textura \_ de proxy 1D ou a textura de proxy \_ \_ 2D.</span><span class="sxs-lookup"><span data-stu-id="de0da-111">Must be TEXTURE\_1D, TEXTURE\_2D, PROXY\_TEXTURE\_1D, or PROXY\_TEXTURE\_2D.</span></span>

</dd> <dt>

<span data-ttu-id="de0da-112">*pname*</span><span class="sxs-lookup"><span data-stu-id="de0da-112">*pname*</span></span> 
</dt> <dd>

<span data-ttu-id="de0da-113">Uma constante simbólica para o tipo de dados de parâmetro de paleta apontados por *params*.</span><span class="sxs-lookup"><span data-stu-id="de0da-113">A symbolic constant for the type of palette parameter data pointed to by *params*.</span></span>

<span data-ttu-id="de0da-114">A seguir estão as constantes simbólicas aceitas e seus significados.</span><span class="sxs-lookup"><span data-stu-id="de0da-114">The following are the accepted symbolic constants and their meanings.</span></span>



| <span data-ttu-id="de0da-115">Valor</span><span class="sxs-lookup"><span data-stu-id="de0da-115">Value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="de0da-116">Significado</span><span class="sxs-lookup"><span data-stu-id="de0da-116">Meaning</span></span>                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COLOR_TABLE_FORMAT_EXT"></span><span id="gl_color_table_format_ext"></span><dl> <span data-ttu-id="de0da-117"><dt>**\_formato de tabela de cores GL \_ \_ \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-117"><dt>**GL\_COLOR\_TABLE\_FORMAT\_EXT**</dt></span></span> </dl>              | <span data-ttu-id="de0da-118">Retornar o formato interno especificado pela chamada mais recente para [**glColorTableEXT**](glcolortableext.md) ou o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="de0da-118">Return the internal format specified by the most recent call to [**glColorTableEXT**](glcolortableext.md) or the default value.</span></span><br/> |
| <span id="GL_COLOR_TABLE_WIDTH_EXT"></span><span id="gl_color_table_width_ext"></span><dl> <span data-ttu-id="de0da-119"><dt>**\_extensão da \_ largura da tabela de cores GL \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-119"><dt>**GL\_COLOR\_TABLE\_WIDTH\_EXT**</dt></span></span> </dl>                 | <span data-ttu-id="de0da-120">Retorna a largura da paleta atual.</span><span class="sxs-lookup"><span data-stu-id="de0da-120">Return the width of the current palette.</span></span><br/>                                                                                         |
| <span id="GL_COLOR_TABLE_RED_SIZE_EXT"></span><span id="gl_color_table_red_size_ext"></span><dl> <span data-ttu-id="de0da-121"><dt>**\_extensão de cor GL \_ \_ Red \_ Size \_ ext**</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-121"><dt>**GL\_COLOR\_TABLE\_RED\_SIZE\_EXT**</dt></span></span> </dl>       | <span data-ttu-id="de0da-122">Retorne o tamanho real usado internamente para armazenar o componente vermelho dos dados da paleta.</span><span class="sxs-lookup"><span data-stu-id="de0da-122">Return the actual size used internally to store the red component of the palette data.</span></span><br/>                                           |
| <span id="GL_COLOR_TABLE_GREEN_SIZE_EXT"></span><span id="gl_color_table_green_size_ext"></span><dl> <span data-ttu-id="de0da-123"><dt>**\_ext. \_ de \_ Tamanho verde da tabela de cores \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-123"><dt>**GL\_COLOR\_TABLE\_GREEN\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="de0da-124">Retorne o tamanho real usado internamente para armazenar o componente verde dos dados da paleta.</span><span class="sxs-lookup"><span data-stu-id="de0da-124">Return the actual size used internally to store the green component of the palette data.</span></span><br/>                                         |
| <span id="GL_COLOR_TABLE_BLUE_SIZE_EXT"></span><span id="gl_color_table_blue_size_ext"></span><dl> <span data-ttu-id="de0da-125"><dt>**\_ext. \_ de \_ tamanho azul da tabela de cores \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-125"><dt>**GL\_COLOR\_TABLE\_BLUE\_SIZE\_EXT**</dt></span></span> </dl>    | <span data-ttu-id="de0da-126">Retorne o tamanho real usado internamente para armazenar o componente azul dos dados da paleta.</span><span class="sxs-lookup"><span data-stu-id="de0da-126">Return the actual size used internally to store the blue component of the palette data.</span></span><br/>                                          |
| <span id="GL_COLOR_TABLE_ALPHA_SIZE_EXT"></span><span id="gl_color_table_alpha_size_ext"></span><dl> <span data-ttu-id="de0da-127"><dt>**\_ext. \_ de \_ tamanho alfa da tabela de cores \_ GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-127"><dt>**GL\_COLOR\_TABLE\_ALPHA\_SIZE\_EXT**</dt></span></span> </dl> | <span data-ttu-id="de0da-128">Retornar o tamanho real usado internamente para armazenar o componente alfa dos dados da paleta.</span><span class="sxs-lookup"><span data-stu-id="de0da-128">Return the actual size used internally to store the alpha component of the palette data.</span></span><br/>                                         |



 

</dd> <dt>

<span data-ttu-id="de0da-129">*params*</span><span class="sxs-lookup"><span data-stu-id="de0da-129">*params*</span></span> 
</dt> <dd>

<span data-ttu-id="de0da-130">Aponta para os dados de parâmetro da tabela de cores especificados pelo parâmetro *pname* .</span><span class="sxs-lookup"><span data-stu-id="de0da-130">Points to the color table parameter data specified by the *pname* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de0da-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="de0da-131">Return value</span></span>

<span data-ttu-id="de0da-132">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="de0da-132">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de0da-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="de0da-133">Remarks</span></span>

<span data-ttu-id="de0da-134">Use as funções **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** para recuperar dados de parâmetro específicos de tabelas de cores definidas com [**glColorTableEXT**](glcolortableext.md) para paletas de textura direcionadas.</span><span class="sxs-lookup"><span data-stu-id="de0da-134">You use the **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** functions to retrieve specific parameter data from color tables set with [**glColorTableEXT**](glcolortableext.md) for targeted texture palettes.</span></span> <span data-ttu-id="de0da-135">Além disso, você pode usar essas funções para determinar o número de entradas da tabela de cores que o **glGetColorTableEXT** retorna.</span><span class="sxs-lookup"><span data-stu-id="de0da-135">Also you can use these functions to determine the number of color table entries that **glGetColorTableEXT** returns.</span></span>

<span data-ttu-id="de0da-136">Quando o parâmetro de *destino* for GL proxy ou textura \_ de proxy ingl \_ \_ \_ 2D ou \_ \_ insupport e a implementação não oferecer suporte aos valores especificados para o *formato* ou a *largura*, **glColorTableEXT** poderá falhar ao criar a tabela de cores solicitada.</span><span class="sxs-lookup"><span data-stu-id="de0da-136">When the *target* parameter is GL\_PROXY\_TEXTURE\_1D or GL\_PROXY\_TEXTURE\_2D, and the implementation does not support the values specified for either *format* or *width*, **glColorTableEXT** can fail to create the requested color table.</span></span> <span data-ttu-id="de0da-137">Nesse caso, a tabela de cores está vazia e todos os parâmetros recuperados serão zero.</span><span class="sxs-lookup"><span data-stu-id="de0da-137">In this case, the color table is empty and all parameters retrieved will be zero.</span></span> <span data-ttu-id="de0da-138">Você pode determinar se o OpenGL dá suporte a um formato e tamanho de tabela de cores específico chamando **glColorTableEXT** com um destino de proxy e, em seguida, chamando **glGetColorTableParameterivEXT** ou **glGetColorTableParameterfvEXT** para determinar se o parâmetro de largura corresponde ao definido por **glColorTableEXT**.</span><span class="sxs-lookup"><span data-stu-id="de0da-138">You can determine whether OpenGL supports a particular color table format and size by calling **glColorTableEXT** with a proxy target, and then calling **glGetColorTableParameterivEXT** or **glGetColorTableParameterfvEXT** to determine whether the width parameter matches that set by **glColorTableEXT**.</span></span> <span data-ttu-id="de0da-139">Se a largura recuperada for zero, a solicitação da tabela de cores por **glColorTable** falhou.</span><span class="sxs-lookup"><span data-stu-id="de0da-139">If the retrieved width is zero, the color table request by **glColorTable** failed.</span></span> <span data-ttu-id="de0da-140">Se a largura recuperada não for zero, você poderá chamar **glColorTable** com o destino real com textura \_ 1D ou \_ a textura 2D para definir a tabela de cores.</span><span class="sxs-lookup"><span data-stu-id="de0da-140">If the retrieved width is not zero, you can call **glColorTable** with the real target with TEXTURE\_1D or TEXTURE\_2D to set the color table.</span></span>

<span data-ttu-id="de0da-141">As funções **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** são funções de extensão que não fazem parte da biblioteca OpenGL padrão, mas fazem parte da extensão de textura da paleta do GL \_ ext \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="de0da-141">The **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** functions are extension functions that are not part of the standard OpenGL library but are part of the GL\_EXT\_paletted\_texture extension.</span></span> <span data-ttu-id="de0da-142">Para verificar se a implementação do OpenGL dá suporte a **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT**, chame [**glGetString**](glgetstring.md)**(** \_ extensões GL **)**.</span><span class="sxs-lookup"><span data-stu-id="de0da-142">To check whether your implementation of OpenGL supports **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT**, call [**glGetString**](glgetstring.md)**(** GL\_EXTENSIONS **)**.</span></span> <span data-ttu-id="de0da-143">Se ele retornar a \_ textura da paleta do GL ext \_ \_ , **glGetColorTableParameterivEXT** e **glGetColorTableParameterfvEXT** têm suporte.</span><span class="sxs-lookup"><span data-stu-id="de0da-143">If it returns GL\_EXT\_paletted\_texture, **glGetColorTableParameterivEXT** and **glGetColorTableParameterfvEXT** are supported.</span></span> <span data-ttu-id="de0da-144">Para obter o endereço da função de uma função de extensão, chame [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span><span class="sxs-lookup"><span data-stu-id="de0da-144">To obtain the function address of an extension function, call [**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress).</span></span>

## <a name="requirements"></a><span data-ttu-id="de0da-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="de0da-145">Requirements</span></span>



| <span data-ttu-id="de0da-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="de0da-146">Requirement</span></span> | <span data-ttu-id="de0da-147">Valor</span><span class="sxs-lookup"><span data-stu-id="de0da-147">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="de0da-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de0da-148">Minimum supported client</span></span><br/> | <span data-ttu-id="de0da-149">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de0da-149">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="de0da-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="de0da-150">Minimum supported server</span></span><br/> | <span data-ttu-id="de0da-151">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="de0da-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="de0da-152">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="de0da-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="de0da-153"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="de0da-153"><dt>Gl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de0da-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="de0da-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de0da-155">**glColorSubTableEXT**</span><span class="sxs-lookup"><span data-stu-id="de0da-155">**glColorSubTableEXT**</span></span>](glcolorsubtableext.md)
</dt> <dt>

[<span data-ttu-id="de0da-156">**glColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="de0da-156">**glColorTableEXT**</span></span>](glcolortableext.md)
</dt> <dt>

[<span data-ttu-id="de0da-157">**glGetColorTableEXT**</span><span class="sxs-lookup"><span data-stu-id="de0da-157">**glGetColorTableEXT**</span></span>](glgetcolortableext.md)
</dt> <dt>

[<span data-ttu-id="de0da-158">**glGetColorTableParameterivEXT**</span><span class="sxs-lookup"><span data-stu-id="de0da-158">**glGetColorTableParameterivEXT**</span></span>](glgetcolortableparameterivext.md)
</dt> <dt>

[<span data-ttu-id="de0da-159">**wglGetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="de0da-159">**wglGetProcAddress**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





