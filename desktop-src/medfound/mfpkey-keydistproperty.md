---
description: Especifica o tempo máximo, em milissegundos, entre quadros-chave na saída do codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: MFPKEY_KEYDIST propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d3c59e3002cff6d0962f0ebf77dc20b2858ab5db3cfda8acceb9c5577d7cb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689925"
---
# <a name="mfpkey_keydist-property"></a>Propriedade MFPKEY \_ KEYDIST

Especifica o tempo máximo, em milissegundos, entre quadros-chave na saída do codec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCKeyframeDistance

## <a name="data-type"></a>Tipo de Dados

VT \_ I4

## <a name="default-value"></a>Valor padrão

O valor padrão depende de qual versão do Windows está em execução, conforme mostrado na tabela a seguir.



| Sistema operacional | Valor padrão |
|------------------|---------------|
| Windows XP       | 8000          |
| Windows Vista    | 8000          |
| Windows 7        | 2000          |



 

## <a name="remarks"></a>Comentários

A lógica interna do codec determina o local real de cada quadro-chave. A distância entre dois quadros-chave pode ser menor que o valor dessa propriedade, no entanto, ela nunca será maior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




