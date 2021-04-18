---
title: função glPixelMapusv (GL. h)
description: A função glPixelMapusv configura mapas de transferência de pixel.
ms.assetid: c542a1be-8fb0-4269-afc0-459182c89534
keywords:
- função glPixelMapusv OpenGL
topic_type:
- apiref
api_name:
- glPixelMapusv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0dd4adc50af4a4168d14ac2e39d465ace360ccbb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754975"
---
# <a name="glpixelmapusv-function"></a><span data-ttu-id="1cb60-104">função glPixelMapusv</span><span class="sxs-lookup"><span data-stu-id="1cb60-104">glPixelMapusv function</span></span>

<span data-ttu-id="1cb60-105">A função **glPixelMapusv** configura mapas de transferência de pixel.</span><span class="sxs-lookup"><span data-stu-id="1cb60-105">The **glPixelMapusv** function sets up pixel transfer maps.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cb60-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1cb60-106">Syntax</span></span>


```C++
void WINAPI glPixelMapusv(
         GLenum   map,
         GLsizei  mapsize,
   const GLushort *values
);
```



## <a name="parameters"></a><span data-ttu-id="1cb60-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1cb60-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cb60-108">*map*</span><span class="sxs-lookup"><span data-stu-id="1cb60-108">*map*</span></span> 
</dt> <dd>

<span data-ttu-id="1cb60-109">Um nome de mapa simbólico.</span><span class="sxs-lookup"><span data-stu-id="1cb60-109">A symbolic map name.</span></span> <span data-ttu-id="1cb60-110">Os dez mapas são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="1cb60-110">The ten maps are as follows.</span></span>



