---
description: Inicia uma técnica ativa.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'Método ID3DXEffect:: Begin (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104173035"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="b52bf-103">Método ID3DXEffect:: Begin</span><span class="sxs-lookup"><span data-stu-id="b52bf-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="b52bf-104">Inicia uma técnica ativa.</span><span class="sxs-lookup"><span data-stu-id="b52bf-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="b52bf-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b52bf-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b52bf-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b52bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b52bf-107">*pPasses* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b52bf-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b52bf-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="b52bf-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="b52bf-109">Ponteiro para um valor retornado que indica o número de passagens necessárias para renderizar a técnica atual.</span><span class="sxs-lookup"><span data-stu-id="b52bf-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="b52bf-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="b52bf-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b52bf-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b52bf-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b52bf-112">DWORD que determina se o estado modificado por um efeito é salvo e restaurado.</span><span class="sxs-lookup"><span data-stu-id="b52bf-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="b52bf-113">O valor padrão 0 especifica que **ID3DXEffect:: Begin** e [**ID3DXEffect:: End**](id3dxeffect--end.md) salvará e restaurará todos os Estados modificados pelo efeito (incluindo constantes de sombreador de pixel e Vertex).</span><span class="sxs-lookup"><span data-stu-id="b52bf-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="b52bf-114">Sinalizadores válidos podem ser vistos nos [sinalizadores de salvar e restaurar de estado do efeito](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="b52bf-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b52bf-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b52bf-115">Return value</span></span>

<span data-ttu-id="b52bf-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b52bf-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b52bf-117">Se o método for bem sucedido, o valor de retorno será D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b52bf-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b52bf-118">Se o método falhar, o valor de retorno poderá ser um dos seguintes: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="b52bf-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="b52bf-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="b52bf-119">Remarks</span></span>

<span data-ttu-id="b52bf-120">Um aplicativo define uma técnica ativa no sistema de efeitos chamando **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="b52bf-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="b52bf-121">O sistema de efeitos responde capturando todo o estado do pipeline que pode ser alterado pela técnica em um bloco de estado.</span><span class="sxs-lookup"><span data-stu-id="b52bf-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="b52bf-122">Um aplicativo sinaliza o final de uma técnica chamando [**ID3DXEffect:: End**](id3dxeffect--end.md), que usa o bloco de estado para restaurar o estado original.</span><span class="sxs-lookup"><span data-stu-id="b52bf-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="b52bf-123">O sistema de efeitos, portanto, cuida do salvamento do estado quando uma técnica se torna ativa e restaura o estado quando uma técnica termina.</span><span class="sxs-lookup"><span data-stu-id="b52bf-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="b52bf-124">Se você optar por desabilitar essa funcionalidade de salvar e restaurar, consulte [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="b52bf-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="b52bf-125">No par **ID3DXEffect:: Begin** e [**ID3DXEffect:: End**](id3dxeffect--end.md) , um aplicativo usa [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) para definir a passagem ativa, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) se alguma alteração de estado ocorreu depois que a passagem foi ativada e [**ID3DXEffect:: endpass**](id3dxeffect--endpass.md) para encerrar a passagem ativa.</span><span class="sxs-lookup"><span data-stu-id="b52bf-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="b52bf-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b52bf-126">Requirements</span></span>



| <span data-ttu-id="b52bf-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="b52bf-127">Requirement</span></span> | <span data-ttu-id="b52bf-128">Valor</span><span class="sxs-lookup"><span data-stu-id="b52bf-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b52bf-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b52bf-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b52bf-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b52bf-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b52bf-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b52bf-131">Library</span></span><br/> | <dl> <span data-ttu-id="b52bf-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b52bf-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b52bf-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="b52bf-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b52bf-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="b52bf-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
