---
description: 'Método IPortableDeviceValuesCollection:: GetCount – o método GetCount recupera o número de itens na coleção.'
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'Método IPortableDeviceValuesCollection:: GetCount (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 8304184f3323feb92a14b523dc629c6ae45f6a85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083174"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a>Método IPortableDeviceValuesCollection:: GetCount

O método **GetCount** recupera o número de itens na coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcElems* \[ no\]
</dt> <dd>

Ponteiro para um **DWORD** que contém o número de interfaces **IPortableDeviceValues** na coleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                               | Descrição                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | O método foi bem-sucedido.<br/>                     |
| <dl> <dt>**\_ponteiro E**</dt> </dl> | Um argumento de ponteiro necessário era **nulo**.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




