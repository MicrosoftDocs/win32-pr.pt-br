---
description: Método IPortableDeviceValues::GetCount – o método GetCount recupera o número de itens na coleção.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: Método IPortableDeviceValues::GetCount (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f53bd254699360de760a9ff60d385020b9c48213d19ce40d53b5b3ebc5ce56e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194107"
---
# <a name="iportabledevicevaluesgetcount-method"></a>Método IPortableDeviceValues::GetCount

O **método GetCount** recupera o número de itens na coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pcelt* \[ Em\]
</dt> <dd>

Ponteiro para um **DWORD** que contém o número de itens na coleção.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> </dl>

 

 




