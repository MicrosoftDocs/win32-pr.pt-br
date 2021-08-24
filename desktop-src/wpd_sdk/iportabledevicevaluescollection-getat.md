---
description: Método IPortableDeviceValuesCollection::GetAt – o método GetAt recupera um item da coleção por um índice baseado em zero.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: Método IPortableDeviceValuesCollection::GetAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 089c6c5c523b6f05f91efb5524904c942a539a7ebbb3cd863c1c07d413cdf1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704626"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>Método IPortableDeviceValuesCollection::GetAt

O **método GetAt** recupera um item da coleção por um índice baseado em zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

**DWORD** que especifica um índice baseado em zero na coleção.

</dd> <dt>

*ppValues* \[ out\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) da coleção. O chamador é responsável por chamar **Release** nessa interface quando terminar com ela.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O índice de base zero passado estava fora do intervalo.<br/>             |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Um argumento de ponteiro necessário era **NULL.**<br/>                             |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | A coleção contém um **ponteiro NULL** **IPortableDeviceValues.**<br/> |



 

## <a name="remarks"></a>Comentários

Todas as alterações feitas nos valores na interface recuperada serão feitas na versão armazenada na coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValuesCollection Interface**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




