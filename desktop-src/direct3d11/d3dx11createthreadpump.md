---
title: Função D3DX11CreateThreadPump (D3DX11core. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Criar uma bomba de thread.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Função D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104968627"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="31408-106">Função D3DX11CreateThreadPump</span><span class="sxs-lookup"><span data-stu-id="31408-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="31408-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="31408-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="31408-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="31408-108">See Remarks.</span></span>

 

<span data-ttu-id="31408-109">Criar uma bomba de thread.</span><span class="sxs-lookup"><span data-stu-id="31408-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="31408-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31408-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="31408-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31408-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31408-112">*cIoThreads* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31408-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31408-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31408-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="31408-114">O número de threads de e/s a serem criados.</span><span class="sxs-lookup"><span data-stu-id="31408-114">The number of I/O threads to create.</span></span> <span data-ttu-id="31408-115">Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="31408-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="31408-116">*cProcThreads* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="31408-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="31408-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="31408-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="31408-118">O número de threads de processo a serem criados.</span><span class="sxs-lookup"><span data-stu-id="31408-118">The number of process threads to create.</span></span> <span data-ttu-id="31408-119">Se 0 for especificado, o Direct3D tentará calcular o número ideal de threads com base na configuração de hardware.</span><span class="sxs-lookup"><span data-stu-id="31408-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="31408-120">*ppThreadPump* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31408-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31408-121">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="31408-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="31408-122">A bomba de thread criada.</span><span class="sxs-lookup"><span data-stu-id="31408-122">The created thread pump.</span></span> <span data-ttu-id="31408-123">Consulte a [**interface ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="31408-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31408-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31408-124">Return value</span></span>

<span data-ttu-id="31408-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="31408-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="31408-126">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="31408-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="31408-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="31408-127">Remarks</span></span>

<span data-ttu-id="31408-128">Uma bomba de thread é um objeto com uso intensivo de recursos.</span><span class="sxs-lookup"><span data-stu-id="31408-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="31408-129">Somente uma bomba de thread deve ser criada por aplicativo.</span><span class="sxs-lookup"><span data-stu-id="31408-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="31408-130">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="31408-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="31408-131">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="31408-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="31408-132">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="31408-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="31408-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31408-133">Requirements</span></span>



| <span data-ttu-id="31408-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="31408-134">Requirement</span></span> | <span data-ttu-id="31408-135">Valor</span><span class="sxs-lookup"><span data-stu-id="31408-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31408-136">parâmetro</span><span class="sxs-lookup"><span data-stu-id="31408-136">Header</span></span><br/>  | <dl> <span data-ttu-id="31408-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="31408-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="31408-138">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="31408-138">Library</span></span><br/> | <dl> <span data-ttu-id="31408-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31408-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="31408-140">Confira também</span><span class="sxs-lookup"><span data-stu-id="31408-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31408-141">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="31408-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

