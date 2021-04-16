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
# <a name="accessing-the-contents-of-a-vertex-buffer-direct3d-9"></a>Acessando o conteúdo de um buffer de vértice (Direct3D 9)

Os objetos de buffer de vértice permitem que os aplicativos acessem diretamente a memória alocada para dados de vértice. Você pode recuperar um ponteiro para a memória de buffer de vértice chamando o método [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock) e, em seguida, acessando a memória conforme necessário para preencher o buffer com novos dados de vértice ou para ler os dados que ele já contém. O método **IDirect3DVertexBuffer9:: Lock** aceita quatro parâmetros. O primeiro, *offsetToLock*, é o deslocamento para os dados de vértice. O segundo parâmetro é o tamanho, medido em bytes, dos dados do vértice. O terceiro parâmetro aceito é o endereço de um ponteiro que aponta para os dados de vértice, caso a chamada tenha sucesso.

O último parâmetro, *flags*, informa ao sistema como a memória deve ser bloqueada. Especifique constantes para o parâmetro *flags* de acordo com a maneira como os dados de vértice serão acessados. Verifique se o valor escolhido para [**D3DUSAGE**](d3dusage.md) corresponde ao valor escolhido para [D3DLOCK](d3dlock.md). Por exemplo, se você estiver criando um buffer de vértice somente com acesso de gravação, não faz sentido tentar ler os dados especificando D3DLOCK \_ ReadOnly. Usar esses sinalizadores com sabedoria permite que o driver bloqueie a memória e forneça o melhor desempenho, dado o tipo de acesso solicitado.

Depois de concluir o preenchimento ou a leitura dos dados do vértice, chame o método [**IDirect3DVertexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-unlock) , conforme mostrado no exemplo de código a seguir.


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



Se você criar um buffer de vértice com o \_ sinalizador WRITEONLY D3DUSAGE, não use o \_ sinalizador de bloqueio ReadOnly D3DLOCK. Use o \_ sinalizador D3DLOCK ReadOnly se seu aplicativo for lido somente da memória de buffer de vértice. A inclusão desse sinalizador permite que o Direct3D Otimize seus procedimentos internos para melhorar a eficiência, Considerando que o acesso à memória será somente leitura.

Consulte [usando o vértice dinâmico e buffers de índice](performance-optimizations.md) para obter informações sobre como usar D3DLOCK \_ descarte ou D3DLOCK \_ NoOverwrite para o parâmetro flags de [**IDirect3DVertexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-lock).

Em C++, como você acessa diretamente a memória alocada para o buffer de vértice, certifique-se de que seu aplicativo acesse a memória alocada corretamente. Caso contrário, você correrá o risco de renderizar a memória inválida. Use o stride do formato de vértice que seu aplicativo usa para mover de um vértice no buffer alocado para outro. A memória de buffer de vértice é uma matriz simples de vértices especificada em FVF. Use o stride de qualquer estrutura de formato de vértice que você definir. Você pode calcular o stride de cada vértice em tempo de execução examinando o [D3DFVF](d3dfvf.md) contido na descrição do buffer de vértice. A tabela a seguir mostra o tamanho de cada componente de vértice.



| Sinalizador de formato de vértice | Tamanho              |
|--------------------|-------------------|
| D3DFVF \_ difuso    | sizeof (DWORD)     |
| D3DFVF \_ normal     | sizeof (float) x 3 |
| \_Especular D3DFVF   | sizeof (DWORD)     |
| D3DFVF \_ TEXn       | sizeof (float) x n |
| D3DFVF \_ XYZ        | sizeof (float) x 3 |
| D3DFVF \_ XYZRHW     | sizeof (float) x 4 |



 

O número de coordenadas de textura presentes no formato de vértice é descrito pelos \_ sinalizadores D3DFVF Tex n (em que n é um valor de 0 a 8). Multiplique o número de conjuntos de coordenadas de textura pelo tamanho de um conjunto de coordenadas de textura, que pode variar de um a quatro floats, para calcular a memória necessária para esse número de coordenadas de textura.

Use a distância total do vértice para incrementar e decrementar o ponteiro de memória conforme necessário para acessar vértices específicos.

## <a name="retrieving-vertex-buffer-descriptions"></a>Recuperando descrições de buffer de vértice

Você pode recuperar informações sobre um buffer de vértice chamando o método [**IDirect3DVertexBuffer9:: GetDesc**](/windows/desktop/api) . Esse método preenche os membros da estrutura [**\_ desc D3DVERTEXBUFFER**](d3dvertexbuffer-desc.md) com informações sobre o buffer de vértice.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> </dl>

 

 
