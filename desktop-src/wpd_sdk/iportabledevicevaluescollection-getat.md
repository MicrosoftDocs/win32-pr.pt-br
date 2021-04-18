---
description: O método GetAt recupera um item da coleção por um índice baseado em zero.
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'Método IPortableDeviceValuesCollection:: GetAt (PortableDeviceTypes. h)'
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
ms.openlocfilehash: ffbc65f39aab63189aa451005008f585c46bd8d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793279"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a>Método IPortableDeviceValuesCollection:: GetAt

O método **GetAt** recupera um item da coleção por um índice baseado em zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ no\]
</dt> <dd>

**DWORD** que especifica um índice de base zero na coleção.

</dd> <dt>

*ppValues* \[ fora\]
</dt> <dd>

Endereço de uma variável que recebe um ponteiro para uma interface [**IPortableDeviceValues**](iportabledevicevalues.md) da coleção. O chamador é responsável por chamar o **lançamento** nessa interface quando feito com ele.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                                                 |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O índice de base zero que foi passado estava fora do intervalo.<br/>             |
| <dl> <dt>**\_ponteiro E**</dt> </dl>    | Um argumento de ponteiro necessário era **nulo**.<br/>                             |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | A coleção contém um ponteiro **IPortableDeviceValues** **nulo** .<br/> |



 

## <a name="remarks"></a>Comentários

Quaisquer alterações feitas aos valores na interface recuperada serão feitas na versão armazenada na coleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




