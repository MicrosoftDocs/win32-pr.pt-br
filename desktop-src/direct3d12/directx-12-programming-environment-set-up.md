---
title: Configuração do ambiente programação do Direct3D 12
description: Descreve a instalação, as ferramentas e as bibliotecas com suporte que compõem um ambiente de desenvolvimento Direct3D 12 produtivo.
ms.assetid: B2288866-E95F-46B8-A7A1-19888F029C03
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7079207f91185cc14b37d9056a4fa813b251bce5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342811"
---
# <a name="direct3d-12-programming-environment-setup"></a>Configuração do ambiente programação do Direct3D 12

Descreve a instalação, as ferramentas e as bibliotecas com suporte que compõem um ambiente de desenvolvimento Direct3D 12 produtivo.

-   [Ambiente de desenvolvimento](#development-environment)
-   [Idiomas com suporte](#supported-languages)
-   [Estruturas auxiliares](#helper-structures)
-   [Biblioteca de gerenciamento de memória](#memory-management-library)
-   [Bibliotecas e ferramentas com suporte](#supported-tools-and-libraries)
-   [Amostras](#samples)
-   [Camada de depuração](#debug-layer)
-   [Vídeos educacionais](#educational-videos)
-   [Tópicos relacionados](#related-topics)

## <a name="development-environment"></a>Ambiente de desenvolvimento

Os cabeçalhos e as bibliotecas do Direct3D 12 fazem parte do SDK do Windows 10. Não há nenhum download ou instalação separado necessário para usar o Direct3D 12.

Depois de instalar o software SDK do Windows 10 e o Visual Studio, a configuração do ambiente de programação do Direct3D 12 estará concluída. O Visual Studio 2019 é recomendado, pois incluirá as ferramentas de depuração de gráficos do D3D12, mas as versões anteriores do Visual Studio funcionarão para o desenvolvimento do programa.

Para usar a [API do Direct3D 12](direct3d-12-reference.md), inclua D3d12. h e vincule a D3d12. lib ou consulte os pontos de entrada diretamente no D3d12.dll.

Os cabeçalhos e as bibliotecas a seguir estão disponíveis. O local das bibliotecas estáticas depende da versão (32 bits ou 64 bits) do Windows 10 em execução no computador.



| Nome do arquivo de cabeçalho ou biblioteca | Descrição                         | Local da instalação      |
|-----------------------------|-------------------------------------|-----------------------|
| D3d12. h                     | Cabeçalho de API do Direct3D 12              | % WindowsSdkDir \\ inclui \% WindowsSDKVersion% \\ \um |
| D3d12. lib                   | Biblioteca de stub de API Direct3D 12 estática | %WindowsSdkDir \\ Lib \% WindowsSDKVersion% \\ \um\arch |
| D3d12.dll                   | Biblioteca de API dinâmica do Direct3D 12     | %WINDIR% \\ System32    |
| D3d12SDKLayers.h            | Header de depuração do Direct3D 12            | %WindowsSdkDir \\ Incluir \% WindowsSDKVersion% \\ \um |
| D3d12SDKLayers.dll          | Biblioteca de depuração dinâmica do Direct3D 12   | %WINDIR% \\ System32    |



## <a name="supported-languages"></a>Idiomas com suporte

O C++ é a única linguagem com suporte para desenvolvimento do Direct3D 12, não há suporte para C# e outras linguagens .NET.

## <a name="helper-structures"></a>Estruturas auxiliares

Há várias estruturas auxiliares que, em particular, facilitam a inicialização de várias estruturas D3D12. Essas estruturas e algumas funções de utilitário estão no header D3dx12.h. Esse header é de software livre e pode ser modificado por um desenvolvedor conforme necessário – baixe-o na Biblioteca auxiliar [D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries/D3DX12) e consulte Estruturas auxiliares e funções para [D3D12](helper-structures-and-functions-for-d3d12.md).

## <a name="memory-management-library"></a>Biblioteca de Gerenciamento de Memória

Uma biblioteca auxiliar de gerenciamento de memória está disponível para download que você pode integrar ao seu aplicativo para corresponder mais de perto ao comportamento de gerenciamento de memória D3D11. Como uma biblioteca de gerenciamento de estilo D3D11, ela é mais eficaz com aplicativos que ainda estão usando uma estratégia *de* alocação de estilo de recurso confirmado. Em particular, a biblioteca deve ser vista como um passo a passo que fará com que você volte ao gerenciamento de memória de desempenho D3D11 quando estiver em cenários com restrição de memória (por exemplo, cartões de memória de baixa extremidade, 4k, configurações ultra e assim por diante). As APIs D3D12 permitem técnicas que permitem que você tenha uma eficiência de memória ainda melhor em relação a D3D11, embora essas técnicas possam ser desafiadoras e demoradas para implementar.

Observe que essa biblioteca é um trabalho em andamento e pode mudar ao longo do tempo. Use os links abaixo para acessar a biblioteca e os exemplos.

-   [A biblioteca de início de residência D3D12](https://github.com/Microsoft/DirectX-Graphics-Samples/tree/master/Libraries)

## <a name="supported-tools-and-libraries"></a>Ferramentas e bibliotecas com suporte

Todas as bibliotecas a seguir podem ser usadas com o Direct3D 12.



| Biblioteca                                                                                 |  Finalidade                                                                                                                                                                                                                                                                      | Documentação                                                                                                           |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [DirectX Tool Kit for DirectX 12](https://github.com/Microsoft/DirectXTK12) | Uma coleção substancial de classes auxiliares para escrever código do Direct3D 12 C++ para aplicativos UWP (Plataforma Universal do Windows), aplicativos da área de trabalho Win32 para Windows 10 e Xbox One exclusivos.                                                                         | [Wiki do DirectX12TK](https://github.com/Microsoft/DirectXTK12/wiki)                                          |
| [DirectXTex](https://github.com/Microsoft/DirectXTex)                      | Use isso para ler e escrever arquivos DDS e executar várias operações de processamento de conteúdo de textura, incluindo reizing, conversão de formato, geração de mapa mip, compactação de bloco para recursos de textura de runtime direct3D e mapa de altura para conversão de mapa normal. | [Wiki do DirectXTex](https://github.com/Microsoft/DirectXTex/wiki)                                            |
| [DirectXMesh](https://github.com/Microsoft/DirectXMesh)                   | Use isso para executar várias operações de processamento de conteúdo geometry, incluindo a geração de normais e quadros tangentes, cálculos de adjaciação de triângulo e otimização de cache de vértice.                                                                                | [Wiki do DirectXMesh](https://github.com/Microsoft/DirectXMesh/wiki)                                          |
| [DirectXMath](https://github.com/Microsoft/DirectXMath)                     | Um grande número de classes auxiliares e métodos para dar suporte a vetores, escalares, matrizes, quatérions e muitas outras operações matemáticas.                                                                                                                               | [Documentação do DirectXMath no MSDN](/windows/desktop/dxmath/ovw-xnamath-progguide) |
| [UVAtlas](https://github.com/Microsoft/UVAtlas)                         | Use isso para criar e empacotar um atlas de textura isochart.                                                                                                                                                                                                           | [Wiki UVAtlas](https://github.com/Microsoft/UVAtlas/wiki)                                                  |



 

## <a name="samples"></a>Exemplos

Para ver uma lista de exemplos D3D12 em funcionamento e como localizá-los e executar, consulte [Amostras de trabalho.](working-samples.md)

Para ver passo a passo sobre como adicionar código para habilitar recursos [específicos, consulte D3D12 Code Walk-Throughs](d3d12-code-walk-throughs.md).

## <a name="debug-layer"></a>Camada de depuração

A camada de depuração fornece uma ampla validação de consistência e parâmetro adicional (como validar vinculação de sombreador e associação de recursos, validar a consistência do parâmetro e relatar descrições de erro).

> [!Note]  
> Para o Windows 10, para criar um dispositivo que dê suporte à camada de depuração, habilite o recurso opcional "ferramentas de gráficos". Vá para o painel configurações, em sistema, aplicativos & recursos, gerencie recursos opcionais, adicione um recurso e procure "ferramentas de gráficos".

O cabeçalho necessário para dar suporte à camada de depuração, D3D12SDKLayers. h, está incluído por padrão em d3d12. h.

Quando a camada de depuração lista vazamentos de memória, ela gera uma lista de ponteiros de interface de objeto junto com seus nomes amigáveis. O nome amigável padrão é " &lt; sem nome &gt; ". Você pode definir o nome amigável usando o método [**ID3D12Object:: SetName**](/windows/desktop/api/d3d12/nf-d3d12-id3d12object-setname) . Normalmente, você deve compilar essas chamadas fora de sua versão de produção.

Recomendamos que você use a camada de depuração para depurar seus aplicativos a fim de garantir que eles estejam com limpeza de erros e avisos. A camada de depuração ajuda a escrever código do Direct3D 12. Além disso, sua produtividade pode aumentar quando você usa a camada de depuração, pois você pode ver imediatamente as causas de erros de renderização obscuras ou até mesmo de telas pretas em sua origem. A camada de depuração fornece avisos para muitos problemas. Por exemplo:

-   Esqueceu de definir uma textura, mas lê-la no sombreador de pixel.
-   Profundidade de saída, mas não há limite de estado de estêncil de profundidade.
-   Falha na criação de textura com INVALIDARG.

Defina o compilador definir D3DCOMPILE \_ debug para instruir o compilador HLSL a incluir informações de depuração no blob de sombreador.

``` syntax
#define D3DCOMPILE_DEBUG 1
```

Para obter detalhes de todos os métodos e interfaces de depuração, consulte a [referência da camada de depuração](direct3d-12-sdklayers-reference.md).

Para obter informações gerais sobre como usar a camada de depuração, consulte [noções básicas sobre a camada de depuração D3D12](understanding-the-d3d12-debug-layer.md).

## <a name="educational-videos"></a>Vídeos educacionais

Há vários vídeos relacionados ao Direct3D 12 e ao Windows 10 em [tutoriais de vídeo do DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA), incluindo vídeos sobre ferramentas de depuração de gráficos e bugs de gráficos de relatórios.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Introdução ao Direct3D 12](directx-12-getting-started.md)
</dt> </dl>

 

 