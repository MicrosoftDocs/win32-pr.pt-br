---
description: Quando o filtro de navegador de DVD entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade AM \_ \_ DVDKARAOKE \_ Enable Property.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propriedades de karaokê de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e9fe53ad35dac0c3c0f54a8e04a6fbe698fc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780637"
---
# <a name="dvd-karaoke-property-set"></a>Conjunto de propriedades de karaokê de DVD

Quando o filtro de [navegador de DVD](dvd-navigator-filter.md) entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade **am \_ \_ DVDKARAOKE \_ Enable** Property. O decodificador deve ativar mudo dos canais de áudio de 2 a 5 até que ele receba do navegador de DVD uma propriedade **am \_ \_ DVDKARAOKE \_ data de propriedade** com um ponteiro para uma estrutura de dados [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) indicando como os canais auxiliares devem ser misturados.



|                   |                             |
|-------------------|-----------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ DvdKaraoke |



 



| ID da propriedade                      | Descrição                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ habilitar DVDKARAOKE de propriedade am \_ | Valor BOOLIANo. O navegador de DVD envia o decodificador que uma \_ Propriedade am \_ DVDKARAOKE \_ habilita com um valor de **true** para habilitar o karaokê downmixing ou **false** para desabilitá-lo.                                                                                                                                    |
| \_dados da propriedade am \_ DVDKARAOKE \_   | O navegador de DVD envia o decodificador uma \_ propriedade de dados DVDKARAOKE de propriedade am \_ \_ com um ponteiro para uma estrutura [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) para alterar a configuração de downmix, ou seja, para ativar ou desativar determinados canais de karaokê e direcioná-los para o canal de saída à direita ou à esquerda. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




