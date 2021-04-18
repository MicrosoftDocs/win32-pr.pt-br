---
title: Estrutura de CD3DX12_GPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ \_ estrutura de identificador do descritor de GPU D3D12 \_ .
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Estrutura de CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105796205"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a><span data-ttu-id="9a398-104">\_Estrutura do \_ identificador do descritor de GPU CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="9a398-104">CD3DX12\_GPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="9a398-105">Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="9a398-105">A helper structure to enable easy initialization of a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a398-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a398-106">Syntax</span></span>


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="9a398-107">Membros</span><span class="sxs-lookup"><span data-stu-id="9a398-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9a398-108">**\_ \_ Identificador do descritor de GPU CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="9a398-108">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-109">Cria uma nova instância, não inicializada, de um \_ identificador de \_ descritor de GPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="9a398-109">Creates a new, uninitialized, instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-110">**identificador explícito \_ \_ do descritor de GPU CD3DX12 \_ (const D3D12 \_ GPU \_ Descriptor \_ identificador &o)**</span><span class="sxs-lookup"><span data-stu-id="9a398-110">**explicit CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-111">Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializado com o conteúdo de outra estrutura de [**\_ \_ \_ identificador de descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="9a398-111">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-112">**\_ \_ Identificador do descritor de GPU CD3DX12 \_ ( \_ padrão CD3DX12)**</span><span class="sxs-lookup"><span data-stu-id="9a398-112">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-113">Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializado com parâmetros padrão (define o ponteiro para zero).</span><span class="sxs-lookup"><span data-stu-id="9a398-113">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (sets the pointer to zero).</span></span>

</dd> <dt>

