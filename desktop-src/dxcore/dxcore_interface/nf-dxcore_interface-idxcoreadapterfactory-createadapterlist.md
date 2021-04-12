---
title: IDXCoreAdapterFactory::CreateAdapterList
description: Gera uma lista de objetos de adaptador que representam o estado atual do adaptador do sistema e atendendo aos critérios especificados.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 0a35d4dd9a481880d66988b6ade079534d1297c1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454222"
---
# <a name="idxcoreadapterfactorycreateadapterlist-method"></a><span data-ttu-id="1f605-103">Método IDXCoreAdapterFactory:: createadapterlist</span><span class="sxs-lookup"><span data-stu-id="1f605-103">IDXCoreAdapterFactory::CreateAdapterList method</span></span>

<span data-ttu-id="1f605-104">Gera uma lista de objetos de adaptador que representam o estado atual do adaptador do sistema e atendendo aos critérios especificados.</span><span class="sxs-lookup"><span data-stu-id="1f605-104">Generates a list of adapter objects representing the current adapter state of the system, and meeting the criteria specified.</span></span> <span data-ttu-id="1f605-105">Para obter diretrizes de programação e exemplos de código, consulte [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md).</span><span class="sxs-lookup"><span data-stu-id="1f605-105">For programming guidance, and code examples, see [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1f605-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f605-106">Syntax</span></span>

```cpp
virtual HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  REFIID riid,
  _COM_Outptr_ void **ppvAdapterList) = 0;

template<class T>
HRESULT STDMETHODCALLTYPE CreateAdapterList(
  uint32_t numAttributes,
  _In_reads_(numAttributes) const GUID *filterAttributes,
  _COM_Outptr_ T **ppvAdapterList);
```

## <a name="parameters"></a><span data-ttu-id="1f605-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1f605-107">Parameters</span></span>

### <a name="numattributes"></a><span data-ttu-id="1f605-108">numAttributes</span><span class="sxs-lookup"><span data-stu-id="1f605-108">numAttributes</span></span>

<span data-ttu-id="1f605-109">Tipo: **uint32_t**</span><span class="sxs-lookup"><span data-stu-id="1f605-109">Type: **uint32_t**</span></span>

<span data-ttu-id="1f605-110">O número de elementos na matriz apontados pelo argumento *FilterAttributes* .</span><span class="sxs-lookup"><span data-stu-id="1f605-110">The number of elements in the array pointed to by the *filterAttributes* argument.</span></span>

### <a name="filterattributes-in"></a><span data-ttu-id="1f605-111">filterAttributes [in]</span><span class="sxs-lookup"><span data-stu-id="1f605-111">filterAttributes [in]</span></span>

<span data-ttu-id="1f605-112">Tipo: **GUID \* const**</span><span class="sxs-lookup"><span data-stu-id="1f605-112">Type: **const GUID\***</span></span>

<span data-ttu-id="1f605-113">Um ponteiro para uma matriz de GUIDs de atributo de adaptador.</span><span class="sxs-lookup"><span data-stu-id="1f605-113">A pointer to an array of adapter attribute GUIDs.</span></span> <span data-ttu-id="1f605-114">Para obter uma lista de GUIDs de atributo, consulte [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md).</span><span class="sxs-lookup"><span data-stu-id="1f605-114">For a list of attribute GUIDs, see [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md).</span></span> <span data-ttu-id="1f605-115">Pelo menos um GUID deve ser fornecido.</span><span class="sxs-lookup"><span data-stu-id="1f605-115">At least one GUID must be provided.</span></span> <span data-ttu-id="1f605-116">Caso mais de um GUID seja fornecido na matriz, somente os adaptadores que atendem a *todos* os atributos solicitados serão incluídos na lista retornada.</span><span class="sxs-lookup"><span data-stu-id="1f605-116">In the case that more than one GUID is provided in the array, only adapters that meet *all* of the requested attributes will be included in the returned list.</span></span>

### <a name="riid"></a><span data-ttu-id="1f605-117">riid</span><span class="sxs-lookup"><span data-stu-id="1f605-117">riid</span></span>

<span data-ttu-id="1f605-118">Tipo: **REFIID**</span><span class="sxs-lookup"><span data-stu-id="1f605-118">Type: **REFIID**</span></span>

<span data-ttu-id="1f605-119">Uma referência ao GUID (identificador global exclusivo) da interface que você deseja retornar em *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="1f605-119">A reference to the globally unique identifier (GUID) of the interface that you wish to be returned in *ppvAdapterList*.</span></span> <span data-ttu-id="1f605-120">Espera-se que seja o identificador de interface (IID) de [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span><span class="sxs-lookup"><span data-stu-id="1f605-120">This is expected to be the interface identifier (IID) of [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md).</span></span>

### <a name="ppvadapterlist-out"></a><span data-ttu-id="1f605-121">ppvAdapterList [saída]</span><span class="sxs-lookup"><span data-stu-id="1f605-121">ppvAdapterList [out]</span></span>

<span data-ttu-id="1f605-122">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="1f605-122">Type: **void\*\***</span></span>

<span data-ttu-id="1f605-123">O endereço de um ponteiro para uma interface com o IID especificado no parâmetro *riid* .</span><span class="sxs-lookup"><span data-stu-id="1f605-123">The address of a pointer to an interface with the IID specified in the *riid* parameter.</span></span> <span data-ttu-id="1f605-124">Após o retorno bem-sucedido, *\* ppvAdapterList* (o endereço desreferenciado) contém um ponteiro para a lista de adaptadores criada.</span><span class="sxs-lookup"><span data-stu-id="1f605-124">Upon successful return, *\*ppvAdapterList* (the dereferenced address) contains a pointer to the adapter list created.</span></span>

## <a name="returns"></a><span data-ttu-id="1f605-125">Retornos</span><span class="sxs-lookup"><span data-stu-id="1f605-125">Returns</span></span>

<span data-ttu-id="1f605-126">Tipo: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="1f605-126">Type: **[HRESULT](../../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="1f605-127">Se a função for realizada com sucesso, ela retornará **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="1f605-127">If the function succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1f605-128">Caso contrário, ele retorna um [código de erro](../../com/com-error-codes-10.md) [**HRESULT**](../../com/structure-of-com-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="1f605-128">Otherwise, it returns an [**HRESULT**](../../com/structure-of-com-error-codes.md) [error code](../../com/com-error-codes-10.md).</span></span>

|<span data-ttu-id="1f605-129">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1f605-129">Return value</span></span>|<span data-ttu-id="1f605-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="1f605-130">Description</span></span>|
|-|-|
|<span data-ttu-id="1f605-131">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="1f605-131">E_INVALIDARG</span></span>|<span data-ttu-id="1f605-132">`nullptr` foi fornecido para *FilterAttributes*, ou o 0 foi fornecido para *numAttributes*.</span><span class="sxs-lookup"><span data-stu-id="1f605-132">`nullptr` was provided for *filterAttributes*, or 0 was provided for *numAttributes*.</span></span>|
|<span data-ttu-id="1f605-133">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="1f605-133">E_NOINTERFACE</span></span>|<span data-ttu-id="1f605-134">Um valor inválido foi fornecido para *riid*.</span><span class="sxs-lookup"><span data-stu-id="1f605-134">An invalid value was provided for *riid*.</span></span>|
|<span data-ttu-id="1f605-135">E_POINTER</span><span class="sxs-lookup"><span data-stu-id="1f605-135">E_POINTER</span></span>|<span data-ttu-id="1f605-136">`nullptr` foi fornecido para *ppvAdapterList*.</span><span class="sxs-lookup"><span data-stu-id="1f605-136">`nullptr` was provided for *ppvAdapterList*.</span></span>|

## <a name="remarks"></a><span data-ttu-id="1f605-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f605-137">Remarks</span></span>

<span data-ttu-id="1f605-138">Mesmo que nenhum adaptador seja encontrado, desde que os argumentos sejam válidos, **Createadapterlist** cria um objeto [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) válido e retorna **S_OK**.</span><span class="sxs-lookup"><span data-stu-id="1f605-138">Even if no adapters are found, as long as the arguments are valid, **CreateAdapterList** creates a valid [IDXCoreAdapterList](./nn-dxcore_interface-idxcoreadapterlist.md) object, and returns **S_OK**.</span></span> <span data-ttu-id="1f605-139">Depois de gerado, os adaptadores nesta lista específica não serão alterados.</span><span class="sxs-lookup"><span data-stu-id="1f605-139">Once generated, the adapters in this specific list won't change.</span></span> <span data-ttu-id="1f605-140">Mas a lista será considerada obsoleta se um dos adaptadores se tornar inválidos posteriormente, ou se um novo adaptador chegar e atender aos critérios de filtro fornecidos.</span><span class="sxs-lookup"><span data-stu-id="1f605-140">But the list will be considered stale if one of the adapters later becomes invalid, or if a new adapter arrives that meets the provided filter criteria.</span></span> <span data-ttu-id="1f605-141">A lista retornada por **Createadapterlist** não é ordenada de nenhuma forma específica, mas a ordenação de uma lista é consistente em várias chamadas e até mesmo entre as reinicializações do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="1f605-141">The list returned by **CreateAdapterList** is not ordered in any particular way, but the ordering of a list is consistent across multiple calls, and even across operating system restarts.</span></span> <span data-ttu-id="1f605-142">A ordenação pode ser alterada nas alterações de configuração do sistema, incluindo a adição ou remoção de um adaptador ou uma atualização de driver em um adaptador existente.</span><span class="sxs-lookup"><span data-stu-id="1f605-142">The ordering may change upon system configuration changes, including the addition or removal of an adapter, or a driver update on an existing adapter.</span></span> <span data-ttu-id="1f605-143">Você pode se registrar para essas alterações com [IDXCoreAdapterFactory:: RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) usando o tipo de notificação **DXCoreNotificationType. AdapterListStale**.</span><span class="sxs-lookup"><span data-stu-id="1f605-143">You can register for these changes with [IDXCoreAdapterFactory::RegisterEventNotification](./nf-dxcore_interface-idxcoreadapterfactory-registereventnotification.md) using the notification type **DXCoreNotificationType.AdapterListStale**.</span></span>

## <a name="see-also"></a><span data-ttu-id="1f605-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="1f605-144">See also</span></span>

<span data-ttu-id="1f605-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [referência de DXCore](../dxcore-reference.md), [GUIDs de atributo do adaptador DXCore](../dxcore-adapter-attribute-guids.md), [usando DXCore para enumerar adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="1f605-145">[IDXCoreAdapterFactory](./nn-dxcore_interface-idxcoreadapterfactory.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>