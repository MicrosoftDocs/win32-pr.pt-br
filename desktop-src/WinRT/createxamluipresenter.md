---
description: Uma função de criador estática que pode criar um XamlUIPresenter para uma superfície de renderização em um aplicativo de área de trabalho.
ms.assetid: 3160E4C2-39D3-8FF5-ED37-78E645D1AC2E
title: Função CreateXamlUIPresenter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateXamlUIPresenter
api_type:
- DllExport
api_location:
- Windows.UI.Xaml.dll
ms.openlocfilehash: f9561a179ec4501406e26cb2bbc38ea69b64b979
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761579"
---
# <a name="createxamluipresenter-function"></a>Função CreateXamlUIPresenter

Uma função de criador estática que pode criar um [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041) para uma superfície de renderização em um aplicativo de área de trabalho.

## <a name="syntax"></a>Sintaxe


```C++
 static HRESULT WINAPI CreateXamlUIPresenter(
  _In_  IViewObjectPresentNotifySite                 *pPresentSite,
  _Out_ Windows::UI::Xaml::Hosting::IXamlUIPresenter **ppPresenter
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pPresentSite* \[ no\]
</dt> <dd>

Uma interface de hospedagem existente. Consulte **IViewObjectPresentNotifySite** na documentação do Internet Explorer.

</dd> <dt>

*ppPresenter* \[ fora\]
</dt> <dd>

A interface **\[ \] exclusiveto** para um [**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **HRESULT** padrão, **S \_ OK** para sucesso.

## <a name="remarks"></a>Comentários

Chamar esse método requer um **DllImport** de Windows.UI.Xaml.dll.

Você não pode chamar esse método de um aplicativo da Windows Store.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Windows. UI. XAML-coretypes. idl</dt> </dl> |
| DLL<br/>    | <dl> <dt>Windows.UI.Xaml.dll</dt> </dl>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**XamlUIPresenter**](/uwp/api/Windows.UI.Xaml.Hosting.XamlUIPresenter?view=winrt-19041)
</dt> </dl>

 

 
