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

Esse conjunto de Propriedades controla o transporte de dados de e para um dispositivo externo. Na maioria dos casos, os aplicativos não devem usar esse conjunto de propriedades diretamente. Em vez disso, use a interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) .

A tabela a seguir lista as propriedades que são relevantes para aplicativos de modo de usuário. para obter uma descrição completa desse conjunto de propriedades, consulte o Microsoft Windows Driver Development Kit DDK.



| Rótulo | Valor |
|-------------------|---------------------------|
| GUID do Conjunto de Propriedades | transporte de extensão propsetid \_ \_ |



 



| ID da propriedade                                                                           | Descrição                                  |
|---------------------------------------------------------------------------------------|----------------------------------------------|
| [**KSPROPERTY \_ EXTXPORT \_ ATN \_ Search**](ksproperty-extxport-atn-search.md)           | Pesquisa um número de faixa absoluto (ATN). |
| [**pesquisa de código de KSPROPERTY \_ EXTXPORT \_ \_**](ksproperty-extxport-timecode-search.md) | Pesquisa um código de tempo.                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 



