---
title: Método IsAvailable IWMPCdromBurn
description: O método IsAvailable fornece informações sobre a unidade de CD e a mídia.
ms.assetid: 75e81f5f-5839-4012-b0b9-e77b3ca6f35c
keywords:
- método IsAvailable Windows Media Player
- método IsAvailable Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método IsAvailable
topic_type:
- apiref
api_name:
- IWMPCdromBurn.isAvailable
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3d604cb9d9e170a3837fbd477db4c7ff309e1df
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780377"
---
# <a name="iwmpcdromburnisavailable-method"></a>Método IWMPCdromBurn:: IsAvailable

O método **IsAvailable** fornece informações sobre a unidade de CD e a mídia.

## <a name="syntax"></a>Sintaxe


```CSharp
public System.Boolean isAvailable(
  System.String bstrItem
);
```


```VB

Public Function isAvailable( _
  ByVal bstrItem As System.String _
) As System.Boolean
Implements IWMPCdromBurn.isAvailable
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bstrItem* \[ no\]
</dt> <dd>

Um **System. String** que contém um dos valores a seguir.



| Valor | Descrição                 |
|-------|-----------------------------|
| Queima  | A unidade é um gravador de CD.   |
| Discos  | Há um CD na unidade. |
| Apagar | O CD pode ser apagado.       |
| Gravar | O CD pode ser gravado.   |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um **System. Boolean** que indica o resultado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> </dl>

 

 





