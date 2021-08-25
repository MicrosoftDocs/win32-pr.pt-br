---
title: Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
description: Cria um objeto de fábrica que pode ser usado para criar Direct2D recursos. | Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) (D2d1.h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- Função D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Direct2D
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
ms.openlocfilehash: 34cbe566b139ebd873e8e9895aa21307113be9632b2045d40c099f52f49fc574
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119824686"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a>Função D2D1CreateFactory <Factory> (D2D1 \_ FACTORY \_ TYPE,D2D1 \_ FACTORY OPTIONS \_&,Factory \* \* )

Cria um objeto de fábrica que pode ser usado para criar Direct2D recursos.

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
| *Fábrica* | O tipo de [**ID2D1Factory a**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ser criado. |



 

## <a name="parameters"></a>Parâmetros



| Parâmetro        | Descrição                                                                     |
|------------------|---------------------------------------------------------------------------------|
| *factoryType*    | O modelo de threading da fábrica e os recursos que ele cria.                |
| *factoryOptions* | O nível de detalhes fornecido à camada de depuração.                            |
| *fábrica*        | Quando este método retorna, contém o endereço de um ponteiro para a nova fábrica. |



 

## <a name="return-value"></a>Valor Retornado

Se o método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7, Windows Vista com SP2 e Atualização de Plataforma para Windows aplicativos \[ UWP da área de trabalho do Vista \|\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows Server 2008 R2, Windows Server 2008 com SP2 e Atualização de Plataforma para aplicativos \[ UWP do Windows Server 2008 \|\]<br/> |
| Telefone mínimo com suporte<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 e Windows runtime\]<br/>                                                  |
| Cabeçalho<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |
| Biblioteca<br/>                  | <dl> <dt>D2d1.lib</dt> </dl>                                                      |
| DLL<br/>                      | <dl> <dt>D2d1.dll</dt> </dl>                                                      |



 

