---
title: Passagens de renderização do Direct3D 12
description: O recurso render passes ajuda seu renderizador a melhorar a eficiência da GPU, reduzindo o tráfego de memória de/para a memória fora do chip; Ele faz isso habilitando seu aplicativo para identificar melhor os requisitos de ordenação de processamento de recursos e as dependências de dados.
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: 96ed14cecd518a3e03672f2667306ee0a4b8d64999aab01aa72aae04975f0a83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069686"
---
# <a name="direct3d-12-render-passes"></a>Passagens de renderização do Direct3D 12

o recurso render passes é novo para o Windows 10, versão 1809 (10,0; Build 17763) e apresenta o conceito de uma passagem de renderização do Direct3D 12. Uma passagem de renderização consiste em um subconjunto dos comandos que você registra em uma lista de comandos.

Para declarar onde cada passagem de renderização começa e termina, você Aninha os comandos que pertencem a essa passagem dentro de chamadas para [**ID3D12GraphicsCommandList4:: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass) e [**EndRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-endrenderpass). Consequentemente, qualquer lista de comandos contém zero, um ou mais passagens de renderização.

## <a name="scenarios"></a>Cenários

As passagens de renderização podem melhorar o desempenho do renderizador se ele for baseado em Tile-Based renderização adiada (TBDR), entre outras técnicas. Mais especificamente, a técnica ajuda seu renderizador a melhorar a eficiência da GPU, reduzindo o tráfego de memória de/para a memória fora do chip, permitindo que seu aplicativo identifique melhor os requisitos de pedidos de processamento de recursos e as dependências de dados.

Um driver de vídeo escrito expressamente para aproveitar o recurso render passes oferece os melhores resultados. Mas as APIs de processamento podem ser executadas mesmo em drivers pré-existentes (embora não necessariamente com melhorias de desempenho).

Esses são os cenários em que as passagens de renderização são projetadas para fornecer valor.

### <a name="allow-your-application-to-avoid-unnecessary-loadsstores-of-resources-fromto-main-memory-on-a-tile-based-deferred-rendering-tbdr-architecture"></a>Permitir que seu aplicativo Evite cargas/armazenamentos desnecessários de/para a memória principal em uma arquitetura de Tile-Based deferidas de renderização (TBDR)

Uma das proposições de valor de render passas é que ele fornece um local central para indicar as dependências de dados do seu aplicativo para um conjunto de operações de renderização. Essas dependências de dados permitem que o driver de vídeo Inspecione esses dados no momento da ligação/barreira e emita instruções que minimizem cargas/armazenamentos de recursos de/para a memória principal.

### <a name="allow-your-tbdr-architecture-to-opportunistically-persistent-resources-in-on-chip-cache-across-render-passes-even-in-separate-command-lists"></a>Permitir que sua arquitetura TBDR para recursos persistentes oportunamente no cache no chip entre passagens de renderização (mesmo em listas de comandos separadas)

> [!NOTE]
> Especificamente, esse cenário é limitado aos casos em que você está gravando no mesmo destino de renderização em várias listas de comandos.

Um padrão de renderização comum é para seu aplicativo renderizar para o mesmo destino de renderização em várias listas de comandos em série, mesmo que os comandos de renderização sejam gerados em paralelo. O uso do processo de renderização neste cenário permite que esses passos sejam combinados de forma alguma (já que o aplicativo sabe que ele retomará a renderização na lista de comandos com sucesso imediato) que o driver de vídeo pode evitar uma liberação para a memória principal nos limites da lista de comandos.

## <a name="your-applications-responsibilities"></a>As responsabilidades do seu aplicativo

Mesmo com o recurso render passes, nem o tempo de execução do Direct3D 12 nem o driver de vídeo assumem a responsabilidade de oportunidades de deduzindo para reordenar/evitar cargas e armazenamentos. Para aproveitar corretamente o recurso de processamento de passagens, seu aplicativo tem essas responsabilidades.

