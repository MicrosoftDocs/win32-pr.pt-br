---
description: Buffers de índice, representados pela interface IDirect3DIndexBuffer9, são buffers de memória que contêm dados de índice.
ms.assetid: baa60cd1-a1f0-4dbe-b934-aeb1a5c6b784
title: Buffers de índice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7151fae6deb72a0c569d269c80e5b13bf946f9d0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825604"
---
# <a name="index-buffers-direct3d-9"></a>Buffers de índice (Direct3D 9)

Buffers de índice, representados pela interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) , são buffers de memória que contêm dados de índice. Os dados de índice, ou índices, são deslocamentos inteiros em buffers de vértice e são usados para renderizar primitivos usando o método [**IDirect3DDevice9::D rawindexedprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) .

Um buffer de vértices contém vértices. Portanto, você pode desenhar um buffer de vértice com ou sem primitivas indexadas. No entanto, como um buffer de índice contém índices, você não pode usar um buffer de índice sem um buffer de vértice correspondente. (Como uma observação adicional, [**IDirect3DDevice9::D rawindexedprimitiveup**](/windows/desktop/api) e [**IDirect3DDevice9::D rawprimitiveup**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitiveup) são os únicos métodos draw que desenham sem um índice ou um buffer de vértice.)

## <a name="index-buffer-description"></a>Descrição de buffer de índice

Um buffer de índice é descrito em termos de suas funcionalidades, como onde ele existe na memória, se suporta leitura e gravação, e o tipo e o número de índices que contém. Essas características são mantidas em uma [**estrutura \_ desc de D3DINDEXBUFFER**](d3dindexbuffer-desc.md) .

Descrições de buffer de índice informam ao seu app como um buffer existente foi criado. Você fornece uma estrutura de descrição vazia para o sistema preencher com os recursos de um buffer de índice criado anteriormente.

-   O membro Format descreve o formato da superfície dos dados do buffer do índice.
-   O tipo identifica o tipo de recurso do buffer de índice.
-   O membro da estrutura de uso contém sinalizadores de capacidade geral. O \_ sinalizador D3DUSAGE SOFTWAREPROCESSING indica que o buffer de índice deve ser usado com o processamento de vértice de software. A presença do \_ sinalizador WRITEONLY D3DUSAGE em uso indica que a memória do buffer de índice é usada somente para operações de gravação. Isso libera o driver para posicionar os dados de índice no melhor local de memória para permitir processamento e renderização rápidos. Se o \_ sinalizador WRITEONLY D3DUSAGE não for usado, será menos provável que o driver Coloque os dados em um local ineficiente para operações de leitura. Isso sacrificaria algum processamento e velocidade de renderização. Se esse sinalizador não for especificado, supõe-se que os aplicativos executam operações de leitura e gravação nos dados no buffer de índice.
-   Pool especifica a classe de memória alocada para o buffer de índice. O \_ sinalizador D3DPOOL SYSTEMMEM indica que o sistema criou o buffer de índice na memória do sistema.
-   O membro de tamanho armazena o tamanho, em bytes, dos dados do buffer de vértice.
-   O último parâmetro pSharedHandle não é usado. Defina-a como **NULL**.

## <a name="index-processing-requirements"></a>Requisitos de processamento de índice

O desempenho das operações de processamento de índice depende muito onde o buffer de índice existe na memória e qual tipo de dispositivo de renderização que está sendo usado. Os apps controlam a alocação de memória para buffers de índice quando eles são criados. Quando o \_ sinalizador de memória D3DPOOL SYSTEMMEM é definido, o buffer de índice é criado na memória do sistema. Quando o \_ sinalizador de memória padrão D3DPOOL é usado, o driver de dispositivo determina onde a memória do buffer de índice é melhor alocada, geralmente conhecida como memória de driver ideal. Driver-a memória ideal pode ser memória de vídeo local, memória de vídeo não local ou memória do sistema.

