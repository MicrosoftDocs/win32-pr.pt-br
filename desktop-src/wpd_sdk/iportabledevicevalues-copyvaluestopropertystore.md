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
ms.openlocfilehash: d6ab6b4614c336d3e0da50c0291b2e69a260ae1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797958"
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

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Este método não converte valores de VT \_ LPWSTR em VT \_ BSTR. Muitos aplicativos externos ou componentes que se comunicam com seu aplicativo, como alguns aplicativos de Shell, usam a interface **IPropertyStore** . Esse método fornece uma maneira rápida e fácil de trocar dados com esses programas.

Esse método tem suporte no Windows Vista e em versões posteriores do Windows.

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

 

 




