---
description: O conjunto de propriedades de alteração de taxa permite que os filtros de origem/analisador MPEG-2 alterem a taxa de reprodução. Os decodificadores MPEG-2 devem dar suporte a esse conjunto de propriedades. O navegador de DVD e o mecanismo de buffer de fluxo usam essa propriedade definida para controlar as taxas de reprodução.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Conjunto de propriedades de alteração de taxa (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb222f8a2fe388d8ea582448d2ba5aa6c9d7e80
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909604"
---
# <a name="rate-change-property-set"></a>Conjunto de propriedades de alteração de taxa

O conjunto de propriedades de alteração de taxa permite que os filtros de origem/analisador MPEG-2 alterem a taxa de reprodução. Os decodificadores MPEG-2 devem dar suporte a esse conjunto de propriedades. O navegador de DVD e o mecanismo de buffer de fluxo usam essa propriedade definida para controlar as taxas de reprodução.



| Label | Valor |
|-------------------|-------------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ TSRateChange |



 



| ID da propriedade                                                                   | Descrição                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_CorrectTS de taxa de am \_**](am-rate-correctts-property.md)                     | Informa ao decodificador que o navegador está definindo os carimbos de data/hora corretos.             |
| \_ExactRateChange de taxa de am \_                                                     | Obsoleto.                                                                              |
| [**\_MaxFullDataRate de taxa de am \_**](am-rate-maxfulldatarate-property.md)         | Consulta o decodificador para a taxa máxima de dados do decodificador.                               |
| [**\_QueryFullFrameRate de taxa de am \_**](am-rate-queryfullframerate-property.md)   | Consulta o decodificador para a taxa máxima de quadro completo do decodificador.                         |
| [**\_QueryLastRateSegPTS de taxa de am \_**](am-rate-querylastratesegpts-property.md) | Consulta o decodificador para a hora de início do segmento de taxa que foi definido mais recentemente. |
| [**\_SimpleRateChange de taxa de am \_**](am-rate-simpleratechange-property.md)       | Envia uma alteração de taxa para o decodificador.                                                    |
| \_Etapa da taxa de am \_                                                                | Obsoleto. Consulte [conjunto de propriedades de revisão de quadro](frame-stepping-property-set.md).          |
| [**\_UseRateVersion de taxa de am \_**](am-rate-userateversion-property.md)           | Especifica qual versão do mecanismo de alteração de taxa usar.                           |



 

## <a name="remarks"></a>Comentários

No contexto desse conjunto de propriedades, a taxa mede a taxa em que os carimbos de hora avançam em relação ao relógio de referência. Classifique o inverso da velocidade de reprodução. Por exemplo, se a velocidade de reprodução for 2x, os carimbos de data/hora devem aumentar em 1/2 a taxa normal. Isso se traduz em uma velocidade de reprodução mais rápida, pois os exemplos são renderizados antes do normal.

Os exemplos são enviados ao decodificador com um carimbo de data/hora igual ao tempo de apresentação na taxa de 1x. O decodificador deve dimensionar os carimbos de data/hora nos exemplos de saída para o tempo de apresentação correto para a taxa atual. Por exemplo, se a taxa for 1/2 (o que significa que a velocidade de reprodução é 2x), o decodificador deverá dimensionar os carimbos de data/hora por 1/2. Em geral, apenas quadros I têm carimbos de data/hora. O decodificador deve interpolar os carimbos de data/hora para os quadros B e P. Observe que durante a reprodução reversa, os carimbos de data/hora continuam aumentando — carimbos de data/hora nunca retrocedem.

Duas versões do conjunto de propriedades de alteração de taxa são definidas, versão 1,0 e versão 1,1. O comportamento padrão é fornecido pela versão 1,0. Os fornecedores de decodificadores são incentivados a dar suporte à versão 1,1, pois ele fornece uma experiência de reprodução mais suave. O navegador de DVD usa a versão 1,0 no momento. O mecanismo de buffer de fluxo usa a versão 1,1.