| <span data-ttu-id="1cb60-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1cb60-111">Value</span></span>                                                                                                                                                                               | <span data-ttu-id="1cb60-112">Significado</span><span class="sxs-lookup"><span data-stu-id="1cb60-112">Meaning</span></span>                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="GL_PIXEL_MAP_I_TO_I"></span><span id="gl_pixel_map_i_to_i"></span><dl> <span data-ttu-id="1cb60-113"><dt>**\_ \_ mapa de pixel GL \_ i \_ para \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-113"><dt>**GL\_PIXEL\_MAP\_I\_TO\_I**</dt></span></span> </dl> | <span data-ttu-id="1cb60-114">Mapeia índices de cores para índices de cores.</span><span class="sxs-lookup"><span data-stu-id="1cb60-114">Maps color indexes to color indexes.</span></span><br/>       |
| <span id="GL_PIXEL_MAP_S_TO_S"></span><span id="gl_pixel_map_s_to_s"></span><dl> <span data-ttu-id="1cb60-115"><dt>**\_ \_ mapas de pixel GL \_ s \_ para \_ s**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-115"><dt>**GL\_PIXEL\_MAP\_S\_TO\_S**</dt></span></span> </dl> | <span data-ttu-id="1cb60-116">Mapeia índices de estêncil para índices de estêncil.</span><span class="sxs-lookup"><span data-stu-id="1cb60-116">Maps stencil indexes to stencil indexes.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_I_TO_R"></span><span id="gl_pixel_map_i_to_r"></span><dl> <span data-ttu-id="1cb60-117"><dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ R**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-117"><dt>**GL\_PIXEL\_MAP\_I\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="1cb60-118">Mapeia índices de cores para componentes vermelhos.</span><span class="sxs-lookup"><span data-stu-id="1cb60-118">Maps color indexes to red components.</span></span><br/>      |
| <span id="GL_PIXEL_MAP_I_TO_G"></span><span id="gl_pixel_map_i_to_g"></span><dl> <span data-ttu-id="1cb60-119"><dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-119"><dt>**GL\_PIXEL\_MAP\_I\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="1cb60-120">Mapeia índices de cores para componentes verdes.</span><span class="sxs-lookup"><span data-stu-id="1cb60-120">Maps color indexes to green components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_I_TO_B"></span><span id="gl_pixel_map_i_to_b"></span><dl> <span data-ttu-id="1cb60-121"><dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ B**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-121"><dt>**GL\_PIXEL\_MAP\_I\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="1cb60-122">Mapeia índices de cores para componentes azuis.</span><span class="sxs-lookup"><span data-stu-id="1cb60-122">Maps color indexes to blue components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_I_TO_A"></span><span id="gl_pixel_map_i_to_a"></span><dl> <span data-ttu-id="1cb60-123"><dt>**\_ \_ mapa de pixel GL \_ I \_ para \_ a**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-123"><dt>**GL\_PIXEL\_MAP\_I\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="1cb60-124">Mapeia índices de cores para componentes alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb60-124">Maps color indexes to alpha components.</span></span><br/>    |
| <span id="GL_PIXEL_MAP_R_TO_R"></span><span id="gl_pixel_map_r_to_r"></span><dl> <span data-ttu-id="1cb60-125"><dt>**\_ \_ mapa de pixel GL \_ r \_ para \_ r**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-125"><dt>**GL\_PIXEL\_MAP\_R\_TO\_R**</dt></span></span> </dl> | <span data-ttu-id="1cb60-126">Mapeia componentes vermelhos para componentes vermelhos.</span><span class="sxs-lookup"><span data-stu-id="1cb60-126">Maps red components to red components.</span></span><br/>     |
| <span id="GL_PIXEL_MAP_G_TO_G"></span><span id="gl_pixel_map_g_to_g"></span><dl> <span data-ttu-id="1cb60-127"><dt>**\_ \_ mapa de pixel GL \_ g \_ a \_ G**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-127"><dt>**GL\_PIXEL\_MAP\_G\_TO\_G**</dt></span></span> </dl> | <span data-ttu-id="1cb60-128">Mapeia componentes verdes para componentes verdes.</span><span class="sxs-lookup"><span data-stu-id="1cb60-128">Maps green components to green components.</span></span><br/> |
| <span id="GL_PIXEL_MAP_B_TO_B"></span><span id="gl_pixel_map_b_to_b"></span><dl> <span data-ttu-id="1cb60-129"><dt>**\_ \_ mapa de pixel GL \_ b \_ para \_ b**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-129"><dt>**GL\_PIXEL\_MAP\_B\_TO\_B**</dt></span></span> </dl> | <span data-ttu-id="1cb60-130">Mapeia componentes azuis para componentes azuis.</span><span class="sxs-lookup"><span data-stu-id="1cb60-130">Maps blue components to blue components.</span></span><br/>   |
| <span id="GL_PIXEL_MAP_A_TO_A"></span><span id="gl_pixel_map_a_to_a"></span><dl> <span data-ttu-id="1cb60-131"><dt>**\_mapa de pixel GL a \_ \_ \_ para \_ um**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-131"><dt>**GL\_PIXEL\_MAP\_A\_TO\_A**</dt></span></span> </dl> | <span data-ttu-id="1cb60-132">Mapeia componentes alfa para componentes alfa.</span><span class="sxs-lookup"><span data-stu-id="1cb60-132">Maps alpha components to alpha components.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="1cb60-133">*mapear*</span><span class="sxs-lookup"><span data-stu-id="1cb60-133">*mapsize*</span></span> 
</dt> <dd>

<span data-ttu-id="1cb60-134">O tamanho do mapa que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="1cb60-134">The size of the map being defined.</span></span>

</dd> <dt>

<span data-ttu-id="1cb60-135">*os*</span><span class="sxs-lookup"><span data-stu-id="1cb60-135">*values*</span></span> 
</dt> <dd>

<span data-ttu-id="1cb60-136">Uma matriz de valores de *mapas* .</span><span class="sxs-lookup"><span data-stu-id="1cb60-136">An array of *mapsize* values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cb60-137">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1cb60-137">Return value</span></span>

<span data-ttu-id="1cb60-138">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1cb60-138">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1cb60-139">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="1cb60-139">Error codes</span></span>