<span data-ttu-id="9a398-114">**\_ \_ Identificador do descritor de GPU CD3DX12 \_ (D3D12 \_ de descritor de GPU conste \_ \_ &outro, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-114">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-115">Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-115">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="9a398-116">\_Identificador do \_ descritor de GPU D3D12 \_ &outros</span><span class="sxs-lookup"><span data-stu-id="9a398-116">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="9a398-117">INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-118">**\_ \_ Identificador do descritor de GPU CD3DX12 \_ (const D3D12 \_ \_ de descritor de GPU \_ &outro, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-118">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-119">Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializando os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-119">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="9a398-120">\_Identificador do \_ descritor de GPU D3D12 \_ &outros</span><span class="sxs-lookup"><span data-stu-id="9a398-120">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="9a398-121">INT offsetInDescriptors: o número de descritores pelos quais incrementar.</span><span class="sxs-lookup"><span data-stu-id="9a398-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="9a398-122">UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.</span><span class="sxs-lookup"><span data-stu-id="9a398-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-123">**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-124">Define o deslocamento com base no número especificado de descritores e o quanto incrementar para cada descritor.</span><span class="sxs-lookup"><span data-stu-id="9a398-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="9a398-125">Usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-125">Uses the following parameters:</span></span>

<span data-ttu-id="9a398-126">INT offsetInDescriptors: o número de descritores pelos quais incrementar.</span><span class="sxs-lookup"><span data-stu-id="9a398-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="9a398-127">UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.</span><span class="sxs-lookup"><span data-stu-id="9a398-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-128">**Deslocamento (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-129">Define o deslocamento com base no número especificado de incrementos.</span><span class="sxs-lookup"><span data-stu-id="9a398-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="9a398-130">Usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-130">Uses the following parameters:</span></span>

<span data-ttu-id="9a398-131">INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-132">**operador embutido = = ( \_ no \_ D3D12 \_ const \_ descritor de GPU \_ identificador& outro) const**</span><span class="sxs-lookup"><span data-stu-id="9a398-132">**inline operator==( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-133">Testes de igualdade entre o identificador do \_ descritor de GPU CD3DX12 atual \_ e o identificador do descritor \_ de GPU D3D12 especificado \_ ou o identificador do \_ \_ \_ descritor de GPU CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a398-133">Tests for equality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-134">**operador embutido! = ( \_ no \_ D3D12 \_ const \_ descritor de GPU \_ identificador& outro) const**</span><span class="sxs-lookup"><span data-stu-id="9a398-134">**inline operator!=( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-135">Testa a desigualdade entre o \_ identificador do descritor de GPU CD3DX12 atual e o identificador do descritor de GPU \_ \_ D3D12 especificado \_ ou o identificador do \_ \_ \_ descritor de GPU CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a398-135">Tests for inequality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-136">**Operator = (const D3D12 \_ o \_ descritor de GPU \_ não &outro)**</span><span class="sxs-lookup"><span data-stu-id="9a398-136">**operator=(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-137">Define o identificador do \_ descritor de GPU CD3DX12 atual \_ \_ com os mesmos valores que o identificador do descritor de GPU D3D12 especificado \_ ou o identificador do \_ \_ \_ descritor de GPU CD3DX12 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a398-137">Sets the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-138">**InitOffsetted embutido ( \_ em \_ const D3D12 o \_ descritor de GPU \_ \_ identificador &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-138">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-139">Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com o número especificado de itens.</span><span class="sxs-lookup"><span data-stu-id="9a398-139">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="9a398-140">Usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-140">Uses the following parameters:</span></span>

<span data-ttu-id="9a398-141">\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-141">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="9a398-142">INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-143">**InitOffsetted embutido ( \_ em \_ const D3D12 \_ identificador de descritor de GPU \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-143">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-144">Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com um deslocamento, usando o número especificado de descritores do tamanho fornecido.</span><span class="sxs-lookup"><span data-stu-id="9a398-144">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="9a398-145">Usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-145">Uses the following parameters:</span></span>

<span data-ttu-id="9a398-146">\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-146">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="9a398-147">INT offsetInDescriptors: o número de descritores pelos quais deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="9a398-148">UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.</span><span class="sxs-lookup"><span data-stu-id="9a398-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-149">**estática embutida InitOffsetted \_ ( \_ saída \_ \_ do descritor de GPU D3D12 \_ &identificador, \_ em \_ const D3D12 \_ identificador de descritores de GPU \_ \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-149">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-150">Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com um deslocamento, usando o número especificado de descritores do tamanho fornecido.</span><span class="sxs-lookup"><span data-stu-id="9a398-150">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="9a398-151">Usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-151">Uses the following parameters:</span></span>

<span data-ttu-id="9a398-152">\_\_D3D12 \_ \_ do descritor \_ de GPU de saída do identificador &: gera o \_ identificador do descritor de GPU D3D12 resultante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a398-152">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="9a398-153">\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-153">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="9a398-154">INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="9a398-155">**estática embutida InitOffsetted \_ ( \_ saída \_ \_ do descritor de GPU D3D12 \_ &identificador, \_ em \_ const D3D12 \_ identificador de descritores de GPU \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="9a398-155">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="9a398-156">Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com um deslocamento, usando o número especificado de descritores do tamanho fornecido.</span><span class="sxs-lookup"><span data-stu-id="9a398-156">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="9a398-157">Usa os seguintes parâmetros:</span><span class="sxs-lookup"><span data-stu-id="9a398-157">Uses the following parameters:</span></span>

<span data-ttu-id="9a398-158">\_\_D3D12 \_ \_ do descritor \_ de GPU de saída do identificador &: gera o \_ identificador do descritor de GPU D3D12 resultante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9a398-158">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="9a398-159">\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-159">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="9a398-160">INT offsetInDescriptors: o número de descritores pelos quais deslocar.</span><span class="sxs-lookup"><span data-stu-id="9a398-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="9a398-161">UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.</span><span class="sxs-lookup"><span data-stu-id="9a398-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9a398-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a398-162">Requirements</span></span>



| <span data-ttu-id="9a398-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a398-163">Requirement</span></span> | <span data-ttu-id="9a398-164">Valor</span><span class="sxs-lookup"><span data-stu-id="9a398-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9a398-165">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a398-165">Header</span></span><br/> | <dl> <span data-ttu-id="9a398-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a398-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a398-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a398-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a398-168">**\_Identificador do \_ descritor de GPU D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="9a398-168">**D3D12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[<span data-ttu-id="9a398-169">Estruturas auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="9a398-169">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





