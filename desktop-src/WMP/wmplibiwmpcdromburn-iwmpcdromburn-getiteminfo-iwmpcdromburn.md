---
title: Método IWMPCdromBurn getItemInfo
description: O método getItemInfo recupera o valor do atributo especificado para o CD.
ms.assetid: 9ca54ec4-42be-40c1-931e-c3bfcbc2b370
keywords:
- método getItemInfo Windows Media Player
- método getItemInfo Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método getItemInfo
topic_type:
- apiref
api_name:
- IWMPCdromBurn.getItemInfo
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9030bd230b2e17bab6ad54dc762a78d2cb343d03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768297"
---
# <a name="iwmpcdromburngetiteminfo-method"></a>Método IWMPCdromBurn:: getItemInfo

O método **getItemInfo** recupera o valor do atributo especificado para o CD.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.String getItemInfo(
  System.String bstrItem
);
```


```VB

Public Function getItemInfo( _
  ByVal bstrItem As System.String _
) As System.String
Implements IWMPCdromBurn.getItemInfo
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrItem* \[ no\]
</dt> <dd>

Um **System. String** que contém um dos valores a seguir.



| Valor         | Descrição                                                                                  |
|---------------|----------------------------------------------------------------------------------------------|
| Disponíveltime | Recupera o tempo disponível no CD, em segundos.                                          |
| Em branco         | Recupera um **System. Boolean** (representado como uma cadeia de caracteres) indicando se o CD está em branco. |
| FreeSpace     | Recupera o espaço livre no CD, em bytes.                                                |
| TotalSpace    | Recupera o espaço total no CD, em bytes.                                               |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. String** que é o valor do atributo especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11<br/>                                                                                     |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





