---
title: função gluTessCallback (Glu. h)
description: A função gluTessCallback define um retorno de chamada para um objeto de mosaico.
ms.assetid: a9709919-d34c-42c4-82b8-6a503f2b39b0
keywords:
- função gluTessCallback OpenGL
topic_type:
- apiref
api_name:
- gluTessCallback
api_location:
- Glu32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17cdba8b9dd9a3e762a93923a3c353fbc9578377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919057"
---
# <a name="glutesscallback-function"></a><span data-ttu-id="49216-104">função gluTessCallback</span><span class="sxs-lookup"><span data-stu-id="49216-104">gluTessCallback function</span></span>

<span data-ttu-id="49216-105">A função **gluTessCallback** define um retorno de chamada para um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="49216-105">The **gluTessCallback** function defines a callback for a tessellation object.</span></span>

## <a name="syntax"></a><span data-ttu-id="49216-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49216-106">Syntax</span></span>


```C++
void WINAPI gluTessCallback(
   GLUtesselator *tess,
   GLenum        which,
   void (CALLBACK *fn)()
);
```



## <a name="parameters"></a><span data-ttu-id="49216-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49216-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49216-108">*tess*</span><span class="sxs-lookup"><span data-stu-id="49216-108">*tess*</span></span> 
</dt> <dd>

<span data-ttu-id="49216-109">O objeto de mosaico (criado com [**gluNewTess**](glunewtess.md)).</span><span class="sxs-lookup"><span data-stu-id="49216-109">The tessellation object (created with [**gluNewTess**](glunewtess.md)).</span></span>

</dd> <dt>

<span data-ttu-id="49216-110">*Onde*</span><span class="sxs-lookup"><span data-stu-id="49216-110">*which*</span></span> 
</dt> <dd>

<span data-ttu-id="49216-111">O retorno de chamada que está sendo definido.</span><span class="sxs-lookup"><span data-stu-id="49216-111">The callback being defined.</span></span> <span data-ttu-id="49216-112">Os valores a seguir são válidos: GLU \_ Tess \_ begin, glu \_ Tess \_ begin \_ data, GLU \_ Tess \_ \_ endflag, glu Tess \_ \_ \_ endflag \_ data, glu \_ Tess \_ vértice, glu \_ Tess \_ Vertex \_ data, glu \_ Tess \_ end, glu \_ Tess \_ end \_ data, glu \_ Tess combine, glu Tess \_ \_ \_ Combine dados, glu Tess \_ \_ \_ Error e Glu Tess \_ \_ Error \_ Data.</span><span class="sxs-lookup"><span data-stu-id="49216-112">The following values are valid: GLU\_TESS\_BEGIN, GLU\_TESS\_BEGIN\_DATA, GLU\_TESS\_EDGE\_FLAG, GLU\_TESS\_EDGE\_FLAG\_DATA, GLU\_TESS\_VERTEX, GLU\_TESS\_VERTEX\_DATA, GLU\_TESS\_END, GLU\_TESS\_END\_DATA, GLU\_TESS\_COMBINE, GLU\_TESS\_COMBINE\_DATA, GLU\_TESS\_ERROR, and GLU\_TESS\_ERROR\_DATA.</span></span>

<span data-ttu-id="49216-113">Para obter mais informações sobre esses retornos de chamada, consulte a seção de comentários a seguir.</span><span class="sxs-lookup"><span data-stu-id="49216-113">For more information on these callbacks, see the following Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="49216-114">*fn*</span><span class="sxs-lookup"><span data-stu-id="49216-114">*fn*</span></span> 
</dt> <dd>

<span data-ttu-id="49216-115">A função a ser chamada.</span><span class="sxs-lookup"><span data-stu-id="49216-115">The function to be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49216-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49216-116">Return value</span></span>

<span data-ttu-id="49216-117">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="49216-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="49216-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="49216-118">Remarks</span></span>

