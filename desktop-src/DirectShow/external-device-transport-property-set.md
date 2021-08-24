---
description: Conjunto de propriedades de transporte de dispositivo externo
ms.assetid: 9c80cf59-054f-49b6-9456-ed5e091cbfaf
title: Conjunto de propriedades de transporte de dispositivo externo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef7db31dfe80fae0178aa329ce7e3c6cd55d3a6acbef7fd5a8ccda07943bef4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685666"
---
# <a name="external-device-transport-property-set"></a>Conjunto de propriedades de transporte de dispositivo externo

Esse conjunto de propriedades controla o transporte de dados de e para um dispositivo externo. Na maioria dos casos, os aplicativos não devem usar esse conjunto de propriedades diretamente. Em vez disso, use a interface [**IAMExtTransport.**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)

A tabela a seguir lista as propriedades relevantes para aplicativos no modo de usuário. Para uma descrição completa desse conjunto de propriedades, consulte o DDK do Microsoft Windows Driver Development Kit.



| Rótulo | Valor |
|-------------------|---------------------------|
| GUID do Conjunto de Propriedades | PROPSETID \_ EXT \_ TRANSPORT |



 



| ID da propriedade                                                                           | Descrição                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH**](ksproperty-extxport-atn-search.md)           | Pesquisa um NÚMERO de faixa absoluto (ATN). |
| [**KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH**](ksproperty-extxport-timecode-search.md) | Pesquisa um código de hora.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 



