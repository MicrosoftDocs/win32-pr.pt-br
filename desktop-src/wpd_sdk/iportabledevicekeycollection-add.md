---
description: O método add adiciona uma chave de propriedade à coleção.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Método IPortableDeviceKeyCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6aa28a7a8a6439f27a095033d35e8b066c1488af13d1ade921f16c4143843adf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118194716"
---
# <a name="iportabledevicekeycollectionadd-method"></a>Método IPortableDeviceKeyCollection:: Add

O método **Add** adiciona uma chave de propriedade à coleção.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Chave* \[ no\]
</dt> <dd>

Um **REFPROPERTYKEY** a ser adicionado à coleção. Esse método copia a chave para a coleção, para que você possa liberar a variável local depois de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT**. Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                                   | Descrição                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                                  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Não há memória suficiente disponível para adicionar a chave à coleção.<br/> |



 

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [Recuperando propriedades de um único objeto](retrieving-properties-for-a-single-object.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes. h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs. lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)
</dt> <dt>

[Recuperando propriedades de conteúdo-objeto](retrieving-content-object-properties.md)
</dt> <dt>

[Recuperando propriedades de um único objeto](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[Recuperando os recursos de renderização suportados por um dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




