---
title: Usar DXCore para enumerar adaptadores
description: Uma visão dos principais recursos do DXCore com alguns exemplos de código, bem como uma listagem completa de código-fonte de um aplicativo DXCore mínimo.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: f1c21971f2daea69de1f317d1db8eceb9ec00118
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105814603"
---
# <a name="using-dxcore-to-enumerate-adapters"></a>Usar DXCore para enumerar adaptadores

DXCore é uma API de enumeração de adaptador para dispositivos DirectX, de modo que algumas de suas instalações se sobrepõem com as de [dxgi](../direct3ddxgi/dx-graphics-dxgi.md).

O DXCore permite a exposição de novos tipos de dispositivos ao modo de usuário, como MCDM (modelo de driver de computação da Microsoft), para uso com [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)e [Windows Machine Learning](/windows/ai/windows-ml/). DXCore, ao contrário de DXGI, não fornece nenhuma informação sobre tecnologia ou propriedades relacionadas à exibição

Nas próximas seções, vamos dar uma olhada nos principais recursos do DXCore com alguns exemplos de código (escritos em [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)). Os exemplos de código mostrados abaixo são extraídos da listagem de código-fonte completo que você pode encontrar no tópico [mínimo do aplicativo DXCore](dxcore-source-code.md).

## <a name="create-an-adapter-factory"></a>Criar uma fábrica de adaptadores

Você começa a enumeração do adaptador DXCore criando um objeto de fábrica de adaptador, que é representado pela interface [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) . Para criar uma fábrica, inclua o `dxcore.h` arquivo de cabeçalho e chame a função gratuita [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a>Recuperar uma lista de adaptadores

Ao contrário de DXGI, uma fábrica de adaptadores DXCore criada recentemente não cria automaticamente um instantâneo do estado do adaptador do sistema. Em vez disso, o DXCore cria esse instantâneo quando você recupera explicitamente um objeto de lista de adaptadores, que é representado pela interface [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a>Selecione um adaptador apropriado na lista

Esta seção demonstra como, dado um objeto de lista de adaptadores, você pode encontrar o primeiro adaptador de hardware na lista.

O método [**IDXCoreAdapterList:: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) informa o número de elementos na lista e [**IDXCoreAdapterList:: getadapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera um adaptador específico por índice.

Em seguida, você pode consultar as propriedades desse adaptador seguindo estas etapas.

- Primeiro, para confirmar que é válido recuperar o valor de uma determinada propriedade para esse adaptador nesta versão do sistema operacional, você chama [**IDXCoreAdapter:: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md). Passe um valor da enumeração [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) para identificar a propriedade que você está consultando.
- Opcionalmente, confirme o tamanho do valor da propriedade com uma chamada para [**IDXCoreAdapter:: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md). Para uma propriedade como **DXCoreAdapterProperty:: isduro**, que é um booliano simples, essa etapa não é necessária.
- E, por fim, recupere o valor da propriedade chamando [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

const uint32_t count{ d3D12CoreComputeAdapters->GetAdapterCount() };

for (uint32_t i = 0; i < count; ++i)
{
    winrt::com_ptr<IDXCoreAdapter> candidateAdapter;
    winrt::check_hresult(
        d3D12CoreComputeAdapters->GetAdapter(i, candidateAdapter.put()));

    bool isHardware{ false };
    winrt::check_hresult(candidateAdapter->GetProperty(
        DXCoreAdapterProperty::IsHardware,
        &isHardware));

    if (isHardware)
    {
        // Choose the first hardware adapter, and stop looping.
        preferredAdapter = candidateAdapter;
        break;
    }

    // Otherwise, ensure that (as long as there are *any* adapters) we'll
    // at least choose one.
    if (!preferredAdapter)
    {
        preferredAdapter = candidateAdapter;
    }
}
```

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a>Selecione o adaptador preferencial classificando uma lista de adaptadores

Você pode classificar uma lista de adaptadores DXCore chamando o método [IDXCoreAdapterList:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .

A enumeração [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) define os valores que representam os critérios de classificação. Passe uma matriz desses valores para **classificar** e, em seguida, leia o primeiro adaptador na lista classificada resultante.

Para determinar se um tipo de classificação será compreendido por **classificação**, primeiro chame [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).

```cppwinrt
winrt::com_ptr<IDXCoreAdapter> TryFindHardwareHighPerformanceGraphicsAdapter()
{
    // You begin DXCore adapter enumeration by creating an adapter factory.
    winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
    winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));

    // From the factory, retrieve a list of all the Direct3D 12 Graphics adapters.
    winrt::com_ptr<IDXCoreAdapterList> d3D12GraphicsAdapters;
    GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_GRAPHICS };
    winrt::check_hresult(
        adapterFactory->CreateAdapterList(_countof(attributes),
            attributes,
            d3D12GraphicsAdapters.put()));

    DXCoreAdapterPreference sortPreferences[]{
        DXCoreAdapterPreference::Hardware, DXCoreAdapterPreference::HighPerformance };

    // Ask the OS to sort for the highest performance hardware adapter.
    winrt::check_hresult(d3D12GraphicsAdapters->Sort(_countof(sortPreferences), sortPreferences));

    winrt::com_ptr<IDXCoreAdapter> preferredAdapter;

    if (d3D12GraphicsAdapters->GetAdapterCount() > 0)
    {
        winrt::check_hresult(d3D12GraphicsAdapters->GetAdapter(0, preferredAdapter.put()));
    }

    return preferredAdapter;
}
```

## <a name="query-and-set-adapter-state-properties"></a>Consultar e definir estado do adaptador (Propriedades)

Você pode recuperar e definir o estado de um item de estado especificado de um adaptador chamando os métodos [**IDXCoreAdapter:: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) e [**IDXCoreAdapter:: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .

```cppwinrt
void SetDesiredMemoryReservation(winrt::com_ptr<IDXCoreAdapter> const& adapter, uint64_t reservation)
{
    DXCoreAdapterMemoryBudgetNodeSegmentGroup nodeSegmentGroup{};
    nodeSegmentGroup.nodeIndex = 0;
    nodeSegmentGroup.segmentGroup = DXCoreSegmentGroup::Local;

    DXCoreAdapterMemoryBudget memoryBudget{};
    winrt::check_hresult(adapter->QueryState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &memoryBudget));

    // Clamp the reservation to what's available.
    reservation = std::min<uint64_t>(reservation, memoryBudget.availableForReservation);

    winrt::check_hresult(adapter->SetState(
        DXCoreAdapterState::AdapterMemoryBudget,
        &nodeSegmentGroup,
        &reservation));
}
```

Na prática, antes de chamar **QueryState** e **SetState**, você deve chamar [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e sistema operacional (SO).

## <a name="adapter-list-freshness"></a>Atualização da lista de adaptadores

Se uma lista de adaptadores se tornar obsoleta devido à alteração das condições do sistema, ela será marcada como tal. Você pode determinar a atualização de uma lista de adaptadores sondando o método [**IDXCoreAdapterList:: isobsoleto**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .

No entanto, de modo mais conveniente, você pode assinar notificações para condições como a desatualização. Para fazer isso, passe [**DXCoreNotificationType:: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) para [**IDXCoreAdapterFactory:: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)e armazene com segurança o cookie retornado para uso posterior.

```cppwinrt
uint32_t m_eventCookie = 0;
...
winrt::check_hresult(factory->RegisterEventNotification(
    m_adapters.get(),
    DXCoreNotificationType::AdapterListStale,
    OnAdapterListStale,
    this,
    &m_eventCookie));
