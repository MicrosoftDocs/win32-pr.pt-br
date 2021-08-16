---
description: O \_ tipo de enumeração excluir opções de objeto \_ descreve as opções que têm suporte de um dispositivo ao excluir um objeto.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Enumeração de DELETE_OBJECT_OPTIONS (PortableDevice. h)
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
# <a name="delete_object_options-enumeration"></a>Enumeração de opções de excluir \_ objeto \_

O tipo de enumeração **excluir \_ \_ Opções de objeto** descreve as opções que têm suporte de um dispositivo ao excluir um objeto.

## <a name="syntax"></a>Syntax


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**\_exclusão de dispositivo portátil \_ \_ sem \_ recursão**
</dt> <dd>

Exclua apenas o objeto e falhe se ele tiver filhos.

</dd> <dt>

<span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_ \_ exclusão de dispositivo portátil \_ com \_ recursão**
</dt> <dd>

Exclua o objeto e todos os seus filhos.

</dd> </dl>

## <a name="remarks"></a>Comentários

O aplicativo pode recuperar as opções de exclusão que o dispositivo suporta chamando [**IPortableDeviceCapabilities:: Getcommandoptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) para o comando de **\_ \_ \_ \_ excluir \_ objetos do gerenciamento** de objetos de comando WPD. Ele deve examinar o valor de opção de **\_ \_ \_ exclusão recursiva do objeto de opção WPD \_ \_ \_ com suporte** que esse método retorna em um objeto [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Estruturas e tipos de enumeração**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




