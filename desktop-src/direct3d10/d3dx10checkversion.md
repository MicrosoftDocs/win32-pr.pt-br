---
description: Função D3DX10CheckVersion – Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Função D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105344"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="7ae56-103">Função D3DX10CheckVersion</span><span class="sxs-lookup"><span data-stu-id="7ae56-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="7ae56-104">Verifique se a versão do D3DX que você compilou com o é a versão que você está executando.</span><span class="sxs-lookup"><span data-stu-id="7ae56-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ae56-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ae56-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="7ae56-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ae56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ae56-107">*D3DSdkVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ae56-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae56-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ae56-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ae56-109">Use a \_ versão do SDK do d3d10 \_ .</span><span class="sxs-lookup"><span data-stu-id="7ae56-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="7ae56-110">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="7ae56-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7ae56-111">*D3DX10SdkVersion* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="7ae56-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ae56-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7ae56-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7ae56-113">Use a \_ versão do SDK do D3DX10 \_ .</span><span class="sxs-lookup"><span data-stu-id="7ae56-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="7ae56-114">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="7ae56-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ae56-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7ae56-115">Return value</span></span>

<span data-ttu-id="7ae56-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7ae56-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7ae56-117">Se a versão não corresponder, a função retornará FALSE (um número menor ou igual a 0, o número em si não terá significado).</span><span class="sxs-lookup"><span data-stu-id="7ae56-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="7ae56-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ae56-118">Remarks</span></span>

<span data-ttu-id="7ae56-119">Use essa função durante a inicialização do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ae56-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="7ae56-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ae56-120">Requirements</span></span>



| <span data-ttu-id="7ae56-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ae56-121">Requirement</span></span> | <span data-ttu-id="7ae56-122">Valor</span><span class="sxs-lookup"><span data-stu-id="7ae56-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7ae56-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ae56-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7ae56-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ae56-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="7ae56-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ae56-125">Library</span></span><br/> | <dl> <span data-ttu-id="7ae56-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ae56-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7ae56-127">Consulte também</span><span class="sxs-lookup"><span data-stu-id="7ae56-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ae56-128">Funções de Uso Geral</span><span class="sxs-lookup"><span data-stu-id="7ae56-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
