---
title: DRV_OPEN mensagem (Mmsystem.h)
description: Direciona o driver para abrir uma nova instância.
ms.assetid: 6b5e21e3-dc29-4f0f-84cb-bd2d2e3c54e9
keywords:
- DRV_OPEN mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- DRV_OPEN
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 537d3067c85cf3f92eaf2fae81cd392490ff9fa728ed8377d8241c7204cf64e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691576"
---
# <a name="drv_open-message"></a>Mensagem DRV \_ OPEN

Direciona o driver para abrir uma nova instância.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="dwDriverId"></span><span id="dwdriverid"></span><span id="DWDRIVERID"></span>*dwDriverId*
</dt> <dd>

Identificador do driver instalável.

</dd> <dt>

<span id="hdrvr"></span><span id="HDRVR"></span>*hdrvr*
</dt> <dd>

Lidar com a instância do driver instanciada.

</dd> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*Lparam1*
</dt> <dd>

Endereço de uma cadeia de caracteres largos terminada em nulo que especifica informações de configuração usadas para abrir a instância. Se nenhuma informação de configuração estiver disponível, essa cadeia de caracteres estará vazia ou o parâmetro será **NULL.**

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Dados específicos do driver de 32 bits.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará um valor diferente de zero se for bem-sucedido ou zero, caso contrário.

## <a name="remarks"></a>Comentários

Se o driver retornar um valor diferente de zero, o sistema usará esse valor como o identificador de driver (o *parâmetro dwDriverId)* nas mensagens que ele envia subsequentemente para a instância do driver. O driver pode retornar qualquer tipo de valor como o identificador. Por exemplo, alguns drivers retornam endereços de memória que apontam para informações específicas da instância. Usar esse método para especificar identificadores para uma instância de driver fornece aos drivers acesso pronto para as informações enquanto eles estão processando mensagens.

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

 

 





