---
description: Quando o filtro de navegador de DVD entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade AM \_ \_ DVDKARAOKE \_ Enable Property.
ms.assetid: 78b2998b-d8b3-424d-85bc-872e64eb4a4f
title: Conjunto de propriedades de karaokê de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2918513de06a657436ed99e67f672fe74a113b78
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909064"
---
# <a name="dvd-karaoke-property-set"></a>Conjunto de propriedades de karaokê de DVD

Quando o filtro de [navegador de DVD](dvd-navigator-filter.md) entra no modo de karaokê, ele informa o decodificador de áudio por meio da propriedade **am \_ \_ DVDKARAOKE \_ Enable** Property. O decodificador deve ativar mudo dos canais de áudio de 2 a 5 até que ele receba do navegador de DVD uma propriedade **am \_ \_ DVDKARAOKE \_ data de propriedade** com um ponteiro para uma estrutura de dados [**am \_ DvdKaraokeData**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdkaraokedata) indicando como os canais auxiliares devem ser misturados.



| Label | Valor |
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

 

 