<span data-ttu-id="49216-119">Use **gluTessCallback** para especificar um retorno de chamada a ser usado por um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="49216-119">Use **gluTessCallback** to specify a callback to be used by a tessellation object.</span></span> <span data-ttu-id="49216-120">Se o retorno de chamada especificado já estiver definido, ele será substituído.</span><span class="sxs-lookup"><span data-stu-id="49216-120">If the specified callback is already defined, then it is replaced.</span></span> <span data-ttu-id="49216-121">Se *FN* for **NULL**, o retorno de chamada existente se tornará indefinido.</span><span class="sxs-lookup"><span data-stu-id="49216-121">If *fn* is **NULL**, then the existing callback becomes undefined.</span></span>

<span data-ttu-id="49216-122">O objeto de mosaico usa esses retornos de chamada para descrever como um polígono especificado é dividido em triângulos.</span><span class="sxs-lookup"><span data-stu-id="49216-122">The tessellation object uses these callbacks to describe how a polygon that you specify is broken into triangles.</span></span>

<span data-ttu-id="49216-123">Há duas versões de cada retorno de chamada, uma com dados de polígono que você pode definir e uma sem.</span><span class="sxs-lookup"><span data-stu-id="49216-123">There are two versions of each callback, one with polygon data that you can define and one without.</span></span> <span data-ttu-id="49216-124">Se ambas as versões de um retorno de chamada específico forem especificadas, o retorno de chamada com os dados de polígono que você especificar será usado.</span><span class="sxs-lookup"><span data-stu-id="49216-124">If both versions of a particular callback are specified, the callback with the polygon data you specify will be used.</span></span> <span data-ttu-id="49216-125">O parâmetro de *\_ dados Polygon* de [**gluTessBeginPolygon**](glutessbeginpolygon.md) é uma cópia do ponteiro que foi especificado quando **gluTessBeginPolygon** foi chamado.</span><span class="sxs-lookup"><span data-stu-id="49216-125">The *polygon\_data* parameter of [**gluTessBeginPolygon**](glutessbeginpolygon.md) is a copy of the pointer that was specified when **gluTessBeginPolygon** was called.</span></span>

