---
title: Função D3DX11CreateAsyncMemoryLoader (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um carregador de memória assíncrona.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- Função D3DX11CreateAsyncMemoryLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989349"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="9a53b-106">Função D3DX11CreateAsyncMemoryLoader</span><span class="sxs-lookup"><span data-stu-id="9a53b-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="9a53b-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="9a53b-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="9a53b-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="9a53b-108">See Remarks.</span></span>

 

<span data-ttu-id="9a53b-109">Crie um carregador de memória assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a53b-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a53b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a53b-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="9a53b-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a53b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a53b-112">*pData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a53b-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a53b-113">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a53b-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a53b-114">Ponteiro para os dados.</span><span class="sxs-lookup"><span data-stu-id="9a53b-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="9a53b-115">*cbData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9a53b-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a53b-116">Tipo: **[ **tamanho \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9a53b-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9a53b-117">Tamanho dos dados.</span><span class="sxs-lookup"><span data-stu-id="9a53b-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="9a53b-118">*ppDataLoader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="9a53b-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a53b-119">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="9a53b-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="9a53b-120">O endereço de um ponteiro para o carregador de dados assíncronos (consulte a [**interface ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="9a53b-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a53b-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a53b-121">Return value</span></span>

<span data-ttu-id="9a53b-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9a53b-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9a53b-123">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="9a53b-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9a53b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a53b-124">Remarks</span></span>

<span data-ttu-id="9a53b-125">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="9a53b-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="9a53b-126">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="9a53b-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="9a53b-127">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9a53b-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a53b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a53b-128">Requirements</span></span>



| <span data-ttu-id="9a53b-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a53b-129">Requirement</span></span> | <span data-ttu-id="9a53b-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9a53b-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a53b-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a53b-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9a53b-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a53b-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="9a53b-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a53b-133">Library</span></span><br/> | <dl> <span data-ttu-id="9a53b-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a53b-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="9a53b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a53b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a53b-136">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="9a53b-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

