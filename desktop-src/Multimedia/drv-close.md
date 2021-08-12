---
title: DRV_CLOSE mensagem (Mmsystem.h)
description: Direciona o driver para fechar a instância determinada. Se nenhuma outra instância estiver aberta, o driver deverá se preparar para a versão subsequente da memória.
ms.assetid: 98d7fe47-5194-4912-a9d6-3af3d1fa4e60
keywords:
- DRV_CLOSE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- DRV_CLOSE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d89be1821b03e43fbe05b5ed2efc90e40db03e36538cf0412201baa7273e596
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622663"
---
# <a name="drv_close-message"></a>Mensagem DRV \_ CLOSE

Direciona o driver para fechar a instância determinada. Se nenhuma outra instância estiver aberta, o driver deverá se preparar para a versão subsequente da memória.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador do driver instalável. Esse é o mesmo valor retornado anteriormente pelo driver da [**mensagem DRV \_ OPEN.**](drv-open.md)

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Lidar com a instância do driver instanciada.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Valor de 32 bits especificado como o *parâmetro lParam1* em uma chamada para a **função DriverClose.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Valor de 32 bits especificado como o *parâmetro lParam2* em uma chamada para a **função DriverClose.**

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará diferente de zero se for bem-sucedido ou zero, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

 





