---
description: O método CopyValuesFromPropertyStore copia o conteúdo de um IPropertyStore na coleção.
ms.assetid: 887c9569-ff76-41cf-8782-62c59c04e831
title: 'Método IPortableDeviceValues:: CopyValuesFromPropertyStore (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.CopyValuesFromPropertyStore
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fbc2508d300fe4d0680d539153fde5f86603e04d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791272"
---
# <a name="iportabledevicevaluescopyvaluesfrompropertystore-method"></a>Método IPortableDeviceValues:: CopyValuesFromPropertyStore

O método **CopyValuesFromPropertyStore** copia o conteúdo de um **IPropertyStore** na coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT CopyValuesFromPropertyStore(
  [in] IPropertyStore *pStore
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pstore* \[ no\]
</dt> <dd>

Ponteiro para um **IPropertyStore** a ser copiado para a coleção.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Esse método converte automaticamente todos os valores **VT \_ BSTR** em valores de **VT \_ LPWSTR** .

Muitos aplicativos externos ou componentes que se comunicam com seu aplicativo, como alguns aplicativos de Shell, usam a interface **IPropertyStore** . Esse método fornece uma maneira rápida e fácil de trocar dados com esses programas.

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

[**IPortableDeviceValues::CopyValuesToPropertyStore**](iportabledevicevalues-copyvaluestopropertystore.md)
</dt> </dl>

 

 




