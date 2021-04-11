---
description: Implementa a interface IInkD2DRenderer.
ms.assetid: d1bd910d-ce64-4424-a0e1-4f55110b0265
title: Classe InkD2DRenderer
ms.topic: language-reference
ms.date: 02/03/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- InkD2DRenderer
api_type:
- COM
api_location:
- Inkrenderer.idl
ms.openlocfilehash: 1649d52c2e9098513c115daaf295c4005e890b8e
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104172443"
---
# <a name="inkd2drenderer-class"></a><span data-ttu-id="32f40-103">Classe InkD2DRenderer</span><span class="sxs-lookup"><span data-stu-id="32f40-103">InkD2DRenderer class</span></span>

<span data-ttu-id="32f40-104">Implementa a interface [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .</span><span class="sxs-lookup"><span data-stu-id="32f40-104">Implements the [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) interface.</span></span>

<span data-ttu-id="32f40-105">Um objeto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) permite a renderização de traços de tinta no contexto do dispositivo Direct2D designado de um aplicativo universal do Windows, em vez do controle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) padrão.</span><span class="sxs-lookup"><span data-stu-id="32f40-105">An [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) object enables the rendering of ink strokes onto the designated Direct2D device context of a Universal Windows app, instead of the default [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) control.</span></span>

## <a name="members"></a><span data-ttu-id="32f40-106">Membros</span><span class="sxs-lookup"><span data-stu-id="32f40-106">Members</span></span>

<span data-ttu-id="32f40-107">A classe **InkD2DRenderer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="32f40-107">The **InkD2DRenderer** class inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="32f40-108">**InkD2DRenderer** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="32f40-108">**InkD2DRenderer** also has these types of members:</span></span>

- [<span data-ttu-id="32f40-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="32f40-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="32f40-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="32f40-110">Methods</span></span>

<span data-ttu-id="32f40-111">A classe **InkD2DRenderer** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="32f40-111">The **InkD2DRenderer** class has these methods.</span></span>

| <span data-ttu-id="32f40-112">Método</span><span class="sxs-lookup"><span data-stu-id="32f40-112">Method</span></span>                              | <span data-ttu-id="32f40-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="32f40-113">Description</span></span>                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [<span data-ttu-id="32f40-114">**Draw**</span><span class="sxs-lookup"><span data-stu-id="32f40-114">**Draw**</span></span>](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | <span data-ttu-id="32f40-115">Renderiza o traço de tinta para o contexto de dispositivo Direct2D designado do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="32f40-115">Renders the ink stroke to the designated Direct2D device context of the app.</span></span><br/> |

## <a name="creationaccess-functions"></a><span data-ttu-id="32f40-116">Criar \\ funções de acesso</span><span class="sxs-lookup"><span data-stu-id="32f40-116">Creation\\Access Functions</span></span>

<span data-ttu-id="32f40-117">Chame [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de classe <strong>InkD2DRenderer</strong> para recuperar uma referência ao objeto.</span><span class="sxs-lookup"><span data-stu-id="32f40-117">Call [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the class identifier <strong>InkD2DRenderer</strong> to retrieve a reference to the object.</span></span>

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a><span data-ttu-id="32f40-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="32f40-118">Examples</span></span>

<span data-ttu-id="32f40-119">Este trecho de código do arquivo "SceneComposer. cpp" do [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/) demonstra a renderização de uma coleção de traços de tinta em um contexto de dispositivo Direct2D.</span><span class="sxs-lookup"><span data-stu-id="32f40-119">This snippet from the "SceneComposer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) demonstrates the rendering of a collection of ink strokes to a Direct2D device context.</span></span>

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

<span data-ttu-id="32f40-120">Este trecho de código do arquivo "InkRenderer. cpp" do [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/) mostra o método de renderização (chamado no trecho anterior) que chama o método [**draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) para renderizar os traços.</span><span class="sxs-lookup"><span data-stu-id="32f40-120">This snippet from the "InkRenderer.cpp" file of the [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/) shows the Render method (called in the previous snippet) that calls the [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) method for rendering the strokes.</span></span>

```C++
void InkRenderer::Render(
    Platform::Collections::Vector<
        Windows::UI::Input::Inking::InkStroke^>^ strokes,
        Microsoft::WRL::ComPtr<ID2D1DeviceContext> d2dContext)
{
    HRESULT hr = S_OK;
    if (_spInkD2DRenderer != nullptr)
    {
        if (strokes != nullptr && strokes->Size > 0)
        {
            // Cast the stroke collection into IUnknown to call Inkd2dRenderer
            ComPtr<IUnknown> spUnkStrokes = 
                reinterpret_cast<IUnknown*>(reinterpret_cast<__abi_IUnknown*>(strokes));
            hr = _spInkD2DRenderer->Draw(d2dContext.Get(), spUnkStrokes.Get(), false);
            if (FAILED(hr))
            {
                DX::ThrowIfFailed(hr);
            }
        }
    }
}
```

## <a name="requirements"></a><span data-ttu-id="32f40-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32f40-121">Requirements</span></span>

| <span data-ttu-id="32f40-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="32f40-122">Requirement</span></span> | <span data-ttu-id="32f40-123">Valor</span><span class="sxs-lookup"><span data-stu-id="32f40-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="32f40-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32f40-124">Minimum supported client</span></span><br/> | <span data-ttu-id="32f40-125">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="32f40-125">Windows 10 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="32f40-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="32f40-126">Minimum supported server</span></span><br/> | <span data-ttu-id="32f40-127">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="32f40-127">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="32f40-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32f40-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="32f40-129"><dt>Inkrenderer. h</dt></span><span class="sxs-lookup"><span data-stu-id="32f40-129"><dt>Inkrenderer.h</dt></span></span> </dl>   |
| <span data-ttu-id="32f40-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="32f40-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="32f40-131"><dt>Inkrenderer. idl</dt></span><span class="sxs-lookup"><span data-stu-id="32f40-131"><dt>Inkrenderer.idl</dt></span></span> </dl> |
| <span data-ttu-id="32f40-132">IID</span><span class="sxs-lookup"><span data-stu-id="32f40-132">IID</span></span><br/>                      | <span data-ttu-id="32f40-133">IID \_ IInkD2DRenderer é definido como 4044e60c-7b01-4671-a97c-04e0210a07a5</span><span class="sxs-lookup"><span data-stu-id="32f40-133">IID\_IInkD2DRenderer is defined as 4044e60c-7b01-4671-a97c-04e0210a07a5</span></span><br/>         |

## <a name="related-topics"></a><span data-ttu-id="32f40-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32f40-134">Related topics</span></span>

<span data-ttu-id="32f40-135">[Processador de tinta](ink-renderer.md), [interações de caneta e](/windows/uwp/design/input/pen-and-stylus-interactions)caneta, [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)</span><span class="sxs-lookup"><span data-stu-id="32f40-135">[Ink renderer](ink-renderer.md), [Pen and stylus interactions](/windows/uwp/design/input/pen-and-stylus-interactions), [Ink Analysis sample](/samples/microsoft/windows-universal-samples/inkanalysis/), [Simple inking sample](/samples/microsoft/windows-universal-samples/simpleink/), [Complex inking sample](/samples/microsoft/windows-universal-samples/complexink/)</span></span>
