---
description: Especifica o nível de economia de energia de um decodificador de vídeo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propriedade AVDecVideoSWPowerLevel (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c362e066a16e333cda402704a720b5e1b0b8534f1b56536d32009e6fa29663
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824216"
---
# <a name="avdecvideoswpowerlevel-property"></a>Propriedade AVDecVideoSWPowerLevel

Especifica o nível de economia de energia de um decodificador de vídeo.

Essa propriedade é leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valor da propriedade

O intervalo de valores possíveis \[ é 0,.100 \] , inclusive, com o seguinte significado.



| Valor | Descrição                 |
|-------|-----------------------------|
| 0     | Otimizar para a vida útil da bateria.  |
| 100   | Otimizar para qualidade de vídeo. |



 

A [**enumeração eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) define algumas constantes específicas dentro desse intervalo.

## <a name="remarks"></a>Comentários

Você pode definir essa propriedade durante a reprodução para alterar o nível de economia de energia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[ aplicativos UWP da área de \| trabalho\]<br/>                     |
| Servidor mínimo com suporte<br/> | Windows aplicativos da área de trabalho do servidor 2000 \[ \| aplicativos UWP\]<br/>                           |
| Cabeçalho<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do Codec](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI Interface**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




