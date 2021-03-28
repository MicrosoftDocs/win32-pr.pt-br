---
title: Função D3DX11CreateAsyncFileLoader (D3DX11async. h)
description: Observe que a biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store. Consulte Observações. Crie um carregador de arquivo assíncrono.
ms.assetid: ee24ac00-3636-4900-9b8a-27778c9a2152
keywords:
- Função D3DX11CreateAsyncFileLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncFileLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637b2eddb035d937315582188295d93d9fd0e9b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104989352"
---
# <a name="d3dx11createasyncfileloader-function"></a><span data-ttu-id="12aa1-106">Função D3DX11CreateAsyncFileLoader</span><span class="sxs-lookup"><span data-stu-id="12aa1-106">D3DX11CreateAsyncFileLoader function</span></span>

> [!Note]  
> <span data-ttu-id="12aa1-107">A biblioteca de utilitários D3DX (D3DX 9, D3DX 10 e D3DX 11) foi preterida para o Windows 8 e não tem suporte para aplicativos da Windows Store.</span><span class="sxs-lookup"><span data-stu-id="12aa1-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="12aa1-108">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="12aa1-108">See Remarks.</span></span>

 

<span data-ttu-id="12aa1-109">Crie um carregador de arquivo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="12aa1-109">Create an asynchronous-file loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="12aa1-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="12aa1-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncFileLoader(
  _In_  LPCTSTR           pFileName,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="12aa1-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12aa1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12aa1-112">*pFileName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="12aa1-112">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12aa1-113">Tipo: **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="12aa1-113">Type: **[**LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="12aa1-114">O nome do arquivo a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="12aa1-114">The name of the file to load.</span></span> <span data-ttu-id="12aa1-115">Se as configurações do compilador exigirem Unicode, o tipo de dados LPCTSTR será resolvido para LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="12aa1-115">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="12aa1-116">Caso contrário, o tipo de dados será resolvido para LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="12aa1-116">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="12aa1-117">*ppDataLoader* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="12aa1-117">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12aa1-118">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="12aa1-118">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="12aa1-119">Endereço de um ponteiro para o carregador de dados assíncronos (consulte a [**interface ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="12aa1-119">Address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12aa1-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="12aa1-120">Return value</span></span>

<span data-ttu-id="12aa1-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12aa1-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12aa1-122">O valor de retorno é um dos valores listados nos [códigos de retorno do Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="12aa1-122">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="12aa1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="12aa1-123">Remarks</span></span>

<span data-ttu-id="12aa1-124">Não há nenhuma implementação do carregador assíncrono fora do D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="12aa1-124">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="12aa1-125">Para aplicativos da Windows Store, os exemplos do DirectX (por exemplo, o [exemplo de tutorial do Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) incluem o módulo **BasicLoader** que usa o modelo de programação assíncrona do Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="12aa1-125">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="12aa1-126">Para aplicativos de área de trabalho Win32, você pode usar o [tempo de execução de simultaneidade](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) para implementar algo semelhante ao modelo de programação Windows Runtime assíncrona.</span><span class="sxs-lookup"><span data-stu-id="12aa1-126">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="12aa1-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12aa1-127">Requirements</span></span>



| <span data-ttu-id="12aa1-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="12aa1-128">Requirement</span></span> | <span data-ttu-id="12aa1-129">Valor</span><span class="sxs-lookup"><span data-stu-id="12aa1-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12aa1-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12aa1-130">Header</span></span><br/>  | <dl> <span data-ttu-id="12aa1-131"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="12aa1-131"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="12aa1-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="12aa1-132">Library</span></span><br/> | <dl> <span data-ttu-id="12aa1-133"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12aa1-133"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="12aa1-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="12aa1-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12aa1-135">Funções D3DX</span><span class="sxs-lookup"><span data-stu-id="12aa1-135">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