<span data-ttu-id="1cb60-140">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="1cb60-140">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="1cb60-141">Nome</span><span class="sxs-lookup"><span data-stu-id="1cb60-141">Name</span></span>                                                                                                  | <span data-ttu-id="1cb60-142">Significado</span><span class="sxs-lookup"><span data-stu-id="1cb60-142">Meaning</span></span>                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1cb60-143"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-143"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="1cb60-144">o *mapa* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="1cb60-144">*map* was not an accepted value.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="1cb60-145"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-145"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1cb60-146">o *Maps* foi negativo ou maior que a \_ tabela de mapa de pixel GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1cb60-146">*mapsize* was negative or larger than GL\_PIXEL\_MAP\_TABLE.</span></span> <br/>                                                                                                                                                   |
| <dl> <span data-ttu-id="1cb60-147"><dt>**\_valor inválido do GL \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-147"><dt>**GL\_INVALID\_VALUE**</dt></span></span> </dl>     | <span data-ttu-id="1cb60-148">o *MAP* foi \_ o \_ mapa de pixel GL \_ i \_ para \_ i, GL o \_ \_ mapa \_ de pixels s \_ para \_ s, o GL do \_ \_ mapa de pixels \_ i \_ para \_ R, GL \_ pixel \_ map \_ i \_ para \_ G, GL \_ pixel \_ map \_ i \_ para \_ B ou GL \_ \_ o MAP pixel \_ i \_ para \_ a, e *Maps* não era uma potência de dois.</span><span class="sxs-lookup"><span data-stu-id="1cb60-148">*map* was GL\_PIXEL\_MAP\_I\_TO\_I, GL\_PIXEL\_MAP\_S\_TO\_S, GL\_PIXEL\_MAP\_I\_TO\_R, GL\_PIXEL\_MAP\_I\_TO\_G, GL\_PIXEL\_MAP\_I\_TO\_B, or GL\_PIXEL\_MAP\_I\_TO\_A, and *mapsize* was not a power of two.</span></span> <br/> |
| <dl> <span data-ttu-id="1cb60-149"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-149"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="1cb60-150">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="1cb60-150">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span> <br/>                                                                                     |



## <a name="remarks"></a><span data-ttu-id="1cb60-151">Comentários</span><span class="sxs-lookup"><span data-stu-id="1cb60-151">Remarks</span></span>

<span data-ttu-id="1cb60-152">A função **glPixelMap** configura tabelas de conversão ou *mapas*, usados por [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)e [**glTexSubImage2D**](gltexsubimage2d.md).</span><span class="sxs-lookup"><span data-stu-id="1cb60-152">The **glPixelMap** function sets up translation tables, or *maps*, used by [**glCopyPixels**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**glDrawPixels**](gldrawpixels.md), [**glReadPixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md), and [**glTexSubImage2D**](gltexsubimage2d.md).</span></span> <span data-ttu-id="1cb60-153">O uso desses mapas é descrito completamente no tópico [**glPixelTransfer**](glpixeltransfer.md) e, em parte, nos tópicos dos comandos de imagem de pixel e textura.</span><span class="sxs-lookup"><span data-stu-id="1cb60-153">Use of these maps is described completely in the [**glPixelTransfer**](glpixeltransfer.md) topic, and partly in the topics for the pixel and texture image commands.</span></span> <span data-ttu-id="1cb60-154">Somente a especificação dos mapas é descrita neste tópico.</span><span class="sxs-lookup"><span data-stu-id="1cb60-154">Only the specification of the maps is described in this topic.</span></span>

<span data-ttu-id="1cb60-155">O parâmetro *MAP* é um nome de mapa simbólico, indicando que um dos dez mapas deve ser definido.</span><span class="sxs-lookup"><span data-stu-id="1cb60-155">The *map* parameter is a symbolic map name, indicating one of ten maps to set.</span></span> <span data-ttu-id="1cb60-156">O parâmetro *Maps* especifica o número de entradas no mapa, e os *valores* são um ponteiro para uma matriz de *mapas* de valores de mapa.</span><span class="sxs-lookup"><span data-stu-id="1cb60-156">The *mapsize* parameter specifies the number of entries in the map, and *values* is a pointer to an array of *mapsize* map values.</span></span>

<span data-ttu-id="1cb60-157">As entradas em um mapa podem ser especificadas como números de ponto flutuante de precisão simples, inteiros curtos não assinados ou inteiros longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="1cb60-157">The entries in a map can be specified as single-precision floating-point numbers, unsigned short integers, or unsigned long integers.</span></span> <span data-ttu-id="1cb60-158">Mapas que armazenam valores de componentes de cores (todos, mas o \_ \_ mapa de pixel GL \_ i \_ e o mapa de \_ \_ pixel GL \_ \_ s \_ para \_ s) retêm seus valores no formato de ponto flutuante, com tamanhos mantissa e expoente não especificados.</span><span class="sxs-lookup"><span data-stu-id="1cb60-158">Maps that store color component values (all but GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S) retain their values in floating-point format, with unspecified mantissa and exponent sizes.</span></span> <span data-ttu-id="1cb60-159">Valores de ponto flutuante especificados por [**glPixelMapfv**](glpixelmap.md) são convertidos diretamente no formato de ponto flutuante interno desses mapas e, em seguida, clamped para o intervalo de \[ 0, 1 \] .</span><span class="sxs-lookup"><span data-stu-id="1cb60-159">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal floating-point format of these maps, and then clamped to the range \[0,1\].</span></span> <span data-ttu-id="1cb60-160">Valores inteiros sem sinal especificados por **glPixelMapusv** e **glPixelMapuiv** são convertidos linearmente de forma que o maior inteiro representável seja mapeado para 1,0 e que seja mapeado para 0,0.</span><span class="sxs-lookup"><span data-stu-id="1cb60-160">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** are converted linearly such that the largest representable integer maps to 1.0, and zero maps to 0.0.</span></span>

