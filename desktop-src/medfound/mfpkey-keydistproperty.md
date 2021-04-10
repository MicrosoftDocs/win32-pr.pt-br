---
description: Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.
ms.assetid: 2a52e6a5-10a0-46dd-aa31-cb55094903b5
title: Propriedade MFPKEY_KEYDIST (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55925811db71f24cf360113aa6d03a325bcdc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827906"
---
# <a name="mfpkey_keydist-property"></a>\_Propriedade MFPKEY KEYdist

Especifica o tempo máximo, em milissegundos, entre os quadros-chave na saída do codec.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCKeyframeDistance

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




