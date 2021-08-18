---
description: O método CopyValuesToPropertyStore copia todos os valores de uma coleção para uma interface IPropertyStore.
ms.assetid: 417a8723-fa46-44c8-9bdc-412c0f20969a
title: 'Método IPortableDeviceValues:: CopyValuesToPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesToPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2d134cb61831426451b1c6068bde5ca787b027fbe5b153587b45d9693ef739c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118697243"
---
# <a name="iportabledevicevaluescopyvaluestopropertystore-method"></a>Método IPortableDeviceValues:: CopyValuesToPropertyStore

O método **CopyValuesToPropertyStore** copia todos os valores de uma coleção para uma interface **IPropertyStore** .

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyValuesToPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstore* \[ no\]
</dt> <dd>

Ponteiro para um objeto de repositório.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Este método não converte valores de VT \_ LPWSTR em VT \_ BSTR. Muitos aplicativos externos ou componentes que se comunicam com seu aplicativo, como alguns aplicativos de Shell, usam a interface **IPropertyStore** . Esse método fornece uma maneira rápida e fácil de trocar dados com esses programas.

esse método tem suporte no Windows Vista e em versões posteriores do Windows.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::CopyValuesFromPropertyStore**](iportabledevicevalues-copyvaluesfrompropertystore.md)
</dt> </dl>

 

 




