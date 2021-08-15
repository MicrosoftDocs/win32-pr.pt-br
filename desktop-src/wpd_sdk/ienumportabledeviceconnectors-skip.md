---
description: Ignora o número especificado de dispositivos na sequência de enumeração.
ms.assetid: 38b72b80-93f5-433e-977c-e3ee503daae5
title: 'Método IEnumPortableDeviceConnectors:: Skip (Devpkey. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Skip
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: ba704a2dd232ce5c8ba08d0271e5e0a8fda72f86f9aef89d2e89b04ca9fe94b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119546546"
---
# <a name="ienumportabledeviceconnectorsskip-method"></a>Método IEnumPortableDeviceConnectors:: Skip

O método **Skip** ignora o número especificado de dispositivos na sequência de enumeração.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Skip(
  [in] UINT32 cConnectors
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*cConnectors* \[ no\]
</dt> <dd>

O número de dispositivos a serem ignorados.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                             | Descrição                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | O método foi bem-sucedido.<br/>                                                                                                                                                          |
| <dl> <dt>**\_falso**</dt> </dl> | O número especificado de dispositivos não pôde ser ignorado. Uma causa possível: o parâmetro *cConnectors* especifica mais dispositivos do que realmente permanecem na sequência de enumeração.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                                                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Devpkey. h; </dt> <dt>Portabledeviceconnectapi. h</dt> </dl> |
| INSERI<br/>                      | <dl> <dt>Portabledeviceconnectapi. idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids. lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




