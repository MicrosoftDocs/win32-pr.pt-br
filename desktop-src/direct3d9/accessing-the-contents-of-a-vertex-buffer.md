---
description: Os objetos de buffer de vértice permitem que os aplicativos acessem diretamente a memória alocada para dados de vértice.
ms.assetid: 63d255b7-fa7d-411b-9cdb-52113f30c933
title: Acessando o conteúdo de um buffer de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1b5e4a4986e064d3736f83567f5dd6d479d0dbc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758714"
---
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="cd4d3-103">Acessando o conteúdo de um buffer de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd4d3-103">Accessing the Contents of a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="cd4d3-104">Os objetos de buffer de vértice permitem que os aplicativos acessem diretamente a memória alocada para dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-104">Vertex buffer objects enable applications to directly access the memory allocated for vertex data.</span></span> <span data-ttu-id="cd4d3-105">Você pode recuperar um ponteiro para a memória de buffer de vértice chamando o método [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) e, em seguida, acessando a memória conforme necessário para preencher o buffer com novos dados de vértice ou para ler os dados que ele já contém.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-105">You can retrieve a pointer to vertex buffer memory by calling the [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) method, and then accessing the memory as needed to fill the buffer with new vertex data or to read any data it already contains.</span></span> <span data-ttu-id="cd4d3-106">O método **IDirect3DVertexBuffer9:: Lock** aceita quatro parâmetros.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-106">The **IDirect3DVertexBuffer9::Lock** method accepts four parameters.</span></span> <span data-ttu-id="cd4d3-107">O primeiro, *offsetToLock*, é o deslocamento para os dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-107">The first, *OffsetToLock*, is the offset into the vertex data.</span></span> <span data-ttu-id="cd4d3-108">O segundo parâmetro é o tamanho, medido em bytes, dos dados do vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-108">The second parameter is the size, measured in bytes, of the vertex data.</span></span> <span data-ttu-id="cd4d3-109">O terceiro parâmetro aceito é o endereço de um ponteiro que aponta para os dados de vértice, caso a chamada tenha sucesso.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-109">The third parameter accepted is the address of a pointer that points to the vertex data, if the call succeeds.</span></span>

<span data-ttu-id="cd4d3-110">O último parâmetro, *flags*, informa ao sistema como a memória deve ser bloqueada.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-110">The last parameter, *Flags*, tells the system how the memory should be locked.</span></span> <span data-ttu-id="cd4d3-111">Especifique constantes para o parâmetro *flags* de acordo com a maneira como os dados de vértice serão acessados.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-111">Specify constants for the *Flags* parameter according to the way the vertex data will be accessed.</span></span> <span data-ttu-id="cd4d3-112">Verifique se o valor escolhido para [**D3DUSAGE**](d3dusage.md) corresponde ao valor escolhido para [D3DLOCK](d3dlock.md).</span><span class="sxs-lookup"><span data-stu-id="cd4d3-112">Make sure the value chosen for [**D3DUSAGE**](d3dusage.md) matches the value chosen for [D3DLOCK](d3dlock.md).</span></span> <span data-ttu-id="cd4d3-113">Por exemplo, se você estiver criando um buffer de vértice somente com acesso de gravação, não faz sentido tentar ler os dados especificando D3DLOCK \_ ReadOnly.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-113">For example, if you are creating a vertex buffer with write access only, it doesn't make sense to try to read the data by specifying D3DLOCK\_READONLY.</span></span> <span data-ttu-id="cd4d3-114">Usar esses sinalizadores com sabedoria permite que o driver bloqueie a memória e forneça o melhor desempenho, dado o tipo de acesso solicitado.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-114">Wisely using these flags allows the driver to lock the memory and provide the best performance, given the requested access type.</span></span>