<span data-ttu-id="49216-126">Veja a seguir os retornos de chamada válidos:</span><span class="sxs-lookup"><span data-stu-id="49216-126">The following are valid callbacks:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="49216-127">Callback</span><span class="sxs-lookup"><span data-stu-id="49216-127">Callback</span></span></th>
<th><span data-ttu-id="49216-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="49216-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="49216-129">GLU_TESS_BEGIN</span><span class="sxs-lookup"><span data-stu-id="49216-129">GLU_TESS_BEGIN</span></span></td>
<td><span data-ttu-id="49216-130">O retorno de chamada GLU_TESS_BEGIN é invocado como <a href="glbegin.md"><strong>glBegin</strong></a> para indicar o início de um primitivo (triângulo).</span><span class="sxs-lookup"><span data-stu-id="49216-130">The GLU_TESS_BEGIN callback is invoked like <a href="glbegin.md"><strong>glBegin</strong></a> to indicate the start of a (triangle) primitive.</span></span> <span data-ttu-id="49216-131">A função usa um único argumento do tipo <strong>GLenum</strong>.</span><span class="sxs-lookup"><span data-stu-id="49216-131">The function takes a single argument of type <strong>GLenum</strong>.</span></span> <span data-ttu-id="49216-132">Se você definir a propriedade GLU_TESS_BOUNDARY_ONLY como GL_FALSE, o argumento será definido como GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP ou GL_TRIANGLES.</span><span class="sxs-lookup"><span data-stu-id="49216-132">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_FALSE, the argument is set to either GL_TRIANGLE_FAN, GL_TRIANGLE_STRIP, or GL_TRIANGLES.</span></span> <span data-ttu-id="49216-133">Se você definir a propriedade GLU_TESS_BOUNDARY_ONLY como GL_TRUE, o argumento será definido como GL_LINE_LOOP.</span><span class="sxs-lookup"><span data-stu-id="49216-133">If you set the GLU_TESS_BOUNDARY_ONLY property to GL_TRUE, the argument is set to GL_LINE_LOOP.</span></span> <span data-ttu-id="49216-134">O protótipo de função para esse retorno de chamada é o seguinte: <strong>void</strong> <strong>begin</strong> ( <em>tipo</em><strong>GLenum</strong> );</span><span class="sxs-lookup"><span data-stu-id="49216-134">The function prototype for this callback is as follows: <strong>void</strong> <strong>begin</strong> (<strong>GLenum</strong> <em>type</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49216-135">GLU_TESS_BEGIN_DATA</span><span class="sxs-lookup"><span data-stu-id="49216-135">GLU_TESS_BEGIN_DATA</span></span></td>
<td><span data-ttu-id="49216-136">GLU_TESS_BEGIN_DATA é o mesmo que o retorno de chamada GLU_TESS_BEGIN, exceto pelo fato de que ele usa um argumento de ponteiro adicional.</span><span class="sxs-lookup"><span data-stu-id="49216-136">GLU_TESS_BEGIN_DATA is the same as the GLU_TESS_BEGIN callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="49216-137">Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-137">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="49216-138">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>beginData</strong> ( <em>tipo</em><strong>GLenum</strong> , <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-138">The function prototype for this callback is: <strong>void</strong> <strong>beginData</strong> (<strong>GLenum</strong> <em>type</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49216-139">GLU_TESS_EDGE_FLAG</span><span class="sxs-lookup"><span data-stu-id="49216-139">GLU_TESS_EDGE_FLAG</span></span></td>
<td><span data-ttu-id="49216-140">O retorno de chamada GLU_TESS_EDGE_FLAG é semelhante a <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-140">The GLU_TESS_EDGE_FLAG callback is similar to <a href="gledgeflag-functions.md"><strong>glEdgeFlag</strong></a>.</span></span> <span data-ttu-id="49216-141">A função usa um único sinalizador booliano que indica quais bordas se encontram no limite do polígono.</span><span class="sxs-lookup"><span data-stu-id="49216-141">The function takes a single Boolean flag that indicates which edges lie on the polygon boundary.</span></span> <span data-ttu-id="49216-142">Se o sinalizador for GL_TRUE, cada vértice a seguir iniciará uma borda que está no limite do polígono; ou seja, uma borda que separa uma região interior de um exterior.</span><span class="sxs-lookup"><span data-stu-id="49216-142">If the flag is GL_TRUE, then each vertex that follows begins an edge that lies on the polygon boundary; that is, an edge which separates an interior region from an exterior one.</span></span> <span data-ttu-id="49216-143">Se o sinalizador for GL_FALSE, cada vértice a seguir iniciará uma borda que está no interior do polígono.</span><span class="sxs-lookup"><span data-stu-id="49216-143">If the flag is GL_FALSE, then each vertex that follows begins an edge that lies in the polygon interior.</span></span> <span data-ttu-id="49216-144">O retorno de chamada GLU_TESS_EDGE_FLAG (se definido) é invocado antes de o primeiro retorno de chamada de vértice ser feito.</span><span class="sxs-lookup"><span data-stu-id="49216-144">The GLU_TESS_EDGE_FLAG callback (if defined) is invoked before the first vertex callback is made.</span></span> <span data-ttu-id="49216-145">Como os ventiladores de triângulo e as faixas de triângulo não dão suporte a sinalizadores de borda, o retorno de chamada de início não é chamado com GL_TRIANGLE_FAN ou GL_TRIANGLE_STRIP se um retorno de chamada de sinalizador de borda for fornecido.</span><span class="sxs-lookup"><span data-stu-id="49216-145">Because triangle fans and triangle strips do not support edge flags, the begin callback is not called with GL_TRIANGLE_FAN or GL_TRIANGLE_STRIP if an edge flag callback is provided.</span></span> <span data-ttu-id="49216-146">Em vez disso, os ventiladores e as faixas são convertidos em triângulos independentes.</span><span class="sxs-lookup"><span data-stu-id="49216-146">Instead, the fans and strips are converted to independent triangles.</span></span> <span data-ttu-id="49216-147">O protótipo de função para este retorno de chamada é:</span><span class="sxs-lookup"><span data-stu-id="49216-147">The function prototype for this callback is:</span></span><br/> <span data-ttu-id="49216-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong></strong> <em>sinalizador</em>GLboolean);</span><span class="sxs-lookup"><span data-stu-id="49216-148"><strong>void</strong> <strong>edgeFlag</strong> (<strong>GLboolean</strong> <em>flag</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49216-149">GLU_TESS_EDGE_FLAG_DATA</span><span class="sxs-lookup"><span data-stu-id="49216-149">GLU_TESS_EDGE_FLAG_DATA</span></span></td>
<td><span data-ttu-id="49216-150">O retorno de chamada GLU_TESS_EDGE_FLAG_DATA é o mesmo que o GLU_TESS_EDGE_FLAG retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional.</span><span class="sxs-lookup"><span data-stu-id="49216-150">The GLU_TESS_EDGE_FLAG_DATA callback is the same as the GLU_TESS_EDGE_FLAG callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="49216-151">Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-151">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="49216-152">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>edgeFlagData</strong> ( <em>sinalizador</em><strong>GLboolean</strong> , <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-152">The function prototype for this callback is: <strong>void</strong> <strong>edgeFlagData</strong> (<strong>GLboolean</strong> <em>flag</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49216-153">GLU_TESS_VERTEX</span><span class="sxs-lookup"><span data-stu-id="49216-153">GLU_TESS_VERTEX</span></span></td>
<td><span data-ttu-id="49216-154">O retorno de chamada GLU_TESS_VERTEX é invocado entre os retornos de chamada Begin e end.</span><span class="sxs-lookup"><span data-stu-id="49216-154">The GLU_TESS_VERTEX callback is invoked between the begin and end callbacks.</span></span> <span data-ttu-id="49216-155">Ele é semelhante a glVertex e define os vértices dos triângulos criados pelo processo de mosaico.</span><span class="sxs-lookup"><span data-stu-id="49216-155">It is similar to glVertex , and it defines the vertexes of the triangles created by the tessellation process.</span></span> <span data-ttu-id="49216-156">A função usa um ponteiro como seu único argumento.</span><span class="sxs-lookup"><span data-stu-id="49216-156">The function takes a pointer as its only argument.</span></span> <span data-ttu-id="49216-157">Esse ponteiro é idêntico ao ponteiro opaco que você forneceu quando definiu o vértice (consulte <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span><span class="sxs-lookup"><span data-stu-id="49216-157">This pointer is identical to the opaque pointer that you provided when you defined the vertex (see <a href="glutessvertex.md"><strong>gluTessVertex</strong></a>).</span></span> <span data-ttu-id="49216-158">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-158">The function prototype for this callback is: <strong>void</strong> <strong>vertex</strong> (<strong>void</strong> \* <em>vertex_data</em>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49216-159">GLU_TESS_VERTEX_DATA</span><span class="sxs-lookup"><span data-stu-id="49216-159">GLU_TESS_VERTEX_DATA</span></span></td>
<td><span data-ttu-id="49216-160">O GLU_TESS_VERTEX_DATA é o mesmo que o retorno de chamada GLU_TESS_VERTEX, exceto pelo fato de que ele usa um argumento de ponteiro adicional.</span><span class="sxs-lookup"><span data-stu-id="49216-160">The GLU_TESS_VERTEX_DATA is the same as the GLU_TESS_VERTEX callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="49216-161">Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-161">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="49216-162">O protótipo de função para este retorno de chamada é: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-162">The function prototype for this callback is: <strong>void</strong>  <strong>vertexData</strong> (void \* <em>vertex_data</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49216-163">GLU_TESS_END</span><span class="sxs-lookup"><span data-stu-id="49216-163">GLU_TESS_END</span></span></td>
<td><span data-ttu-id="49216-164">O retorno de chamada GLU_TESS_END tem a mesma finalidade que <a href="glend.md"><strong>glEnd</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-164">The GLU_TESS_END callback serves the same purpose as <a href="glend.md"><strong>glEnd</strong></a>.</span></span> <span data-ttu-id="49216-165">Indica o fim de um primitivo e não usa argumentos.</span><span class="sxs-lookup"><span data-stu-id="49216-165">It indicates the end of a primitive, and it takes no arguments.</span></span> <span data-ttu-id="49216-166">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span><span class="sxs-lookup"><span data-stu-id="49216-166">The function prototype for this callback is: <strong>void</strong> <strong>end</strong> (<strong>void</strong>);</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49216-167">GLU_TESS_END_DATA</span><span class="sxs-lookup"><span data-stu-id="49216-167">GLU_TESS_END_DATA</span></span></td>
<td><span data-ttu-id="49216-168">O retorno de chamada GLU_TESS_END_DATA é o mesmo que o GLU_TESS_END retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional.</span><span class="sxs-lookup"><span data-stu-id="49216-168">The GLU_TESS_END_DATA callback is the same as the GLU_TESS_END callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="49216-169">Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-169">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="49216-170">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-170">The function prototype for this callback is: <strong>void</strong> <strong>endData</strong> (<strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49216-171">GLU_TESS_COMBINE</span><span class="sxs-lookup"><span data-stu-id="49216-171">GLU_TESS_COMBINE</span></span></td>
<td><span data-ttu-id="49216-172">Chame o GLU_TESS_COMBINE retorno de chamada para criar um novo vértice quando o mosaico detectar uma interseção ou para mesclar recursos.</span><span class="sxs-lookup"><span data-stu-id="49216-172">Call the GLU_TESS_COMBINE callback to create a new vertex when the tessellation detects an intersection, or to merge features.</span></span> <span data-ttu-id="49216-173">A função usa quatro argumentos: uma matriz de três elementos, cada um do tipo Gldouble.</span><span class="sxs-lookup"><span data-stu-id="49216-173">The function takes four arguments: An array of three elements, each of type Gldouble.</span></span><br/> <span data-ttu-id="49216-174">Uma matriz de quatro ponteiros.</span><span class="sxs-lookup"><span data-stu-id="49216-174">An array of four pointers.</span></span><br/> <span data-ttu-id="49216-175">Uma matriz de quatro elementos, cada um do tipo GLfloat.</span><span class="sxs-lookup"><span data-stu-id="49216-175">An array of four elements, each of type GLfloat.</span></span><br/> <span data-ttu-id="49216-176">Um ponteiro para um ponteiro.</span><span class="sxs-lookup"><span data-stu-id="49216-176">A pointer to a pointer.</span></span><br/> <span data-ttu-id="49216-177">O protótipo de função para este retorno de chamada é:</span><span class="sxs-lookup"><span data-stu-id="49216-177">The function prototype for this callback is:</span></span> <br/> <span data-ttu-id="49216-178"><strong>void</strong> <strong>Combine</strong>(<strong>GLdouble</strong> <em>CoOrds</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong></strong> <em>peso</em>de GLfloat [4], <strong></strong>  \*\* <em>indados</em>nulos);</span><span class="sxs-lookup"><span data-stu-id="49216-178"><strong>void</strong> <strong>combine</strong>(<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \* <em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>);</span></span><br/> <span data-ttu-id="49216-179">O vértice é definido como uma combinação linear de até quatro vértices existentes, armazenados em vertex_data.</span><span class="sxs-lookup"><span data-stu-id="49216-179">The vertex is defined as a linear combination of up to four existing vertexes, stored in vertex_data.</span></span> <span data-ttu-id="49216-180">Os coeficientes da combinação linear são fornecidos por peso; esses pesos sempre somam 1,0.</span><span class="sxs-lookup"><span data-stu-id="49216-180">The coefficients of the linear combination are given by weight; these weights always sum to 1.0.</span></span> <span data-ttu-id="49216-181">Todos os ponteiros de vértice são válidos mesmo quando alguns dos pesos são zero.</span><span class="sxs-lookup"><span data-stu-id="49216-181">All vertex pointers are valid even when some of the weights are zero.</span></span> <span data-ttu-id="49216-182">O parâmetro CoOrds fornece o local do novo vértice.</span><span class="sxs-lookup"><span data-stu-id="49216-182">The coords parameter gives the location of the new vertex.</span></span><br/> <span data-ttu-id="49216-183">Aloque outro vértice, interpolar parâmetros usando vertex_data e peso e retornar o novo ponteiro de vértice em OutData.</span><span class="sxs-lookup"><span data-stu-id="49216-183">Allocate another vertex, interpolate parameters using vertex_data and weight, and return the new vertex pointer in outData.</span></span> <span data-ttu-id="49216-184">Esse identificador é fornecido durante os retornos de chamada de renderização.</span><span class="sxs-lookup"><span data-stu-id="49216-184">This handle is supplied during rendering callbacks.</span></span> <span data-ttu-id="49216-185">Libere a memória em algum momento depois de chamar <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-185">Free the memory sometime after calling <a href="glutessendpolygon.md"><strong>gluTessEndPolygon</strong></a>.</span></span><br/> <span data-ttu-id="49216-186">Por exemplo, se o polígono estiver em um plano arbitrário no espaço tridimensional e você associar uma cor a cada vértice, o retorno de chamada GLU_TESS_COMBINE poderá ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="49216-186">For example, if the polygon lies in an arbitrary plane in three-dimensional space, and you associate a color with each vertex, the GLU_TESS_COMBINE callback might look like the following:</span></span><br/>
<pre data-space="preserve"><code>void myCombine( GLdouble coords[3], VERTEX *d[4], 
                GLfloat w[4], VERTEX **dataOut ) 
{ 
    VERTEX *newVertex = new_vertex(); 
    newVertex->x = coords[0]; 
    newVertex->y = coords[1]; 
    newVertex->z = coords[2]; 
    newVertex->r = w[0]*d[0]->r + w[1]*d[1]->r + w[2]*d[2]->r + 
                   w[3]*d[3]->r; 
    newVertex->g = w[0]*d[0]->g + w[1]*d[1]->g + w[2]*d[2]->g + 
                   w[3]*d[3]->g; 
    newVertex->b = w[0]*d[0]->b + w[1]*d[1]->b + w[2]*d[2]->b + 
                   w[3]*d[3]->b; 
    newVertex->a = w[0]*d[0]->a + w[1]*d[1]->a + w[2]*d[2]->a + 
                   w[3]*d[3]->a; 
    *dataOut = newVertex; 
}</code></pre>
<span data-ttu-id="49216-187">Quando o mosaico detecta uma interseção, o GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA retorno de chamada (veja abaixo) deve ser definido e deve gravar um ponteiro não<strong>nulo</strong> no dataout.</span><span class="sxs-lookup"><span data-stu-id="49216-187">When the tessellation detects an intersection, the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback (see below) must be defined, and must write a non-<strong>NULL</strong> pointer into dataOut.</span></span> <span data-ttu-id="49216-188">Caso contrário, o erro GLU_TESS_NEED_COMBINE_CALLBACK ocorrerá e nenhuma saída será gerada.</span><span class="sxs-lookup"><span data-stu-id="49216-188">Otherwise the GLU_TESS_NEED_COMBINE_CALLBACK error occurs, and no output is generated.</span></span> <span data-ttu-id="49216-189">(Esse é o único erro que pode ocorrer durante o mosaico e a renderização.)</span><span class="sxs-lookup"><span data-stu-id="49216-189">(This is the only error that can occur during tessellation and rendering.)</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49216-190">GLU_TESS_COMBINE_DATA</span><span class="sxs-lookup"><span data-stu-id="49216-190">GLU_TESS_COMBINE_DATA</span></span></td>
<td><span data-ttu-id="49216-191">O retorno de chamada GLU_TESS_COMBINE_DATA é o mesmo que o GLU_TESS_COMBINE retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional.</span><span class="sxs-lookup"><span data-stu-id="49216-191">The GLU_TESS_COMBINE_DATA callback is the same as the GLU_TESS_COMBINE callback except that it takes an additional pointer argument.</span></span> <span data-ttu-id="49216-192">Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-192">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="49216-193">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>CoOrds</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>Weight</em>[4], <strong>void</strong>  \*\* <em>Indata</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-193">The function prototype for this callback is: <strong>void</strong> <strong>combineData</strong> (<strong>GLdouble</strong> <em>coords</em>[3], <strong>void</strong> \*<em>vertex_data</em>[4], <strong>GLfloat</strong> <em>weight</em>[4], <strong>void</strong> \*\*<em>outData</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="49216-194">GLU_TESS_ERROR</span><span class="sxs-lookup"><span data-stu-id="49216-194">GLU_TESS_ERROR</span></span></td>
<td><span data-ttu-id="49216-195">O retorno de chamada GLU_TESS_ERROR é chamado quando um erro é encontrado.</span><span class="sxs-lookup"><span data-stu-id="49216-195">The GLU_TESS_ERROR callback is called when an error is encountered.</span></span> <span data-ttu-id="49216-196">O argumento One é do tipo <strong>GLenum</strong>; Ele indica o erro específico que ocorreu e é definido como um dos seguintes: GLU_TESS_MISSING_BEGIN_POLYGON</span><span class="sxs-lookup"><span data-stu-id="49216-196">The one argument is of type <strong>GLenum</strong>; it indicates the specific error that occurred and is set to one of the following: GLU_TESS_MISSING_BEGIN_POLYGON</span></span><br/> <span data-ttu-id="49216-197">GLU_TESS_MISSING_END_POLYGON</span><span class="sxs-lookup"><span data-stu-id="49216-197">GLU_TESS_MISSING_END_POLYGON</span></span><br/> <span data-ttu-id="49216-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="49216-198">GLU_TESS_MISSING_BEGIN_CONTOUR</span></span><br/> <span data-ttu-id="49216-199">GLU_TESS_MISSING_END_CONTOUR</span><span class="sxs-lookup"><span data-stu-id="49216-199">GLU_TESS_MISSING_END_CONTOUR</span></span><br/> <span data-ttu-id="49216-200">GLU_TESS_COORD_TOO_LARGE</span><span class="sxs-lookup"><span data-stu-id="49216-200">GLU_TESS_COORD_TOO_LARGE</span></span><br/> <span data-ttu-id="49216-201">GLU_TESS_NEED_COMBINE_CALLBACK</span><span class="sxs-lookup"><span data-stu-id="49216-201">GLU_TESS_NEED_COMBINE_CALLBACK</span></span><br/> <span data-ttu-id="49216-202">Chame gluErrorString para recuperar cadeias de caracteres que descrevem esses erros.</span><span class="sxs-lookup"><span data-stu-id="49216-202">Call gluErrorString to retrieve character strings describing these errors.</span></span> <span data-ttu-id="49216-203">O protótipo de função para esse retorno de chamada é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="49216-203">The function prototype for this callback is as follows:</span></span><br/> <span data-ttu-id="49216-204"><strong></strong> <strong>erro</strong> de void (<strong>GLenum</strong> <em>errno</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-204"><strong>void</strong> <strong>error</strong> (<strong>GLenum</strong> <em>errno</em>);</span></span><br/> <span data-ttu-id="49216-205">A biblioteca GLU recupera os quatro primeiros erros inserindo a chamada ou chamadas ausentes.</span><span class="sxs-lookup"><span data-stu-id="49216-205">The GLU library recovers from the first four errors by inserting the missing call or calls.</span></span> <span data-ttu-id="49216-206">GLU_TESS_COORD_TOO_LARGE indica que alguma coordenada de vértice excedeu a constante predefinida GLU_TESS_MAX_COORD em valor absoluto e que o valor foi clamped.</span><span class="sxs-lookup"><span data-stu-id="49216-206">GLU_TESS_COORD_TOO_LARGE indicates that some vertex coordinate exceeded the predefined constant GLU_TESS_MAX_COORD in absolute value, and that the value has been clamped.</span></span> <span data-ttu-id="49216-207">(Os valores de coordenadas devem ser pequenos o suficiente para que dois possam ser multiplicados em conjunto sem estouro.) GLU_TESS_NEED_COMBINE_CALLBACK indica que o mosaico detectou uma interseção entre duas bordas nos dados de entrada e o retorno de chamada GLU_TESS_COMBINE ou GLU_TESS_COMBINE_DATA não foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="49216-207">(Coordinate values must be small enough that two can be multiplied together without overflow.) GLU_TESS_NEED_COMBINE_CALLBACK indicates that the tessellation detected an intersection between two edges in the input data, and the GLU_TESS_COMBINE or GLU_TESS_COMBINE_DATA callback was not provided.</span></span> <span data-ttu-id="49216-208">Nenhuma saída será gerada.</span><span class="sxs-lookup"><span data-stu-id="49216-208">No output will be generated.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="49216-209">GLU_TESS_ERROR_DATA</span><span class="sxs-lookup"><span data-stu-id="49216-209">GLU_TESS_ERROR_DATA</span></span></td>
<td><span data-ttu-id="49216-210">O retorno de chamada GLU_TESS_ERROR_DATA é o mesmo que o GLU_TESS_ERROR retorno de chamada, exceto pelo fato de que ele usa um argumento de ponteiro adicional.</span><span class="sxs-lookup"><span data-stu-id="49216-210">The GLU_TESS_ERROR_DATA callback is the same as the GLU_TESS_ERROR callback, except that it takes an additional pointer argument.</span></span> <span data-ttu-id="49216-211">Esse ponteiro é idêntico ao ponteiro opaco fornecido quando você chama <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="49216-211">This pointer is identical to the opaque pointer provided when you call <a href="glutessbeginpolygon.md"><strong>gluTessBeginPolygon</strong></a>.</span></span> <span data-ttu-id="49216-212">O protótipo de função para este retorno de chamada é: <strong>void</strong> <strong>ErrorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span><span class="sxs-lookup"><span data-stu-id="49216-212">The function prototype for this callback is: <strong>void</strong> <strong>errorData</strong> (<strong>GLenum</strong> <em>errno</em>, <strong>void</strong> \* <em>polygon_data</em>);</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="49216-213">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49216-213">Requirements</span></span>



| <span data-ttu-id="49216-214">Requisito</span><span class="sxs-lookup"><span data-stu-id="49216-214">Requirement</span></span> | <span data-ttu-id="49216-215">Valor</span><span class="sxs-lookup"><span data-stu-id="49216-215">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="49216-216">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49216-216">Minimum supported client</span></span><br/> | <span data-ttu-id="49216-217">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49216-217">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="49216-218">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49216-218">Minimum supported server</span></span><br/> | <span data-ttu-id="49216-219">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="49216-219">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="49216-220">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="49216-220">Header</span></span><br/>                   | <dl> <span data-ttu-id="49216-221"><dt>GLU. h</dt></span><span class="sxs-lookup"><span data-stu-id="49216-221"><dt>Glu.h</dt></span></span> </dl>     |
| <span data-ttu-id="49216-222">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="49216-222">Library</span></span><br/>                  | <dl> <span data-ttu-id="49216-223"><dt>Glu32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49216-223"><dt>Glu32.lib</dt></span></span> </dl> |
| <span data-ttu-id="49216-224">DLL</span><span class="sxs-lookup"><span data-stu-id="49216-224">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49216-225"><dt>Glu32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49216-225"><dt>Glu32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49216-226">Confira também</span><span class="sxs-lookup"><span data-stu-id="49216-226">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49216-227">**glBegin**</span><span class="sxs-lookup"><span data-stu-id="49216-227">**glBegin**</span></span>](glbegin.md)
</dt> <dt>

[<span data-ttu-id="49216-228">**glEdgeFlag**</span><span class="sxs-lookup"><span data-stu-id="49216-228">**glEdgeFlag**</span></span>](gledgeflag-functions.md)
</dt> <dt>

[<span data-ttu-id="49216-229">**glEnd**</span><span class="sxs-lookup"><span data-stu-id="49216-229">**glEnd**</span></span>](glend.md)
</dt> <dt>

[<span data-ttu-id="49216-230">**glVertex**</span><span class="sxs-lookup"><span data-stu-id="49216-230">**glVertex**</span></span>](glvertex-functions.md)
</dt> <dt>

[<span data-ttu-id="49216-231">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="49216-231">**gluDeleteTess**</span></span>](gludeletetess.md)
</dt> <dt>

[<span data-ttu-id="49216-232">**gluErrorString**</span><span class="sxs-lookup"><span data-stu-id="49216-232">**gluErrorString**</span></span>](gluerrorstring.md)
</dt> <dt>

[<span data-ttu-id="49216-233">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="49216-233">**gluNewTess**</span></span>](glunewtess.md)
</dt> <dt>

[<span data-ttu-id="49216-234">**gluTessBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="49216-234">**gluTessBeginPolygon**</span></span>](glutessbeginpolygon.md)
</dt> <dt>

[<span data-ttu-id="49216-235">**gluTessEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="49216-235">**gluTessEndPolygon**</span></span>](glutessendpolygon.md)
</dt> <dt>

[<span data-ttu-id="49216-236">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="49216-236">**gluTessVertex**</span></span>](glutessvertex.md)
</dt> </dl>

 

 





