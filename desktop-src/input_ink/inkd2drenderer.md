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
# <a name="inkd2drenderer-class"></a>Classe InkD2DRenderer

Implementa a interface [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) .

Um objeto [**IInkD2DRenderer**](/windows/win32/api/inkrenderer/nn-inkrenderer-iinkd2drenderer) permite a renderização de traços de tinta no contexto do dispositivo Direct2D designado de um aplicativo universal do Windows, em vez do controle [**InkCanvas**](/uwp/api/Windows.UI.Xaml.Controls.InkCanvas) padrão.

## <a name="members"></a>Membros

A classe **InkD2DRenderer** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **InkD2DRenderer** também tem estes tipos de membros:

- [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **InkD2DRenderer** tem esses métodos.

| Método                              | Descrição                                                                             |
|:------------------------------------|:----------------------------------------------------------------------------------------|
| [**Draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) | Renderiza o traço de tinta para o contexto de dispositivo Direct2D designado do aplicativo.<br/> |

## <a name="creationaccess-functions"></a>Criar \\ funções de acesso

Chame [<strong>CoCreateInstance</strong>](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o identificador de classe <strong>InkD2DRenderer</strong> para recuperar uma referência ao objeto.

``` C++
CoCreateInstance(__uuidof(InkD2DRenderer),
  nullptr,
  CLSCTX_INPROC_SERVER,
  IID_PPV_ARGS(&_spInkD2DRenderer));
```

## <a name="examples"></a>Exemplos

Este trecho de código do arquivo "SceneComposer. cpp" do [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/) demonstra a renderização de uma coleção de traços de tinta em um contexto de dispositivo Direct2D.

```C++
_inkRenderer->Render(strokes, _deviceResources->GetD2DDeviceContext());
strokes->Clear();
```

Este trecho de código do arquivo "InkRenderer. cpp" do [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/) mostra o método de renderização (chamado no trecho anterior) que chama o método [**draw**](/windows/win32/api/inkrenderer/nf-inkrenderer-iinkd2drenderer-draw) para renderizar os traços.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                  |
| parâmetro<br/>                   | <dl> <dt>Inkrenderer. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Inkrenderer. idl</dt> </dl> |
| IID<br/>                      | IID \_ IInkD2DRenderer é definido como 4044e60c-7b01-4671-a97c-04e0210a07a5<br/>         |

## <a name="related-topics"></a>Tópicos relacionados

[Processador de tinta](ink-renderer.md), [interações de caneta e](/windows/uwp/design/input/pen-and-stylus-interactions)caneta, [exemplo de análise de tinta](/samples/microsoft/windows-universal-samples/inkanalysis/), exemplo de [escrita simples](/samples/microsoft/windows-universal-samples/simpleink/), [exemplo de escrita complexa](/samples/microsoft/windows-universal-samples/complexink/)