...
static void WINAPI OnAdapterListStale(
    DXCoreNotificationType notificationType,
    IUnknown* staleObject,
    void* context)
{
    ...
}
```

Em seguida, você pode gerar um objeto de lista de adaptadores novo e atual a partir do objeto de fábrica que você já tem. Lidar com essas condições é essencial para a sua capacidade de responder diretamente a eventos, como a chegada e remoção de adaptadores (seja ela uma GPU ou um adaptador de computação especializado), e para alternar adequadamente as cargas de trabalho em resposta.

Antes de destruir o objeto de lista de adaptadores, você deve usar o valor de cookie para cancelar o registro desse objeto de notificações chamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md). Se você não cancelar o registro, uma exceção fatal será gerada quando a situação for detectada.

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a>Exibir informações

> [!NOTE]
> O DXCore não fornece nenhuma informação de exibição. Quando necessário, você deve usar a classe Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) para recuperar essas informações. O [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) de um adaptador fornece um identificador comum que você pode usar para mapear um adaptador DXCore para informações de [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) . Para obter o LUID de um adaptador, passe [**DXCoreAdapterProperty:: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) para o método [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .

## <a name="see-also"></a>Confira também

* [Aplicativo DXCore mínimo](dxcore-source-code.md)
* [Referência de DXCore](./dxcore-reference.md)
* [Gráficos do Direct3D 12](../direct3d12/direct3d-12-graphics.md)