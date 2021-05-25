---
description: Constantes de formato de vértice flexíveis, ou códigos FVF, são usadas para descrever o conteúdo de vértices intercalados em um único fluxo de dados que será processado pelo pipeline de função fixa.
ms.assetid: 85d9f5b2-8e4a-4f92-a587-eae5b293778c
title: D3DFVF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a088dda530904c320720371c76601fd4fb254481
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343254"
---
# <a name="d3dfvf"></a><span data-ttu-id="8286b-103">D3DFVF</span><span class="sxs-lookup"><span data-stu-id="8286b-103">D3DFVF</span></span>

<span data-ttu-id="8286b-104">Constantes de formato de vértice flexíveis, ou códigos FVF, são usadas para descrever o conteúdo de vértices intercalados em um único fluxo de dados que será processado pelo pipeline de função fixa.</span><span class="sxs-lookup"><span data-stu-id="8286b-104">Flexible Vertex Format Constants, or FVF codes, are used to describe the contents of vertices interleaved in a single data stream that will be processed by the fixed-function pipeline.</span></span>

## <a name="vertex-data-flags"></a><span data-ttu-id="8286b-105">Sinalizadores de dados de vértice</span><span class="sxs-lookup"><span data-stu-id="8286b-105">Vertex Data Flags</span></span>

