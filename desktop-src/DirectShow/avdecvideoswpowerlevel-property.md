---
description: Especifica o nível de economia de energia de um decodificador de vídeo.
ms.assetid: 7e2ff8be-b21f-4833-a165-0112d4220677
title: Propriedade AVDecVideoSWPowerLevel (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1196c45cf038085856b1d63a5cd3a1c7dc350d0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105756833"
---
# <a name="avdecvideoswpowerlevel-property"></a>Propriedade AVDecVideoSWPowerLevel

Especifica o nível de economia de energia de um decodificador de vídeo.

Esta propriedade é de leitura/gravação.

## <a name="data-type"></a>Tipo de dados

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>GUID da propriedade

**CODECAPI \_ AVDecVideoSWPowerLevel**

## <a name="property-value"></a>Valor da propriedade

O intervalo de valores possíveis é \[ 0.. 100 \] , inclusive, com o significado a seguir.



| Valor | Descrição                 |
|-------|-----------------------------|
| 0     | Otimizar para a vida útil da bateria.  |
| 100   | Otimizar para qualidade de vídeo. |



 

A enumeração [**eAVDecVideoSWPowerLevel**](/windows/desktop/api/codecapi/ne-codecapi-eavdecvideoswpowerlevel) define algumas constantes específicas dentro desse intervalo.

## <a name="remarks"></a>Comentários

Você pode definir essa propriedade durante a reprodução para alterar o nível de economia de energia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]<br/>                     |
| Servidor mínimo com suporte<br/> | Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]<br/>                           |
| parâmetro<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades da API do codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