Definir o \_ sinalizador de comportamento D3DUSAGE SOFTWAREPROCESSING ao chamar o método [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) especifica que o buffer de índice deve ser usado com o processamento de vértice de software. Esse sinalizador é necessário no processamento de vértices de modo misto (D3DCREATE \_ Mixed \_ VERTEXPROCESSING) quando o processamento de vértice de software é usado.

O app pode gravar diretamente índices em um buffer de índice alocado na memória ideal de driver. Essa técnica impede uma operação de cópia redundante mais tarde. Essa técnica não funciona bem se o app lê dados de um buffer de índice, pois operações de leitura feitas pelo host da memória ideal de driver podem ser muito lentas. Portanto, se seu app precisar ler durante o processamento ou gravar dados no buffer de modo irregular, um buffer de índice de memória do sistema é a melhor opção.

> [!Note]  
> Sempre use D3DPOOL \_ padrão, exceto quando você não quiser usar a memória de vídeo ou usar grandes quantidades de RAM bloqueada por página quando o driver estiver colocando buffers de vértice ou de índice na memória AGP.

 

## <a name="create-an-index-buffer"></a>Criar um buffer de índice

Crie um objeto de buffer de índice chamando o método [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) , que aceita seis parâmetros.

-   O primeiro parâmetro especifica o tamanho do buffer de índice, em bytes.
-   O segundo parâmetro é um conjunto de controles de uso. Entre outras coisas, seu valor determina se os vértices que estão sendo referenciados pelos índices são capazes de conter informações de recorte. Para melhorar o desempenho, especifique D3DUSAGE \_ DONOTCLIP quando o recorte não for necessário.

    O \_ sinalizador D3DUSAGE SOFTWAREPROCESSING pode ser definido quando o processamento de vértices de software ou de modo misto (D3DCREATE \_ Misto \_ VERTEXPROCESSING/D3DCREATE \_ software \_ VERTEXPROCESSING) está habilitado para esse dispositivo. D3DUSAGE \_ SOFTWAREPROCESSING deve ser definido para os buffers a serem usados com o processamento de vértice de software no modo misto, mas não deve ser definido para o melhor desempenho possível ao usar o processamento de índice de hardware no modo misto (D3DCREATE \_ hardware \_ VERTEXPROCESSING). No entanto, definir D3DUSAGE \_ SOFTWAREPROCESSING é a única opção quando um único buffer é usado com o processamento de vértice de hardware e software. D3DUSAGE \_ SOFTWAREPROCESSING é permitido para dispositivos mistos e de software.

    É possível forçar os buffers de vértice e de índice na memória do sistema, especificando D3DPOOL \_ SYSTEMMEM, mesmo quando o processamento do índice está sendo feito no hardware. Essa é uma maneira de evitar grandes quantidades de memória bloqueada por página quando um driver está colocando esses buffers na memória AGP.

-   O terceiro parâmetro é o membro D3DFMT \_ INDEX16 ou D3DFMT \_ INDEX32 do tipo enumerado [D3DFORMAT](d3dformat.md) que especifica o tamanho de cada índice.

-   O quarto parâmetro é um membro do tipo enumerado [**D3DPOOL**](./d3dpool.md) que informa ao sistema onde a memória deve posicionar o novo buffer de índice.

-   O parâmetro final que [**IDirect3DDevice9:: CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer) aceita é o endereço de uma variável que é preenchida com um ponteiro para a nova interface [**IDirect3DIndexBuffer9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dindexbuffer9) do objeto de buffer de vértice, caso a chamada tenha sucesso.

O exemplo de código C++ a seguir mostra como a criação de um buffer de índice pode ser semelhante ao código.


```
/*
 * For the purposes of this example, the d3dDevice variable is the 
 * address of an IDirect3DDevice9 interface exposed by a 
 * Direct3DDevice object, g_IB is a variable of type 
 * LPDIRECT3DINDEXBUFFER9.
 */

if( FAILED( d3dDevice->CreateIndexBuffer( 16384 *sizeof(WORD),
           D3DUSAGE_WRITEONLY, D3DFMT_INDEX16, D3DPOOL_DEFAULT, 
           &g_IB, NULL ) ) )
    return E_FAIL;
```



## <a name="access-an-index-buffer"></a>Acessar um buffer de índice

