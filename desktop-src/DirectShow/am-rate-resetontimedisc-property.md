---
description: propriedade AM_RATE_ResetOnTimeDisc – aplica-se ao Windows Vista e posterior.
ms.assetid: 3e342219-341e-49a2-9f8f-4188dd7bf719
title: Propriedade AM_RATE_ResetOnTimeDisc (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c42b8e9d158f644d9e630555d96bf4d06e4ea9ef3cddced67742c057d0ab3859
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120079516"
---
# <a name="am_rate_resetontimedisc-property"></a>Propriedade de ResetOnTimeDisc da \_ taxa de am \_

aplica-se ao Windows Vista e posterior.

Essa propriedade consulta se o decodificador ressincroniza os carimbos de hora de saída para os carimbos de hora de entrada quando o decodificador recebe um exemplo com o sinalizador de descontinuidade.

Esta propriedade é de leitura/gravação.



| Rótulo | Valor |
|-------------------|-------------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ TSRateChange |
| ID da propriedade       | \_ResetOnTimeDisc de taxa de am \_     |
| Tipo de Dados         | **DWORD**                     |



 

## <a name="remarks"></a>Comentários

Esta propriedade dá suporte a alterações de taxa suave. Se o valor dessa propriedade for **true** e o decodificador receber um exemplo de entrada com o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, o quadro decodificado deverá ter o mesmo carimbo de data/hora que o quadro de entrada.

Para recuperar o \_ sinalizador am Sample \_ TIMEDISCONTINUITY, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo. O sinalizador é definido no membro **dwSampleFlags** da estrutura de [**\_ \_ Propriedades am SAMPLE2**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) .

para obter mais informações, consulte [aprimoramentos de reprodução de DVD no Windows Vista](dvd-playback-enhancements-in-windows-vista.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




