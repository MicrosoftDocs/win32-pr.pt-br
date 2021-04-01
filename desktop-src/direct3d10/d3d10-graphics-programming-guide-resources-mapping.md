---
description: Copiando e acessando dados de recurso (Direct3D 10)
ms.assetid: 34fd4d15-ee64-4acf-967d-a4afb6f26329
title: Copiando e acessando dados de recurso (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38bd075585ee3123e163075a50b06b53a77a214c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646404"
---
# <a name="copying-and-accessing-resource-data-direct3d-10"></a>Copiando e acessando dados de recurso (Direct3D 10)

Não é mais necessário pensar em recursos como sendo criados na memória de vídeo ou na memória do sistema. Ou se o tempo de execução deve ou não gerenciar a memória. Graças à arquitetura do novo WDDM (modelo de driver de vídeo do Windows), agora os aplicativos criam recursos do Direct3D 10 com sinalizadores de [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) diferentes para indicar como o aplicativo pretende usar os dados do recurso. O novo modelo de driver virtualiza a memória usada pelos recursos; em seguida, ele se torna responsável pelo Gerenciador de sistema operacional/driver/memória para posicionar recursos na área de mais desempenho da memória possível, dado o uso esperado.

Por padrão, os recursos estão disponíveis para a GPU. É claro que, tendo dito isso, há ocasiões em que os dados de recursos precisam estar disponíveis para a CPU. Copiar os dados de recurso ao redor para que o processador apropriado possa acessá-los sem afetar o desempenho exige algum conhecimento de como funcionam os métodos da API.

-   [Copiando dados de recurso](#copying-and-accessing-resource-data-direct3d-10)
-   [Acessando dados de recursos](#copying-and-accessing-resource-data-direct3d-10)

## <a name="copying-resource-data"></a>Copiando dados de recurso

Os recursos são criados na memória quando o Direct3D executa uma chamada de criação. Eles podem ser criados na memória de vídeo, memória do sistema ou qualquer outro tipo de memória. Como o modelo de driver WDDM virtualiza essa memória, apps não precisam mais acompanhar que tipo de recursos de memória são criados.

Idealmente, todos os recursos devem estar localizados na memória de vídeo para que a GPU possa ter acesso imediato a eles. No entanto, às vezes, é necessário que a CPU leia os dados de recurso ou que a GPU acesse os dados de recurso nos quais a CPU realizou gravações. O Direct3D 10 lida com esses cenários diferentes solicitando que o aplicativo especifique um uso e, em seguida, oferece vários métodos para copiar os dados de recursos quando necessário.

Dependendo de como o recurso foi criado, ele nem sempre é capaz de acessar diretamente os dados subjacentes. Isso pode significar que os dados de recurso devem ser copiados do recurso de origem para outro recurso que seja acessível pelo processador apropriado. Em termos de Direct3D 10, os recursos padrão podem ser acessados diretamente pela GPU, os recursos dinâmicos e de preparo podem ser acessados diretamente pela CPU.

Depois que um recurso tiver sido criado, seu [**uso**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) não poderá ser alterado. Em vez disso, copie o conteúdo de um recurso para outro recurso que foi criado com um uso diferente. O Direct3D 10 fornece essa funcionalidade com três métodos diferentes. Os dois primeiros métodos ( [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)) são projetados para copiar dados de recurso de um recurso para outro. O terceiro método ([**ID3D10Device:: UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource)) foi projetado para copiar dados da memória para um recurso.

Existem dois tipos principais de recursos: mapeáveis e não mapeáveis. Os recursos criados com usos dinâmico ou de preparo são mapeáveis, enquanto os recursos criados com os usos padrão ou imutável são não mapeáveis.

Copiar dados entre recursos não mapeáveis é muito rápido porque esse é o caso mais comum e foi otimizado para uma boa execução. Como esses recursos não são diretamente acessíveis pela CPU, eles são otimizados para que a GPU possa manipulá-los rapidamente.

Copiar dados entre recursos mapeáveis é mais problemático porque o desempenho depende do uso com o qual o recurso foi criado. Por exemplo, a GPU pode ler um recurso dinâmico rapidamente, mas não pode gravá-los, e a GPU não pode ler ou gravar recursos de preparo diretamente.

Aplicativos que desejam copiar dados de um recurso com uso padrão para um recurso com uso de preparo (para permitir que a CPU Leia os dados – ou seja, o problema de readback da GPU) devem fazer isso com cuidado. Consulte [acessando dados de recursos](#copying-and-accessing-resource-data-direct3d-10) para obter mais detalhes sobre esse último caso.

## <a name="accessing-resource-data"></a>Acessando dados de recursos

Acessar um recurso requer o mapeamento do recurso; mapeando significa essencialmente que o app está tentando dar acesso à CPU para a memória. O processo de mapeamento de um recurso para que a CPU possa acessar a memória subjacente pode causar alguns afunilamentos de desempenho e por esse motivo, é obrigatório ter cautela com a forma e o momento da execução dessa tarefa.

O desempenho pode ser interrompidas se o app tentar mapear um recurso no momento errado. Se o app tentar acessar os resultados de uma operação antes que essa operação esteja concluída, ocorrerá uma vaga de pipeline.

Executar uma operação de mapeamento no momento errado pode causar uma queda grave no desempenho, forçando a GPU e CPU a sincronizarem entre si. Essa sincronização ocorrerá se o app quiser acessar um recurso antes que a GPU termine de copiá-lo para um recurso que a CPU pode mapear.

A CPU só pode ler de recursos criados com o sinalizador de preparo de uso de D3D10 \_ \_ . Como os recursos criados com esse sinalizador não podem ser definidos como saídas do pipeline, se a CPU quiser ler os dados em um recurso gerado pela GPU, os dados deverão ser copiados para um recurso criado com o sinalizador de preparo. O aplicativo pode fazer isso usando os métodos [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) para copiar o conteúdo de um recurso para outro. O aplicativo pode, então, obter acesso a esse recurso chamando o método MAP apropriado. Quando o acesso ao recurso não for mais necessário, o aplicativo deverá chamar o método de mapeamento correspondente. Por exemplo, [**ID3D10Texture2D:: map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) e [**ID3D10Texture2D:: remapeamento**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-unmap). Os diferentes métodos de mapa retornam alguns valores específicos, dependendo dos sinalizadores de entrada. Consulte a [**seção comentários do mapa**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture1d-map) para obter detalhes.

> [!Note]  
> Quando o aplicativo chama o método MAP, ele recebe um ponteiro para os dados do recurso a serem acessados. O tempo de execução garante que o ponteiro tenha um alinhamento específico, dependendo do [nível de recurso](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md). Para o [**nível de recurso do D3D \_ \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level) e superior, o ponteiro é alinhado a 16 bytes. Para o nível de recurso do D3D inferior a [**\_ \_ \_ 10 \_ 0**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_feature_level), o ponteiro é alinhado a 4 bytes. O alinhamento de 16 bytes permite que o aplicativo execute operações otimizadas para [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))nos dados nativamente, sem realinhamento ou cópia.

 

### <a name="performance-considerations"></a>Considerações sobre desempenho

É melhor pensar em um computador como sendo uma máquina funcionando como uma arquitetura paralela com dois tipos principais de processadores: uma ou mais CPUs e uma ou mais GPUs. Como em qualquer arquitetura paralela, o melhor desempenho é atingido quando cada processador está programado tarefas o suficiente para impedir que ele fique ocioso e que o trabalho de um processador não fique aguardando o trabalho do outro.

O pior cenário para o paralelismo de GPU/CPU é a necessidade de forçar um processador a esperar pelos resultados do trabalho feito pelo outro. O Direct3D 10 tenta remover esse custo, tornando os métodos [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) e [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) assíncronos; a cópia não é necessariamente executada no momento em que o método retorna. A vantagem disso é que o app não paga o custo de desempenho de copiar realmente os dados até que a CPU acesse os dados, que é quando é chamado o mapa. Se o método de mapa for chamado depois que os dados realmente foram copiados, nenhuma perda de desempenho ocorre. Por outro lado, se o método de mapa for chamado antes dos dados terem sido copiados, uma vaga de pipeline ocorrerá.

As chamadas assíncronas no Direct3D 10 (que são a grande maioria dos métodos e especialmente chamadas de renderização) são armazenadas no que chamamos de buffer de comando. Esse buffer encontra-se no interior do driver de elementos gráficos e é usado para compilar em lotes as chamadas para o hardware subjacente, para que a alternância dispendiosa do modo de usuário para o modo de kernel no Microsoft Windows ocorra com a menor frequência possível.

O buffer de comando é liberado, causando uma alternância de modo de usuário/kernel, em uma das quatro situações, que são as seguintes.

1.  [**Presente**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) é chamado.
2.  [**ID3D10Device:: flush**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-flush) é chamado.
3.  O buffer de comando está cheio; seu tamanho é dinâmico e é controlado pelo sistema operacional e pelo driver gráfico.
4.  A CPU requer acesso aos resultados de um comando que está aguardando para ser executado no buffer de comando.

Das quatro situações acima, a número quatro é a mais crítica para o desempenho. Se o aplicativo emitir uma chamada [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) , essa chamada será enfileirada no buffer de comando. Se o aplicativo tentar mapear o recurso de preparo que foi o destino da chamada de cópia antes de o buffer de comando ter sido liberado, ocorrerá uma parada de pipeline porque não apenas a chamada do método de cópia precisará ser executada, mas todos os outros comandos em buffer no buffer de comando também devem ser executados. Isso fará com que a GPU e a CPU sincronizem porque a CPU aguardará para acessar o recurso de preparo enquanto a GPU esvazia o buffer de comando e finalmente preenche o recurso que a CPU precisa. Depois que a GPU finalizar a cópia, a CPU começará a acessar o recurso de preparo, mas durante esse tempo, a GPU estará ociosa.

Fazer isso com frequência em tempo de execução prejudicará gravemente o desempenho. Por esse motivo, o mapeamento de recursos criado com o uso padrão deve ser feito com cautela. O app precisa esperar tempo suficiente para que o buffer de comando seja esvaziado e, portanto, espera que todos esses comandos encerrem a execução antes de tentar mapear o recurso de preparo correspondente. Quanto tempo o app deve esperar? Pelo menos dois quadros porque isso permitirá que o paralelismo entre as CPUs e a GPU seja utilizado ao máximo. A GPU funciona da seguinte forma: enquanto o app está processando o quadro N enviando chamadas para o buffer de comando, a GPU está ocupada executando as chamadas do quadro anterior, N-1.

Portanto, se um aplicativo quiser mapear um recurso originado na memória de vídeo e chamar [**ID3D10Device:: CopyResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource) ou [**ID3D10Device:: CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion) no quadro n, essa chamada começará a ser executada no quadro n + 1, quando o aplicativo estiver enviando chamadas para o próximo quadro. A cópia deve ser concluída quando o app estiver processando o quadro N+2.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Quadro</th>
<th>Status da GPU/CPU</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>N</td>
<td><ul>
<li>A CPU emite chamadas de renderização para o quadro atual.</li>
</ul></td>
</tr>
<tr class="even">
<td>N+1</td>
<td><ul>
<li>GPU executando chamadas enviadas da CPU durante o quadro N.</li>
<li>A CPU emite chamadas de renderização para o quadro atual.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N+2</td>
<td><ul>
<li>A GPU encerrou as chamadas enviadas da CPU durante o quadro N. Resultados prontos.</li>
<li>GPU executando chamadas enviadas da CPU durante o quadro N+1.</li>
<li>A CPU emite chamadas de renderização para o quadro atual.</li>
</ul></td>
</tr>
<tr class="even">
<td>N+3</td>
<td><ul>
<li>A GPU encerrou as chamadas enviadas da CPU durante o quadro N+1. Resultados prontos.</li>
<li>GPU executando chamadas enviadas da CPU durante o quadro N+2.</li>
<li>A CPU emite chamadas de renderização para o quadro atual.</li>
</ul></td>
</tr>
<tr class="odd">
<td>N+4</td>
<td>...</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