Os objetos de buffer de índice permitem que os aplicativos acessem diretamente a memória alocada para dados de índice. Você pode recuperar um ponteiro para indexar a memória do buffer chamando o método [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) e, em seguida, acessando a memória conforme necessário para preencher o buffer com novos dados de índice ou para ler os dados que ele contém. O método Lock aceita quatro parâmetros. O primeiro, *offsetToLock*, é o deslocamento nos dados do índice. O segundo parâmetro é o tamanho, medido em bytes, dos dados do índice. O terceiro parâmetro aceito pelo método **IDirect3DIndexBuffer9:: Lock** , *ppbData*, é o endereço de um ponteiro de byte preenchido com um ponteiro para os dados do índice, caso a chamada tenha sucesso.

O último parâmetro, *flags*, informa ao sistema como a memória deve ser bloqueada. Você pode usá-lo para indicar como o aplicativo acessa os dados no buffer. Especifique constantes para o parâmetro *flags* de acordo com a maneira como os dados de índice serão acessados pelo seu aplicativo. Isso permite que o driver bloqueie a memória e forneça o melhor desempenho de acordo com o tipo de acesso solicitado. Use \_ o sinalizador ReadOnly D3DLOCK se seu aplicativo for lido somente da memória do buffer de índice. A inclusão desse sinalizador permite que o Direct3D Otimize seus procedimentos internos para melhorar a eficiência, Considerando que o acesso à memória será somente leitura.

Depois de preencher ou ler os dados do índice, chame o método [**IDirect3DIndexBuffer9:: Unlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-unlock) , conforme mostrado no exemplo de código a seguir.


```
// This code example assumes the m_pIndexBuffer is a variable of type 
// LPDIRECT3DINDEXBUFFER9 and that g_Indices has been properly 
// initialized with indices.

// To fill the index buffer, you must lock the buffer to gain 
// access to the indices. This mechanism is required because index
// buffers may be in device memory.

VOID* pIndices;

if( FAILED( m_pIndexBuffer->Lock( 
      0,                 // Fill from start of the buffer
      sizeof(g_Indices), // Size of the data to load
      BYTE**)&pIndices,  // Returned index data
      0 ) ) )            // Send default flags to the lock
{
    SAFE_RELEASE(m_pIndexBuffer);
    return E_FAIL;
}

memcpy( pIndices, g_Indices, sizeof(g_Indices) );
m_pIndexBuffer->Unlock();
```



> [!Note]
>
> Se você criar um buffer de índice com o \_ sinalizador WRITEONLY D3DUSAGE, não use o \_ sinalizador de bloqueio ReadOnly do D3DLOCK. Use o \_ sinalizador D3DLOCK ReadOnly se seu aplicativo for ler apenas da memória do buffer de índice. A inclusão desse sinalizador permite que o Direct3D Otimize seus procedimentos internos para melhorar a eficiência, Considerando que o acesso à memória será somente leitura.
>
> Para obter informações sobre como usar D3DLOCK \_ descarte ou D3DLOCK \_ NoOverwrite para o parâmetro *flags* do método [**IDirect3DIndexBuffer9:: Lock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock) , consulte [otimizações de desempenho (Direct3D 9)](performance-optimizations.md).

 

Em C++, como você acessa diretamente a memória alocada para o buffer de índice, verifique se o aplicativo acessa corretamente a memória alocada. Caso contrário, você correrá o risco de renderizar a memória inválida. Use o stride do formato de índice que seu aplicativo usa para mover de um índice no buffer alocado para outro.

Recupere informações sobre um buffer de índice chamando o método [**IDirect3DIndexBuffer9:: GetDesc**](/windows/desktop/api) . Esse método preenche os membros da estrutura [**\_ desc D3DINDEXBUFFER**](d3dindexbuffer-desc.md) com informações sobre o buffer de índice.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos do Direct3D](direct3d-resources.md)
</dt> <dt>

[Renderização de vértices e buffers de índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> <dt>

[Buffers de vértice (Direct3D 9)](vertex-buffers.md)
</dt> </dl>

 

 
