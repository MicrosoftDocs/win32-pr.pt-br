---
title: Mensagem de DRV_INSTALL (mmsystem. h)
description: Notifica o driver que está sendo instalado. O driver deve criar e inicializar quaisquer chaves e valores de registro necessários e verificar se os drivers de suporte e o hardware estão instalados e corretamente configurados.
ms.assetid: 8ee7b30b-600b-49f3-93a7-8faa7b87cfd8
keywords:
- Multimídia do Windows de mensagem DRV_INSTALL
topic_type:
- apiref
api_name:
- DRV_INSTALL
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c91c71a4cb65bfaffa07bf16e09bec0d16b7b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919147"
---
# <a name="drv_install-message"></a>Mensagem de instalação do DRV \_

Notifica o driver que está sendo instalado. O driver deve criar e inicializar quaisquer chaves e valores de registro necessários e verificar se os drivers de suporte e o hardware estão instalados e corretamente configurados.

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

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Endereço de uma estrutura [**DRVCONFIGINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-drvconfiginfo) ou **NULL**. Se uma estrutura for fornecida, ela conterá os nomes da chave do registro e do valor associado ao driver.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna um destes valores:



| Requisito | Valor |
|-----------------|--------------------------------------------------------------------------------------------|
| DRVCNF \_ OK      | A instalação foi bem-sucedida; nenhuma ação adicional é necessária.                             |
| DRVCNF \_ cancelar  | Falha na instalação..                                                                  |
| \_reinicialização DRVCNF | A instalação foi bem-sucedida, mas não entrará em vigor até que o sistema seja reiniciado. |



 

## <a name="remarks"></a>Comentários

O parâmetro *lParam1* não é usado.

Alguns drivers instaláveis acrescentam informações de configuração ao valor atribuído ao valor de registro associado ao driver.

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

 

