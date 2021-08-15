---
description: O tipo de enumeração DELETE OBJECT OPTIONS descreve as opções com suporte de um \_ dispositivo ao excluir um objeto \_ .
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: DELETE_OBJECT_OPTIONS enumeração (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 018c47a383a4fcd95d25bd13b00628678c6fa4a71e608f82544429020ea3f2c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194862"
---
# <a name="delete_object_options-enumeration"></a>\_Enumeração DELETE OBJECT \_ OPTIONS

O **tipo \_ de \_ enumeração DELETE OBJECT OPTIONS** descreve as opções com suporte de um dispositivo ao excluir um objeto .

## <a name="syntax"></a>Syntax


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**DISPOSITIVO \_ \_ PORTÁTIL EXCLUIR \_ NENHUMA \_ RECURSÃO**
</dt> <dd>

Exclua o objeto somente e falhe se ele tiver filhos.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**EXCLUSÃO \_ DE \_ DISPOSITIVO \_ PORTÁTIL COM \_ RECURSÃO**
</dt> <dd>

Exclua o objeto e todos os seus filhos.

</dd> </dl>

## <a name="remarks"></a>Comentários

O aplicativo pode recuperar as opções de exclusão compatíveis com o dispositivo chamando [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) para o **comando WPD \_ COMMAND OBJECT MANAGEMENT DELETE \_ \_ \_ \_ OBJECTS.** Ele deve examinar o valor da opção **WPD \_ OPTION OBJECT MANAGEMENT \_ \_ \_ RECURSIVE \_ DELETE \_ SUPPORTED** que esse método retorna em [**um objeto IPortableDeviceValuesCollection.**](iportabledevicevaluescollection.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




