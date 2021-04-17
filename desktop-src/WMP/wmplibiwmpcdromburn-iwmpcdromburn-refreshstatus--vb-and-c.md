---
title: Método IWMPCdromBurn refreshStatus
description: O método refreshStatus atualiza as informações de status para a lista de reprodução de gravação atual.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- método refreshStatus Windows Media Player
- método refreshStatus Windows Media Player, interface IWMPCdromBurn
- Interface IWMPCdromBurn Windows Media Player, método refreshStatus
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812293"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>Método IWMPCdromBurn:: refreshStatus

O método **refreshStatus** atualiza as informações de status para a lista de reprodução de gravação atual.

## <a name="syntax"></a>Sintaxe


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Você deve chamar esse método depois de criar ou alterar uma lista de reprodução de gravação antes de ler as informações de status ou gravar o CD. Você pode testar se uma atualização é necessária obtendo o valor de **burnstate** e verificando wmpbsRefreshStatusPending.

A atualização do status é uma operação síncrona. Isso significa que um longo período de tempo pode decorrer antes que esse método retorne se a lista de reprodução de gravação atual for grande e contiver muitas alterações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**IWMPCdromBurn. burnstate (VB e C#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





