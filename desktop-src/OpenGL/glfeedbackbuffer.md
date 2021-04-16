---
title: função glFeedbackBuffer (GL. h)
description: A função glFeedbackBuffer controla o modo de comentários.
ms.assetid: fe3773a7-c264-4d49-8f90-1f2319f9af4f
keywords:
- função glFeedbackBuffer OpenGL
topic_type:
- apiref
api_name:
- glFeedbackBuffer
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64b232db640d41ca9a1e1f75d6ab766597d6511
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751092"
---
# <a name="glfeedbackbuffer-function"></a><span data-ttu-id="e3bf6-104">função glFeedbackBuffer</span><span class="sxs-lookup"><span data-stu-id="e3bf6-104">glFeedbackBuffer function</span></span>

<span data-ttu-id="e3bf6-105">A função **glFeedbackBuffer** controla o modo de comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-105">The **glFeedbackBuffer** function controls feedback mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3bf6-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3bf6-106">Syntax</span></span>


```C++
void WINAPI glFeedbackBuffer(
   GLsizei size,
   GLenum  type,
   GLfloat *buffer
);
```



## <a name="parameters"></a><span data-ttu-id="e3bf6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3bf6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3bf6-108">*size*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-108">*size*</span></span> 
</dt> <dd>

<span data-ttu-id="e3bf6-109">O número máximo de valores que podem ser gravados no *buffer*.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-109">The maximum number of values that can be written into *buffer*.</span></span>

</dd> <dt>

<span data-ttu-id="e3bf6-110">*tipo*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-110">*type*</span></span> 
</dt> <dd>

<span data-ttu-id="e3bf6-111">Uma constante simbólica que descreve as informações que serão retornadas para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-111">A symbolic constant that describes the information that will be returned for each vertex.</span></span> <span data-ttu-id="e3bf6-112">As seguintes constantes simbólicas são aceitas: GL \_ 2D, GL \_ 3D, Recall \_ 3D \_ Color, GL \_ 3D Color \_ \_ Texture e GL \_ 4D \_ Color \_ Texture.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-112">The following symbolic constants are accepted: GL\_2D, GL\_3D, GL\_3D\_COLOR, GL\_3D\_COLOR\_TEXTURE, and GL\_4D\_COLOR\_TEXTURE.</span></span>

</dd> <dt>

<span data-ttu-id="e3bf6-113">*completo*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-113">*buffer*</span></span> 
</dt> <dd>

<span data-ttu-id="e3bf6-114">Retorna os dados de comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-114">Returns the feedback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3bf6-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3bf6-115">Return value</span></span>

<span data-ttu-id="e3bf6-116">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-116">This function does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e3bf6-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="e3bf6-117">Error codes</span></span>

<span data-ttu-id="e3bf6-118">Os códigos de erro a seguir podem ser recuperados pela função [**glGetError**](glgeterror.md) .</span><span class="sxs-lookup"><span data-stu-id="e3bf6-118">The following error codes can be retrieved by the [**glGetError**](glgeterror.md) function.</span></span>



| <span data-ttu-id="e3bf6-119">Nome</span><span class="sxs-lookup"><span data-stu-id="e3bf6-119">Name</span></span>                                                                                                  | <span data-ttu-id="e3bf6-120">Significado</span><span class="sxs-lookup"><span data-stu-id="e3bf6-120">Meaning</span></span>                                                                                                                                                                                                                |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3bf6-121"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-121"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e3bf6-122">o *tipo* não era um valor aceito.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-122">*type* was not an accepted value.</span></span><br/>                                                                                                                                                                           |
| <dl> <span data-ttu-id="e3bf6-123"><dt>**GL \_ inválido de \_ enumeração**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-123"><dt>**GL\_INVALID\_ENUM**</dt></span></span> </dl>      | <span data-ttu-id="e3bf6-124">o *tamanho* era negativo.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-124">*size* was negative.</span></span><br/>                                                                                                                                                                                        |
| <dl> <span data-ttu-id="e3bf6-125"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-125"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e3bf6-126">**glFeedbackBuffer** foi chamado enquanto o modo render tinha \_ comentários GL ou [**glRenderMode**](glrendermode.md) foi chamado com comentários Argument GL \_ antes de **glFeedbackBuffer** ser chamado pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-126">**glFeedbackBuffer** was called while the render mode was GL\_FEEDBACK, or [**glRenderMode**](glrendermode.md) was called with argument GL\_FEEDBACK before **glFeedbackBuffer** was called at least once.</span></span><br/> |
| <dl> <span data-ttu-id="e3bf6-127"><dt>**GL \_ operação inválida \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-127"><dt>**GL\_INVALID\_OPERATION**</dt></span></span> </dl> | <span data-ttu-id="e3bf6-128">A função foi chamada entre uma chamada para [**glBegin**](glbegin.md) e a chamada correspondente para [**glEnd**](glend.md).</span><span class="sxs-lookup"><span data-stu-id="e3bf6-128">The function was called between a call to [**glBegin**](glbegin.md) and the corresponding call to [**glEnd**](glend.md).</span></span><br/>                                                                                  |



