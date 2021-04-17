---
description: Vários subtipos são definidos para vídeo DV. Cada um tem um código FOURCC e um valor GUID correspondente. Nem todos esses formatos têm suporte; consulte a seção comentários para obter mais informações.
ms.assetid: d8390bd4-0339-4955-992c-92b8c9f6bf88
title: Subtipos de vídeo DV (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbacb15f5801d959fbc5150546cff04dea687753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770080"
---
# <a name="dv-video-subtypes"></a>Subtipos de vídeo DV

Vários subtipos são definidos para vídeo DV. Cada um tem um código FOURCC e um valor GUID correspondente. Nem todos esses formatos têm suporte; consulte a seção comentários para obter mais informações.

## <a name="consumer-formats"></a>Formatos de consumidor



| FOURCC | GUID               | Taxa de dados | Descrição                  |
|--------|--------------------|-----------|------------------------------|
| 'dvsl' | MEDIASUBTYPE \_ dvsl | 12,5 Mbps | SD-DVCR (525-60 ou 625-50)   |
| 'dvsd' | MEDIASUBTYPE \_ dvsd | 25 Mbps   | SDL-DVCR (525-60 ou 625-50)  |
| 'dvhd' | MEDIASUBTYPE \_ dvhd | 50 Mbps   | HD-DVCR (1125-60 ou 1250-50) |



 

Consulte IEC-61834 para obter mais informações sobre esses formatos.

## <a name="professional-formats"></a>Formatos profissionais



| FOURCC | GUID               | Taxa de dados | Descrição                                 |
|--------|--------------------|-----------|---------------------------------------------|
| 'dv25' | MEDIASUBTYPE \_ DV25 | 25 Mbps   | DVCPRO 25 (525-60 ou 625-50).               |
| 'dv50' | MEDIASUBTYPE \_ DV50 | 50 Mbps   | DVCPRO 50 (525-60 ou 625-50)                |
| 'dvh1' | MEDIASUBTYPE \_ dvh1 | 100 Mbps  | DVCPRO 100 (1080/60i, 1080/50i ou 720/60P) |



 

Consulte o SMPTE 314M para obter mais informações sobre DV25 e DV50 e SMPTE 370M para obter mais informações sobre dvh1.

## <a name="miscellaneous"></a>Diversos

Dois subtipos de DV adicionais são definidos no arquivo de cabeçalho UUIDs. h. Eles correspondem a códigos FOURCC que são produzidos por determinados codecs de DV; Eles não correspondem a nenhum padrão de DV definido. Esses subtipos são obsoletos e não devem ser usados.



| FOURCC | GUID               |
|--------|--------------------|
| DVCS | MEDIASUBTYPE \_ DVCS |
| 'DVSD' | MEDIASUBTYPE \_ DVSD |



 

## <a name="remarks"></a>Comentários

A tabela a seguir mostra as taxas de dados com suporte, em megabits por segundo (Mbps), para os drivers MSDV e UVC.



| Sistema operacional                                                                 | Driver MSDV (IEEE 1394) | Driver UVC    |
|----------------------------------------------------------------------------------|-------------------------|---------------|
| Windows XP Service Pack 1 ou anterior                                             | 12,5, 25                | Não disponível |
| Windows XP Service Pack 2 ou posterior, Windows Server 2003 Service Pack 1 ou posterior. | 12,5, 25, 50, 100       | 12,5, 25      |



 

Para fluxos de 25 Mbps, o comportamento do driver MSDV foi alterado no Windows Vista antes do Windows Vista, o driver MSDV sempre definiu o tipo de mídia como MEDIASUBTYPE \_ dvsd para fluxos de 25 Mbps, independentemente de a origem ser o SDL-DVCR ou DVCPRO 25. O tipo de mídia ' DV25 ' não foi usado. A partir do Windows Vista, o driver MSDV agora distingue entre esses dois formatos. Para o SDL-DVCR, ele continua a usar o subtipo ' dvsd '. Para o DVCPRO 25, ele agora usa o subtipo ' DV25 '.

Os filtros de [revisor](dv-splitter-filter.md) de vídeo do DirectShow e do [codificador DV Video](dv-video-decoder-filter.md) dão suporte apenas aos formatos SDL-DVCR. Os dados podem ser PAL ou NTSC. Filtros ou codecs de terceiros podem estar disponíveis e podem analisar outros formatos de DV, desde que a taxa de dados seja suportada pelo driver MSDV ou UVC.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Vídeo digital no DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Driver MSDV](msdv-driver.md)
</dt> <dt>

[Subtipos de vídeo](video-subtypes.md)
</dt> </dl>

 

 




