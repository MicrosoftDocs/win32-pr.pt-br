---
title: Classe CD3DX12_STATE_OBJECT_DESC (D3dx12. h)
description: A classe central dos auxiliares de criação de objeto de estado D3DX12, que são classes auxiliares para a criação de objetos de estado de um conjunto arbitrário de subobjetos.
keywords:
- Classe CD3DX12_STATE_OBJECT_DESC
topic_type:
- apiref
api_name:
- CD3DX12_STATE_OBJECT_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/03/2021
ms.openlocfilehash: cc3d65a9779c379debd94e7872717e4449a71ac8
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813074"
---
# <a name="cd3dx12_state_object_desc-class"></a>Classe CD3DX12_STATE_OBJECT_DESC

A classe central dos auxiliares de criação de objeto de estado D3DX12, que são classes auxiliares para a criação de objetos de estado de um conjunto arbitrário de subobjetos.

## <a name="syntax"></a>Sintaxe

```cpp
class CD3DX12_STATE_OBJECT_DESC
{
    CD3DX12_STATE_OBJECT_DESC() noexcept;
    CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE) noexcept;
    void SetStateObjectType(D3D12_STATE_OBJECT_TYPE) noexcept;
    operator const D3D12_STATE_OBJECT_DESC& ();
    operator const D3D12_STATE_OBJECT_DESC* ();
    template<typename T> T* CreateSubobject();
};
```

## <a name="members"></a>Membros

`CD3DX12_STATE_OBJECT_DESC`

Construtor padrão. Cria uma instância nova, inicializada por padrão, de um **CD3DX12_STATE_OBJECT_DESC**.

`CD3DX12_STATE_OBJECT_DESC(D3D12_STATE_OBJECT_TYPE)`

Construtor que cria uma nova instância de um **CD3DX12_STATE_OBJECT_DESC** inicializado com um tipo de subjobject correspondente ao valor do [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) passado para ele.

`SetStateObjectType(D3D12_STATE_OBJECT_TYPE)`

Método que define o tipo subjobject como o valor do [**D3D12_STATE_OBJECT_TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_state_object_type) passado para ele.

`operator const D3D12_STATE_OBJECT_DESC&`

Operador de conversão que retorna uma referência a uma constante [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) objeto que descreve o objeto de estado.

`operator const D3D12_STATE_OBJECT_DESC*`

Operador de conversão que retorna um ponteiro para uma constante [**D3D12_STATE_OBJECT_DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_state_object_desc) objeto que descreve o objeto de estado.

`CreateSubobject`

Um modelo de função que cria um auxiliar sububject cujo tempo de vida pertence a essa classe.

O parâmetro de modelo *T* especifica o tipo de auxiliar subjobject, por exemplo, [CD3DX12_HIT_GROUP_SUBOBJECT](cd3dx12-hit-group-subobject.md).

## <a name="remarks"></a>Comentários

Para usar os auxiliares de criação de objeto de estado D3DX12, comece instanciando um objeto **CD3DX12_STATE_OBJECT_DESC** e chame sua função **CreateSubobject** para criar subobjetos. Os auxiliares de subobjetos têm métodos específicos a esse subobjeto para configurar seu conteúdo.

```cpp
CD3DX12_STATE_OBJECT_DESC Collection1(D3D12_STATE_OBJECT_TYPE_COLLECTION);
auto Lib0 = Collection1.CreateSubobject<CD3DX12_DXIL_LIBRARY_SUBOBJECT>();
Lib0->SetDXILLibrary(&pMyAppDxilLibs[0]);
Lib0->DefineExport(L"rayGenShader0");
// In practice, these export listings might be data/engine-driven.
...
```

Como alternativa, você pode criar uma instância de auxiliares de subobjeto explicitamente, como por meio de variáveis locais, passando o objeto de estado DESC (que deve apontar para ele) para o Construtor auxiliar (ou chamar `mySubobjectHelper.AddToStateObject(Collection1)` ).

Nesse cenário alternativo, você precisa manter o subobjeto ativo, desde que o objeto de estado ao qual ele está associado esteja ativo, caso contrário, suas referências de ponteiro serão obsoletas.

```cpp
CD3DX12_STATE_OBJECT_DESC RaytracingState2(D3D12_STATE_OBJECT_TYPE_RAYTRACING_PIPELINE);
CD3DX12_DXIL_LIBRARY_SUBOBJECT LibA(RaytracingState2);
LibA.SetDXILLibrary(&pMyAppDxilLibs[4]);
// Not manually specifying exports; meaning that all exports in the libraries are exported.
...
```

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro | [D3dx12. h](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h) |

## <a name="see-also"></a>Confira também

* [Estruturas auxiliares para Direct3D 12](helper-structures-for-d3d12.md)
