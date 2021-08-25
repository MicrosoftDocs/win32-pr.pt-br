---
title: Função D3DX12SerializeVersionedRootSignature (D3dx12.h)
description: Ajuda a habilitar recursos de assinatura raiz 1.1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz. Esse método auxiliar reconstrói uma assinatura raiz da versão 1.0 quando não há suporte para a versão 1.1.
ms.assetid: 0F6BA6C1-9A33-4E99-BF34-4A0358E7427D
keywords:
- Função D3DX12SerializeVersionedRootSignature
topic_type:
- apiref
api_name:
- D3DX12SerializeVersionedRootSignature
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f69e3bf66bcbad61e3d9bf676038f27511f756d7a3a473be2c513553862eb90
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851150"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>Função D3DX12SerializeVersionedRootSignature

Ajuda a habilitar recursos de assinatura raiz 1.1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz. Esse método auxiliar reconstrói uma assinatura raiz da versão 1.0 quando não há suporte para a versão 1.1.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pRootSignatureDesc* \[ Em\]
</dt> <dd>

Tipo: **const D3D12 \_ VERSIONED ROOT SIGNATURE \_ \_ \_ DESC \***

Especifica uma [**\_ \_ \_ \_ DESC DESC DE ASSINATURA RAIZ COM VERSÃO D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) que contém uma descrição de qualquer versão de uma assinatura raiz.

</dd> <dt>

*Maxversion* 
</dt> <dd>

Tipo: **VERSÃO DE ASSINATURA \_ RAIZ \_ \_ D3D**

Especifica a versão máxima de [**ASSINATURA RAIZ D3D \_ com \_ \_ suporte.**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)

</dd> <dt>

*ppBlob* \[ out\]
</dt> <dd>

Tipo: **\* \* ID3DBlob**

Um ponteiro para um bloco de memória que recebe um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar a assinatura raiz serializada.

</dd> <dt>

*ppErrorBlob* \[ out, opcional\]
</dt> <dd>

Tipo: **\* \* ID3DBlob**

Um ponteiro para um bloco de memória que recebe um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar mensagens de erro do serializador ou **NULL** se não houver erros.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retornará **S \_ OK** se for bem-sucedido; caso contrário, retornará um dos Códigos de Retorno [do Direct3D 12.](d3d12-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Comentários

Essa função foi lançada para coincidir com a Atualização Windows 10 aniversário (14393). Para dar suporte Windows 10 versões anteriores a essa, o uso dessa função requer que d3d12.lib seja definido para carregamento *de atraso.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