<span data-ttu-id="cd4d3-115">Depois de concluir o preenchimento ou a leitura dos dados do vértice, chame o método [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , conforme mostrado no exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-115">After you finish filling or reading the vertex data, call the [**IDirect3DVertexBuffer9::Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) method, as shown in the following code example.</span></span>


```
// This code example assumes the g_pVB is a variable of type 
//   LPDIRECT3DVERTEXBUFFER9 and that g_Vertices has been  
//   properly initialized with vertices

// Lock the buffer to gain access to the vertices 
VOID* pVertices;

if(FAILED(g_pVB->Lock(0, sizeof(g_Vertices), 
        (BYTE**)&pVertices, 0 ) ) ) 
    return E_FAIL;

memcpy(pVertices, g_Vertices, sizeof(g_Vertices));
g_pVB->Unlock();
```



<span data-ttu-id="cd4d3-116">Se você criar um buffer de vértice com o \_ sinalizador WRITEONLY D3DUSAGE, não use o \_ sinalizador de bloqueio ReadOnly D3DLOCK.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-116">If you create a vertex buffer with the D3DUSAGE\_WRITEONLY flag, do not use the D3DLOCK\_READONLY locking flag.</span></span> <span data-ttu-id="cd4d3-117">Use o \_ sinalizador D3DLOCK ReadOnly se seu aplicativo for lido somente da memória de buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-117">Use the D3DLOCK\_READONLY flag if your application will read only from the vertex buffer memory.</span></span> <span data-ttu-id="cd4d3-118">A inclusão desse sinalizador permite que o Direct3D Otimize seus procedimentos internos para melhorar a eficiência, Considerando que o acesso à memória será somente leitura.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-118">Including this flag enables Direct3D to optimize its internal procedures to improve efficiency, given that access to the memory will be read-only.</span></span>

<span data-ttu-id="cd4d3-119">Consulte [usando o vértice dinâmico e buffers de índice](performance-optimizations.md) para obter informações sobre como usar D3DLOCK \_ descarte ou D3DLOCK \_ NoOverwrite para o parâmetro flags de [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span><span class="sxs-lookup"><span data-stu-id="cd4d3-119">See [Using Dynamic Vertex and Index Buffers](performance-optimizations.md) for information about using D3DLOCK\_DISCARD or D3DLOCK\_NOOVERWRITE for the Flags parameter of [**IDirect3DVertexBuffer9::Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).</span></span>

<span data-ttu-id="cd4d3-120">Em C++, como você acessa diretamente a memória alocada para o buffer de vértice, certifique-se de que seu aplicativo acesse a memória alocada corretamente.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-120">In C++, because you directly access the memory allocated for the vertex buffer, make sure your application properly accesses the allocated memory.</span></span> <span data-ttu-id="cd4d3-121">Caso contrário, você correrá o risco de renderizar a memória inválida.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-121">Otherwise, you risk rendering that memory invalid.</span></span> <span data-ttu-id="cd4d3-122">Use o stride do formato de vértice que seu aplicativo usa para mover de um vértice no buffer alocado para outro.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-122">Use the stride of the vertex format that your application uses to move from one vertex in the allocated buffer to another.</span></span> <span data-ttu-id="cd4d3-123">A memória de buffer de vértice é uma matriz simples de vértices especificada em FVF.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-123">The vertex buffer memory is a simple array of vertices specified in FVF.</span></span> <span data-ttu-id="cd4d3-124">Use o stride de qualquer estrutura de formato de vértice que você definir.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-124">Use the stride of whatever vertex format structure you define.</span></span> <span data-ttu-id="cd4d3-125">Você pode calcular o stride de cada vértice em tempo de execução examinando o [D3DFVF](d3dfvf.md) contido na descrição do buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-125">You can calculate the stride of each vertex at run time by examining the [D3DFVF](d3dfvf.md) contained in the vertex buffer description.</span></span> <span data-ttu-id="cd4d3-126">A tabela a seguir mostra o tamanho de cada componente de vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-126">The following table shows the size for each vertex component.</span></span>



| <span data-ttu-id="cd4d3-127">Sinalizador de formato de vértice</span><span class="sxs-lookup"><span data-stu-id="cd4d3-127">Vertex Format Flag</span></span> | <span data-ttu-id="cd4d3-128">Tamanho</span><span class="sxs-lookup"><span data-stu-id="cd4d3-128">Size</span></span>              |
|--------------------|-------------------|
| <span data-ttu-id="cd4d3-129">D3DFVF \_ difuso</span><span class="sxs-lookup"><span data-stu-id="cd4d3-129">D3DFVF\_DIFFUSE</span></span>    | <span data-ttu-id="cd4d3-130">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="cd4d3-130">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="cd4d3-131">D3DFVF \_ normal</span><span class="sxs-lookup"><span data-stu-id="cd4d3-131">D3DFVF\_NORMAL</span></span>     | <span data-ttu-id="cd4d3-132">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="cd4d3-132">sizeof(float) x 3</span></span> |
| <span data-ttu-id="cd4d3-133">\_Especular D3DFVF</span><span class="sxs-lookup"><span data-stu-id="cd4d3-133">D3DFVF\_SPECULAR</span></span>   | <span data-ttu-id="cd4d3-134">sizeof (DWORD)</span><span class="sxs-lookup"><span data-stu-id="cd4d3-134">sizeof(DWORD)</span></span>     |
| <span data-ttu-id="cd4d3-135">D3DFVF \_ TEXn</span><span class="sxs-lookup"><span data-stu-id="cd4d3-135">D3DFVF\_TEXn</span></span>       | <span data-ttu-id="cd4d3-136">sizeof (float) x n</span><span class="sxs-lookup"><span data-stu-id="cd4d3-136">sizeof(float) x n</span></span> |
| <span data-ttu-id="cd4d3-137">D3DFVF \_ XYZ</span><span class="sxs-lookup"><span data-stu-id="cd4d3-137">D3DFVF\_XYZ</span></span>        | <span data-ttu-id="cd4d3-138">sizeof (float) x 3</span><span class="sxs-lookup"><span data-stu-id="cd4d3-138">sizeof(float) x 3</span></span> |
| <span data-ttu-id="cd4d3-139">D3DFVF \_ XYZRHW</span><span class="sxs-lookup"><span data-stu-id="cd4d3-139">D3DFVF\_XYZRHW</span></span>     | <span data-ttu-id="cd4d3-140">sizeof (float) x 4</span><span class="sxs-lookup"><span data-stu-id="cd4d3-140">sizeof(float) x 4</span></span> |



 

<span data-ttu-id="cd4d3-141">O número de coordenadas de textura presentes no formato de vértice é descrito pelos \_ sinalizadores D3DFVF Tex n (em que n é um valor de 0 a 8).</span><span class="sxs-lookup"><span data-stu-id="cd4d3-141">The number of texture coordinates present in the vertex format is described by the D3DFVF\_TEX n flags (where n is a value from 0 to 8).</span></span> <span data-ttu-id="cd4d3-142">Multiplique o número de conjuntos de coordenadas de textura pelo tamanho de um conjunto de coordenadas de textura, que pode variar de um a quatro floats, para calcular a memória necessária para esse número de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-142">Multiply the number of texture coordinate sets by the size of one set of texture coordinates, which can range from one to four floats, to calculate the memory required for that number of texture coordinates.</span></span>

<span data-ttu-id="cd4d3-143">Use a distância total do vértice para incrementar e decrementar o ponteiro de memória conforme necessário para acessar vértices específicos.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-143">Use the total vertex stride to increment and decrement the memory pointer as needed to access particular vertices.</span></span>

## <a name="retrieving-vertex-buffer-descriptions"></a><span data-ttu-id="cd4d3-144">Recuperando descrições de buffer de vértice</span><span class="sxs-lookup"><span data-stu-id="cd4d3-144">Retrieving Vertex Buffer Descriptions</span></span>

<span data-ttu-id="cd4d3-145">Você pode recuperar informações sobre um buffer de vértice chamando o método [**IDirect3DVertexBuffer9:: GetDesc**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="cd4d3-145">You can retrieve information about a vertex buffer by calling the [**IDirect3DVertexBuffer9::GetDesc**](/windows/desktop/api) method.</span></span> <span data-ttu-id="cd4d3-146">Esse método preenche os membros da estrutura [**\_ desc D3DVERTEXBUFFER**](d3dvertexbuffer-desc.md) com informações sobre o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="cd4d3-146">This method fills the members of the [**D3DVERTEXBUFFER\_DESC**](d3dvertexbuffer-desc.md) structure with information about the vertex buffer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd4d3-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd4d3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd4d3-148">Buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="cd4d3-148">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