<span data-ttu-id="1cb60-161">Mapas que armazenam índices, \_ o GL de \_ mapa \_ de pixel \_ para \_ i e GL \_ \_ mapeiam \_ s \_ para \_ s, retêm seus valores em formato de ponto fixo, com um número não especificado de bits à direita do ponto binário.</span><span class="sxs-lookup"><span data-stu-id="1cb60-161">Maps that store indexes, GL\_PIXEL\_MAP\_I\_TO\_I and GL\_PIXEL\_MAP\_S\_TO\_S, retain their values in fixed-point format, with an unspecified number of bits to the right of the binary point.</span></span> <span data-ttu-id="1cb60-162">Os valores de ponto flutuante especificados por [**glPixelMapfv**](glpixelmap.md) são convertidos diretamente no formato de ponto fixo interno desses mapas.</span><span class="sxs-lookup"><span data-stu-id="1cb60-162">Floating-point values specified by [**glPixelMapfv**](glpixelmap.md) are converted directly to the internal fixed-point format of these maps.</span></span> <span data-ttu-id="1cb60-163">Valores inteiros sem sinal especificados por **glPixelMapusv** e **glPixelMapuiv** especificam valores inteiros, com todos os zeros à direita do ponto binário.</span><span class="sxs-lookup"><span data-stu-id="1cb60-163">Unsigned integer values specified by **glPixelMapusv** and **glPixelMapuiv** specify integer values, with all zeros to the right of the binary point.</span></span>

<span data-ttu-id="1cb60-164">A tabela a seguir mostra os tamanhos e valores iniciais para cada um dos mapas.</span><span class="sxs-lookup"><span data-stu-id="1cb60-164">The following table shows the initial sizes and values for each of the maps.</span></span> <span data-ttu-id="1cb60-165">Mapas que são indexados por índices de cor ou de estêncil devem ter o *Maps* = 2 ^ *n* para alguns *n* ou os resultados são indefinidos.</span><span class="sxs-lookup"><span data-stu-id="1cb60-165">Maps that are indexed by either color or stencil indexes must have *mapsize* = 2 ^ *n* for some *n* or results are undefined.</span></span> <span data-ttu-id="1cb60-166">O tamanho máximo permitido para cada mapa depende da implementação e pode ser determinado com a chamada de **glGet** com a \_ tabela de mapa de pixels máxima do Argument GL \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1cb60-166">The maximum allowable size for each map depends on the implementation and can be determined by calling **glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE.</span></span> <span data-ttu-id="1cb60-167">O máximo único se aplica a todos os mapas e é pelo menos 32.</span><span class="sxs-lookup"><span data-stu-id="1cb60-167">The single maximum applies to all maps, and it is at least 32.</span></span>



