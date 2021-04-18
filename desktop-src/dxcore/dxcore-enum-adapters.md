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
# <a name="using-dxcore-to-enumerate-adapters"></a><span data-ttu-id="339cc-103">Usar DXCore para enumerar adaptadores</span><span class="sxs-lookup"><span data-stu-id="339cc-103">Using DXCore to enumerate adapters</span></span>

<span data-ttu-id="339cc-104">DXCore é uma API de enumeração de adaptador para dispositivos DirectX, de modo que algumas de suas instalações se sobrepõem com as de [dxgi](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-104">DXCore is an adapter enumeration API for DirectX devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span>

<span data-ttu-id="339cc-105">O DXCore permite a exposição de novos tipos de dispositivos ao modo de usuário, como MCDM (modelo de driver de computação da Microsoft), para uso com [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md)e [Windows Machine Learning](/windows/ai/windows-ml/).</span><span class="sxs-lookup"><span data-stu-id="339cc-105">DXCore enables the exposure of new device types to user mode, such as MCDM (Microsoft Compute Driver Model), for use with [Direct3D 12](../direct3d12/directx-12-programming-guide.md), [DirectML](../direct3d12/dml.md), and [Windows Machine Learning](/windows/ai/windows-ml/).</span></span> <span data-ttu-id="339cc-106">DXCore, ao contrário de DXGI, não fornece nenhuma informação sobre tecnologia ou propriedades relacionadas à exibição</span><span class="sxs-lookup"><span data-stu-id="339cc-106">DXCore, unlike DXGI, does not provide any information about display-related technology or properties</span></span>

<span data-ttu-id="339cc-107">Nas próximas seções, vamos dar uma olhada nos principais recursos do DXCore com alguns exemplos de código (escritos em [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span><span class="sxs-lookup"><span data-stu-id="339cc-107">In the next few sections, we'll take a look at the main features of DXCore with some code examples (written in [C++/WinRT](/windows/uwp/cpp-and-winrt-apis)).</span></span> <span data-ttu-id="339cc-108">Os exemplos de código mostrados abaixo são extraídos da listagem de código-fonte completo que você pode encontrar no tópico [mínimo do aplicativo DXCore](dxcore-source-code.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-108">The code examples shown below are extracted from the full source code listing that you can find in the topic [Minimal DXCore application](dxcore-source-code.md).</span></span>

## <a name="create-an-adapter-factory"></a><span data-ttu-id="339cc-109">Criar uma fábrica de adaptadores</span><span class="sxs-lookup"><span data-stu-id="339cc-109">Create an adapter factory</span></span>

<span data-ttu-id="339cc-110">Você começa a enumeração do adaptador DXCore criando um objeto de fábrica de adaptador, que é representado pela interface [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-110">You begin DXCore adapter enumeration by creating an adapter factory object, which is represented by the [**IDXCoreAdapterFactory**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterfactory.md) interface.</span></span> <span data-ttu-id="339cc-111">Para criar uma fábrica, inclua o `dxcore.h` arquivo de cabeçalho e chame a função gratuita [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-111">To create a factory, include the `dxcore.h` header file, and call the [**DXCoreCreateAdapterFactory**](./dxcore/nf-dxcore-dxcorecreateadapterfactory.md) free function.</span></span>

```cppwinrt
#include <dxcore.h>
...
winrt::com_ptr<IDXCoreAdapterFactory> adapterFactory;
winrt::check_hresult(::DXCoreCreateAdapterFactory(adapterFactory.put()));
```

## <a name="retrieve-an-adapter-list"></a><span data-ttu-id="339cc-112">Recuperar uma lista de adaptadores</span><span class="sxs-lookup"><span data-stu-id="339cc-112">Retrieve an adapter list</span></span>

<span data-ttu-id="339cc-113">Ao contrário de DXGI, uma fábrica de adaptadores DXCore criada recentemente não cria automaticamente um instantâneo do estado do adaptador do sistema.</span><span class="sxs-lookup"><span data-stu-id="339cc-113">Unlike with DXGI, a newly-created DXCore adapter factory doesn't automatically create a snapshot of the adapter state of the system.</span></span> <span data-ttu-id="339cc-114">Em vez disso, o DXCore cria esse instantâneo quando você recupera explicitamente um objeto de lista de adaptadores, que é representado pela interface [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-114">Instead, DXCore creates that snapshot when you explicitly retrieve an adapter list object, which is represented by the [**IDXCoreAdapterList**](./dxcore_interface/nn-dxcore_interface-idxcoreadapterlist.md) interface.</span></span>

```cppwinrt
winrt::com_ptr<IDXCoreAdapterList> d3D12CoreComputeAdapters;
GUID attributes[]{ DXCORE_ADAPTER_ATTRIBUTE_D3D12_CORE_COMPUTE };
winrt::check_hresult(
    adapterFactory->CreateAdapterList(_countof(attributes),
        attributes,
        d3D12CoreComputeAdapters.put()));
```

## <a name="select-an-appropriate-adapter-from-the-list"></a><span data-ttu-id="339cc-115">Selecione um adaptador apropriado na lista</span><span class="sxs-lookup"><span data-stu-id="339cc-115">Select an appropriate adapter from the list</span></span>

<span data-ttu-id="339cc-116">Esta seção demonstra como, dado um objeto de lista de adaptadores, você pode encontrar o primeiro adaptador de hardware na lista.</span><span class="sxs-lookup"><span data-stu-id="339cc-116">This section demonstrates how, given an adapter list object, you could find the first hardware adapter in the list.</span></span>

<span data-ttu-id="339cc-117">O método [**IDXCoreAdapterList:: GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) informa o número de elementos na lista e [**IDXCoreAdapterList:: getadapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) recupera um adaptador específico por índice.</span><span class="sxs-lookup"><span data-stu-id="339cc-117">The [**IDXCoreAdapterList::GetAdapterCount**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadaptercount.md) method tells you the number of elements in the list, and [**IDXCoreAdapterList::GetAdapter**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-getadapter.md) retrieves a specific adapter by index.</span></span>

<span data-ttu-id="339cc-118">Em seguida, você pode consultar as propriedades desse adaptador seguindo estas etapas.</span><span class="sxs-lookup"><span data-stu-id="339cc-118">You can then query the properties of that adapter, by following these steps.</span></span>

- <span data-ttu-id="339cc-119">Primeiro, para confirmar que é válido recuperar o valor de uma determinada propriedade para esse adaptador nesta versão do sistema operacional, você chama [**IDXCoreAdapter:: IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-119">First, to confirm that it's valid to retrieve the value of a given property for this adapter on this operating system version, you call [**IDXCoreAdapter::IsPropertySupported**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-ispropertysupported.md).</span></span> <span data-ttu-id="339cc-120">Passe um valor da enumeração [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) para identificar a propriedade que você está consultando.</span><span class="sxs-lookup"><span data-stu-id="339cc-120">Pass a value of the [**DXCoreAdapterProperty**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) enumeration to identify which property you're querying about.</span></span>
- <span data-ttu-id="339cc-121">Opcionalmente, confirme o tamanho do valor da propriedade com uma chamada para [**IDXCoreAdapter:: GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-121">Optionally confirm the size of the property value with a call to [**IDXCoreAdapter::GetPropertySize**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getpropertysize.md).</span></span> <span data-ttu-id="339cc-122">Para uma propriedade como **DXCoreAdapterProperty:: isduro**, que é um booliano simples, essa etapa não é necessária.</span><span class="sxs-lookup"><span data-stu-id="339cc-122">For a property such as **DXCoreAdapterProperty::IsHardware**, which is a simple Boolean, this step isn't necessary.</span></span>
- <span data-ttu-id="339cc-123">E, por fim, recupere o valor da propriedade chamando [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-123">And, finally, retrieve the property's value by calling [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md).</span></span>

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

## <a name="select-the-preferred-adapter-by-sorting-an-adapter-list"></a><span data-ttu-id="339cc-124">Selecione o adaptador preferencial classificando uma lista de adaptadores</span><span class="sxs-lookup"><span data-stu-id="339cc-124">Select the preferred adapter by sorting an adapter list</span></span>

<span data-ttu-id="339cc-125">Você pode classificar uma lista de adaptadores DXCore chamando o método [IDXCoreAdapterList:: Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-125">You can sort a DXCore adapter list by calling the [IDXCoreAdapterList::Sort](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-sort.md) method.</span></span>

<span data-ttu-id="339cc-126">A enumeração [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) define os valores que representam os critérios de classificação.</span><span class="sxs-lookup"><span data-stu-id="339cc-126">The [DXCoreAdapterPreference](./dxcore_interface/ne-dxcore_interface-dxcoreadapterpreference.md) enumeration defines values that representing sort criteria.</span></span> <span data-ttu-id="339cc-127">Passe uma matriz desses valores para **classificar** e, em seguida, leia o primeiro adaptador na lista classificada resultante.</span><span class="sxs-lookup"><span data-stu-id="339cc-127">Pass an array of those values to **Sort**, and then read off the first adapter in the resulting sorted list.</span></span>

<span data-ttu-id="339cc-128">Para determinar se um tipo de classificação será compreendido por **classificação**, primeiro chame [IDXCoreAdapterList:: IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-128">To determine whether a sort type is going to be understood by **Sort**, first call [IDXCoreAdapterList::IsAdapterPreferenceSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isadapterpreferencesupported.md).</span></span>

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

## <a name="query-and-set-adapter-state-properties"></a><span data-ttu-id="339cc-129">Consultar e definir estado do adaptador (Propriedades)</span><span class="sxs-lookup"><span data-stu-id="339cc-129">Query and set adapter state (properties)</span></span>

<span data-ttu-id="339cc-130">Você pode recuperar e definir o estado de um item de estado especificado de um adaptador chamando os métodos [**IDXCoreAdapter:: QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) e [**IDXCoreAdapter:: SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-130">You can retrieve and set the state of a specified state item of an adapter by calling the [**IDXCoreAdapter::QueryState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-querystate.md) and [**IDXCoreAdapter::SetState**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-setstate.md) methods.</span></span>

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

<span data-ttu-id="339cc-131">Na prática, antes de chamar **QueryState** e **SetState**, você deve chamar [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) para confirmar que a consulta do tipo de estado está disponível para esse adaptador e sistema operacional (SO).</span><span class="sxs-lookup"><span data-stu-id="339cc-131">In practice, before calling **QueryState** and **SetState**, you should call [IsQueryStateSupported](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-isquerystatesupported.md) to confirm that querying the state kind is available for this adapter and operating system (OS).</span></span>

## <a name="adapter-list-freshness"></a><span data-ttu-id="339cc-132">Atualização da lista de adaptadores</span><span class="sxs-lookup"><span data-stu-id="339cc-132">Adapter list freshness</span></span>

<span data-ttu-id="339cc-133">Se uma lista de adaptadores se tornar obsoleta devido à alteração das condições do sistema, ela será marcada como tal.</span><span class="sxs-lookup"><span data-stu-id="339cc-133">Should an adapter list become stale due to changing system conditions, it will be marked as such.</span></span> <span data-ttu-id="339cc-134">Você pode determinar a atualização de uma lista de adaptadores sondando o método [**IDXCoreAdapterList:: isobsoleto**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-134">You can determine an adapter list's freshness by polling its [**IDXCoreAdapterList::IsStale**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterlist-isstale.md) method.</span></span>

<span data-ttu-id="339cc-135">No entanto, de modo mais conveniente, você pode assinar notificações para condições como a desatualização.</span><span class="sxs-lookup"><span data-stu-id="339cc-135">More conveniently, though, you can subscribe to notifications for conditions such as staleness.</span></span> <span data-ttu-id="339cc-136">Para fazer isso, passe [**DXCoreNotificationType:: AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) para [**IDXCoreAdapterFactory:: RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md)e armazene com segurança o cookie retornado para uso posterior.</span><span class="sxs-lookup"><span data-stu-id="339cc-136">To do that, pass [**DXCoreNotificationType::AdapterListStale**](./dxcore_interface/ne-dxcore_interface-dxcorenotificationtype.md) to [**IDXCoreAdapterFactory::RegisterEventNotification**](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md), and safely store the returned cookie for use later.</span></span>

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

<span data-ttu-id="339cc-137">Em seguida, você pode gerar um objeto de lista de adaptadores novo e atual a partir do objeto de fábrica que você já tem.</span><span class="sxs-lookup"><span data-stu-id="339cc-137">You can then generate a new, current, adapter list object from the factory object that you already have.</span></span> <span data-ttu-id="339cc-138">Lidar com essas condições é essencial para a sua capacidade de responder diretamente a eventos, como a chegada e remoção de adaptadores (seja ela uma GPU ou um adaptador de computação especializado), e para alternar adequadamente as cargas de trabalho em resposta.</span><span class="sxs-lookup"><span data-stu-id="339cc-138">Handling these conditions is critical to your ability to seamlessly respond to events such as adapter arrival and removal (whether that be a GPU, or a specialized compute adapter), and to appropriately shift workloads in response.</span></span>

<span data-ttu-id="339cc-139">Antes de destruir o objeto de lista de adaptadores, você deve usar o valor de cookie para cancelar o registro desse objeto de notificações chamando [IDXCoreAdapterFactory:: UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span><span class="sxs-lookup"><span data-stu-id="339cc-139">Before you destroy the adapter list object, you must use the cookie value to unregister that object from notifications by calling [IDXCoreAdapterFactory::UnregisterEventNotification](./dxcore_interface/nf-dxcore_interface-idxcoreadapterfactory-unregistereventnotification.md).</span></span> <span data-ttu-id="339cc-140">Se você não cancelar o registro, uma exceção fatal será gerada quando a situação for detectada.</span><span class="sxs-lookup"><span data-stu-id="339cc-140">If you don't unregister, then a fatal exception is raised when the situation is detected.</span></span>

```cppwinrt
HRESULT hr = factory->UnregisterEventNotification(m_eventCookie);
```

## <a name="display-information"></a><span data-ttu-id="339cc-141">Exibir informações</span><span class="sxs-lookup"><span data-stu-id="339cc-141">Display information</span></span>

> [!NOTE]
> <span data-ttu-id="339cc-142">O DXCore não fornece nenhuma informação de exibição.</span><span class="sxs-lookup"><span data-stu-id="339cc-142">DXCore doesn't itself provide any display information.</span></span> <span data-ttu-id="339cc-143">Quando necessário, você deve usar a classe Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) para recuperar essas informações.</span><span class="sxs-lookup"><span data-stu-id="339cc-143">Where necessary, you should use the Windows Runtime [**DisplayMonitor**](/uwp/api/windows.devices.display.displaymonitor) class to retrieve this information.</span></span> <span data-ttu-id="339cc-144">O [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) de um adaptador fornece um identificador comum que você pode usar para mapear um adaptador DXCore para informações de [**DisplayMonitor. DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) .</span><span class="sxs-lookup"><span data-stu-id="339cc-144">An adapter's [**LUID**](/windows/win32/api/winnt/ns-winnt-luid) provides a common identifier that you can use to map a DXCore adapter to [**DisplayMonitor.DisplayAdapterId**](/uwp/api/windows.devices.display.displaymonitor.displayadapterid) information.</span></span> <span data-ttu-id="339cc-145">Para obter o LUID de um adaptador, passe [**DXCoreAdapterProperty:: InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) para o método [**IDXCoreAdapter:: GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="339cc-145">To obtain an adapter's LUID, pass [**DXCoreAdapterProperty::InstanceLuid**](./dxcore_interface/ne-dxcore_interface-dxcoreadapterproperty.md) to the [**IDXCoreAdapter::GetProperty**](./dxcore_interface/nf-dxcore_interface-idxcoreadapter-getproperty.md) method.</span></span>

## <a name="see-also"></a><span data-ttu-id="339cc-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="339cc-146">See also</span></span>

* [<span data-ttu-id="339cc-147">Aplicativo DXCore mínimo</span><span class="sxs-lookup"><span data-stu-id="339cc-147">Minimal DXCore application</span></span>](dxcore-source-code.md)
* [<span data-ttu-id="339cc-148">Referência de DXCore</span><span class="sxs-lookup"><span data-stu-id="339cc-148">DXCore Reference</span></span>](./dxcore-reference.md)
* [<span data-ttu-id="339cc-149">Gráficos do Direct3D 12</span><span class="sxs-lookup"><span data-stu-id="339cc-149">Direct3D 12 graphics</span></span>](../direct3d12/direct3d-12-graphics.md)