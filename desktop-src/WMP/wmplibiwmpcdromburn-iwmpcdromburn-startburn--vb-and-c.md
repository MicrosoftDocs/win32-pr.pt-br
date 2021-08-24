---
title: Método startEar IWMPCdrom Ltd
description: O método start Ltda para o CD.
ms.assetid: e852c011-5f54-469f-aead-37fa711ef876
keywords:
- Método start Ltda Windows Media Player
- Método startEar Windows Media Player , interface IWMPCdrom Ltd
- Interface IWMPCdrom Ltda Windows Media Player método , startEar
topic_type:
- apiref
api_name:
- IWMPCdromBurn.startBurn
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7806501a619d6172d9f1ce0715045c822b30326c2b59c268f432708ea13923ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761066"
---
# <a name="iwmpcdromburnstartburn-method"></a>Método IWMPCdrom Ltd::startEar

O **método start Ltda** para o CD.

## <a name="syntax"></a>Sintaxe


```CSharp
public void startBurn();
```


```VB

Public Sub startBurn()
Implements IWMPCdromBurn.startBurn
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O valor de **burnstate** deve ser wmpbsReady ou wmpbsStopped antes de chamar esse método.

Esse método não funcionará se a unidade de CD não for um ataque ou se o disco na unidade não for writable. Use **isAvailable para** determinar se um CD pode ser gravado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdrom Ltda (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromState.burnState (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom Deve.isAvailable (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-isavailable--vb-and-c.md)
</dt> <dt>

[**IWMPCdrom Ltd.stopEar (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-stopburn-iwmpcdromburn.md)
</dt> </dl>

 

 