| <span data-ttu-id="1cb60-168">Mapeamento</span><span class="sxs-lookup"><span data-stu-id="1cb60-168">Map</span></span>                      | <span data-ttu-id="1cb60-169">Índice de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1cb60-169">Lookup Index</span></span>  | <span data-ttu-id="1cb60-170">Valor de pesquisa</span><span class="sxs-lookup"><span data-stu-id="1cb60-170">Lookup Value</span></span>  | <span data-ttu-id="1cb60-171">Tamanho Inicial</span><span class="sxs-lookup"><span data-stu-id="1cb60-171">Initial Size</span></span> | <span data-ttu-id="1cb60-172">Valor inicial</span><span class="sxs-lookup"><span data-stu-id="1cb60-172">Initial Value</span></span> |
|--------------------------|---------------|---------------|--------------|---------------|
| <span data-ttu-id="1cb60-173">\_ \_ mapa de pixel GL \_ i \_ para \_</span><span class="sxs-lookup"><span data-stu-id="1cb60-173">GL\_PIXEL\_MAP\_I\_TO\_I</span></span> | <span data-ttu-id="1cb60-174">índice de cores</span><span class="sxs-lookup"><span data-stu-id="1cb60-174">color index</span></span>   | <span data-ttu-id="1cb60-175">índice de cores</span><span class="sxs-lookup"><span data-stu-id="1cb60-175">color index</span></span>   | <span data-ttu-id="1cb60-176">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-176">1</span></span>            | <span data-ttu-id="1cb60-177">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-177">0.0</span></span>           |
| <span data-ttu-id="1cb60-178">\_ \_ mapas de pixel GL \_ s \_ para \_ s</span><span class="sxs-lookup"><span data-stu-id="1cb60-178">GL\_PIXEL\_MAP\_S\_TO\_S</span></span> | <span data-ttu-id="1cb60-179">índice de estêncil</span><span class="sxs-lookup"><span data-stu-id="1cb60-179">stencil index</span></span> | <span data-ttu-id="1cb60-180">índice de estêncil</span><span class="sxs-lookup"><span data-stu-id="1cb60-180">stencil index</span></span> | <span data-ttu-id="1cb60-181">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-181">1</span></span>            | <span data-ttu-id="1cb60-182">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-182">0.0</span></span>           |
| <span data-ttu-id="1cb60-183">\_ \_ mapa de pixel GL \_ I \_ para \_ R</span><span class="sxs-lookup"><span data-stu-id="1cb60-183">GL\_PIXEL\_MAP\_I\_TO\_R</span></span> | <span data-ttu-id="1cb60-184">índice de cores</span><span class="sxs-lookup"><span data-stu-id="1cb60-184">color index</span></span>   | <span data-ttu-id="1cb60-185">R</span><span class="sxs-lookup"><span data-stu-id="1cb60-185">R</span></span>             | <span data-ttu-id="1cb60-186">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-186">1</span></span>            | <span data-ttu-id="1cb60-187">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-187">0.0</span></span>           |
| <span data-ttu-id="1cb60-188">\_ \_ mapa de pixel GL \_ I \_ para \_ G</span><span class="sxs-lookup"><span data-stu-id="1cb60-188">GL\_PIXEL\_MAP\_I\_TO\_G</span></span> | <span data-ttu-id="1cb60-189">índice de cores</span><span class="sxs-lookup"><span data-stu-id="1cb60-189">color index</span></span>   | <span data-ttu-id="1cb60-190">G</span><span class="sxs-lookup"><span data-stu-id="1cb60-190">G</span></span>             | <span data-ttu-id="1cb60-191">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-191">1</span></span>            | <span data-ttu-id="1cb60-192">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-192">0.0</span></span>           |
| <span data-ttu-id="1cb60-193">\_ \_ mapa de pixel GL \_ I \_ para \_ B</span><span class="sxs-lookup"><span data-stu-id="1cb60-193">GL\_PIXEL\_MAP\_I\_TO\_B</span></span> | <span data-ttu-id="1cb60-194">índice de cores</span><span class="sxs-lookup"><span data-stu-id="1cb60-194">color index</span></span>   | <span data-ttu-id="1cb60-195">B</span><span class="sxs-lookup"><span data-stu-id="1cb60-195">B</span></span>             | <span data-ttu-id="1cb60-196">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-196">1</span></span>            | <span data-ttu-id="1cb60-197">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-197">0.0</span></span>           |
| <span data-ttu-id="1cb60-198">\_ \_ mapa de pixel GL \_ I \_ para \_ a</span><span class="sxs-lookup"><span data-stu-id="1cb60-198">GL\_PIXEL\_MAP\_I\_TO\_A</span></span> | <span data-ttu-id="1cb60-199">índice de cores</span><span class="sxs-lookup"><span data-stu-id="1cb60-199">color index</span></span>   | <span data-ttu-id="1cb60-200">Um</span><span class="sxs-lookup"><span data-stu-id="1cb60-200">A</span></span>             | <span data-ttu-id="1cb60-201">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-201">1</span></span>            | <span data-ttu-id="1cb60-202">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-202">0.0</span></span>           |
| <span data-ttu-id="1cb60-203">\_ \_ mapa de pixel GL \_ r \_ para \_ r</span><span class="sxs-lookup"><span data-stu-id="1cb60-203">GL\_PIXEL\_MAP\_R\_TO\_R</span></span> | <span data-ttu-id="1cb60-204">R</span><span class="sxs-lookup"><span data-stu-id="1cb60-204">R</span></span>             | <span data-ttu-id="1cb60-205">R</span><span class="sxs-lookup"><span data-stu-id="1cb60-205">R</span></span>             | <span data-ttu-id="1cb60-206">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-206">1</span></span>            | <span data-ttu-id="1cb60-207">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-207">0.0</span></span>           |
| <span data-ttu-id="1cb60-208">\_ \_ mapa de pixel GL \_ g \_ a \_ G</span><span class="sxs-lookup"><span data-stu-id="1cb60-208">GL\_PIXEL\_MAP\_G\_TO\_G</span></span> | <span data-ttu-id="1cb60-209">G</span><span class="sxs-lookup"><span data-stu-id="1cb60-209">G</span></span>             | <span data-ttu-id="1cb60-210">G</span><span class="sxs-lookup"><span data-stu-id="1cb60-210">G</span></span>             | <span data-ttu-id="1cb60-211">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-211">1</span></span>            | <span data-ttu-id="1cb60-212">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-212">0.0</span></span>           |
| <span data-ttu-id="1cb60-213">\_ \_ mapa de pixel GL \_ b \_ para \_ b</span><span class="sxs-lookup"><span data-stu-id="1cb60-213">GL\_PIXEL\_MAP\_B\_TO\_B</span></span> | <span data-ttu-id="1cb60-214">B</span><span class="sxs-lookup"><span data-stu-id="1cb60-214">B</span></span>             | <span data-ttu-id="1cb60-215">B</span><span class="sxs-lookup"><span data-stu-id="1cb60-215">B</span></span>             | <span data-ttu-id="1cb60-216">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-216">1</span></span>            | <span data-ttu-id="1cb60-217">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-217">0.0</span></span>           |
| <span data-ttu-id="1cb60-218">\_mapa de pixel GL a \_ \_ \_ para \_ um</span><span class="sxs-lookup"><span data-stu-id="1cb60-218">GL\_PIXEL\_MAP\_A\_TO\_A</span></span> | <span data-ttu-id="1cb60-219">Um</span><span class="sxs-lookup"><span data-stu-id="1cb60-219">A</span></span>             | <span data-ttu-id="1cb60-220">Um</span><span class="sxs-lookup"><span data-stu-id="1cb60-220">A</span></span>             | <span data-ttu-id="1cb60-221">1</span><span class="sxs-lookup"><span data-stu-id="1cb60-221">1</span></span>            | <span data-ttu-id="1cb60-222">0.0</span><span class="sxs-lookup"><span data-stu-id="1cb60-222">0.0</span></span>           |



 

