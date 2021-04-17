---
title: Estrutura de CD3DX12_SHADER_BYTECODE (D3dx12. h)
description: Uma estrutura auxiliar para habilitar a inicialização fácil de uma \_ estrutura de código de bytes do sombreador D3D12 \_ .
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- Estrutura de CD3DX12_SHADER_BYTECODE
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105765356"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>\_Estrutura de código de bytes do sombreador CD3DX12 \_

Uma estrutura auxiliar para habilitar a inicialização fácil de uma estrutura de [**\_ código de \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

## <a name="syntax"></a>Sintaxe


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>Membros

<dl> <dt>

**\_ \_ Código de bytes do sombreador CD3DX12 ()**
</dt> <dd>

Cria uma nova instância, não inicializada, de um \_ código de bytes do sombreador CD3DX12 \_ .

</dd> <dt>

**\_ \_ código de bytes CD3DX12 do sombreador explícito (const D3D12 do \_ sombreador de \_ bytes &o)**
</dt> <dd>

Cria uma nova instância de um \_ código de bytes do sombreador CD3DX12 \_ , inicializado com o conteúdo de outra estrutura de [**código de \_ \_ bytes do sombreador D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) .

</dd> <dt>

**\_ \_ Código de bytes do sombreador CD3DX12 (ID3DBlob \* pShaderBlob)**
</dt> <dd>

Cria uma nova instância de um \_ código de bytes do sombreador CD3DX12 \_ , inicializando os seguintes parâmetros:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**\_ \_ Código de bytes do sombreador CD3DX12 (const void \* \_ PShaderBytecode, Size \_ T bytecodeLength)**
</dt> <dd>

Cria uma nova instância de um \_ código de bytes do sombreador CD3DX12 \_ , inicializando os seguintes parâmetros:

anular \* \_ pShaderBytecode

DIMENSIONAR \_ T bytecodeLength

</dd> <dt>

**\_ \_ constante de D3D12 de código de bytes de sombreador const a& () const**
</dt> <dd>

Define o & operador de passagem por referência para o tipo de estrutura pai.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|-------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Código de bytes do sombreador D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Estruturas auxiliares do D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

