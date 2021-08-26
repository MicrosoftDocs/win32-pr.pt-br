---
description: Método IPortableDevicePropVariantCollection::Add – o método Add adiciona um item à coleção.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: Método IPortableDevicePropVariantCollection::Add (PortableDeviceTypes.h)
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
ms.openlocfilehash: fd90e4702045200e4f2766f6dcdd661ff83b6cd3370970a22e3211eebfa13c90
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120055256"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a>Método IPortableDevicePropVariantCollection::Add

O **método** Add adiciona um item à coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pValue* \[ Em\]
</dt> <dd>

Ponteiro para um novo **objeto PROPVARIANT** a ser adicionar à coleção. Esse método copia o **PROPVARIANT** para a coleção, portanto, você deve liberar sua cópia local da variável chamando **PropVariantClear** depois de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Quando o VARTYPE para *pValue* for VT VECTOR ou \_ VT \_ UI1, não há suporte para a configuração e a recuperação de um buffer **NULL** ou de tamanho zero. Por exemplo, nem pValue.caub.pElems = **NULL** nem pValue.caub.cElems = 0 são permitidos.

Se um chamador tentar adicionar um item de um VARTYPE diferente contido na coleção e o valor PROPVARIANT não puder ser alterado automaticamente por essa interface, esse método falhará. Para alterar o tipo de coleção manualmente, chame [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).

## <a name="examples"></a>Exemplos

Para ver um exemplo de como usar esse método, consulte Recuperando um [identificador de objeto de um identificador exclusivo persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Movendo o conteúdo no dispositivo](moving-content-on-the-device.md)
</dt> <dt>

[Recuperando um identificador de objeto de um identificador exclusivo persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