<span data-ttu-id="1cb60-223">As funções a seguir recuperam informações relacionadas ao **glPixelMap**:</span><span class="sxs-lookup"><span data-stu-id="1cb60-223">The following functions retrieve information related to **glPixelMap**:</span></span>

<span data-ttu-id="1cb60-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com Argument GL \_ pixel \_ mapa \_ i \_ i \_ \_ size</span><span class="sxs-lookup"><span data-stu-id="1cb60-224">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_PIXEL\_MAP\_I\_TO\_I\_SIZE</span></span>

<span data-ttu-id="1cb60-225">**glGet** com o argumento GL \_ pixel \_ mapa \_ S para o \_ \_ \_ tamanho s</span><span class="sxs-lookup"><span data-stu-id="1cb60-225">**glGet** with argument GL\_PIXEL\_MAP\_S\_TO\_S\_SIZE</span></span>

<span data-ttu-id="1cb60-226">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ R \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="1cb60-226">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_R\_SIZE</span></span>

<span data-ttu-id="1cb60-227">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ G \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="1cb60-227">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_G\_SIZE</span></span>

<span data-ttu-id="1cb60-228">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ o \_ tamanho B</span><span class="sxs-lookup"><span data-stu-id="1cb60-228">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_B\_SIZE</span></span>

