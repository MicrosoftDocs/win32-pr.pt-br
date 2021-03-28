---
title: O que há de novo na visualização técnica do Direct3D 11 de novembro de 2008
description: Esta versão do Direct3D 11 contém novos recursos, ferramentas e documentação.
ms.assetid: 7d259764-b826-4609-b415-2093cc6df874
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81a49529882eafaf092a866d1b172de62fe15c8e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366065"
---
# <a name="whats-new-in-the-nov-2008-direct3d-11-tech-preview"></a>O que há de novo na visualização técnica do Direct3D 11 de novembro de 2008

Esta versão do Direct3D 11 contém novos recursos, ferramentas e documentação.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Tessellation"></span><span id="tessellation"></span><span id="TESSELLATION"></span>Mosaico<br/></td>
<td>O Direct3D 11 fornece estágios de pipeline adicionais para dar suporte ao <a href="direct3d-11-advanced-stages-tessellation.md">mosaico em tempo real</a> de primitivos de ordem alta. Com recursos amplamente programáveis, esse recurso permite muitos métodos diferentes para avaliar superfícies de ordem superior, incluindo superfícies de subdivisão usando técnicas de aproximação, patches de Bézier, mosaico adaptável e mapeamento de deslocamento. Esse recurso só estará disponível no hardware do Direct3D 11, portanto, para avaliar esse recurso, será necessário usar o rasterizador de referência. Para uma demonstração do mosaico em ação, confira o exemplo <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> disponível por meio do navegador de exemplo.<br/></td>
</tr>
<tr class="even">
<td><span id="Compute_Shader"></span><span id="compute_shader"></span><span id="COMPUTE_SHADER"></span>Sombreador de computação<br/></td>
<td>O <a href="direct3d-11-advanced-stages-compute-shader.md">sombreador de computação</a> é um estágio adicional independente do pipeline do Direct3D 11 que permite a computação de uso geral na GPU. Além de todos os recursos de sombreador fornecidos pelo núcleo do sombreador unificado, o sombreador de computação também dá suporte a leituras e gravações espalhadas em recursos por meio de exibições de acesso não ordenado, um pool de memória compartilhada dentro de um grupo de threads em execução, primitivos de sincronização, operadores atômicos e muitos outros recursos avançados de dados em paralelo. Uma variante do sombreador de computação do Direct3D 11 foi habilitada nesta versão que pode operar no hardware do Direct3D de 10 classes. Portanto, é possível desenvolver sombreadores de computação no hardware real, mas é necessário um driver atualizado. A funcionalidade completa do sombreador de computação do Direct3D 11 destina-se ao suporte do hardware do Direct3D 11 Class. portanto, para avaliar a funcionalidade completa, você precisará usar o rasterizador de referência até que esse hardware esteja disponível. Para uma demonstração do sombreador de computação em ação, confira o exemplo <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> disponível por meio do navegador de exemplo.<br/></td>
</tr>
<tr class="odd">
<td><span id="Multithreaded_Rendering"></span><span id="multithreaded_rendering"></span><span id="MULTITHREADED_RENDERING"></span>Renderização multi-threaded<br/></td>
<td>A principal diferença da API do Direct3D 10 no Direct3D 11 é a adição de <a href="overviews-direct3d-11-render-multi-thread.md">contextos adiados</a>, que permite a execução escalonável de comandos do Direct3D distribuídos em vários núcleos. Um contexto adiado captura e monta ações como alterações de estado e envios de desenho que podem ser executados no dispositivo real posteriormente. Ao utilizar contextos adiados em vários threads, um aplicativo pode distribuir a sobrecarga de CPU necessária no tempo de execução do Direct3D11 e o driver para vários núcleos, permitindo um melhor uso da configuração da máquina de um usuário final. Esse recurso está disponível para uso no hardware atual do Direct3D 10, bem como no rasterizador de referência. Para uma demonstração do uso da API, confira o exemplo <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> disponível por meio do navegador de exemplo.<br/></td>
</tr>
<tr class="even">
<td><span id="Dynamic_Shader_Linkage_"></span><span id="dynamic_shader_linkage_"></span><span id="DYNAMIC_SHADER_LINKAGE_"></span>Vinculação de sombreador dinâmico <br/></td>
<td>Para resolver o problema de explosão do combinador visto em especializar sombreadores para desempenho, o Direct3D 11 apresenta uma forma limitada de <a href="/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking">vínculo de sombreador</a> de tempo de execução que permite uma especialização de sombreamento quase ideal durante a execução de um aplicativo. Isso é feito especificando as implementações de funções específicas no código do sombreador quando o sombreador é atribuído ao pipeline, permitindo que o driver embutisse as instruções do sombreador nativo rapidamente, em vez de forçar o driver a recompilar a linguagem intermediária em instruções nativas com a nova configuração. O desenvolvimento de sombreador é exposto por meio da introdução de classes e interfaces para HLSL. Para uma demonstração, confira o exemplo de <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">vinculação de sombreador dinâmico 11</a> disponível por meio do navegador de exemplo.<br/></td>
</tr>
<tr class="odd">
<td><span id="Windows_Advanced_Rasterizer__WARP_"></span><span id="windows_advanced_rasterizer__warp_"></span><span id="WINDOWS_ADVANCED_RASTERIZER__WARP_"></span>Rasterizador avançado do Windows (WARP)<br/></td>
<td>Disponível neste SDK por meio do Direct3D 11 e, eventualmente, por meio do Direct3D 10,1, WARP é um rasterizador rápido de dimensionamento de vários núcleos que é totalmente compatível com o Direct3D 10,1. Usar essa tecnologia é tão simples quanto passar o sinalizador de D3D_DRIVER_TYPE_WARP na criação do dispositivo.<br/></td>
</tr>
<tr class="even">
<td><span id="Direct3D_10_and_Direct3D_11_on_Direct3D_9_Hardware__D3D10_Level_9_"></span><span id="direct3d_10_and_direct3d_11_on_direct3d_9_hardware__d3d10_level_9_"></span><span id="DIRECT3D_10_AND_DIRECT3D_11_ON_DIRECT3D_9_HARDWARE__D3D10_LEVEL_9_"></span>Direct3D 10 e Direct3D 11 no hardware do Direct3D 9 (D3D10 nível 9)<br/></td>
<td>Disponível neste SDK por meio do Direct3D 11 e, eventualmente, por meio do Direct3D 10,1, a API do Direct3D pode ter como destino a maioria dos hardwares do Direct3D 9, bem como o hardware do Direct3D 10, do Direct3D 10,1 e do Direct3D 11. Isso é obtido fornecendo o mecanismo de nível de recurso, que agrupa o hardware em seis categorias, dependendo da funcionalidade: 9_1, 9_2, 9_3, 10_0, 10_1 e 11_0. Um cartão só atenderá a um nível de recurso se ele for totalmente compatível com esse nível, e cada nível for um superconjunto estrito deles abaixo dele. A funcionalidade é desemulada minimamente para garantir que nenhum beira de desempenho inesperado seja encontrado. Assim, recursos como sombreadores de geometria não estão disponíveis para destinos de nível do Direct3D 9. <br/></td>
</tr>
<tr class="odd">
<td><span id="Runtime_Binaries"></span><span id="runtime_binaries"></span><span id="RUNTIME_BINARIES"></span>Binários de tempo de execução<br/></td>
<td>Todos os binários de tempo de execução fornecidos no Direct3D 11 Tech Preview que estarão disponíveis no Windows 7 e no Windows Vista SP1 são instalados com o SDK e são rotulados como &quot; &quot; componentes beta (ou seja, D3D11_beta.DLL). Todos os componentes com rótulo beta têm um tempo de bomba. Para criar projetos para avaliar esses novos componentes, você deve vincular a suas bibliotecas de importação de rótulo beta equivalentes (ou seja, D3D11_beta. lib). Se você tiver uma cópia de PDC do Windows 7, os cabeçalhos, bibliotecas e PDBs fornecidos no SDK do Windows com a compilação são apropriados para o desenvolvimento usando os componentes do Direct3D 11 que fornecem no Windows 7. Reserve o uso dos cabeçalhos, bibliotecas e PDBs neste SDK para os componentes beta fornecidos neste documento.<br/></td>
</tr>
<tr class="even">
<td><span id="D3DX11"></span><span id="d3dx11"></span>D3DX11<br/></td>
<td>O D3DX11 atualmente dá suporte ao carregamento de textura, à compilação de sombreador, ao carregamento de dados e às funções de thread de trabalho para recursos do Direct3D No futuro, esse componente fornecerá mais das tecnologias disponíveis no D3DX10. A funcionalidade de compilação do sombreador também é fornecida diretamente por meio do componente do compilador do Direct3D, descrito a seguir.<br/></td>
</tr>
<tr class="odd">
<td><span id="HLSL_and_Direct3D_Compiler"></span><span id="hlsl_and_direct3d_compiler"></span><span id="HLSL_AND_DIRECT3D_COMPILER"></span>Compilador HLSL e Direct3D<br/></td>
<td>O compilador HLSL tem vários recursos novos para dar suporte às novas tecnologias disponíveis no Direct3D 11. Isso inclui a programação orientada a objeto por meio de interfaces e classes, uma sintaxe de indexação direta para cargas de recursos e a palavra-chave "preciso" para garantir que todas as operações executadas com uma variável específica aderem às regras estritas de ponto flutuante. Quase todos os novos recursos lingüísticos têm uma funcionalidade válida em destinos de sombreador existentes. Além de dar suporte a todos os sombreadores do Direct3D 9, Direct3D 10, Direct3D 10,1 e Direct3D 11, o compilador do HLSL também dá suporte a destinos especiais necessários para gravar sombreadores para destinos do Direct3D 10 nível 9. O compilador D3D agora está diretamente acessível fora de D3DX10 e D3DX11 por meio de D3DCompiler. H e D3DCompiler. lib. Com esses novos arquivos, um aplicativo não precisa vincular ao D3DX para executar a compilação em tempo de execução, e um aplicativo não precisa incluir o compilador se apenas a funcionalidade de D3DX for necessária.<br/></td>
</tr>
<tr class="even">
<td><span id="D3D11_Reference_Rasterizer"></span><span id="d3d11_reference_rasterizer"></span><span id="D3D11_REFERENCE_RASTERIZER"></span>Rasterizador de referência do D3D11<br/></td>
<td>O rasterizador de referência fornece uma implementação de rasterização padrão Gold para avaliação dos recursos do Direct3D 11 que ainda não estão disponíveis no hardware. O rasterizador de referência também é fornecido como uma maneira de verificar a precisão de uma implementação de hardware específica para o padrão de rasterização. O rasterizador de referência foi projetado para correção, não para o desempenho. Para criar um dispositivo de referência, basta passar o sinalizador de D3D_DRIVER_TYPE_REFERENCE na criação do dispositivo. <br/></td>
</tr>
<tr class="odd">
<td><span id="D3D11_SDK_Layers"></span><span id="d3d11_sdk_layers"></span><span id="D3D11_SDK_LAYERS"></span>Camadas do SDK do D3D11<br/></td>
<td>As camadas do SDK do Direct3D11 fornecem um mecanismo para acompanhar a operação do tempo de execução do Direct3D 11 durante o desenvolvimento. Atualmente, isso é usado para fornecer informações de depuração úteis, que não incluem apenas erros de uso impróprio, mas também avisos que recomendam o uso da prática recomendada do tempo de execução e, muitas vezes, fornecem informações detalhadas e úteis para depuração. É altamente recomendável que a saída de depuração de camadas do SDK do D3D11 esteja ativada em todos os momentos durante o desenvolvimento e um aplicativo não gere nenhuma saída de depuração durante a execução antes de ser liberada ou usada com o PIX para Windows para criação de perfil. Habilitar a camada de depuração é tão simples quanto passar o sinalizador de D3D11_CREATE_DEVICE_DEBUG no momento da criação do dispositivo. Os desenvolvedores são altamente incentivados a usar camadas em compilações de depuração. As camadas não são recomendadas para uso em compilações de perfil ou versão.<br/></td>
</tr>
<tr class="even">
<td><span id="New_Samples"></span><span id="new_samples"></span><span id="NEW_SAMPLES"></span>Novos exemplos<br/></td>
<td>Esta versão tem quatro novos exemplos.<br/>
<ul>
<li>O exemplo de <a href="https://msdn.microsoft.com/library/Ee416565(v=VS.85).aspx">vinculação de sombreador dinâmico 11</a> demonstra o uso de interfaces de sombreador do modelo do sombreador 5 e o suporte do Direct3D 11 para vinculação de métodos de interface do sombreador</li>
<li>O exemplo <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">HDRToneMappingCS11</a> demonstra como configurar e executar o sombreador de computação (cs para breve), que é um dos novos recursos mais interessantes do Direct3D 11. Embora o exemplo utilize apenas o CS para implementar o mapeamento de Tom HDR, o conceito deve se estender facilmente a outros algoritmos de pós-processamento, bem como a cálculos mais gerais.</li>
<li>O exemplo <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">MultithreadedRendering11</a> demonstra como dividir a renderização entre vários threads, com sobrecarga muito baixa.</li>
<li>O novo exemplo de <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">SubD11</a> é muito semelhante ao exemplo de SUBD10 no SDK do DirectX, exceto que foi aprimorado para aproveitar três novos estágios de pipeline do Direct3D 11: o sombreador envoltória, o Tessellator e o sombreador de domínio.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos introduzidos em versões anteriores](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

 

