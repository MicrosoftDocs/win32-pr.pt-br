---
title: Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) (D2d1.h)
description: Cria um objeto de fábrica que pode ser usado para criar Direct2D recursos. | Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) (D2d1.h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af5635a6f996ea6cd3af2c3b3022efa054cd27605430c8230143980e00b9abbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117826465"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a>Função D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,Factory \* \* )

Cria um objeto de fábrica que pode ser usado para criar Direct2D recursos.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Parâmetros de modelo



| Parâmetro | Descrição                                                 |
|-----------|-------------------------------------------------------------|
| *Fábrica* | O tipo de [**ID2D1Factory a**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ser criado. |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro     | Descrição                                                                     |
|---------------|---------------------------------------------------------------------------------|
| *factoryType* | O modelo de threading da fábrica e os recursos que ele cria.                |
| *fábrica*     | Quando este método retorna, contém o endereço de um ponteiro para a nova fábrica. |



 

## <a name="return-value"></a>Valor Retornado

Se o método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="examples"></a>Exemplos

O exemplo a seguir cria uma fábrica.


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

