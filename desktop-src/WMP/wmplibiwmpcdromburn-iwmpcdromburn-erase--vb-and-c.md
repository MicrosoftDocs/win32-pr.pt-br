---
title: Método de apagamento IWMPCdromBurn
description: O método Erase apaga o CD atual.
ms.assetid: ed0fbd7e-61a6-445a-bca5-ed2969d5cadc
keywords:
- método Erase Windows Media Player
- método erase Windows Media Player, interface IWMPCdromBurn
- Windows Media Player de interface IWMPCdromBurn, método erase
topic_type:
- apiref
api_name:
- IWMPCdromBurn.erase
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 356b7bcdd332198c40760860e69741e76e0e993b6b47b3c5a5ff207d3d55bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118116329"
---
# <a name="iwmpcdromburnerase-method"></a>Método IWMPCdromBurn:: Erase

O método **Erase** apaga o CD atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public void erase();
```


```VB

Public Sub erase()
Implements IWMPCdromBurn.erase
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método não funcionará se o disco na unidade não for regravável. Use [IWMPCdromBurn. IsAvailable](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md) para determinar se um CD pode ser apagado.

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

 

 





