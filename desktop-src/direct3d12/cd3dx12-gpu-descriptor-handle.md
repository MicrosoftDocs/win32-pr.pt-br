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
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>\_Estrutura do \_ identificador do descritor de GPU CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

## <a name="syntax"></a>Sintaxe


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



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Identificador do descritor de GPU CD3DX12 \_ ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ identificador de \_ descritor de GPU CD3DX12 \_ .

</dd> <dt>

**identificador explícito \_ \_ do descritor de GPU CD3DX12 \_ (const D3D12 \_ GPU \_ Descriptor \_ identificador &o)**
</dt> <dd>

Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializado com o conteúdo de outra estrutura de [**\_ \_ \_ identificador de descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .

</dd> <dt>

**\_ \_ Identificador do descritor de GPU CD3DX12 \_ ( \_ padrão CD3DX12)**
</dt> <dd>

Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializado com parâmetros padrão (define o ponteiro para zero).

</dd> <dt>

**\_ \_ Identificador do descritor de GPU CD3DX12 \_ (D3D12 \_ de descritor de GPU conste \_ \_ &outro, int offsetScaledByIncrementSize)**
</dt> <dd>

Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializando os seguintes parâmetros:

\_Identificador do \_ descritor de GPU D3D12 \_ &outros

INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.

</dd> <dt>

**\_ \_ Identificador do descritor de GPU CD3DX12 \_ (const D3D12 \_ \_ de descritor de GPU \_ &outro, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Cria uma nova instância de um \_ identificador de \_ descritor de GPU CD3DX12 \_ , inicializando os seguintes parâmetros:

\_Identificador do \_ descritor de GPU D3D12 \_ &outros

INT offsetInDescriptors: o número de descritores pelos quais incrementar.

UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.

</dd> <dt>

**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Define o deslocamento com base no número especificado de descritores e o quanto incrementar para cada descritor. Usa os seguintes parâmetros:

INT offsetInDescriptors: o número de descritores pelos quais incrementar.

UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.

</dd> <dt>

**Deslocamento (INT offsetScaledByIncrementSize)**
</dt> <dd>

Define o deslocamento com base no número especificado de incrementos. Usa os seguintes parâmetros:

INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.

</dd> <dt>

**operador embutido = = ( \_ no \_ D3D12 \_ const \_ descritor de GPU \_ identificador& outro) const**
</dt> <dd>

Testes de igualdade entre o identificador do \_ descritor de GPU CD3DX12 atual \_ e o identificador do descritor \_ de GPU D3D12 especificado \_ ou o identificador do \_ \_ \_ descritor de GPU CD3DX12 \_ \_ .

</dd> <dt>

**operador embutido! = ( \_ no \_ D3D12 \_ const \_ descritor de GPU \_ identificador& outro) const**
</dt> <dd>

Testa a desigualdade entre o \_ identificador do descritor de GPU CD3DX12 atual e o identificador do descritor de GPU \_ \_ D3D12 especificado \_ ou o identificador do \_ \_ \_ descritor de GPU CD3DX12 \_ \_ .

</dd> <dt>

**Operator = (const D3D12 \_ o \_ descritor de GPU \_ não &outro)**
</dt> <dd>

Define o identificador do \_ descritor de GPU CD3DX12 atual \_ \_ com os mesmos valores que o identificador do descritor de GPU D3D12 especificado \_ ou o identificador do \_ \_ \_ descritor de GPU CD3DX12 \_ \_ .

</dd> <dt>

**InitOffsetted embutido ( \_ em \_ const D3D12 o \_ descritor de GPU \_ \_ identificador &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com o número especificado de itens. Usa os seguintes parâmetros:

\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.

INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.

</dd> <dt>

**InitOffsetted embutido ( \_ em \_ const D3D12 \_ identificador de descritor de GPU \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com um deslocamento, usando o número especificado de descritores do tamanho fornecido. Usa os seguintes parâmetros:

\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.

INT offsetInDescriptors: o número de descritores pelos quais deslocar.

UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.

</dd> <dt>

**estática embutida InitOffsetted \_ ( \_ saída \_ \_ do descritor de GPU D3D12 \_ &identificador, \_ em \_ const D3D12 \_ identificador de descritores de GPU \_ \_ &base, int offsetScaledByIncrementSize)**
</dt> <dd>

Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com um deslocamento, usando o número especificado de descritores do tamanho fornecido. Usa os seguintes parâmetros:

\_\_D3D12 \_ \_ do descritor \_ de GPU de saída do identificador &: gera o \_ identificador do descritor de GPU D3D12 resultante \_ \_ .

\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.

INT offsetScaledByIncrementSize: o número de incrementos pelos quais deslocar.

</dd> <dt>

**estática embutida InitOffsetted \_ ( \_ saída \_ \_ do descritor de GPU D3D12 \_ &identificador, \_ em \_ const D3D12 \_ identificador de descritores de GPU \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**
</dt> <dd>

Inicializa uma estrutura de [**\_ \_ \_ identificador do descritor de GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) com um deslocamento, usando o número especificado de descritores do tamanho fornecido. Usa os seguintes parâmetros:

\_\_D3D12 \_ \_ do descritor \_ de GPU de saída do identificador &: gera o \_ identificador do descritor de GPU D3D12 resultante \_ \_ .

\_Em \_ const D3D12 \_ o \_ descritor de GPU \_ identificador &base: o endereço base do qual deslocar.

INT offsetInDescriptors: o número de descritores pelos quais deslocar.

UINT descriptorIncrementSize: o valor pelo qual incrementar para cada descritor, incluindo Padding.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Identificador do \_ descritor de GPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