<span data-ttu-id="8286b-106">Os sinalizadores a seguir descrevem um formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="8286b-106">The following flags describe a vertex format.</span></span> <span data-ttu-id="8286b-107">Para obter informações sobre formatos de vértice, consulte Códigos FVF de função [fixa (Direct3D 9)](fixed-function-fvf-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8286b-107">For information regarding vertex formats, see [Fixed Function FVF Codes (Direct3D 9)](fixed-function-fvf-codes.md).</span></span>



| <span data-ttu-id="8286b-108">\#Definir</span><span class="sxs-lookup"><span data-stu-id="8286b-108">\#define</span></span>                            | <span data-ttu-id="8286b-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="8286b-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             | <span data-ttu-id="8286b-110">Ordem e tipo de dados</span><span class="sxs-lookup"><span data-stu-id="8286b-110">Data order and type</span></span>                                                                                       |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8286b-111">D3DFVF \_ DIFUSO</span><span class="sxs-lookup"><span data-stu-id="8286b-111">D3DFVF\_DIFFUSE</span></span>                     | <span data-ttu-id="8286b-112">O formato de vértice inclui um componente de cor difusa.</span><span class="sxs-lookup"><span data-stu-id="8286b-112">Vertex format includes a diffuse color component.</span></span>                                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="8286b-113">DWORD na ordem ARGB.</span><span class="sxs-lookup"><span data-stu-id="8286b-113">DWORD in ARGB order.</span></span> <span data-ttu-id="8286b-114">Consulte [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="8286b-114">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="8286b-115">D3DFVF \_ NORMAL</span><span class="sxs-lookup"><span data-stu-id="8286b-115">D3DFVF\_NORMAL</span></span>                      | <span data-ttu-id="8286b-116">O formato de vértice inclui um vetor normal de vértice.</span><span class="sxs-lookup"><span data-stu-id="8286b-116">Vertex format includes a vertex normal vector.</span></span> <span data-ttu-id="8286b-117">Esse sinalizador não pode ser usado com o sinalizador \_ XYZRHW D3DFVF.</span><span class="sxs-lookup"><span data-stu-id="8286b-117">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                                   | <span data-ttu-id="8286b-118">float, float, float</span><span class="sxs-lookup"><span data-stu-id="8286b-118">float, float, float</span></span>                                                                                       |
| <span data-ttu-id="8286b-119">D3DFVF \_ PSIZE</span><span class="sxs-lookup"><span data-stu-id="8286b-119">D3DFVF\_PSIZE</span></span>                       | <span data-ttu-id="8286b-120">Formato de vértice especificado no tamanho do ponto.</span><span class="sxs-lookup"><span data-stu-id="8286b-120">Vertex format specified in point size.</span></span> <span data-ttu-id="8286b-121">Esse tamanho é expresso em unidades de espaço da câmera para vértices que não são transformados e acesos e em unidades de espaço do dispositivo para vértices transformados e acesos.</span><span class="sxs-lookup"><span data-stu-id="8286b-121">This size is expressed in camera space units for vertices that are not transformed and lit, and in device-space units for transformed and lit vertices.</span></span>                                                                                                                                                                          | <span data-ttu-id="8286b-122">FLOAT</span><span class="sxs-lookup"><span data-stu-id="8286b-122">float</span></span>                                                                                                     |
| <span data-ttu-id="8286b-123">\_Especular D3DFVF</span><span class="sxs-lookup"><span data-stu-id="8286b-123">D3DFVF\_SPECULAR</span></span>                    | <span data-ttu-id="8286b-124">O formato de vértice inclui um componente de cor especular.</span><span class="sxs-lookup"><span data-stu-id="8286b-124">Vertex format includes a specular color component.</span></span>                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="8286b-125">DWORD na ordem ARGB.</span><span class="sxs-lookup"><span data-stu-id="8286b-125">DWORD in ARGB order.</span></span> <span data-ttu-id="8286b-126">Consulte [**D3DCOLOR \_ ARGB**](d3dcolor-argb.md).</span><span class="sxs-lookup"><span data-stu-id="8286b-126">See [**D3DCOLOR\_ARGB**](d3dcolor-argb.md).</span></span>                                         |
| <span data-ttu-id="8286b-127">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="8286b-127">D3DFVF\_XYZ</span></span>                         | <span data-ttu-id="8286b-128">O formato de vértice inclui a posição de um vértice não transformado.</span><span class="sxs-lookup"><span data-stu-id="8286b-128">Vertex format includes the position of an untransformed vertex.</span></span> <span data-ttu-id="8286b-129">Esse sinalizador não pode ser usado com o \_ sinalizador D3DFVF XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="8286b-129">This flag cannot be used with the D3DFVF\_XYZRHW flag.</span></span>                                                                                                                                                                                                                                                  | <span data-ttu-id="8286b-130">float, float, float.</span><span class="sxs-lookup"><span data-stu-id="8286b-130">float, float, float.</span></span>                                                                                      |
| <span data-ttu-id="8286b-131">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="8286b-131">D3DFVF\_XYZRHW</span></span>                      | <span data-ttu-id="8286b-132">O formato de vértice inclui a posição de um vértice transformado.</span><span class="sxs-lookup"><span data-stu-id="8286b-132">Vertex format includes the position of a transformed vertex.</span></span> <span data-ttu-id="8286b-133">Esse sinalizador não pode ser usado com os \_ sinalizadores normais D3DFVF XYZ ou D3DFVF \_ .</span><span class="sxs-lookup"><span data-stu-id="8286b-133">This flag cannot be used with the D3DFVF\_XYZ or D3DFVF\_NORMAL flags.</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="8286b-134">float, float, float, float.</span><span class="sxs-lookup"><span data-stu-id="8286b-134">float, float, float, float.</span></span>                                                                               |
| <span data-ttu-id="8286b-135">D3DFVF \_ XYZB1 D3DFVF \_ XYZB5</span><span class="sxs-lookup"><span data-stu-id="8286b-135">D3DFVF\_XYZB1 through D3DFVF\_XYZB5</span></span> | <span data-ttu-id="8286b-136">O formato de vértice contém dados de posição e um número correspondente de valores de peso (beta) a serem usados para operações de mesclagem de vértice de várias matrizes.</span><span class="sxs-lookup"><span data-stu-id="8286b-136">Vertex format contains position data, and a corresponding number of weighting (beta) values to use for multimatrix vertex blending operations.</span></span> <span data-ttu-id="8286b-137">Atualmente, o Direct3D pode misturar com até três valores de peso e quatro matrizes de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="8286b-137">Currently, Direct3D can blend with up to three weighting values and four blending matrices.</span></span> <span data-ttu-id="8286b-138">Para obter mais informações sobre o uso de matrizes de mesclagem, consulte [Direct3D 9 (índice de vértices indexados)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="8286b-138">For more information about using blending matrices, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span> | <span data-ttu-id="8286b-139">1, 2 ou 3 floats.</span><span class="sxs-lookup"><span data-stu-id="8286b-139">1, 2, or 3 floats.</span></span> <span data-ttu-id="8286b-140">Quando D3DFVF \_ LASTBETA \_ UBYTE4 é usado, o último peso de mesclagem é tratado como um DWORD.</span><span class="sxs-lookup"><span data-stu-id="8286b-140">When D3DFVF\_LASTBETA\_UBYTE4 is used, the last blending weight is treated as a DWORD.</span></span> |
| <span data-ttu-id="8286b-141">D3DFVF \_ XYZW</span><span class="sxs-lookup"><span data-stu-id="8286b-141">D3DFVF\_XYZW</span></span>                        | <span data-ttu-id="8286b-142">O formato de vértice contém dados transformados e recortados (x, y, z, w).</span><span class="sxs-lookup"><span data-stu-id="8286b-142">Vertex format contains transformed and clipped (x, y, z, w) data.</span></span> <span data-ttu-id="8286b-143">ProcessVertices não invoca o clipper, em vez disso, a saída de dados em coordenadas de clipe.</span><span class="sxs-lookup"><span data-stu-id="8286b-143">ProcessVertices does not invoke the clipper, instead outputting data in clip coordinates.</span></span> <span data-ttu-id="8286b-144">Essa constante foi projetada para e só pode ser usada com o pipeline de vértice programável.</span><span class="sxs-lookup"><span data-stu-id="8286b-144">This constant is designed for, and can only be used with, the programmable vertex pipeline.</span></span>                                                                                                                 | <span data-ttu-id="8286b-145">float, float, float, float</span><span class="sxs-lookup"><span data-stu-id="8286b-145">float, float, float, float</span></span>                                                                                |



 

## <a name="texture-flags"></a><span data-ttu-id="8286b-146">Sinalizadores de textura</span><span class="sxs-lookup"><span data-stu-id="8286b-146">Texture Flags</span></span>

<span data-ttu-id="8286b-147">Os sinalizadores a seguir descrevem sinalizadores de textura usados pelo pipeline de função fixa.</span><span class="sxs-lookup"><span data-stu-id="8286b-147">The following flags describe texture flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="8286b-148">\#Definir</span><span class="sxs-lookup"><span data-stu-id="8286b-148">\#define</span></span>                          | <span data-ttu-id="8286b-149">Descrição</span><span class="sxs-lookup"><span data-stu-id="8286b-149">Description</span></span>                                                                                                                                                                                                                                                                        |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8286b-150">D3DFVF \_ TEX0 – D3DFVF \_ TEXAS8</span><span class="sxs-lookup"><span data-stu-id="8286b-150">D3DFVF\_TEX0 - D3DFVF\_TEX8</span></span>       | <span data-ttu-id="8286b-151">Número de conjuntos de coordenadas de textura para esse vértice.</span><span class="sxs-lookup"><span data-stu-id="8286b-151">Number of texture coordinate sets for this vertex.</span></span> <span data-ttu-id="8286b-152">Os valores reais para esses sinalizadores não são sequenciais.</span><span class="sxs-lookup"><span data-stu-id="8286b-152">The actual values for these flags are not sequential.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="8286b-153">D3DFVF \_ TEXCOORDSIZEN(coordIndex)</span><span class="sxs-lookup"><span data-stu-id="8286b-153">D3DFVF\_TEXCOORDSIZEN(coordIndex)</span></span> | <span data-ttu-id="8286b-154">Defina um conjunto de dados de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="8286b-154">Define a texture coordinate data set.</span></span> <span data-ttu-id="8286b-155">n indica a dimensão das coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="8286b-155">n indicates the dimension of the texture coordinates.</span></span> <span data-ttu-id="8286b-156">coordIndex indica o número do índice da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="8286b-156">coordIndex indicates texture coordinate index number.</span></span> <span data-ttu-id="8286b-157">Consulte [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) e Coordenadas de textura [e Estágios de textura](texture-coordinates.md).</span><span class="sxs-lookup"><span data-stu-id="8286b-157">See [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) and [Texture coordinates and Texture Stages](texture-coordinates.md).</span></span> |



 

## <a name="mask-flags"></a><span data-ttu-id="8286b-158">Sinalizadores de máscara</span><span class="sxs-lookup"><span data-stu-id="8286b-158">Mask Flags</span></span>

<span data-ttu-id="8286b-159">Os sinalizadores a seguir descrevem sinalizadores de máscara usados pelo pipeline de função fixa.</span><span class="sxs-lookup"><span data-stu-id="8286b-159">The following flags describe mask flags used by the fixed-function pipeline.</span></span>



| <span data-ttu-id="8286b-160">\#Definir</span><span class="sxs-lookup"><span data-stu-id="8286b-160">\#define</span></span>                             | <span data-ttu-id="8286b-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="8286b-161">Description</span></span>                                           |
|--------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="8286b-162">MÁSCARA DE POSIÇÃO D3DFVF \_ \_</span><span class="sxs-lookup"><span data-stu-id="8286b-162">D3DFVF\_POSITION\_MASK</span></span>               | <span data-ttu-id="8286b-163">Máscara para bits de posição.</span><span class="sxs-lookup"><span data-stu-id="8286b-163">Mask for position bits.</span></span>                               |
| <span data-ttu-id="8286b-164">D3DFVF \_ RESERVED0, D3DFVF \_ RESERVED2</span><span class="sxs-lookup"><span data-stu-id="8286b-164">D3DFVF\_RESERVED0, D3DFVF\_RESERVED2</span></span> | <span data-ttu-id="8286b-165">Mascarar valores para bits reservados no FVF.</span><span class="sxs-lookup"><span data-stu-id="8286b-165">Mask values for reserved bits in the FVF.</span></span> <span data-ttu-id="8286b-166">Não use.</span><span class="sxs-lookup"><span data-stu-id="8286b-166">Do not use.</span></span> |
| <span data-ttu-id="8286b-167">\_Máscara de TEXCOUNT D3DFVF \_</span><span class="sxs-lookup"><span data-stu-id="8286b-167">D3DFVF\_TEXCOUNT\_MASK</span></span>               | <span data-ttu-id="8286b-168">Valor de máscara para bits de sinalizador de textura.</span><span class="sxs-lookup"><span data-stu-id="8286b-168">Mask value for texture flag bits.</span></span>                     |



 

## <a name="miscellaneous-flags"></a><span data-ttu-id="8286b-169">Sinalizadores diversos</span><span class="sxs-lookup"><span data-stu-id="8286b-169">Miscellaneous Flags</span></span>

<span data-ttu-id="8286b-170">Os sinalizadores a seguir descrevem uma variedade de sinalizadores usados pelo pipeline de função fixa.</span><span class="sxs-lookup"><span data-stu-id="8286b-170">The following flags describe a variety of flags used by the fixed-function pipeline.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8286b-171">#definir</span><span class="sxs-lookup"><span data-stu-id="8286b-171">#define</span></span></td>
<td><span data-ttu-id="8286b-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="8286b-172">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8286b-173">D3DFVF_LASTBETA_D3DCOLOR</span><span class="sxs-lookup"><span data-stu-id="8286b-173">D3DFVF_LASTBETA_D3DCOLOR</span></span></td>
<td><span data-ttu-id="8286b-174">O último campo beta nos dados da posição do vértice será do tipo D3DCOLOR.</span><span class="sxs-lookup"><span data-stu-id="8286b-174">The last beta field in the vertex position data will be of type D3DCOLOR.</span></span> <span data-ttu-id="8286b-175">Os dados nos campos beta são usados com a aparência da paleta de matriz para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="8286b-175">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8286b-176">D3DFVF_LASTBETA_UBYTE4</span><span class="sxs-lookup"><span data-stu-id="8286b-176">D3DFVF_LASTBETA_UBYTE4</span></span></td>
<td><span data-ttu-id="8286b-177">O último campo beta nos dados da posição do vértice será do tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="8286b-177">The last beta field in the vertex position data will be of type UBYTE4.</span></span> <span data-ttu-id="8286b-178">Os dados nos campos beta são usados com a aparência da paleta de matriz para especificar índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="8286b-178">The data in the beta fields are used with matrix palette skinning to specify matrix indices.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>// Given the following vertex data definition: 
struct VERTEXPOSITION
{
   float pos[3];
   union 
   {
      float beta[5];
      struct
      {
         float weights[4];
         DWORD MatrixIndices;  // Used as UBYTEs
      }
   }
};</code></pre></td>
</tr>
</tbody>
</table>

<p><span data-ttu-id="8286b-179">Dado que o FVF é declarado como: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="8286b-179">Given the FVF is declared as: D3DFVF_XYZB5 | D3DFVF_LASTBETA_UBYTE4.</span></span> <span data-ttu-id="8286b-180">Peso e MatrixIndices são incluídos na versão beta [5], em que D3DFVF_LASTBETA_UBYTE4 diz para interpretar a última DWORD em beta [5] como tipo UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="8286b-180">Weight and MatrixIndices are included in beta[5], where D3DFVF_LASTBETA_UBYTE4 says to interpret the last DWORD in beta[5] as type UBYTE4.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8286b-181">D3DFVF_TEXCOUNT_SHIFT</span><span class="sxs-lookup"><span data-stu-id="8286b-181">D3DFVF_TEXCOUNT_SHIFT</span></span></td>
<td><span data-ttu-id="8286b-182">O número de bits pelo qual mover um valor inteiro que identifica o número de coordenadas de textura de um vértice.</span><span class="sxs-lookup"><span data-stu-id="8286b-182">The number of bits by which to shift an integer value that identifies the number of texture coordinates for a vertex.</span></span> <span data-ttu-id="8286b-183">Esse valor pode ser usado conforme mostrado abaixo.</span><span class="sxs-lookup"><span data-stu-id="8286b-183">This value might be used as shown below.</span></span>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>DWORD dwNumTextures = 1;  // Vertex has only one set of coordinates.

// Shift the value for use when creating a 
//   flexible vertex format (FVF) combination.
dwFVF = dwNumTextures << D3DFVF_TEXCOUNT_SHIFT;

// Now, create an FVF combination using the shifted value.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

### <a name="examples"></a><span data-ttu-id="8286b-184">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8286b-184">Examples</span></span>

<span data-ttu-id="8286b-185">Os exemplos a seguir mostram outras combinações de sinalizador comuns.</span><span class="sxs-lookup"><span data-stu-id="8286b-185">The following examples show other common flag combinations.</span></span>


```
// Untransformed vertex for lit, untextured, Gouraud-shaded content.
dwFVF = ( D3DFVF_XYZ | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for unlit, untextured, Gouraud-shaded 
//   content with diffuse material color specified per vertex.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE );
```




```
// Untransformed vertex for light-map-based lighting.
dwFVF = ( D3DFVF_XYZ | D3DFVF_TEX2 );
```




```
// Transformed vertex for light-map-based lighting with shared rhw.
dwFVF = ( D3DFVF_XYZRHW | D3DFVF_TEX2 );
```




```
// Heavyweight vertex for unlit, colored content with two 
//   sets of texture coordinates.
dwFVF = ( D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_DIFFUSE | 
          D3DFVF_SPECULAR | D3DFVF_TEX2 );
```



## <a name="constant-information"></a><span data-ttu-id="8286b-186">Informações constantes</span><span class="sxs-lookup"><span data-stu-id="8286b-186">Constant Information</span></span>



| <span data-ttu-id="8286b-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="8286b-187">Requirement</span></span>                         | <span data-ttu-id="8286b-188">Valor</span><span class="sxs-lookup"><span data-stu-id="8286b-188">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="8286b-189">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8286b-189">Header</span></span>                   | <span data-ttu-id="8286b-190">d3d9types. h</span><span class="sxs-lookup"><span data-stu-id="8286b-190">d3d9types.h</span></span> |
| <span data-ttu-id="8286b-191">Sistema operacional mínimo</span><span class="sxs-lookup"><span data-stu-id="8286b-191">Minimum operating system</span></span> | <span data-ttu-id="8286b-192">Windows 98</span><span class="sxs-lookup"><span data-stu-id="8286b-192">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="8286b-193">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8286b-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8286b-194">Constantes Direct3D</span><span class="sxs-lookup"><span data-stu-id="8286b-194">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="8286b-195">Códigos FVF de função fixa (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8286b-195">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)
</dt> <dt>

[<span data-ttu-id="8286b-196">Geometry Blending (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="8286b-196">Geometry Blending (Direct3D 9)</span></span>](geometry-blending.md)
</dt> </dl>

 

 



