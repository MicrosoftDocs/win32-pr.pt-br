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
# <a name="d3dx12serializeversionedrootsignature-function"></a><span data-ttu-id="fa96c-105">Função D3DX12SerializeVersionedRootSignature</span><span class="sxs-lookup"><span data-stu-id="fa96c-105">D3DX12SerializeVersionedRootSignature function</span></span>

<span data-ttu-id="fa96c-106">Ajuda a habilitar os recursos da assinatura raiz 1,1 quando eles estão disponíveis e não requer a manutenção de dois caminhos de código para a criação de assinaturas raiz.</span><span class="sxs-lookup"><span data-stu-id="fa96c-106">Helps enable root signature 1.1 features when they are available, and does not require maintaining two code paths for building root signatures.</span></span> <span data-ttu-id="fa96c-107">Esse método auxiliar reconstrói uma assinatura raiz da versão 1,0 quando a versão 1,1 não tem suporte.</span><span class="sxs-lookup"><span data-stu-id="fa96c-107">This helper method reconstructs a version 1.0 root signature when version 1.1 is not supported.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa96c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fa96c-108">Syntax</span></span>


```C++
HRESULT inline D3DX12SerializeVersionedRootSignature(
  _In_      const D3D12_VERSIONED_ROOT_SIGNATURE_DESC *pRootSignatureDesc,
                  D3D_ROOT_SIGNATURE_VERSION          MaxVersion,
  _Out_           ID3DBlob                            **ppBlob,
  _Out_opt_       ID3DBlob                            **ppErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="fa96c-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa96c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa96c-110">*pRootSignatureDesc* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fa96c-110">*pRootSignatureDesc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa96c-111">Tipo: **const D3D12 com \_ versão \_ raiz \_ assinatura \_ desc \***</span><span class="sxs-lookup"><span data-stu-id="fa96c-111">Type: **const D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC\***</span></span>

<span data-ttu-id="fa96c-112">Especifica um [**\_ \_ \_ \_ desc de assinatura raiz D3D12 com versão**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) que contém uma descrição de qualquer versão de uma assinatura raiz.</span><span class="sxs-lookup"><span data-stu-id="fa96c-112">Specifies a [**D3D12\_VERSIONED\_ROOT\_SIGNATURE\_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_versioned_root_signature_desc) that contains a description of any version of a root signature.</span></span>

</dd> <dt>

<span data-ttu-id="fa96c-113">*MaxVersion*</span><span class="sxs-lookup"><span data-stu-id="fa96c-113">*MaxVersion*</span></span> 
</dt> <dd>

<span data-ttu-id="fa96c-114">Tipo: **\_ versão da \_ assinatura \_ raiz do D3D**</span><span class="sxs-lookup"><span data-stu-id="fa96c-114">Type: **D3D\_ROOT\_SIGNATURE\_VERSION**</span></span>

<span data-ttu-id="fa96c-115">Especifica a versão máxima [**da \_ \_ assinatura raiz \_ do D3D**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version)com suporte.</span><span class="sxs-lookup"><span data-stu-id="fa96c-115">Specifies the maximum supported [**D3D\_ROOT\_SIGNATURE\_VERSION**](/windows/desktop/api/d3d12/ne-d3d12-d3d_root_signature_version).</span></span>

</dd> <dt>

<span data-ttu-id="fa96c-116">*ppBlob* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="fa96c-116">*ppBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa96c-117">Tipo: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="fa96c-117">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="fa96c-118">Um ponteiro para um bloco de memória que recebe um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar a assinatura raiz serializada.</span><span class="sxs-lookup"><span data-stu-id="fa96c-118">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access the serialized root signature.</span></span>

</dd> <dt>

<span data-ttu-id="fa96c-119">*ppErrorBlob* \[ out, opcional\]</span><span class="sxs-lookup"><span data-stu-id="fa96c-119">*ppErrorBlob* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="fa96c-120">Tipo: **ID3DBlob \* \***</span><span class="sxs-lookup"><span data-stu-id="fa96c-120">Type: **ID3DBlob\*\***</span></span>

<span data-ttu-id="fa96c-121">Um ponteiro para um bloco de memória que recebe um ponteiro para a interface [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) que você pode usar para acessar mensagens de erro do serializador ou **NULL** se não houver erros.</span><span class="sxs-lookup"><span data-stu-id="fa96c-121">A pointer to a memory block that receives a pointer to the [**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) interface that you can use to access serializer error messages, or **NULL** if there are no errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa96c-122">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fa96c-122">Return value</span></span>

<span data-ttu-id="fa96c-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fa96c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fa96c-124">Retorna **S \_ OK** se obtiver êxito; caso contrário, retorna um dos [códigos de retorno do Direct3D 12](d3d12-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="fa96c-124">Returns **S\_OK** if successful; otherwise, returns one of the [Direct3D 12 Return Codes](d3d12-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fa96c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa96c-125">Remarks</span></span>

<span data-ttu-id="fa96c-126">Esta função foi liberada para coincidir com a atualização de aniversário do Windows 10 (14393).</span><span class="sxs-lookup"><span data-stu-id="fa96c-126">This function was released to coincide with the Windows 10 Anniversary Update (14393).</span></span> <span data-ttu-id="fa96c-127">Para dar suporte a versões do Windows 10 anteriores a isso, o uso dessa função requer que o d3d12. lib seja configurado para o *carregamento de atraso*.</span><span class="sxs-lookup"><span data-stu-id="fa96c-127">In order to support Windows 10 versions prior to this, use of this function requires d3d12.lib be set up for *delay loading*.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa96c-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fa96c-128">Requirements</span></span>



| <span data-ttu-id="fa96c-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fa96c-129">Requirement</span></span> | <span data-ttu-id="fa96c-130">Valor</span><span class="sxs-lookup"><span data-stu-id="fa96c-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fa96c-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fa96c-131">Header</span></span><br/>  | <dl> <span data-ttu-id="fa96c-132"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa96c-132"><dt>D3dx12.h</dt></span></span> </dl>  |
| <span data-ttu-id="fa96c-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fa96c-133">Library</span></span><br/> | <dl> <span data-ttu-id="fa96c-134"><dt>D3D12. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fa96c-134"><dt>D3D12.lib</dt></span></span> </dl> |
| <span data-ttu-id="fa96c-135">DLL</span><span class="sxs-lookup"><span data-stu-id="fa96c-135">DLL</span></span><br/>     | <dl> <span data-ttu-id="fa96c-136"><dt>D3D12.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fa96c-136"><dt>D3D12.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa96c-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa96c-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa96c-138">**D3D12SerializeVersionedRootSignature**</span><span class="sxs-lookup"><span data-stu-id="fa96c-138">**D3D12SerializeVersionedRootSignature**</span></span>](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature)
</dt> <dt>

[<span data-ttu-id="fa96c-139">Funções auxiliares do D3D12</span><span class="sxs-lookup"><span data-stu-id="fa96c-139">Helper Functions for D3D12</span></span>](helper-functions-for-d3d12.md)
</dt> </dl>

 