## <a name="remarks"></a><span data-ttu-id="e3bf6-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3bf6-129">Remarks</span></span>

<span data-ttu-id="e3bf6-130">A função **glFeedbackBuffer** controla os comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-130">The **glFeedbackBuffer** function controls feedback.</span></span> <span data-ttu-id="e3bf6-131">Comentários, como seleção, é um modo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-131">Feedback, like selection, is an OpenGL mode.</span></span> <span data-ttu-id="e3bf6-132">O modo é selecionado chamando [**glRenderMode**](glrendermode.md) com os \_ comentários GL.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-132">The mode is selected by calling [**glRenderMode**](glrendermode.md) with GL\_FEEDBACK.</span></span> <span data-ttu-id="e3bf6-133">Quando OpenGL está no modo de comentários, nenhum pixel é produzido pela rasterização.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-133">When OpenGL is in feedback mode, no pixels are produced by rasterization.</span></span> <span data-ttu-id="e3bf6-134">Em vez disso, as informações sobre primitivas que teriam sido rasterizadas são voltadas para o aplicativo usando OpenGL.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-134">Instead, information about primitives that would have been rasterized is fed back to the application using OpenGL.</span></span>

<span data-ttu-id="e3bf6-135">A função **glFeedbackBuffer** tem três argumentos:</span><span class="sxs-lookup"><span data-stu-id="e3bf6-135">The **glFeedbackBuffer** function has three arguments:</span></span>

-   <span data-ttu-id="e3bf6-136">*buffer* é um ponteiro para uma matriz de valores de ponto flutuante em que as informações de comentários são colocadas.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-136">*buffer* is a pointer to an array of floating-point values into which feedback information is placed.</span></span>
-   <span data-ttu-id="e3bf6-137">*tamanho* indica o tamanho da matriz.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-137">*size* indicates the size of the array.</span></span>
-   <span data-ttu-id="e3bf6-138">*Type* é uma constante simbólica que descreve as informações que são voltadas para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-138">*type* is a symbolic constant describing the information that is fed back for each vertex.</span></span>