### <a name="rate-change-version-10"></a>Alteração de taxa versão 1,0

A versão 1,0 do conjunto de propriedades de alteração de taxa define o comportamento padrão para decodificadores MPEG-2.

O filtro de origem sinaliza uma alteração de taxa definindo a propriedade [**\_ \_ SimpleRateChange da taxa de am**](am-rate-simpleratechange-property.md) . Os dados dessa propriedade são a nova taxa, mais a hora de início no exemplo de entrada quando a taxa entra em vigor. O decodificador mantém uma fila de alterações de taxa pendentes, classificadas por hora de início.

Antes que o navegador de DVD mude para uma velocidade não 1x, ele entrega todas as amostras pendentes, define temporariamente a taxa como 1,0 e libera o grafo. Em seguida, ele define a nova taxa. Todas as alterações de taxa são agendadas para o final do VOBU atual (unidade de objeto de vídeo). Observe que a liberação do grafo redefine o tempo de apresentação como zero.

O navegador de DVD funciona no *modo Smooth* ou no *modo de verificação*. No modo Smooth, ele envia todos os quadros para o decodificador, incluindo quadros B e quadros P. O navegador de DVD usa o modo Smooth sempre que a velocidade de reprodução for maior que zero, mas menor que a taxa de dados maxmimum do decodificador. Se a velocidade de reprodução for menor que zero (reprodução reversa) ou exceder a taxa máxima de dados do decodificador, o navegador de DVD usará o modo de verificação, onde enviará apenas os quadros I para o decodificador. Em velocidades muito altas, ele pode ignorar alguns I-quadros; por exemplo, ele pode enviar a cada outro quadro.

Por padrão, o navegador de DVD desativa o fluxo de áudio para taxas diferentes de 1,0. Você pode alterar isso chamando [**IDvdControl2:: SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) com o \_ sinalizador AudioDuringFFwdRew de DVD.

### <a name="rate-change-version-11"></a>Alteração de taxa versão 1,1

A versão 1,1 do conjunto de propriedades de alteração de taxa segue os mesmos princípios básicos da versão 1,0, com as seguintes diferenças:

-   O filtro de origem sinaliza o decodificador para usar a versão 1,1, definindo a propriedade [**\_ \_ UseRateVersion da taxa de am**](am-rate-userateversion-property.md) . Caso contrário, o decodificador deve usar o comportamento da versão 1,0.
-   O filtro de origem não libera o grafo entre as alterações de taxa. Portanto, os carimbos de data/hora aumentam de forma monotônico entre os limites de alteração de taxa, em vez de redefinir para zero.
-   Em vez de enfileirar uma alteração de taxa para um determinado tempo de referência, o filtro de origem pode especificar que uma alteração de taxa se aplica à *amostra mais direta* do decodificador, definida como o exemplo no cabeçalho da fila de saída do decodificador. Para fazer isso, o filtro de origem usa a propriedade [**\_ \_ SimpleRateChange da taxa de am**](am-rate-simpleratechange-property.md) , mas define a hora de início igual a-1.
-   O filtro de origem pode consultar o decodificador para a hora de início da alteração de taxa que foi enfileirada mais recentemente. Ele usa a [**propriedade \_ \_ QueryLastRateSegPTS da taxa de am**](am-rate-querylastratesegpts-property.md) para essa finalidade.
-   O filtro de origem não descarta amostras. Se a taxa exceder a taxa máxima de dados do decodificador, o decodificador deverá descartar os quadros conforme necessário.
-   O filtro de origem não faz o áudio do fluxo de áudio, independentemente da taxa máxima de dados do decodificador de áudio. O decodificador de áudio pode descartar os exemplos se a velocidade de reprodução exceder a taxa máxima do decodificador. No entanto, ele ainda deve manter a fila de alterações de taxa agendada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




