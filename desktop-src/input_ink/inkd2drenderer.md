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
ms.openlocfilehash: 51383770b8eb0c5dca5efbb5f1756bee81ece506c0e92337e9df9a60eb0a8aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726726"
---
# <a name="inkd2drenderer-class"></a>Classe InkD2DRenderer

Implementa a interface [**IInkD2DRenderer.**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer)

Um [**objeto IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) permite a renderização de traços de tinta no contexto do dispositivo Direct2D designado de um aplicativo universal Windows, em vez do controle [**InkCanvas padrão.**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas)

## <a name="members"></a>Membros

A **classe InkD2DRenderer** herda da interface [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **InkD2DRenderer** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A **classe InkD2DRenderer** tem esses métodos.

| Método                              | Descrição                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Renderiza o traço de tinta para o Direct2D do dispositivo designado do aplicativo.<br/> |

## <a name="creationaccess-functions"></a>Funções \\ de acesso de criação

Chame [<strong>CoCreateInstance com</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) o identificador de <strong>classe InkD2DRenderer</strong> para recuperar uma referência ao objeto .

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Exemplos

Este snippet do arquivo "SceneComposer.cpp" do exemplo de inking complexo demonstra a renderização de uma coleção de traços de tinta em um contexto Direct2D dispositivo. [](/samples/microsoft/windows-universal-samples/complexink/)

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Este snippet do arquivo "InkRenderer.cpp" do exemplo de inking complexo mostra o método Render (chamado no snippet anterior) que chama o método [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) para renderizar os traços. [](/samples/microsoft/windows-universal-samples/complexink/)

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

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| Cabeçalho<br/>                   | <dl> <dt>Inkrenderer.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Inkrenderer.idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer é definido como 4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Tópicos relacionados

[Renderdor de tinta,](ink-renderer.md) [interações de caneta](/windows/uwp/design/input/pen-and-stylus-interactions)e caneta, exemplo de Análise de [Tinta,](/samples/microsoft/windows-universal-samples/inkanalysis/)Exemplo de tinta [simples,](/samples/microsoft/windows-universal-samples/simpleink/) [Amostra de tinta complexa](/samples/microsoft/windows-universal-samples/complexink/)