<span data-ttu-id="e3bf6-139">Você deve emitir **glFeedbackBuffer** antes que o modo de comentários esteja habilitado (chamando **glRenderMode** com comentários do Argument GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="e3bf6-139">You must issue **glFeedbackBuffer** before feedback mode is enabled (by calling **glRenderMode** with argument GL\_FEEDBACK).</span></span> <span data-ttu-id="e3bf6-140">Definir \_ comentários GL sem estabelecer o buffer de comentários ou chamar **GlFeedbackBuffer** enquanto OpenGL está no modo de comentários, é um erro.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-140">Setting GL\_FEEDBACK without establishing the feedback buffer, or calling **glFeedbackBuffer** while OpenGL is in feedback mode, is an error.</span></span>

<span data-ttu-id="e3bf6-141">Retire o OpenGL do modo de comentários chamando [**glRenderMode**](glrendermode.md) com um valor de parâmetro diferente do GL \_ .</span><span class="sxs-lookup"><span data-stu-id="e3bf6-141">Take OpenGL out of feedback mode by calling [**glRenderMode**](glrendermode.md) with a parameter value other than GL\_FEEDBACK.</span></span> <span data-ttu-id="e3bf6-142">Quando você faz isso enquanto OpenGL está no modo de comentários, **glRenderMode** retorna o número de entradas colocadas na matriz de comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-142">When you do this while OpenGL is in feedback mode, **glRenderMode** returns the number of entries placed in the feedback array.</span></span> <span data-ttu-id="e3bf6-143">O valor retornado nunca excede o *tamanho*.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-143">The returned value never exceeds *size*.</span></span> <span data-ttu-id="e3bf6-144">Se os dados de comentários precisarem de mais espaço que o disponível no *buffer*, **glRenderMode** retornará um valor negativo.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-144">If the feedback data required more room than was available in *buffer*, **glRenderMode** returns a negative value.</span></span>

<span data-ttu-id="e3bf6-145">No modo de comentários, cada primitivo que seria rasterizado gera um bloco de valores que são copiados para a matriz de comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-145">While in feedback mode, each primitive that would be rasterized generates a block of values that gets copied into the feedback array.</span></span> <span data-ttu-id="e3bf6-146">Se isso fizer com que o número de entradas exceda o máximo, o **glFeedbackBuffer** gravará parcialmente o bloco para preencher a matriz (se houver alguma sala restante) e definir um sinalizador de estouro.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-146">If doing so would cause the number of entries to exceed the maximum, **glFeedbackBuffer** partially writes the block so as to fill the array (if there is any room left at all), and sets an overflow flag.</span></span> <span data-ttu-id="e3bf6-147">Cada bloco começa com um código que indica o tipo primitivo, seguido por valores que descrevem os vértices e os dados associados do primitivo.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-147">Each block begins with a code indicating the primitive type, followed by values that describe the primitive's vertices and associated data.</span></span> <span data-ttu-id="e3bf6-148">A função **glFeedbackBuffer** também grava entradas para bitmaps e retângulos de pixel.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-148">The **glFeedbackBuffer** function also writes entries for bitmaps and pixel rectangles.</span></span> <span data-ttu-id="e3bf6-149">Os comentários ocorrem após a remoção do polígono e a interpretação [**glPolygonMode**](glpolygonmode.md) dos polígonos, portanto, os polígonos que são retirados não são retornados no buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-149">Feedback occurs after polygon culling and [**glPolygonMode**](glpolygonmode.md) interpretation of polygons has taken place, so polygons that are culled are not returned in the feedback buffer.</span></span> <span data-ttu-id="e3bf6-150">Isso também pode ocorrer depois que polígonos com mais de três bordas são divididos em triângulos, se a implementação do OpenGL renderiza polígonos executando essa decomposição.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-150">It can also occur after polygons with more than three edges are broken up into triangles, if the OpenGL implementation renders polygons by performing this decomposition.</span></span>

<span data-ttu-id="e3bf6-151">Você pode inserir um marcador no buffer de comentários com [**glPassThrough**](glpassthrough.md).</span><span class="sxs-lookup"><span data-stu-id="e3bf6-151">You can insert a marker into the feedback buffer with [**glPassThrough**](glpassthrough.md).</span></span>

<span data-ttu-id="e3bf6-152">Veja a seguir a gramática para os blocos de valores gravados no buffer de comentários.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-152">The following is the grammar for the blocks of values written into the feedback buffer.</span></span> <span data-ttu-id="e3bf6-153">Cada primitiva é indicada com um valor de identificação exclusivo seguido por algum número de vértices.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-153">Each primitive is indicated with a unique identifying value followed by some number of vertices.</span></span> <span data-ttu-id="e3bf6-154">As entradas de polígono incluem um valor inteiro indicando quantos vértices seguem.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-154">Polygon entries include an integer value indicating how many vertices follow.</span></span> <span data-ttu-id="e3bf6-155">Um vértice é devolvido como um número de valores de ponto flutuante, conforme determinado pelo *tipo*.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-155">A vertex is fed back as some number of floating-point values, as determined by *type*.</span></span> <span data-ttu-id="e3bf6-156">As cores são realimentadas como quatro valores no modo RGBA e um valor no modo de índice de cor.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-156">Colors are fed back as four values in RGBA mode and one value in color-index mode.</span></span>

<span data-ttu-id="e3bf6-157">feedbacklist < feedbackItem feedbacklist \| feedbackItem</span><span class="sxs-lookup"><span data-stu-id="e3bf6-157">feedbackList <  feedbackItem feedbackList \| feedbackItem</span></span>

<span data-ttu-id="e3bf6-158">feedbackItem < ponto \| lineSegment \| Polygon \| bitmap \| pixelRectangle \| PassThru</span><span class="sxs-lookup"><span data-stu-id="e3bf6-158">feedbackItem <  point \| lineSegment \| polygon \| bitmap \| pixelRectangle \| passThru</span></span>

<span data-ttu-id="e3bf6-159">\_vértice do token de ponto do < GL \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-159">point <  GL\_POINT\_TOKEN vertex</span></span>

<span data-ttu-id="e3bf6-160">vértice do vértice do \_ token de linha do lineSegment < GL \_ \| \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-160">lineSegment <  GL\_LINE\_TOKEN vertex vertex \| GL\_LINE\_RESET\_TOKEN vertex vertex</span></span>

<span data-ttu-id="e3bf6-161">símbolo de polígono < GL do polígono \_ \_ n da polispec</span><span class="sxs-lookup"><span data-stu-id="e3bf6-161">polygon <  GL\_POLYGON\_TOKEN n polySpec</span></span>

<span data-ttu-id="e3bf6-162">polispec < vértice de vértice do vértice de vértice do polispec \|</span><span class="sxs-lookup"><span data-stu-id="e3bf6-162">polySpec <  polySpec vertex \| vertex vertex vertex</span></span>

<span data-ttu-id="e3bf6-163">\_vértice do token de bitmap do bitmap < GL \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-163">bitmap <  GL\_BITMAP\_TOKEN vertex</span></span>

<span data-ttu-id="e3bf6-164">vértice do \_ \_ \_ token \| \_ \_ \_ pixel do pixelRectangle < GL</span><span class="sxs-lookup"><span data-stu-id="e3bf6-164">pixelRectangle <  GL\_DRAW\_PIXEL\_TOKEN vertex \| GL\_COPY\_PIXEL\_TOKEN vertex</span></span>

<span data-ttu-id="e3bf6-165">passThru < GL \_ o \_ valor do token de passagem \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-165">passThru <  GL\_PASS\_THROUGH\_TOKEN value</span></span>

<span data-ttu-id="e3bf6-166">vértice < 2D \| 3D \| 3dColor \| 3dColorTexture \| 4dColorTexture</span><span class="sxs-lookup"><span data-stu-id="e3bf6-166">vertex <  2d \| 3d \| 3dColor \| 3dColorTexture \| 4dColorTexture</span></span>

<span data-ttu-id="e3bf6-167">valor de valor de < 2D</span><span class="sxs-lookup"><span data-stu-id="e3bf6-167">2d <  value value</span></span>

<span data-ttu-id="e3bf6-168">valor do valor do valor de < 3D</span><span class="sxs-lookup"><span data-stu-id="e3bf6-168">3d <  value value value</span></span>

<span data-ttu-id="e3bf6-169">cor do valor do valor de < de valor de 3dColor</span><span class="sxs-lookup"><span data-stu-id="e3bf6-169">3dColor <  value value value color</span></span>

<span data-ttu-id="e3bf6-170">3dColorTexture < valor Value valor Color Tex</span><span class="sxs-lookup"><span data-stu-id="e3bf6-170">3dColorTexture <  value value value color tex</span></span>

<span data-ttu-id="e3bf6-171">4dColorTexture < valor valor valor da cor Tex</span><span class="sxs-lookup"><span data-stu-id="e3bf6-171">4dColorTexture <  value value value value color tex</span></span>

<span data-ttu-id="e3bf6-172">índice de < de cores RGBA \|</span><span class="sxs-lookup"><span data-stu-id="e3bf6-172">color <  rgba \| index</span></span>

<span data-ttu-id="e3bf6-173">RGBA < valor do valor do valor do valor</span><span class="sxs-lookup"><span data-stu-id="e3bf6-173">rgba <  value value value value</span></span>

<span data-ttu-id="e3bf6-174">valor de < de índice</span><span class="sxs-lookup"><span data-stu-id="e3bf6-174">index <  value</span></span>

<span data-ttu-id="e3bf6-175">valor do valor do valor de < de valor de Tex</span><span class="sxs-lookup"><span data-stu-id="e3bf6-175">tex <  value value value value</span></span>

<span data-ttu-id="e3bf6-176">O parâmetro *Value* é um número de ponto flutuante, e *n* é um inteiro de ponto flutuante fornecendo o número de vértices no polígono.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-176">The *value* parameter is a floating-point number, and *n* is a floating-point integer giving the number of vertices in the polygon.</span></span> <span data-ttu-id="e3bf6-177">Veja a seguir constantes de ponto flutuante simbólico: \_ token de ponto GL \_ , \_ \_ token de linha gl, token de \_ redefinição de linha GL, token de \_ \_ \_ polígono GL \_ , \_ \_ token de bitmap GL, token \_ \_ de pixel de desenho GL \_ , token de pixel de \_ cópia GL e o \_ \_ \_ token de passagem GL \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e3bf6-177">The following are symbolic floating-point constants: GL\_POINT\_TOKEN, GL\_LINE\_TOKEN, GL\_LINE\_RESET\_TOKEN, GL\_POLYGON\_TOKEN, GL\_BITMAP\_TOKEN, GL\_DRAW\_PIXEL\_TOKEN, GL\_COPY\_PIXEL\_TOKEN, and GL\_PASS\_THROUGH\_TOKEN.</span></span> <span data-ttu-id="e3bf6-178">\_ \_ \_ O token de redefinição de linha GL é retornado sempre que o padrão de Stipple de linha é redefinido.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-178">GL\_LINE\_RESET\_TOKEN is returned whenever the line stipple pattern is reset.</span></span> <span data-ttu-id="e3bf6-179">Os dados retornados como um vértice dependem do *tipo* de comentário.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-179">The data returned as a vertex depends on the feedback *type*.</span></span>

<span data-ttu-id="e3bf6-180">A tabela a seguir fornece a correspondência entre o *tipo* e o número de valores por vértice; *k* é 1 no modo de índice de cor e 4 no modo RGBA.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-180">The following table gives the correspondence between *type* and the number of values per vertex; *k* is 1 in color-index mode and 4 in RGBA mode.</span></span>



| <span data-ttu-id="e3bf6-181">Tipo</span><span class="sxs-lookup"><span data-stu-id="e3bf6-181">Type</span></span>                   | <span data-ttu-id="e3bf6-182">Coordenadas</span><span class="sxs-lookup"><span data-stu-id="e3bf6-182">Coordinates</span></span>        | <span data-ttu-id="e3bf6-183">Cor</span><span class="sxs-lookup"><span data-stu-id="e3bf6-183">Color</span></span> | <span data-ttu-id="e3bf6-184">Textura</span><span class="sxs-lookup"><span data-stu-id="e3bf6-184">Texture</span></span> | <span data-ttu-id="e3bf6-185">Número total de valores</span><span class="sxs-lookup"><span data-stu-id="e3bf6-185">Total number of values</span></span> |
|------------------------|--------------------|-------|---------|------------------------|
| <span data-ttu-id="e3bf6-186">GL \_ 2D</span><span class="sxs-lookup"><span data-stu-id="e3bf6-186">GL\_2D</span></span>                 | <span data-ttu-id="e3bf6-187">*x*, *y*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-187">*x*, *y*</span></span>           |       |         | <span data-ttu-id="e3bf6-188">2</span><span class="sxs-lookup"><span data-stu-id="e3bf6-188">2</span></span>                      |
| <span data-ttu-id="e3bf6-189">GL \_ 3D</span><span class="sxs-lookup"><span data-stu-id="e3bf6-189">GL\_3D</span></span>                 | <span data-ttu-id="e3bf6-190">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-190">*x*, *y*, *z*</span></span>      |       |         | <span data-ttu-id="e3bf6-191">3</span><span class="sxs-lookup"><span data-stu-id="e3bf6-191">3</span></span>                      |
| <span data-ttu-id="e3bf6-192">Cor do GL \_ 3D \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-192">GL\_3D\_COLOR</span></span>          | <span data-ttu-id="e3bf6-193">*x*, *y*, *z*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-193">*x*, *y*, *z*</span></span>      | <span data-ttu-id="e3bf6-194">*c*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-194">*k*</span></span>   |         | <span data-ttu-id="e3bf6-195">3 + *k*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-195">3 + *k*</span></span>                |
| <span data-ttu-id="e3bf6-196">\_Textura de \_ cores \_ 3D GL</span><span class="sxs-lookup"><span data-stu-id="e3bf6-196">GL\_3D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="e3bf6-197">*x*, *y*, *z*,</span><span class="sxs-lookup"><span data-stu-id="e3bf6-197">*x*, *y*, *z*,</span></span>     | <span data-ttu-id="e3bf6-198">*c*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-198">*k*</span></span>   | <span data-ttu-id="e3bf6-199">4</span><span class="sxs-lookup"><span data-stu-id="e3bf6-199">4</span></span>       | <span data-ttu-id="e3bf6-200">7 + *k*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-200">7 + *k*</span></span>                |
| <span data-ttu-id="e3bf6-201">\_Textura de \_ cores GL 4D \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-201">GL\_4D\_COLOR\_TEXTURE</span></span> | <span data-ttu-id="e3bf6-202">*x*, *y*, *z*, *w*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-202">*x*, *y*, *z*, *w*</span></span> | <span data-ttu-id="e3bf6-203">*c*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-203">*k*</span></span>   | <span data-ttu-id="e3bf6-204">4</span><span class="sxs-lookup"><span data-stu-id="e3bf6-204">4</span></span>       | <span data-ttu-id="e3bf6-205">8 + *k*</span><span class="sxs-lookup"><span data-stu-id="e3bf6-205">8 + *k*</span></span>                |



 

<span data-ttu-id="e3bf6-206">As coordenadas de vértice de comentários estão em coordenadas de janela, exceto *w*, que está em coordenadas de clipe.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-206">Feedback vertex coordinates are in window coordinates, except *w*, which is in clip coordinates.</span></span> <span data-ttu-id="e3bf6-207">As cores de comentários serão iluminadas se a iluminação estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-207">Feedback colors are lighted, if lighting is enabled.</span></span> <span data-ttu-id="e3bf6-208">As coordenadas de textura de comentários serão geradas se a geração de coordenadas de textura estiver habilitada.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-208">Feedback texture coordinates are generated, if texture coordinate generation is enabled.</span></span> <span data-ttu-id="e3bf6-209">Eles são sempre transformados pela matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-209">They are always transformed by the texture matrix.</span></span>

<span data-ttu-id="e3bf6-210">A função **glFeedbackBuffer** , quando usada em uma lista de exibição, não é compilada na lista de exibição, mas sim executada imediatamente.</span><span class="sxs-lookup"><span data-stu-id="e3bf6-210">The **glFeedbackBuffer** function, when used in a display list, is not compiled into the display list but rather is executed immediately.</span></span>

<span data-ttu-id="e3bf6-211">A função a seguir recupera informações relacionadas a **glFeedbackBuffer**:</span><span class="sxs-lookup"><span data-stu-id="e3bf6-211">The following function retrieves information related to **glFeedbackBuffer**:</span></span>

<span data-ttu-id="e3bf6-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) com o \_ modo de renderização Argument GL \_</span><span class="sxs-lookup"><span data-stu-id="e3bf6-212">[**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) with argument GL\_RENDER\_MODE</span></span>

## <a name="requirements"></a><span data-ttu-id="e3bf6-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3bf6-213">Requirements</span></span>



| <span data-ttu-id="e3bf6-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3bf6-214">Requirement</span></span> | <span data-ttu-id="e3bf6-215">Valor</span><span class="sxs-lookup"><span data-stu-id="e3bf6-215">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3bf6-216">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3bf6-216">Minimum supported client</span></span><br/> | <span data-ttu-id="e3bf6-217">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3bf6-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e3bf6-218">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3bf6-218">Minimum supported server</span></span><br/> | <span data-ttu-id="e3bf6-219">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e3bf6-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e3bf6-220">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e3bf6-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3bf6-221"><dt>GL. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-221"><dt>Gl.h</dt></span></span> </dl>         |
| <span data-ttu-id="e3bf6-222">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e3bf6-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3bf6-223"><dt>Opengl32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-223"><dt>Opengl32.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3bf6-224">DLL</span><span class="sxs-lookup"><span data-stu-id="e3bf6-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3bf6-225"><dt>Opengl32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3bf6-225"><dt>Opengl32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3bf6-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3bf6-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3bf6-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-228">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-228">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-229">**glGet**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-229">**glGet**</span></span>](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-230">**glLineStipple**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-230">**glLineStipple**</span></span>](gllinestipple.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-231">**glPassThrough**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-231">**glPassThrough**</span></span>](glpassthrough.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-232">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-232">**glPolygonMode**</span></span>](glpolygonmode.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-233">**glRenderMode**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-233">**glRenderMode**</span></span>](glrendermode.md)
</dt> <dt>

[<span data-ttu-id="e3bf6-234">**glSelectBuffer**</span><span class="sxs-lookup"><span data-stu-id="e3bf6-234">**glSelectBuffer**</span></span>](glselectbuffer.md)
</dt> </dl>

 

 





