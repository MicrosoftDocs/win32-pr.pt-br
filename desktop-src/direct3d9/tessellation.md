---
description: Mosaico (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Mosaico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82378caac1218158ffc1834c9a9b56fb8cbd250e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646008"
---
# <a name="tessellation-direct3d-9"></a><span data-ttu-id="02682-103">Mosaico (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="02682-103">Tessellation (Direct3D 9)</span></span>

## <a name="tessellator-unit"></a><span data-ttu-id="02682-104">Unidade Tessellator</span><span class="sxs-lookup"><span data-stu-id="02682-104">Tessellator Unit</span></span>

<span data-ttu-id="02682-105">A unidade Tessellator foi aprimorada.</span><span class="sxs-lookup"><span data-stu-id="02682-105">The tessellator unit has been enhanced.</span></span> <span data-ttu-id="02682-106">Agora você pode usá-lo para:</span><span class="sxs-lookup"><span data-stu-id="02682-106">You can now use it to:</span></span>

-   <span data-ttu-id="02682-107">Execute mosaico adaptável de todos os primitivos de ordem superior.</span><span class="sxs-lookup"><span data-stu-id="02682-107">Perform adaptive tessellation of all higher-order primitives.</span></span>
-   <span data-ttu-id="02682-108">Pesquisar valores de deslocamento por vértice de um mapa de deslocamento e passá-los para um sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="02682-108">Look up per-vertex displacement values from a displacement map and pass them on to a vertex shader.</span></span>
-   <span data-ttu-id="02682-109">Suporte retângulo-mosaico de patch.</span><span class="sxs-lookup"><span data-stu-id="02682-109">Support rectangle-patch tessellation.</span></span> <span data-ttu-id="02682-110">Isso é especificado por meio de uma declaração de vértice usando D3DDECLMETHOD \_ partiald ou D3DDECLMETHOD \_ PARTIALV.</span><span class="sxs-lookup"><span data-stu-id="02682-110">This is specified through a vertex declaration using D3DDECLMETHOD\_PARTIALU or D3DDECLMETHOD\_PARTIALV.</span></span> <span data-ttu-id="02682-111">Se uma declaração de vértice contendo esses métodos for usada para desenhar um patch de triângulo, [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) falhará.</span><span class="sxs-lookup"><span data-stu-id="02682-111">If a vertex declaration containing these methods is used to draw a triangle patch, [**IDirect3DDevice9::DrawTriPatch**](/windows/desktop/api) will fail.</span></span> <span data-ttu-id="02682-112">Para obter mais informações sobre declarações de vértice, consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="02682-112">For more information about vertex declarations, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="02682-113">No DirectX 8. x, o que era chamado de ordem era realmente o grau.</span><span class="sxs-lookup"><span data-stu-id="02682-113">In DirectX 8.x, what was called ORDER was really the degree.</span></span> <span data-ttu-id="02682-114">No Direct3D 9, o grau agora é especificado por [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="02682-114">In Direct3D 9, the degree is now specified by [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>


```
 // This used to be D3DORDERTYPE and D3DORDER* 
 typedef enum _D3DDEGREETYPE 
 { 
 D3DDEGREE_LINEAR = 1, 
 D3DDEGREE_QUADRATIC = 2, 
 D3DDEGREE_CUBIC = 3, 
 D3DDEGREE_QUINTIC = 5, 
 D3DDEGREE_FORCE_DWORD = 0x7fffffff, 
 } D3DDEGREETYPE; 
```



<span data-ttu-id="02682-115">A alteração no tipo de grau afetou duas outras estruturas.</span><span class="sxs-lookup"><span data-stu-id="02682-115">The change in degree type affected two other structures.</span></span>


```
typedef struct _D3DRECTPATCH_INFO 
 { 
 UINT StartVertexOffsetWidth; 
 UINT StartVertexOffsetHeight; 
 UINT Width; 
 UINT Height; 
 UINT Stride; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DRECTPATCH_INFO; 
```




```
 typedef struct _D3DTRIPATCH_INFO 
 { 
 UINT StartVertexOffset; 
 UINT NumVertices; 
 D3DBASISTYPE Basis; 
 D3DDEGREETYPE Degree; 
 } D3DTRIPATCH_INFO; 
```



<span data-ttu-id="02682-116">Os drivers precisam corrigir erros de compilação que resultarão dessa alteração quando forem compilados com os novos cabeçalhos.</span><span class="sxs-lookup"><span data-stu-id="02682-116">Drivers need to fix compilation errors that will result from this change when they compile with the new headers.</span></span> <span data-ttu-id="02682-117">Nenhuma funcionalidade deve ser alterada.</span><span class="sxs-lookup"><span data-stu-id="02682-117">No functionality has to be changed.</span></span>

## <a name="adaptive-tessellation"></a><span data-ttu-id="02682-118">Mosaico adaptável</span><span class="sxs-lookup"><span data-stu-id="02682-118">Adaptive Tessellation</span></span>

<span data-ttu-id="02682-119">O mosaico adaptável pode ser aplicado a primitivos de ordem superior, incluindo N-patches, patches de retângulo e patches de triângulo.</span><span class="sxs-lookup"><span data-stu-id="02682-119">Adaptive tessellation can be applied to high-order primitives including N-patches, rectangle patches, and triangle patches.</span></span> <span data-ttu-id="02682-120">Esse recurso é habilitado pelo D3DRS \_ ENABLEADAPTIVETESSELLATION e de maneira adaptativa tessellates um patch, com base no valor de profundidade do vértice de controle no espaço de olho.</span><span class="sxs-lookup"><span data-stu-id="02682-120">This feature is enabled by the D3DRS\_ENABLEADAPTIVETESSELLATION and adaptively tessellates a patch, based on the depth value of the control vertex in eye space.</span></span>

<span data-ttu-id="02682-121">As coordenadas z (Zi) de vértices de controle (vi), que são transformadas em espaço de olho (Zieye) executando um produto de ponto com um quatro vetor, são usadas como valores de profundidade.</span><span class="sxs-lookup"><span data-stu-id="02682-121">The z-coordinates (Zi) of control vertices (Vi), which are transformed into eye space (Zieye) by performing a dot product with a 4-vector, are used as the depth values.</span></span> <span data-ttu-id="02682-122">O vetor 4D (MDM) é especificado pelo aplicativo usando quatro Estados de renderização (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z e D3DRS \_ ADAPTIVETESS \_ W).</span><span class="sxs-lookup"><span data-stu-id="02682-122">The 4D vector (Mdm) is specified by the application using four render states (D3DRS\_ADAPTIVETESS\_X, D3DRS\_ADAPTIVETESS\_Y, D3DRS\_ADAPTIVETESS\_Z, and D3DRS\_ADAPTIVETESS\_W).</span></span> <span data-ttu-id="02682-123">Esse quatro vetor poderia ser a terceira coluna do mundo concatenado e as matrizes de exibição.</span><span class="sxs-lookup"><span data-stu-id="02682-123">This 4-vector could be the third column of the concatenated world and view matrices.</span></span> <span data-ttu-id="02682-124">Ele também pode ser usado para aplicar uma escala a Zieye.</span><span class="sxs-lookup"><span data-stu-id="02682-124">It also could be used to apply a scale to Zieye.</span></span>

<span data-ttu-id="02682-125">A função para computar um ti de nível de mosaico de Zieye é considerada (MaxTessellationLevel/Zieye), o que significa que o MaxTessellationLevel é o nível de mosaico em Z = 1 no espaço de olho.</span><span class="sxs-lookup"><span data-stu-id="02682-125">The function to compute a tessellation level Ti from Zieye is assumed to be (MaxTessellationLevel/Zieye), which means that the MaxTessellationLevel is the tessellation level at Z = 1 in eye space.</span></span> <span data-ttu-id="02682-126">O MaxTessellationLevel é igual a um valor definido por [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) para N-patches e, para o RT-patches, é igual a pNumSegs.</span><span class="sxs-lookup"><span data-stu-id="02682-126">The MaxTessellationLevel is equal to a value set by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) for N-patches and, for RT-patches, it is equal to pNumSegs.</span></span> <span data-ttu-id="02682-127">O nível de mosaico é, então, clamped a valores, definidos pelos dois Estados de renderização adicionais D3DRS \_ MINTESSELLATIONLEVEL e D3DRS \_ MAXTESSELLATIONLEVEL, que definem os níveis mínimo e máximo de mosaico a serem clamped.</span><span class="sxs-lookup"><span data-stu-id="02682-127">The tessellation level is then clamped to values, defined by the two additional render states D3DRS\_MINTESSELLATIONLEVEL and D3DRS\_MAXTESSELLATIONLEVEL, which define the minimum and maximum tessellation levels to be clamped to.</span></span> <span data-ttu-id="02682-128">A média do it para cada vértice ao longo de uma borda de um patch é calculada para obter um nível de mosaico para essa borda.</span><span class="sxs-lookup"><span data-stu-id="02682-128">The Ti's for each vertex along an edge of a patch are averaged to obtain a tessellation level for that edge.</span></span> <span data-ttu-id="02682-129">O algoritmo para computação de ti para patches de retângulo, patches de triângulo e N-patches difere em quais vértices de controle são usados para calcular o nível de mosaico.</span><span class="sxs-lookup"><span data-stu-id="02682-129">The algorithm for computing Ti for rectangle patches, triangle patches, and N-patches differs in what control vertices are used to compute the tessellation level.</span></span>

<span data-ttu-id="02682-130">Para os patches de retângulo com uma base B-spline, são usados os quatro vértices de controle mais externos.</span><span class="sxs-lookup"><span data-stu-id="02682-130">For the rectangle patches with a B-spline basis, the four outermost control vertices are used.</span></span> <span data-ttu-id="02682-131">Por exemplo, com a \_ ordem CÚBICA D3DORDER: os vértices (1, 1) e (1, Width-2) são usados com pNumSegs \[ 0 \] , vértices (1, Width-2) e (Height-2, Height-2) são usados com pNumSegs \[ 1 \] , vértices (Height-2, Width-2) e (1, Width-2) são usados com pNumSegs 2 e os \[ \] vértices (2, 1) e (1, 1) são usados com pNumSegs \[ 3 \]</span><span class="sxs-lookup"><span data-stu-id="02682-131">For example, with D3DORDER\_CUBIC order: vertices (1,1) and (1,width-2) are used with pNumSegs\[0\], vertices (1,width-2) and (height-2,height-2) are used with pNumSegs\[1\], vertices (height-2,width-2) and (1,width-2) are used with pNumSegs\[2\], and vertices (2,1) and (1,1) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="02682-132">Para os patches de triângulo, os vértices de patch de canto são usados.</span><span class="sxs-lookup"><span data-stu-id="02682-132">For the triangle patches, the corner patch vertices are used.</span></span> <span data-ttu-id="02682-133">Com a \_ ordem CÚBICA D3DORDER: os vértices (0) e (9) são usados com pNumSegs \[ 0 \] , os vértices (9) e (6) são usados com pNumSegs \[ 1 \] e vértices (6) e (0) são usados com pNumSegs \[ 3 \] .</span><span class="sxs-lookup"><span data-stu-id="02682-133">With D3DORDER\_CUBIC order: vertices (0) and (9) are used with pNumSegs\[0\], vertices (9) and (6) are used with pNumSegs\[1\] and vertices (6) and (0) are used with pNumSegs\[3\].</span></span>

<span data-ttu-id="02682-134">Para N-patches, os vértices do triângulo são usados.</span><span class="sxs-lookup"><span data-stu-id="02682-134">For N-patches the triangle vertices are used.</span></span>

<span data-ttu-id="02682-135">Para os patches de retângulo e triângulo com uma base de Bézier, os vértices de controle de canto são usados.</span><span class="sxs-lookup"><span data-stu-id="02682-135">For the rectangle and triangle patches with a Bezier basis, the corner-control vertices are used.</span></span>

<span data-ttu-id="02682-136">Controle de taxa de mosaico por vértice.</span><span class="sxs-lookup"><span data-stu-id="02682-136">Per-vertex tessellation rate control.</span></span> <span data-ttu-id="02682-137">Um aplicativo pode, opcionalmente, fornecer um único valor de ponto flutuante positivo por vértice, que pode ser usado para controlar a taxa de mosaico.</span><span class="sxs-lookup"><span data-stu-id="02682-137">An application can optionally supply a single positive floating-point value per vertex, which can be used to control the rate of tessellation.</span></span> <span data-ttu-id="02682-138">Isso é fornecido usando o D3DDECLUSAGE \_ TESSFACTOR, para o qual o índice de uso deve ser 0 e o tipo de entrada deve ser D3DDECLTYPE \_ FLOAT1.</span><span class="sxs-lookup"><span data-stu-id="02682-138">This is supplied using the D3DDECLUSAGE\_TESSFACTOR, for which usage index must be 0 and input type must be D3DDECLTYPE\_FLOAT1.</span></span> <span data-ttu-id="02682-139">Isso é multiplicado ao nível de mosaico por vértice.</span><span class="sxs-lookup"><span data-stu-id="02682-139">This is multiplied to the per-vertex tessellation level.</span></span>

### <a name="math"></a><span data-ttu-id="02682-140">Matemática</span><span class="sxs-lookup"><span data-stu-id="02682-140">Math</span></span>

<span data-ttu-id="02682-141">O nível de mosaico (te) para uma borda e, representado por dois vértices de controle (Ve1, Ve2), é calculado conforme mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="02682-141">The tessellation level (Te) for an edge e, represented by two control vertices (Ve1, Ve2), is computed as shown below :</span></span>


```
Vertex Vi: (Xi, Yi, Zi, TFactori (optional)). 
Ze1eye = Ve1 . Mdm 
Ze2eye = Ve2 . Mdm 
Te1 = MaxTessellationLevel * TFactore1 / Ze1eye 
Te2 = MaxTessellationLevel * TFactore2 / Ze2eye 
Te = ( Te1 + Te2 ) / 2; 
if Te > D3DRS_MAXTESSELLATIONLEVEL || Te < 0, then Te = D3DRS_MAXTESSELLATIONLEVEL 
if Te < D3DRS_MINTESSELLATIONLEVEL, then Te = D3DRS_MINTESSELLATIONLEVEL 
```



<span data-ttu-id="02682-142">Quando D3DRS \_ ENABLEADAPTIVETESSELLATION for **true**, os primitivos de triângulo (listas de triângulo, ventiladores, faixas) serão desenhados como N-patches, [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) tiver definido um valor menor que 1,0.</span><span class="sxs-lookup"><span data-stu-id="02682-142">When D3DRS\_ENABLEADAPTIVETESSELLATION is **TRUE**, triangle primitives (triangle lists, fans, strips) are drawn as N-patches, [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) has set value less than 1.0.</span></span>

### <a name="api-changes"></a><span data-ttu-id="02682-143">Alterações de API</span><span class="sxs-lookup"><span data-stu-id="02682-143">API Changes</span></span>

<span data-ttu-id="02682-144">Novos Estados de renderização:</span><span class="sxs-lookup"><span data-stu-id="02682-144">New render states:</span></span>


```
 D3DRS_ENABLEADAPTIVETESSELLATION // BOOL 
 D3DRS_MAXTESSELLATIONLEVEL       // Float 
 D3DRS_MINTESSELLATIONLEVEL       // Float 
 D3DRS_ADAPTIVETESS_X             // Float 
 D3DRS_ADAPTIVETESS_Y             // Float 
 D3DRS_ADAPTIVETESS_Z             // Float 
 D3DRS_ADAPTIVETESS_W             // Float 
 
 // D3DRS_MINTESSELLATIONLEVEL and D3DRS_MAXTESSELLATIONLEVEL 
 // cannot be less than 1 
```



<span data-ttu-id="02682-145">E seus valores padrão:</span><span class="sxs-lookup"><span data-stu-id="02682-145">And their default values:</span></span>


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



<span data-ttu-id="02682-146">Novos limites de hardware:</span><span class="sxs-lookup"><span data-stu-id="02682-146">New hardware caps:</span></span>


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a><span data-ttu-id="02682-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02682-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02682-148">Pipeline de vértice</span><span class="sxs-lookup"><span data-stu-id="02682-148">Vertex Pipeline</span></span>](vertex-pipeline.md)
</dt> </dl>

 

 
