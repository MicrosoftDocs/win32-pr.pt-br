---
description: O método SetStringValue adiciona um novo valor de cadeia de caracteres (tipo VT LPWSTR) ou substitui \_ um existente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: Método IPortableDeviceValues::SetStringValue (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c00195823d71a59e706af1c0a627670f583776140772c3b8634ac10d7d95919
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806856"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a>Método IPortableDeviceValues::SetStringValue

O **método SetStringValue** adiciona um novo valor de cadeia de caracteres (tipo VT LPWSTR) ou substitui \_ um existente.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*chave* \[ Em\]
</dt> <dd>

Uma **REFPROPERTYKEY** que especifica o item a ser criado ou substituido.

</dd> <dt>

*Valor* \[ Em\]
</dt> <dd>

Um **LPCWSTR** que especifica o novo valor. A cadeia de caracteres é copiada para que o chamador possa liberar a memória alocada para esse valor depois de chamar esse método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O método retorna um **HRESULT.** Os possíveis valores incluem, mas sem limitação, aqueles na tabela a seguir.



| Código de retorno                                                                          | Descrição                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | O método foi bem-sucedido.<br/> |



 

## <a name="remarks"></a>Comentários

Qualquer memória de chave existente será liberada adequadamente.

## <a name="examples"></a>Exemplos

Para obter um exemplo de como usar esse método, consulte [Especificando informações do cliente](specifying-client-information.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>PortableDeviceTypes.h</dt> </dl>   |
| Biblioteca<br/> | <dl> <dt>PortableDeviceGUIDs.lib</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Adicionando um recurso a um objeto](adding-a-resource-to-an-object.md)
</dt> <dt>

[**IPortableDeviceValues Interface**](iportabledevicevalues.md)
</dt> <dt>

[**IPortableDeviceValues::GetStringValue**](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[Definindo propriedades para um único objeto](setting-properties-for-a-single-object.md)
</dt> <dt>

[Definindo propriedades para vários objetos](setting-properties-for-multiple-objects.md)
</dt> <dt>

[Especificando informações do cliente](specifying-client-information.md)
</dt> <dt>

[Escrevendo propriedades de objeto de conteúdo](writing-content-object-properties.md)
</dt> </dl>

 

 




