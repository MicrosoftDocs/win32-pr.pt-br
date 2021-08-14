---
title: Método getAttributeCountByType de IWMPMedia3
description: O método getAttributeCountByType retorna o número de atributos associados ao tipo de atributo especificado.
ms.assetid: d692635f-f9f1-4d8e-a9c5-9d7fa84f41bd
keywords:
- Método getAttributeCountByType Windows Media Player
- Método getAttributeCountByType Windows Media Player interface , IWMPMedia3
- Interface IWMPMedia3 Windows Media Player , método getAttributeCountByType
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
ms.openlocfilehash: 2c8e3fc681ea5471457bd9a80ac3e26dabc08b2112387dd8c5f785bf5f055dfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000106"
---
# <a name="iwmpmedia3getattributecountbytype-method"></a>Método IWMPMedia3::getAttributeCountByType

O **método getAttributeCountByType** retorna o número de atributos associados ao tipo de atributo especificado.

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

*bstrType* \[ Em\]
</dt> <dd>

Um **System.String** que é o tipo de atributo.

</dd> <dt>

*bstrLanguage* \[ Em\]
</dt> <dd>

Um **System.String** que é o idioma. Se o valor for definido como nulo ou uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deverá ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-us".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um **System.Int32 que** é a contagem de atributos associados ao tipo.

## <a name="remarks"></a>Comentários

Esse método é usado para descobrir o número de atributos correspondentes a um nome de atributo específico para um determinado item de mídia. Os números de índice podem ser passados para o **método getItemInfoByType.** Isso é útil, por exemplo, quando um item de mídia foi categorizado em vários gêneros.

Antes de chamar esse método, você deve ter acesso de leitura à biblioteca. Para obter mais informações, consulte [Acesso à biblioteca.](library-access.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPMedia3 (VB e C#)**](iwmpmedia3--vb-and-c.md)
</dt> <dt>

[**IWMPMedia3.getItemInfoByType (VB e C#)**](wmplibiwmpmedia3-iwmpmedia3-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





