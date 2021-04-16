---
description: As propriedades de subimagem do DVD controlam a cor, o contraste e a saída da exibição da subimagem.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Conjunto de propriedades de subimagem de DVD (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779490"
---
# <a name="dvd-subpicture-property-set"></a>Conjunto de propriedades de subimagem de DVD

As propriedades de subimagem do DVD controlam a cor, o contraste e a saída da exibição da subimagem.

As informações a seguir apresentam as constantes e os tipos de dados necessários a serem usados para esse conjunto de propriedades em chamadas para métodos [**IKsPropertySet**](ikspropertyset.md) . Ele fornece valores para os parâmetros **GUID** (*GUIDPROPSET*), ID de propriedade (*dwPropId*) e tipo de dados de propriedade (*pPropData*).



|                   |                            |
|-------------------|----------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ DvdSubPic |



 



| ID da propriedade                           | Descrição                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ \_ \_ composição \_ de DVDSUBPIC da propriedade am | Propriedade somente definição que habilita ou desabilita a exibição de subimagem. O DirectShow define **a \_ composição da propriedade am \_ \_ no** tipo de dados booliano para essa propriedade, bem como a \_ composição da propriedade \_ do Pam \_ como um ponteiro para esse tipo de dados. **Verdadeiro** indica que a subimagem é exibida, **falso** indica desabilitá-la. Consulte a parte WDM do Windows DDK para obter mais informações. |
| \_Propriedade am \_ DVDSUBPIC \_ HLI          | Propriedade somente definição que especifica um retângulo de subimagem ou tela cuja cor ou contraste será alterado. O tipo de dados é [**\_ propriedade \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli). Consulte Observações.                                                                                                                                                                                |
| \_ \_ paleta DVDSUBPIC da propriedade am \_      | Define a paleta para uma subimagem. O tipo de dados é [**\_ propriedade \_ SPPAL**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Comentários

A propriedade **am da \_ propriedade \_ DVDSUBPIC \_ HLI** é somente definido. Especifica um retângulo de subimagem ou tela cuja cor ou contraste será alterado. Isso difere da especificação de DVD-Video, pois o navegador de DVD da Microsoft analisa todas as informações de botão e teclado e passa apenas um retângulo de realce para o decodificador de subimagem em um determinado momento. Como resultado, as informações de realce são enviadas para o decodificador com mais frequência do que está presente no fluxo de DVD.

As informações de realce chegam de forma assíncrona ao fluxo de dados. O decodificador usa os carimbos de data e hora de início e término para correlacionar as informações de realce às informações relevantes da subimagem, se houver. Se o decodificador não recebeu nenhuma informação de fluxo de subimagem para os carimbos de data/hora solicitados, o decodificador supõe que as informações de realce são autônomas e não se aplicam a uma subimagem. Nesse caso, o decodificador assume que as informações de cor e contraste têm a mesma cor.

Os dados não estão totalmente no formato de disco DVD. A Microsoft fornece uma estrutura adicional da [**Propriedade Type am \_ \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) que é passada como o parâmetro para essa propriedade. Esta estrutura descreve o botão atualmente selecionado das informações de realce de DVD.

O navegador de DVD processa todas as informações de pressionamento de tecla e envia novas informações de realce sempre que um estado de botão é alterado. As informações descrevem apenas um modo de um botão por vez. Ele inclui um retângulo de exibição em coordenadas de pixel da tela ou uma exibição da subimagem, se presente. A estrutura também contém informações de cor e contraste, mas apenas para o estado atual do botão atualmente selecionado. O formato é definido na especificação de DVD.

Informações de realce contêm carimbos de data/hora de início e término. Elas estão nas mesmas unidades que outros carimbos de data/hora, com duas exceções: um carimbo de data/hora de início de 0xFFFFFFFF significa que a propriedade de realce é efetivada após o recebimento e um carimbo de hora de término de 0xFFFFFFFF significa que a propriedade realce é válida até que o próximo realce seja recebido.

O campo HLISS é conforme definido na especificação do DVD. Um valor de zero indica que todos os realces são inválidos e o decodificador deve desabilitar todos os realces.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




