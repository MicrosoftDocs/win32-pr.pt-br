---
title: Mensagem de DRV_CONFIGURE (mmsystem. h)
description: Direciona o driver instalável para exibir sua caixa de diálogo de configuração e permitir que o usuário especifique novas configurações para a instância de driver instalável fornecida.
ms.assetid: 0d99fad7-ce79-4574-9fd8-262f7e758866
keywords:
- Multimídia do Windows de mensagem DRV_CONFIGURE
topic_type:
- apiref
api_name:
- DRV_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30a761e7bda7188e93b02e436f2e952bed61bee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919150"
---
# <a name="drv_configure-message"></a>Mensagem de configuração de DRV \_

Direciona o driver instalável para exibir sua caixa de diálogo de configuração e permitir que o usuário especifique novas configurações para a instância de driver instalável fornecida.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador do driver instalável. Esse é o mesmo valor retornado anteriormente pelo driver da mensagem de [**\_ abertura do drv**](drv-open.md) .

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Identificador da instância de driver instalável.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Identificador da janela pai. Essa janela é usada como a janela pai da caixa de diálogo de configuração.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **NULL**. Se a estrutura for fornecida, ela conterá os nomes da chave do registro e do valor associado ao driver.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um destes valores:



| Requisito | Valor |
|-----------------|----------------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | A configuração foi bem-sucedida; nenhuma ação adicional é necessária.                                    |
| DRVCNF \_ cancelar  | O usuário cancelou a caixa de diálogo; nenhuma ação adicional é necessária.                                   |
| \_reinicialização DRVCNF | A configuração foi bem-sucedida, mas as alterações não entram em vigor até que o sistema seja reiniciado. |



 

## <a name="remarks"></a>Comentários

Alguns drivers instaláveis acrescentam informações de configuração ao valor atribuído ao valor de registro associado ao driver.

Os valores de retorno do DRV \_ Cancel, drv \_ OK e drv \_ Restart são obsoletos; eles foram substituídos por DRVCNF \_ Cancel, DRVCNF \_ OK e DRVCNF \_ restart, respectivamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                      |
| Cabeçalho<br/>                   | <dl> <dt>Mmsystem. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Drivers instaláveis](installable-drivers.md)
</dt> <dt>

[Mensagens de driver instaláveis](installable-driver-messages.md)
</dt> </dl>

 

