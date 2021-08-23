---
description: Método IPortableDevicePropVariantCollection::GetAt – o método GetAt recupera um item da coleção por um índice baseado em zero.
ms.assetid: c7119ba6-e6fc-4cb6-a8ab-3bf7b6bfe850
title: Método IPortableDevicePropVariantCollection::GetAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 02fa273b3bedea78884e15d2dedb5b7d2f675c78330c735e3bfb1896bc9d5199
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118963725"
---
# <a name="iportabledevicepropvariantcollectiongetat-method"></a>Método IPortableDevicePropVariantCollection::GetAt

O **método GetAt** recupera um item da coleção por um índice baseado em zero.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetAt(
  [in]  const DWORD       dwIndex,
  [out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwIndex* \[ Em\]
</dt> <dd>

**DWORD** que contém o índice baseado em zero do item a ser recuperado.

</dd> <dt>

*pValue* \[ out\]
</dt> <dd>

Ponteiro para uma **estrutura PROPVARIANT.** O chamador é responsável por liberar essa memória chamando **PropVariantClear**.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                  | Descrição                                               |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | O método foi bem-sucedido.<br/>                          |
| <dl> <dt>**PONTEIRO \_ E**</dt> </dl>    | Um argumento de ponteiro necessário era **NULL.**<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | O índice passado estava fora do intervalo.<br/> |



 

## <a name="examples"></a>Exemplos

Para ver um exemplo de como usar esse método, consulte Recuperando as [categorias](retrieving-the-functional-categories-supported-by-a-device.md)funcionais com suporte por um dispositivo .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IPortableDevicePropVariantCollection Interface**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[Recuperando um identificador de objeto de um identificador exclusivo persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> <dt>

[Recuperando eventos de serviço com suporte](retrieving-supported-events.md)
</dt> <dt>

[Recuperando formatos de serviço com suporte](retrieving-supported-formats.md)
</dt> <dt>

[Recuperando métodos de serviço com suporte](retrieving-supported-methods.md)
</dt> <dt>

[Recuperando os tipos de conteúdo com suporte por um dispositivo](retrieving-the-content-types-supported-by-a-device.md)
</dt> <dt>

[Recuperando as categorias funcionais com suporte por um dispositivo](retrieving-the-functional-categories-supported-by-a-device.md)
</dt> <dt>

[Recuperando os identificadores de objeto funcional para um dispositivo](retrieving-the-functional-object-identifiers-for-a-device.md)
</dt> <dt>

[Recuperando os recursos de renderização com suporte por um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[Definindo propriedades para vários objetos](setting-properties-for-multiple-objects.md)
</dt> </dl>

 

 




