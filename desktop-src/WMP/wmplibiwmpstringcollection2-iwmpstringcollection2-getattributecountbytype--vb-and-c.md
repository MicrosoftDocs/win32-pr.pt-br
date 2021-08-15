---
title: Método IWMPStringCollection2 getAttributeCountByType
description: O método getAttributeCountByType retorna o número de atributos associados ao índice de coleção de cadeia de caracteres especificado, ao nome do atributo e ao idioma.
ms.assetid: 30312039-3676-4322-b6f6-fb86098bf578
keywords:
- Windows Media Player do método getAttributeCountByType
- método getAttributeCountByType Windows Media Player, interface IWMPStringCollection2
- Windows Media Player de interface IWMPStringCollection2, método getAttributeCountByType
topic_type:
- apiref
api_name:
- IWMPStringCollection2.getAttributeCountByType
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c236d03cad0612d8306b8ccde370136cb9b31acca82e0aa52761ed56fb4b9bb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118330910"
---
# <a name="iwmpstringcollection2getattributecountbytype-method"></a>Método IWMPStringCollection2:: getAttributeCountByType

O método **getAttributeCountByType** retorna o número de atributos associados ao índice de coleção de cadeia de caracteres especificado, ao nome do atributo e ao idioma.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Int32 getAttributeCountByType(
  System.Int32 lCollectionIndex,
  System.String bstrType,
  System.String bstrLanguage
);
```


```VB

Public Function getAttributeCountByType( _
  ByVal lCollectionIndex As System.Int32, _
  ByVal bstrType As System.String, _
  ByVal bstrLanguage As System.String _
) As System.Int32
Implements IWMPStringCollection2.getAttributeCountByType
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lCollectionIndex* \[ no\]
</dt> <dd>

O **System. Int32** que especifica o índice de base zero do item de coleção de cadeia de caracteres a partir do qual obter o atributo.

</dd> <dt>

*bstrtype* \[ no\]
</dt> <dd>

O **System. String** que é o nome do atributo.

</dd> <dt>

*bstrLanguage* \[ no\]
</dt> <dd>

O **System. String** que é o nome do idioma. Se o valor for definido como NULL ou para uma cadeia de caracteres de comprimento zero (""), a cadeia de caracteres de localidade atual será usada. Caso contrário, o valor deve ser uma cadeia de caracteres de linguagem RFC 1766 válida, como "en-US".

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O **System. Int32** que é a contagem.

## <a name="remarks"></a>Comentários

Esse método é usado para descobrir o número de atributos correspondentes a um determinado nome de atributo para um determinado item **StringCollection** . Os números de índice podem então ser passados para o quarto parâmetro do método **getItemInfoByType** .

Para usar esse método, é necessário ter acesso de leitura à biblioteca. Para obter mais informações, consulte [acesso à biblioteca](library-access.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
</dt> <dt>

[**IWMPStringCollection2. getItemInfoByType (VB e C#)**](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)
</dt> </dl>

 

 





