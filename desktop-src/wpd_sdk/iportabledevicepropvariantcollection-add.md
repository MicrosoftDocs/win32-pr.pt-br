---
description: 'Método IPortableDevicePropVariantCollection:: Add – o método add adiciona um item à coleção.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Método IPortableDevicePropVariantCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112454"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Método IPortableDevicePropVariantCollection:: Add

O método **Add** adiciona um item à coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valores* \[ no\]
</dt> <dd>

Ponteiro para um novo objeto **PROPVARIANT** para adicionar à coleção. Esse método copia o **PROPVARIANT** para a coleção, de modo que você deve liberar sua cópia local da variável chamando **PropVariantClear** depois de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Quando o VARTYPE de  zero é VT \_ vector ou VT \_ UI1, não há suporte para a configuração e a recuperação de um buffer de tamanho **nulo** ou zero. Por exemplo, não há um zero. caub. pElems = **NULL** nem 1. caub. cElems = 0 são permitidos.

Se um chamador tentar adicionar um item de um VARTYPE diferente contido na coleção e o valor de PROPVARIANT não puder ser alterado por essa interface automaticamente, esse método falhará. Para alterar o tipo de coleção manualmente, chame [**IPortableDevicePropVariantCollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [recuperando um identificador de objeto de um identificador exclusivo persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**Interface IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Movendo o conteúdo no dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recuperando um identificador de objeto de um identificador exclusivo persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




