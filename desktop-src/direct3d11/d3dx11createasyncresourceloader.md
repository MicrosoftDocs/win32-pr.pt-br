---
title: Função D3DX11CreateAsyncResourceLoader (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um carregador de recurso assíncrono.
ms.assetid: b49900a1-866d-4a4a-bf3a-2deb9ce4a208
keywords:
- Função D3DX11CreateAsyncResourceLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncResourceLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc7dd914250f3d47b80643d88ef055681f2e8a9f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104012140"
---
# <a name="d3dx11createasyncresourceloader-function"></a><span data-ttu-id="f0194-106">Função D3DX11CreateAsyncResourceLoader</span><span class="sxs-lookup"><span data-stu-id="f0194-106">D3DX11CreateAsyncResourceLoader function</span></span>

> [!Note]  
> <span data-ttu-id="f0194-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="f0194-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="f0194-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="f0194-108">See Remarks.</span></span>

 

<span data-ttu-id="f0194-109">Crie um carregador de recurso assíncrono.</span><span class="sxs-lookup"><span data-stu-id="f0194-109">Create an asynchronous-resource loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0194-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f0194-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncResourceLoader(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="f0194-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0194-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f0194-112">*hSrcModule* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0194-112">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0194-113">Tipo: **[ **HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f0194-113">Type: **[**HMODULE**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f0194-114">Identificador para o módulo de recurso.</span><span class="sxs-lookup"><span data-stu-id="f0194-114">Handle to the resource module.</span></span> <span data-ttu-id="f0194-115">Use a [função GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para obter o identificador.</span><span class="sxs-lookup"><span data-stu-id="f0194-115">Use [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) to get the handle.</span></span>

</dd> <dt>

<span data-ttu-id="f0194-116">*pSrcResource* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f0194-116">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f0194-117">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="f0194-117">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="f0194-118">Nome do recurso no hSrcModule.</span><span class="sxs-lookup"><span data-stu-id="f0194-118">Name of the resource in hSrcModule.</span></span> <span data-ttu-id="f0194-119">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="f0194-119">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="f0194-120">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="f0194-120">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="f0194-121">*ppDataLoader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="f0194-121">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f0194-122">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="f0194-122">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="f0194-123">O endereço de um ponteiro para o carregador de dados assíncronos (consulte a [**interface ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="f0194-123">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f0194-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f0194-124">Return value</span></span>

<span data-ttu-id="f0194-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f0194-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f0194-126">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="f0194-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="f0194-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0194-127">Remarks</span></span>

<span data-ttu-id="f0194-128">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="f0194-128">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="f0194-129">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="f0194-129">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="f0194-130">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="f0194-130">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0194-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f0194-131">Requirements</span></span>



| <span data-ttu-id="f0194-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="f0194-132">Requirement</span></span> | <span data-ttu-id="f0194-133">Valor</span><span class="sxs-lookup"><span data-stu-id="f0194-133">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0194-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f0194-134">Header</span></span><br/>  | <dl> <span data-ttu-id="f0194-135"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="f0194-135"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="f0194-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f0194-136">Library</span></span><br/> | <dl> <span data-ttu-id="f0194-137"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f0194-137"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="f0194-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0194-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0194-139">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="f0194-139">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

