---
description: Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: Propriedade MFPKEY_PRODUCEDUMMYFRAMES (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165378"
---
# <a name="mfpkey_producedummyframes-property"></a>\_Propriedade MFPKEY PRODUCEDUMMYFRAMES

Especifica se o codificador produz entradas de quadro fictícias no fluxo de bits para quadros duplicados.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCProduceDummyFrames

## <a name="data-type"></a>Tipo de Dados

BOOL do VT \_

## <a name="default-value"></a>Valor padrão

VARIANTE \_ falso

## <a name="remarks"></a>Comentários

Se esse valor for VARIANT \_ false, o codec não colocará nenhum dado no fluxo de bits para quadros duplicados.

Quadros fictícios podem ser importantes em aplicativos em que os números de quadro são persistidos. Um exemplo comum é quando os códigos de tempo SMPTE são mantidos para conteúdo codificado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




