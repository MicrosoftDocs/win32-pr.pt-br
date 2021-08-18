---
description: Mosaico (Direct3D 9)
ms.assetid: ae39b0e1-d2ae-449e-89db-0a2b24171531
title: Mosaico (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9aedc6b435c2993e213e8a4445682725ddb4d460c146afbe420da996e3dbb887
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984826"
---
# <a name="tessellation-direct3d-9"></a>Mosaico (Direct3D 9)

## <a name="tessellator-unit"></a>Unidade Tessellator

A unidade Tessellator foi aprimorada. Agora você pode usá-lo para:

-   Execute mosaico adaptável de todos os primitivos de ordem superior.
-   Pesquisar valores de deslocamento por vértice de um mapa de deslocamento e passá-los para um sombreador de vértice.
-   Suporte retângulo-mosaico de patch. Isso é especificado por meio de uma declaração de vértice usando D3DDECLMETHOD \_ partiald ou D3DDECLMETHOD \_ PARTIALV. Se uma declaração de vértice contendo esses métodos for usada para desenhar um patch de triângulo, [**IDirect3DDevice9::D rawtripatch**](/windows/desktop/api) falhará. Para obter mais informações sobre declarações de vértice, consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).

No DirectX 8. x, o que era chamado de ordem era realmente o grau. No Direct3D 9, o grau agora é especificado por [**D3DDEGREETYPE**](./d3ddegreetype.md).


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



A alteração no tipo de grau afetou duas outras estruturas.


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



Os drivers precisam corrigir erros de compilação que resultarão dessa alteração quando forem compilados com os novos cabeçalhos. Nenhuma funcionalidade deve ser alterada.

## <a name="adaptive-tessellation"></a>Mosaico adaptável

O mosaico adaptável pode ser aplicado a primitivos de ordem superior, incluindo N-patches, patches de retângulo e patches de triângulo. Esse recurso é habilitado pelo D3DRS \_ ENABLEADAPTIVETESSELLATION e de maneira adaptativa tessellates um patch, com base no valor de profundidade do vértice de controle no espaço de olho.

As coordenadas z (Zi) de vértices de controle (vi), que são transformadas em espaço de olho (Zieye) executando um produto de ponto com um quatro vetor, são usadas como valores de profundidade. O vetor 4D (MDM) é especificado pelo aplicativo usando quatro Estados de renderização (D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z e D3DRS \_ ADAPTIVETESS \_ W). Esse quatro vetor poderia ser a terceira coluna do mundo concatenado e as matrizes de exibição. Ele também pode ser usado para aplicar uma escala a Zieye.

A função para computar um ti de nível de mosaico de Zieye é considerada (MaxTessellationLevel/Zieye), o que significa que o MaxTessellationLevel é o nível de mosaico em Z = 1 no espaço de olho. O MaxTessellationLevel é igual a um valor definido por [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) para N-patches e, para o RT-patches, é igual a pNumSegs. O nível de mosaico é, então, clamped a valores, definidos pelos dois Estados de renderização adicionais D3DRS \_ MINTESSELLATIONLEVEL e D3DRS \_ MAXTESSELLATIONLEVEL, que definem os níveis mínimo e máximo de mosaico a serem clamped. A média do it para cada vértice ao longo de uma borda de um patch é calculada para obter um nível de mosaico para essa borda. O algoritmo para computação de ti para patches de retângulo, patches de triângulo e N-patches difere em quais vértices de controle são usados para calcular o nível de mosaico.

Para os patches de retângulo com uma base B-spline, são usados os quatro vértices de controle mais externos. Por exemplo, com a \_ ordem CÚBICA D3DORDER: os vértices (1, 1) e (1, Width-2) são usados com pNumSegs \[ 0 \] , vértices (1, Width-2) e (Height-2, Height-2) são usados com pNumSegs \[ 1 \] , vértices (Height-2, Width-2) e (1, Width-2) são usados com pNumSegs 2 e os \[ \] vértices (2, 1) e (1, 1) são usados com pNumSegs \[ 3 \]

Para os patches de triângulo, os vértices de patch de canto são usados. Com a \_ ordem CÚBICA D3DORDER: os vértices (0) e (9) são usados com pNumSegs \[ 0 \] , os vértices (9) e (6) são usados com pNumSegs \[ 1 \] e vértices (6) e (0) são usados com pNumSegs \[ 3 \] .

Para N-patches, os vértices do triângulo são usados.

Para os patches de retângulo e triângulo com uma base de Bézier, os vértices de controle de canto são usados.

Controle de taxa de mosaico por vértice. Um aplicativo pode, opcionalmente, fornecer um único valor de ponto flutuante positivo por vértice, que pode ser usado para controlar a taxa de mosaico. Isso é fornecido usando o D3DDECLUSAGE \_ TESSFACTOR, para o qual o índice de uso deve ser 0 e o tipo de entrada deve ser D3DDECLTYPE \_ FLOAT1. Isso é multiplicado ao nível de mosaico por vértice.

### <a name="math"></a>Matemática

O nível de mosaico (te) para uma borda e, representado por dois vértices de controle (Ve1, Ve2), é calculado conforme mostrado abaixo:


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



Quando D3DRS \_ ENABLEADAPTIVETESSELLATION for **true**, os primitivos de triângulo (listas de triângulo, ventiladores, faixas) serão desenhados como N-patches, [**IDirect3DDevice9:: SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode) tiver definido um valor menor que 1,0.

### <a name="api-changes"></a>Alterações de API

Novos Estados de renderização:


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



E seus valores padrão:


```
D3DRS_MAXTESSELLATIONLEVEL = 1.0f 
D3DRS_MINTESSELLATIONLEVEL = 1.0f 
D3DRS_ADAPTIVETESS_X = 0.0f 
D3DRS_ADAPTIVETESS_Y = 0.0f 
D3DRS_ADAPTIVETESS_Z = 1.0f 
D3DRS_ADAPTIVETESS_W = 0.0f 
D3DRS_ENABLEADAPTIVETESSELLATION = FALSE 
```



Novos limites de hardware:


```
D3DDEVCAPS2_ADAPTIVETESSRTPATCH // Can adaptively tessellate RT-patches 
D3DDEVCAPS2_ADAPTIVETESSNPATCH  // Can adaptively tessellate N-patches 
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de vértice](vertex-pipeline.md)
</dt> </dl>

 

 
