---
title: Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT (D3dx12. h)
description: Uma estrutura auxiliar de modelo usada para encapsular os pares de dados de tipo de subobjeto e subobjeto como um único objeto adequado para uma descrição de fluxo.
ms.assetid: 4C59D483-6ED8-49BD-B91B-2A912AFE2409
keywords:
- Estrutura de CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
topic_type:
- apiref
api_name:
- CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11353581dddc2bd0d438b955d1292b667fba39ad
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105793837"
---
# <a name="cd3dx12_pipeline_state_stream_subobject-structure"></a><span data-ttu-id="799da-104">\_Estrutura de \_ \_ subobjeto de fluxo do estado do pipeline CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="799da-104">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT structure</span></span>

<span data-ttu-id="799da-105">Uma estrutura auxiliar de modelo usada para encapsular os pares de dados de tipo de subobjeto e subobjeto como um único objeto adequado para uma descrição de fluxo.</span><span class="sxs-lookup"><span data-stu-id="799da-105">A templated helper structure used to encapsulate subobject type and subobject data pairs as a single object suitable for a stream description.</span></span>

## <a name="syntax"></a><span data-ttu-id="799da-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="799da-106">Syntax</span></span>


```C++
struct CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT {
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT;
                                          CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const &i);
  CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT operator=(InnerStructType const& i);
                                          operator InnerStructType() const;
};
```



## <a name="members"></a><span data-ttu-id="799da-107">Membros</span><span class="sxs-lookup"><span data-stu-id="799da-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="799da-108">**Subobjeto de fluxo do estado do \_ pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-108">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT**</span></span>
</dt> <dd>

<span data-ttu-id="799da-109">Cria uma nova instância, não inicializada, de um \_ subobjeto de fluxo de estado de pipeline CD3DX12 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="799da-109">Creates a new, uninitialized, instance of a CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT.</span></span>

</dd> <dt>