- Identifique corretamente as dependências de dados/ordenação para suas operações.
- Solicite seus envios de uma maneira que minimize as liberações (portanto, minimize o uso de sinalizadores de **_PRESERVE** ).
- Faça uso correto das barreiras de recurso e acompanhe o estado do recurso.
- Evite cópias/limpezas desnecessárias. para ajudar a identificá-los, você pode usar os avisos de desempenho automatizados do [PIX na ferramenta Windows](https://devblogs.microsoft.com/pix/).

## <a name="using-the-render-pass-feature"></a>Usando o recurso render Pass

### <a name="what-is-a-render-pass"></a>O que é uma *passagem de renderização*?

Uma passagem de renderização é definida por esses elementos.

- Um conjunto de associações de saída que são fixas para a duração da passagem de renderização. Essas associações são para uma ou mais exibições de destino de renderização (RTVs) e/ou para uma exibição de estêncil de profundidade (DSV).
- Uma lista de operações de GPU que visam esse conjunto de associações de saída.
- Metadados que descrevem as dependências de carga/armazenamento para todas as associações de saída direcionadas pela passagem de renderização.

### <a name="declare-your-output-bindings"></a>Declarar suas associações de saída

No início de uma passagem de renderização, você declara associações para os destinos de renderização e/ou para o buffer de profundidade/estêncil. É opcional associar a destino (s) de renderização, e é opcional associar a um buffer de profundidade/estêncil. Mas você deve associar a pelo menos um dos dois e, no exemplo de código abaixo, ligamos a ambos.

Você declara essas associações em uma chamada para [**ID3D12GraphicsCommandList4:: BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass).

```cppwinrt
void render_passes(::ID3D12GraphicsCommandList4 * pIGCL4,
    D3D12_CPU_DESCRIPTOR_HANDLE const& rtvCPUDescriptorHandle,
    D3D12_CPU_DESCRIPTOR_HANDLE const& dsvCPUDescriptorHandle)
{
    const float clearColor4[]{ 0.f, 0.f, 0.f, 0.f };
    CD3DX12_CLEAR_VALUE clearValue{ DXGI_FORMAT_R32G32B32_FLOAT, clearColor4 };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessClear{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_CLEAR, { clearValue } };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessPreserve{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_PRESERVE, {} };
    D3D12_RENDER_PASS_RENDER_TARGET_DESC renderPassRenderTargetDesc{ rtvCPUDescriptorHandle, renderPassBeginningAccessClear, renderPassEndingAccessPreserve };

    D3D12_RENDER_PASS_BEGINNING_ACCESS renderPassBeginningAccessNoAccess{ D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_ENDING_ACCESS renderPassEndingAccessNoAccess{ D3D12_RENDER_PASS_ENDING_ACCESS_TYPE_NO_ACCESS, {} };
    D3D12_RENDER_PASS_DEPTH_STENCIL_DESC renderPassDepthStencilDesc{ dsvCPUDescriptorHandle, renderPassBeginningAccessNoAccess, renderPassBeginningAccessNoAccess, renderPassEndingAccessNoAccess, renderPassEndingAccessNoAccess };

    pIGCL4->BeginRenderPass(1, &renderPassRenderTargetDesc, &renderPassDepthStencilDesc, D3D12_RENDER_PASS_FLAG_NONE);
    // Record command list.
    pIGCL4->EndRenderPass();
    // Begin/End further render passes and then execute the command list(s).
}
```

Você define o primeiro campo da estrutura de [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) como o identificador do descritor de CPU correspondente a uma ou mais exibições de destino de renderização (RTVs). Da mesma forma, [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) contém o identificador do descritor de CPU correspondente a uma exibição de estêncil de profundidade (DSV). Os identificadores do descritor de CPU são os mesmos que você passaria para [**ID3D12GraphicsCommandList:: OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets). E, assim como com **OMSetRenderTargets**, os descritores de CPU são *encaixados* de seus respectivos heaps (descritores de CPU) no momento da chamada para **BeginRenderPass**.

O RTVs e DSV não são herdados para a passagem de renderização. Em vez disso, eles devem ser definidos. Nem os RTVs e DSV declarados em **BeginRenderPass** propagados para a lista de comandos. Em vez disso, eles estão em um estado indefinido após a passagem de renderização.

### <a name="render-passes-and-workloads"></a>Passes de renderização e cargas de trabalho

Você não pode aninhar passagens de renderização e não pode fazer com que uma passagem de renderização se aprofunde mais de uma lista de comandos (elas devem começar e terminar durante a gravação em uma única lista de comandos). As otimizações projetadas para habilitar a geração de transmissão multithread eficiente de passagens de renderização são discutidas na seção [ processar sinalizadores de passagem](#render-pass-flags), abaixo.

Uma gravação que você faz de dentro de uma passagem de renderização não é *válida* para você ler até uma passagem de renderização subsequente. Isso impede alguns tipos de barreiras de dentro da passagem de renderização &mdash; , por exemplo, a barreira de **RENDER_TARGET** para **SHADER_RESOURCE** no destino de renderização atualmente associado. Para obter mais informações, consulte a seção [renderizar passagens e barreiras de recursos](#render-passes-and-resource-barriers), abaixo.

A única exceção para a restrição Write-Read que acabamos de mencionar envolve as leituras implícitas que ocorrem como parte do teste de profundidade e da mesclagem de destino de renderização.
Portanto, essas APIs não são permitidas dentro de uma passagem de renderização (o tempo de execução principal remove a lista de comandos se qualquer uma delas for chamada durante a gravação).

- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint)
- [**ID3D12GraphicsCommandList1::AtomicCopyBufferUINT64**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-atomiccopybufferuint64)
- [**ID3D12GraphicsCommandList4::BeginRenderPass**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-beginrenderpass)
- [**ID3D12GraphicsCommandList::ClearDepthStencilView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-cleardepthstencilview)
- [**ID3D12GraphicsCommandList::ClearRenderTargetView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearrendertargetview)
- [**ID3D12GraphicsCommandList:: Clearstate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewFloat**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
- [**ID3D12GraphicsCommandList::ClearUnorderedAccessViewUint**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
- [**ID3D12GraphicsCommandList::CopyBufferRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
- [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
- [**ID3D12GraphicsCommandList::CopyTextureRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
- [**ID3D12GraphicsCommandList::CopyTiles**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
- [**ID3D12GraphicsCommandList::D iscardResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
- [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
- [**ID3D12GraphicsCommandList::OMSetRenderTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)
- [**ID3D12GraphicsCommandList::ResolveQueryData**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata)
- [**ID3D12GraphicsCommandList::ResolveSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvesubresource)
- [**ID3D12GraphicsCommandList1::ResolveSubresourceRegion**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-resolvesubresourceregion)
- [**ID3D12GraphicsCommandList3::SetProtectedResourceSession**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist3-setprotectedresourcesession)

### <a name="render-passes-and-resource-barriers"></a>Passagens de renderização e barreiras de recursos

Você não pode ler ou consumir uma gravação que ocorreu na mesma passagem de renderização. Determinadas barreiras não estão em conformidade com essa restrição, por exemplo, de **D3D12_RESOURCE_STATE_RENDER_TARGET** para **\* _SHADER_RESOURCE** no destino de renderização atualmente associado (e a camada de depuração apresentará um erro para esse efeito). Porém, essa mesma barreira em um destino de renderização que foi gravado *fora* da passagem de renderização atual é compatível, pois as gravações serão concluídas antes da fase de renderização atual iniciando.
Você pode se beneficiar do conhecimento de determinadas otimizações que um driver de vídeo pode fazer nesse sentido. Devido a uma carga de trabalho compatível, um driver de vídeo pode mover as barreiras encontradas em sua passagem de renderização para o início da passagem de renderização. Lá, eles podem ser agrupados (e não interferem em nenhuma operação de divisão/compartimentalização). Essa é uma otimização válida desde que todas as suas gravações tenham sido concluídas antes do início da fase de renderização atual.

Veja um exemplo de otimização de driver mais completo, que pressupõe que você tenha um mecanismo de renderização que tenha um design de associação de recursos de estilo anterior ao Direct3D de 12 estilos &mdash; fazendo barreiras *sob demanda* com base em como os recursos são associados. Ao gravar em um modo de exibição de acesso não ordenado (UAV) em direção ao final de um quadro (para ser consumido no quadro a seguir), o mecanismo pode acontecer em deixar o recurso no estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** na conclusão do quadro. No quadro a seguir, quando o mecanismo vai para associar o recurso como um modo de exibição de recurso do sombreador (SRV), ele descobrirá que o recurso não está no estado correto e emitirá uma barreira de **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** para **D3D12_RESOURCE_STATE_PIXEL_SHADER_RESOURCE**. Se essa barreira ocorrer dentro da passagem de renderização, o driver de vídeo será justificado Considerando que todas as gravações já ocorreram *fora* dessa passagem de renderização atual e, consequentemente, (e aqui está o local em que a otimização entra), o driver de vídeo poderá *mover* a barreira para o início da passagem de renderização. Novamente, isso é válido, desde que seu código esteja em conformidade com a restrição Write-Read descrita nesta seção e o último.


Esses são exemplos de barreiras em conformidade.
- **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** **D3D12_RESOURCE_STATE_INDIRECT_ARGUMENT**.
- **D3D12_RESOURCE_STATE_COPY_DEST** **\* _SHADER_RESOURCE**.

E esses são exemplos de barreiras não conformadas.

- **D3D12_RESOURCE_STATE_RENDER_TARGET** a qualquer estado de leitura no RTVs/DSVs associado no momento.
- **D3D12_RESOURCE_STATE_DEPTH_WRITE** a qualquer estado de leitura no RTVs/DSVs associado no momento.
- Qualquer barreira de alias.
- Barreiras de UAV (exibição de acesso não ordenado). 

### <a name="resource-access-declaration"></a>Declaração de acesso a recursos

No momento do **BeginRenderPass** , além de declarar todos os recursos que estão servindo como RTVs e/ou DSV dentro desse passo, você também deve especificar suas características de *acesso* inicial e final. Como você pode ver no exemplo de código da seção [declare suas associações de saída](#declare-your-output-bindings) acima, faça isso com as estruturas [**D3D12_RENDER_PASS_RENDER_TARGET_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_render_target_desc) e [**D3D12_RENDER_PASS_DEPTH_STENCIL_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_depth_stencil_desc) .

Para obter mais detalhes, consulte as estruturas [**D3D12_RENDER_PASS_BEGINNING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_beginning_access) e [**D3D12_RENDER_PASS_ENDING_ACCESS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_render_pass_ending_access) e as enumerações [**D3D12_RENDER_PASS_BEGINNING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_beginning_access_type) e [**D3D12_RENDER_PASS_ENDING_ACCESS_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_ending_access_type) .

### <a name="render-pass-flags"></a>Renderizar sinalizadores de passagem

O último parâmetro passado para **BeginRenderPass** é um sinalizador de passagem de renderização (um valor da [**enumeração D3D12_RENDER_PASS_FLAGS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_render_pass_flags) renderização).

```cppwinrt
enum D3D12_RENDER_PASS_FLAGS
{
    D3D12_RENDER_PASS_FLAG_NONE = 0,
    D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES = 0x1,
    D3D12_RENDER_PASS_FLAG_SUSPENDING_PASS = 0x2,
    D3D12_RENDER_PASS_FLAG_RESUMING_PASS = 0x4
};
```

#### <a name="uav-writes-within-a-render-pass"></a>Gravações UAV em uma passagem de renderização

As gravações UAV (exibição de acesso não organizado) são permitidas em uma passagem de renderização, mas você deve indicar especificamente que você emifique gravações UAV dentro da passagem de renderização especificando **D3D12_RENDER_PASS_FLAG_ALLOW_UAV_WRITES**, para que o driver de exibição possa optar por não lado a lado, se necessário.

Os acessos UAV devem seguir a restrição de leitura de gravação descrita acima (as gravações em uma passagem de renderização não são válidas para leitura até uma passagem de renderização subsequente). As barreiras de UAV não são permitidas em uma passagem de renderização.

As vinculações UAV (por meio de tabelas raiz ou descritores raiz) são herdadas em passagens de renderização e são propagadas para fora de passagens de renderização.

#### <a name="suspending-passes-and-resuming-passes"></a>Suspending-passes e resumindo-passes

Você pode indicar uma passagem de renderização inteira como sendo um suspending-pass e/ou uma passagem de retomada. Um par suspending-followed-by-a-resumindo deve ter sinalizadores de exibição/acesso idênticos entre as passagens e pode não ter nenhuma operação de GPU intermediária (por exemplo, desenho, expedições, descartes, limpas, cópias, update-tile-mappings, write-buffer-immediates, consultas, resolveções de consulta) entre a passagem de renderização suspensa e a passagem de renderização de retomada.

O caso de uso pretendido é a renderização multi-threaded, em que, digamos, quatro listas de comandos (cada uma com suas próprias passagens de renderização) pode ter como destino os mesmos destinos de renderização. Quando as passagens de renderização são suspensas/retomadas em listas de comandos, as listas de comandos devem ser executadas na mesma chamada para [**ID3D12CommandQueue::ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Uma passagem de renderização pode ser retomada e suspensa. No exemplo de vários threads que acabou de ser determinado, as listas de comandos 2 e 3 seriam retomadas de 1 e 2, respectivamente. E, ao mesmo tempo, 2 e 3 seriam suspensos para 3 e 4, respectivamente.

## <a name="query-for-render-passes-feature-support"></a>Consulta de suporte a recursos de aprovações de renderização

Você pode chamar [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) para consultar a extensão até a qual um driver de dispositivo e/ou o hardware dá suporte eficiente a passagens de renderização.

```cppwinrt
D3D12_RENDER_PASS_TIER get_render_passes_tier(::ID3D12Device * pIDevice)
{
    D3D12_FEATURE_DATA_D3D12_OPTIONS5 featureSupport{};
    winrt::check_hresult(
        pIDevice->CheckFeatureSupport(D3D12_FEATURE_D3D12_OPTIONS5, &featureSupport, sizeof(featureSupport))
    );
    return featureSupport.RenderPassesTier;
}
...
    D3D12_RENDER_PASS_TIER renderPassesTier{ get_render_passes_tier(pIDevice) };
```

Devido à lógica de mapeamento do runtime, renderizar passa sempre função. Mas, dependendo do suporte ao recurso, eles nem sempre fornecerão um benefício. Você pode usar código semelhante ao exemplo de código acima para determinar se/quando vale a pena emitir comandos conforme a renderização passa e quando ele definitivamente não é um benefício (ou seja, quando o runtime está apenas mapeando para a superfície de API existente). Executar essa verificação é particularmente importante se você estiver usando [D3D11On12](/windows/desktop/direct3d12/direct3d-11-on-12)).

Para uma descrição das três camadas de suporte, consulte a [**enumeração D3D12_RENDER_PASS_TIER**](/windows/win32/api/d3d12/ne-d3d12-d3d12_render_pass_tier) dados.