<span data-ttu-id="1cb60-229">**glGet** com Argument GL \_ pixel \_ mapa \_ I \_ para \_ um \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="1cb60-229">**glGet** with argument GL\_PIXEL\_MAP\_I\_TO\_A\_SIZE</span></span>

<span data-ttu-id="1cb60-230">**glGet** com argumento GL \_ pixel \_ mapa \_ r \_ para \_ r \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="1cb60-230">**glGet** with argument GL\_PIXEL\_MAP\_R\_TO\_R\_SIZE</span></span>

<span data-ttu-id="1cb60-231">**glGet** com Argument GL \_ o \_ mapa \_ \_ de pixel de tamanho de g a \_ G \_</span><span class="sxs-lookup"><span data-stu-id="1cb60-231">**glGet** with argument GL\_PIXEL\_MAP\_G\_TO\_G\_SIZE</span></span>

<span data-ttu-id="1cb60-232">**glGet** com Argument GL \_ pixel \_ mapa \_ b \_ para \_ B \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="1cb60-232">**glGet** with argument GL\_PIXEL\_MAP\_B\_TO\_B\_SIZE</span></span>

<span data-ttu-id="1cb60-233">**glGet** com Argument GL \_ pixel \_ Mapear \_ um \_ para \_ um \_ tamanho</span><span class="sxs-lookup"><span data-stu-id="1cb60-233">**glGet** with argument GL\_PIXEL\_MAP\_A\_TO\_A\_SIZE</span></span>

<span data-ttu-id="1cb60-234">tabela de mapa de pixels de **glGet** com Argument GL \_ Max \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="1cb60-234">**glGet** with argument GL\_MAX\_PIXEL\_MAP\_TABLE</span></span>

## <a name="requirements"></a><span data-ttu-id="1cb60-235">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cb60-235">Requirements</span></span>



| <span data-ttu-id="1cb60-236">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cb60-236">Requirement</span></span> | <span data-ttu-id="1cb60-237">Valor</span><span class="sxs-lookup"><span data-stu-id="1cb60-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1cb60-238">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cb60-238">Minimum supported client</span></span><br/> | <span data-ttu-id="1cb60-239">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1cb60-239">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="1cb60-240">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1cb60-240">Minimum supported server</span></span><br/> | <span data-ttu-id="1cb60-241">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1cb60-241">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="1cb60-242">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="1cb60-242">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cb60-243"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-243"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="1cb60-244">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1cb60-244">Library</span></span><br/>                  | <dl> <span data-ttu-id="1cb60-245"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-245"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="1cb60-246">DLL</span><span class="sxs-lookup"><span data-stu-id="1cb60-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1cb60-247"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1cb60-247"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cb60-248">Confira também</span><span class="sxs-lookup"><span data-stu-id="1cb60-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cb60-249">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="1cb60-249">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="1cb60-250">**glCopyPixels**</span><span class="sxs-lookup"><span data-stu-id="1cb60-250">**glCopyPixels**</span></span>](glcopypixels.md)
</dt> <dt>

[<span data-ttu-id="1cb60-251">**glDrawPixels**</span><span class="sxs-lookup"><span data-stu-id="1cb60-251">**glDrawPixels**</span></span>](gldrawpixels.md)
</dt> <dt>

[<span data-ttu-id="1cb60-252">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="1cb60-252">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="1cb60-253">**glPixelStore**</span><span class="sxs-lookup"><span data-stu-id="1cb60-253">**glPixelStore**</span></span>](glpixelstore-functions.md)
</dt> <dt>

[<span data-ttu-id="1cb60-254">**glPixelTransfer**</span><span class="sxs-lookup"><span data-stu-id="1cb60-254">**glPixelTransfer**</span></span>](glpixeltransfer.md)
</dt> <dt>

[<span data-ttu-id="1cb60-255">**glReadPixels**</span><span class="sxs-lookup"><span data-stu-id="1cb60-255">**glReadPixels**</span></span>](glreadpixels.md)
</dt> <dt>

[<span data-ttu-id="1cb60-256">**glTexImage1D**</span><span class="sxs-lookup"><span data-stu-id="1cb60-256">**glTexImage1D**</span></span>](glteximage1d.md)
</dt> <dt>

[<span data-ttu-id="1cb60-257">**glTexImage2D**</span><span class="sxs-lookup"><span data-stu-id="1cb60-257">**glTexImage2D**</span></span>](glteximage2d.md)
</dt> </dl>

 

 





