---
title: Método IWMPMedia3 getAttributeCountByType
description: O método getAttributeCountByType retorna o número de atributos associados ao tipo de atributo especificado.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- método getAttributeCountByType Windows Media Player
- método getAttributeCountByType Windows Media Player, interface IWMPMedia3
- Interface IWMPMedia3 Windows Media Player, método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPMedia3.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49505f9e9df8778cc2c17ba062da6700b9b8aec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811777"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>Método IWMPMedia3:: getAttributeCountByType

O método **getAttributeCountByType** retorna o número de atributos associados ao tipo de atributo especificado.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getAttributeCountByType(
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPMedia3.getAttributeCountByType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrtype* \[ no\]
</dt> <dd>

Um **System. String** que é o tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ no\]
</dt> <dd>

Um **System. String** que é o idioma. Se o valor for definido como NULL ou uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Int32** que é a contagem de atributos que estão associados ao tipo.

## <a name="remarks"></a>Comentários

Esse método é usado para descobrir o número de atributos correspondentes a um nome de atributo específico para um determinado item de mídia. Os números de índice podem então ser passados para o método **getItemInfoByType** . Isso é útil, por exemplo, quando um item de mídia é categorizado em vários gêneros.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3. getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





