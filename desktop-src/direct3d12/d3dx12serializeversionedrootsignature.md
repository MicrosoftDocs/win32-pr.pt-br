---
title: Função D3DX12SerializeVersionedRootSignature (D3dx12. h)
description: Ajuda a habilitar os recursos da assinatura raiz 1,1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz. Esse método auxiliar reconstrói uma assinatura raiz da versão 1,0 quando a versão 1,1 não tem suporte.
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
ms.openlocfilehash: 70a9d0424f7f7a7f89edde18273c5d1fa22fae28
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "105784560"
---
# <a name="d3dx12serializeversionedrootsignature-function"></a>Função D3DX12SerializeVersionedRootSignature

Ajuda a habilitar os recursos da assinatura raiz 1,1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz. Esse método auxiliar reconstrói uma assinatura raiz da versão 1,0 quando a versão 1,1 não tem suporte.

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

*pRootSignatureDesc* \[ no\]
</dt> <dd>

Tipo: **const D3D12 com \_ versão \_ raiz \_ assinatura \_ desc \***

Especifica um [**\_ \_ \_ \_ desc de assinatura raiz D3D12 com versão**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) que contém uma descrição de qualquer versão de uma assinatura raiz.

</dd> <dt>

*MaxVersion* 
</dt> <dd>

Tipo: **\_ versão da \_ assinatura \_ raiz do D3D**

Especifica a versão máxima [**da \_ \_ assinatura raiz \_ do D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)com suporte.

</dd> <dt>

*ppBlob* \[ fora\]
</dt> <dd>

Tipo: **ID3DBlob \* \***

Um ponteiro para um bloco de memória que recebe um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar a assinatura raiz serializada.

</dd> <dt>

*ppErrorBlob* \[ out, opcional\]
</dt> <dd>

Tipo: **ID3DBlob \* \***

Um ponteiro para um bloco de memória que recebe um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar mensagens de erro do serializador ou **NULL** se não houver erros.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Retorna **S \_ OK** se obtiver êxito; caso contrário, retorna um dos [códigos de retorno do Direct3D 12](d3d12-graphics-reference-returnvalues.md).

## <a name="remarks"></a>Comentários

Esta função foi liberada para coincidir com a atualização de aniversário do Windows 10 (14393). Para dar suporte a versões do Windows 10 anteriores a isso, o uso dessa função requer que o d3d12. lib seja configurado para o *carregamento de atraso*.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Biblioteca<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[Funções auxiliares do D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

