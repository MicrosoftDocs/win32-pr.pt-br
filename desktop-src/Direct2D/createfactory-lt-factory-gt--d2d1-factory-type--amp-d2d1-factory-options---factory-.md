---
title: Função de fábrica D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Cria um objeto de fábrica que pode ser usado para criar recursos de Direct2D. | Função de fábrica D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105754074"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>D2D1CreateFactory <Factory> ( \_ \_ tipo de fábrica d2d1, \_ D2D1 \_ Opções de fábrica&, fábrica \* \* ) função

Cria um objeto de fábrica que pode ser usado para criar recursos de Direct2D.

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a>Parâmetros de modelo



| Parâmetro | Descrição                                                 |
|-----------|-------------------------------------------------------------|
| *Padrões* | O tipo de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) a ser criado. |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro        | Descrição                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | O modelo de Threading da fábrica e os recursos que ele cria.                |
| *factoryoptions* | O nível de detalhe fornecido à camada de depuração.                            |
| *fábrica*        | Quando esse método retorna, contém o endereço de um ponteiro para a nova fábrica. |



 

## <a name="return-value"></a>Valor Retornado

Se o método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e atualização de plataforma para aplicativos UWP do Windows Vista \[ Desktop apps \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e atualização de plataforma para aplicativos de aplicativos de desktop do Windows Server 2008 \[ \| UWP\]<br/> |
| Número mínimo de telefone com suporte<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 e aplicativos de Windows Runtime\]<br/>                                                  |
| parâmetro<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |
| Biblioteca<br/>                  | <dl> <dt>D2d1. lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

