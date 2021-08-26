---
description: Cria uma cópia da interface IEnumPortableDeviceConnectors atual.
ms.assetid: 64274cb0-1f57-481d-914f-41238cbe2f1b
title: Método IEnumPortableDeviceConnectors::Clone (Devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumPortableDeviceConnectors.Clone
api_type:
- COM
api_location:
- PortableDeviceGuids.lib
- PortableDeviceGuids.dll
ms.openlocfilehash: 53b9c49b5bf36571409cd49026d5d08fced80c3e43aee63d844abd481e51aa3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055326"
---
# <a name="ienumportabledeviceconnectorsclone-method"></a>Método IEnumPortableDeviceConnectors::Clone

O **método Clone** cria uma cópia da interface [**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md) atual.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Clone(
  [out] IEnumPortableDeviceConnectors **ppEnum
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ppEnum* \[ out\]
</dt> <dd>

O endereço de um ponteiro para uma interface [**IEnumPortableDeviceConnectors.**](ienumportabledeviceconnectors.md) O aplicativo de chamada deve liberar essa interface quando terminar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                                                                                                             |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                                                                                              |
| Cabeçalho<br/>                   | <dl> <dt>Devpkey.h; </dt> <dt>Portabledeviceconnectapi.h</dt> </dl> |
| Idl<br/>                      | <dl> <dt>Portabledeviceconnectapi.idl</dt> </dl>                                                                |
| Biblioteca<br/>                  | <dl> <dt>PortableDeviceGuids.lib</dt> </dl>                                                                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IEnumPortableDeviceConnectors**](ienumportabledeviceconnectors.md)
</dt> </dl>

 

 