<span data-ttu-id="799da-110">**CD3DX12 \_ \_Subobjeto \_ \_ de fluxo do estado do pipeline (** InnerStructType \* \* const &i) \* \*</span><span class="sxs-lookup"><span data-stu-id="799da-110">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT(** InnerStructType\*\* const &i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="799da-111">Cria uma nova \_ \_ \_ \_ instância de modelo de subobjeto de fluxo de estado de pipeline do CD3DX12, inicializada com um tipo de subobjeto do tipo de subobjeto do [**estado do \_ pipeline \_ \_ \_ D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) e dados de subobjeto copiados de i.</span><span class="sxs-lookup"><span data-stu-id="799da-111">Creates a new CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT template instance, initialized with a subobject type of [**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type) and subobject data copied from *i*.</span></span> <span data-ttu-id="799da-112">Tanto o tipo de subobjeto quanto o tipo de dados de subobjeto são fornecidos como parâmetros de modelo, **Type** e **InnerStructType**, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="799da-112">Both the subobject type and subobject data type are given as template parameters, **Type** and **InnerStructType**, respectively.</span></span> <span data-ttu-id="799da-113">Para obter mais informações, consulte os comentários abaixo.</span><span class="sxs-lookup"><span data-stu-id="799da-113">For more information, see Remarks below.</span></span>

</dd> <dt>

<span data-ttu-id="799da-114">**Operator = (** InnerStructType \* \* const& i) \* \*</span><span class="sxs-lookup"><span data-stu-id="799da-114">**operator=(** InnerStructType\*\* const& i)\*\*</span></span>
</dt> <dd>

<span data-ttu-id="799da-115">Operador de atribuição de cópia.</span><span class="sxs-lookup"><span data-stu-id="799da-115">Copy-assignment operator.</span></span>

</dd> <dt>

<span data-ttu-id="799da-116">**constante **InnerStructType**() de operador**</span><span class="sxs-lookup"><span data-stu-id="799da-116">**operator **InnerStructType**() const**</span></span>
</dt> <dd>

<span data-ttu-id="799da-117">Conversão implícita para o tipo de dados de subobjeto fornecido pelo parâmetro de modelo **InnerStructType** .</span><span class="sxs-lookup"><span data-stu-id="799da-117">Implicit conversion to the subobject data type given by the **InnerStructType** template parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="799da-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="799da-118">Remarks</span></span>

<span data-ttu-id="799da-119">O \_ \_ subobjeto de fluxo do estado do pipeline CD3DX12 \_ \_ é um modelo definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="799da-119">CD3DX12\_PIPELINE\_STATE\_STREAM\_SUBOBJECT is a template defined as follows:</span></span>


```C++
template <typename InnerStructType, D3D12_PIPELINE_STATE_SUBOBJECT_TYPE Type, typename DefaultArg = InnerStructType>
class alignas(void*) CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT
{
private:
    D3D12_PIPELINE_STATE_SUBOBJECT_TYPE _Type;
    InnerStructType _Inner;
public:
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT() : _Type(Type), _Inner(DefaultArg()) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT(InnerStructType const& i) : _Type(Type), _Inner(i) {}
    CD3DX12_PIPELINE_STATE_STREAM_SUBOBJECT& operator=(InnerStructType const& i) { _Inner = i; return *this; }
    operator InnerStructType() const { return _Inner; }
};  
          
```



<span data-ttu-id="799da-120">O parâmetro de modelo **InnerStructType** especifica o tipo de dados de subobjeto; ou seja, os detalhes do subobjeto a serem codificados em um fluxo.</span><span class="sxs-lookup"><span data-stu-id="799da-120">The template parameter **InnerStructType** specifies the subobject data type; that is, the subobject details to be encoded into a stream.</span></span> <span data-ttu-id="799da-121">O **tipo** de parâmetro de modelo especifica o tipo de subobjeto; ou seja, o tipo da estrutura especificada pelo parâmetro de modelo **InnerStructType**.</span><span class="sxs-lookup"><span data-stu-id="799da-121">The template parameter **Type** specifies the subobject type; that is, the type of the structure specified by the template parameter **InnerStructType**.</span></span> <span data-ttu-id="799da-122">O parâmetro de modelo **defaultArg** especifica um valor opcional para o qual os dados de subobjeto serão inicializados quando uma instância da instanciação de modelo correspondente é construída por padrão; por exemplo, para construir por padrão um [**fluxo de estado do pipeline do CD3DX12, o \_ \_ \_ Stream \_ Blend \_ desc**](cd3dx12-pipeline-state-stream-blend-desc.md) foi inicializado com padrões de estado de mesclagem comuns usando o [**\_ padrão CD3DX12**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="799da-122">The template parameter **DefaultArg** specifies an optional value that the subobject data will be initialized to when an instance of the corresponding template instantiation is default-constructed; for example, to default-construct a [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md) initialized with common blend-state defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

<span data-ttu-id="799da-123">Aqui estão as instanciações de modelo que são definidas:</span><span class="sxs-lookup"><span data-stu-id="799da-123">Here are the template instantiations that are defined:</span></span>

-   [<span data-ttu-id="799da-124">**\_Sinalizadores de \_ fluxo de estado do pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-124">**CD3DX12\_PIPELINE\_STATE\_STREAM\_FLAGS**</span></span>](cd3dx12-pipeline-state-stream-flags.md)
-   [<span data-ttu-id="799da-125">**\_Máscara de \_ nó de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-125">**CD3DX12\_PIPELINE\_STATE\_STREAM\_NODE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-node-mask.md)
-   [<span data-ttu-id="799da-126">**\_ \_ \_ Assinatura raiz do fluxo de estado \_ do pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="799da-126">**CD3DX12\_PIPELINE\_STATE\_STREAM\_ROOT\_SIGNATURE**</span></span>](cd3dx12-pipeline-state-stream-root-signature.md)
-   [<span data-ttu-id="799da-127">**\_Layout de \_ entrada de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-127">**CD3DX12\_PIPELINE\_STATE\_STREAM\_INPUT\_LAYOUT**</span></span>](cd3dx12-pipeline-state-stream-input-layout.md)
-   [<span data-ttu-id="799da-128">**\_Valor de \_ \_ \_ \_ \_ recorte de faixa \_ do Stream IB do CD3DX12 pipeline**</span><span class="sxs-lookup"><span data-stu-id="799da-128">**CD3DX12\_PIPELINE\_STATE\_STREAM\_IB\_STRIP\_CUT\_VALUE**</span></span>](cd3dx12-pipeline-state-stream-ib-strip-cut-value.md)
-   [<span data-ttu-id="799da-129">**\_ \_ \_ Topologia primitiva de fluxo de estado \_ de pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="799da-129">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PRIMITIVE\_TOPOLOGY**</span></span>](cd3dx12-pipeline-state-stream-primitive-topology.md)
-   [<span data-ttu-id="799da-130">**\_Fluxo de estado do pipeline CD3DX12 \_ \_ \_ vs**</span><span class="sxs-lookup"><span data-stu-id="799da-130">**CD3DX12\_PIPELINE\_STATE\_STREAM\_VS**</span></span>](cd3dx12-pipeline-state-stream-vs.md)
-   [<span data-ttu-id="799da-131">**\_Fluxo de estado do pipeline CD3DX12 \_ \_ \_ GS**</span><span class="sxs-lookup"><span data-stu-id="799da-131">**CD3DX12\_PIPELINE\_STATE\_STREAM\_GS**</span></span>](cd3dx12-pipeline-state-stream-gs.md)
-   [<span data-ttu-id="799da-132">**\_Saída de \_ fluxo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-132">**CD3DX12\_PIPELINE\_STATE\_STREAM\_STREAM\_OUTPUT**</span></span>](cd3dx12-pipeline-state-stream-stream-output.md)
-   [<span data-ttu-id="799da-133">**Fluxo de estado de pipeline do CD3DX12 \_ \_ \_ \_ HS**</span><span class="sxs-lookup"><span data-stu-id="799da-133">**CD3DX12\_PIPELINE\_STATE\_STREAM\_HS**</span></span>](cd3dx12-pipeline-state-stream-hs.md)
-   [<span data-ttu-id="799da-134">**Fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ DS**</span><span class="sxs-lookup"><span data-stu-id="799da-134">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DS**</span></span>](cd3dx12-pipeline-state-stream-ds.md)
-   [<span data-ttu-id="799da-135">**\_PS de \_ fluxo de estado do pipeline CD3DX12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-135">**CD3DX12\_PIPELINE\_STATE\_STREAM\_PS**</span></span>](cd3dx12-pipeline-state-stream-ps.md)
-   [<span data-ttu-id="799da-136">**\_Fluxo de \_ estado do pipeline \_ do CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="799da-136">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CS**</span></span>](cd3dx12-pipeline-state-stream-cs.md)
-   [<span data-ttu-id="799da-137">**\_ \_ \_ Stream \_ Blend de estado \_ do pipeline CD3DX12**</span><span class="sxs-lookup"><span data-stu-id="799da-137">**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**</span></span>](cd3dx12-pipeline-state-stream-blend-desc.md)
-   [<span data-ttu-id="799da-138">**\_Estêncil de \_ profundidade do fluxo de estado do pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-138">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil.md)
-   [<span data-ttu-id="799da-139">**\_STENCIL1 de \_ profundidade de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-139">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil1.md)
-   [<span data-ttu-id="799da-140">**\_Formato de \_ \_ estêncil de profundidade do fluxo de estado \_ do \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="799da-140">**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL\_FORMAT**</span></span>](cd3dx12-pipeline-state-stream-depth-stencil-format.md)
-   [<span data-ttu-id="799da-141">**\_ \_ \_ Rasterizador de fluxo de estado de pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="799da-141">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**</span></span>](cd3dx12-pipeline-state-stream-rasterizer.md)
-   [<span data-ttu-id="799da-142">**\_Formatos de \_ \_ destino de renderização de fluxo de estado \_ de \_ pipeline CD3DX12 \_**</span><span class="sxs-lookup"><span data-stu-id="799da-142">**CD3DX12\_PIPELINE\_STATE\_STREAM\_RENDER\_TARGET\_FORMATS**</span></span>](cd3dx12-pipeline-state-stream-render-target-formats.md)
-   [<span data-ttu-id="799da-143">**\_Exemplo de fluxo de estado do pipeline CD3DX12 \_ \_ \_ \_ desc**</span><span class="sxs-lookup"><span data-stu-id="799da-143">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_DESC**</span></span>](cd3dx12-pipeline-state-stream-sample-desc.md)
-   [<span data-ttu-id="799da-144">**\_Máscara de \_ exemplo de fluxo de estado de pipeline CD3DX12 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-144">**CD3DX12\_PIPELINE\_STATE\_STREAM\_SAMPLE\_MASK**</span></span>](cd3dx12-pipeline-state-stream-sample-mask.md)
-   [<span data-ttu-id="799da-145">**PSO do fluxo de estado do pipeline do CD3DX12 \_ \_ \_ \_ em cache \_**</span><span class="sxs-lookup"><span data-stu-id="799da-145">**CD3DX12\_PIPELINE\_STATE\_STREAM\_CACHED\_PSO**</span></span>](cd3dx12-pipeline-state-stream-cached-pso.md)

<span data-ttu-id="799da-146">O [**CD3DX12 \_ pipeline \_ State \_ Stream \_ Blend \_**](cd3dx12-pipeline-state-stream-blend-desc.md), o [**\_ \_ \_ \_ \_ estêncil profundidade do fluxo do CD3DX12**](cd3dx12-pipeline-state-stream-depth-stencil.md)do pipeline, o CD3DX12 pipeline de nível de fluxo de perfil [**\_ \_ \_ \_ \_ STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md)e as estruturas do [**\_ \_ \_ \_ rasterizador de fluxo de perfil CD3DX12**](cd3dx12-pipeline-state-stream-rasterizer.md) são definidas para inicializar seus dados de subobjeto com padrões comuns usando [**CD3DX12 \_ padrão**](cd3dx12-default.md).</span><span class="sxs-lookup"><span data-stu-id="799da-146">The [**CD3DX12\_PIPELINE\_STATE\_STREAM\_BLEND\_DESC**](cd3dx12-pipeline-state-stream-blend-desc.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL**](cd3dx12-pipeline-state-stream-depth-stencil.md), [**CD3DX12\_PIPELINE\_STATE\_STREAM\_DEPTH\_STENCIL1**](cd3dx12-pipeline-state-stream-depth-stencil1.md), and [**CD3DX12\_PIPELINE\_STATE\_STREAM\_RASTERIZER**](cd3dx12-pipeline-state-stream-rasterizer.md) structures are defined to initialize their subobject data with common defaults using [**CD3DX12\_DEFAULT**](cd3dx12-default.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="799da-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="799da-147">Requirements</span></span>



| <span data-ttu-id="799da-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="799da-148">Requirement</span></span> | <span data-ttu-id="799da-149">Valor</span><span class="sxs-lookup"><span data-stu-id="799da-149">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="799da-150">parâmetro</span><span class="sxs-lookup"><span data-stu-id="799da-150">Header</span></span><br/> | <dl> <span data-ttu-id="799da-151"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="799da-151"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="799da-152">Confira também</span><span class="sxs-lookup"><span data-stu-id="799da-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="799da-153">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="799da-153">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> <dt>

[<span data-ttu-id="799da-154">**\_Tipo de \_ subobjeto de estado de pipeline D3D12 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="799da-154">**D3D12\_PIPELINE\_STATE\_SUBOBJECT\_TYPE**</span></span>](/windows/desktop/api/d3d12/ne-d3d12-d3d12_pipeline_state_subobject_type)
</dt> </dl>

 

