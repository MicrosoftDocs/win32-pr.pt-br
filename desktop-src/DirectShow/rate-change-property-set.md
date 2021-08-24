---
description: O conjunto de propriedades De alteração de taxa permite que filtros de origem/analisador MPEG-2 alterem a taxa de reprodução. Os decodificadores MPEG-2 devem dar suporte a esse conjunto de propriedades. O Navegador de DVD e o Mecanismo de Buffer de Fluxo usam essa propriedade definida para controlar as taxas de reprodução.
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: Conjunto de propriedades de alteração de taxa (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5299b744869a4c9a12b50a9e738104999aab5dcd19a800fc0ac3ddb3717e8617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747406"
---
# <a name="rate-change-property-set"></a>Conjunto de propriedades de alteração de taxa

O conjunto de propriedades De alteração de taxa permite que filtros de origem/analisador MPEG-2 alterem a taxa de reprodução. Os decodificadores MPEG-2 devem dar suporte a esse conjunto de propriedades. O Navegador de DVD e o Mecanismo de Buffer de Fluxo usam essa propriedade definida para controlar as taxas de reprodução.



| Rótulo | Valor |
|-------------------|-------------------------------|
| GUID do Conjunto de Propriedades | AM \_ KSPROPSETID \_ TSRateChange |



 



| ID da propriedade                                                                   | Descrição                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**AM \_ RATE \_ CorrectTS**](am-rate-correctts-property.md)                     | Informa ao decodificador que o Navegador está definindo os carimbos de data/hora corretos.             |
| AM \_ RATE \_ ExactRateChange                                                     | Obsoleto.                                                                              |
| [**AM \_ RATE \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | Consulta o decodificador para a taxa de dados máxima do decodificador.                               |
| [**AM \_ RATE \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | Consulta o decodificador para a taxa máxima de quadro completo do decodificador.                         |
| [**CONSULTA \_ RATE \_ AMLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | Consulta o decodificador para a hora de início do segmento de taxa que foi definido mais recentemente. |
| [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | Envia uma alteração de taxa para o decodificador.                                                    |
| Etapa AM \_ \_ RATE                                                                | Obsoleto. Consulte [Conjunto de propriedades de passo a passo do quadro.](frame-stepping-property-set.md)          |
| [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)           | Especifica qual versão do mecanismo de alteração de taxa usar.                           |



 

## <a name="remarks"></a>Comentários

No contexto desse conjunto de propriedades, a taxa mede a taxa na qual os carimbos de data/hora avançam em relação ao relógio de referência. Taxa o inverso da velocidade de reprodução. Por exemplo, se a velocidade de reprodução for 2x, os carimbos de data/hora deverão aumentar em 1/2 a taxa normal. Isso se traduz em uma velocidade de reprodução mais rápida, porque os exemplos são renderizados antes do normal.

Os exemplos são enviados para o decodificador com um carimbo de data/hora igual ao tempo de apresentação a uma taxa de 1x. O decodificador deve dimensionar os carimbos de data/hora nas amostras de saída para o tempo de apresentação correto para a taxa atual. Por exemplo, se a taxa for 1/2 (o que significa que a velocidade de reprodução é 2x), o decodificador deverá dimensionar os carimbos de data/hora em 1/2. Em geral, somente os quadros I têm carimbos de data/hora. O decodificador deve interpolar os carimbos de data/hora para os quadros B e P. Observe que, durante a reprodução inversa, os carimbos de data/hora continuam a aumentar – os carimbos de data/hora nunca retrocedem.

Duas versões do conjunto de propriedades De alteração de taxa são definidas, versão 1.0 e versão 1.1. O comportamento padrão é dado pela versão 1.0. Os fornecedores do decodificador são incentivados a dar suporte à versão 1.1, pois ele fornece uma experiência de reprodução mais suave. Atualmente, o Navegador de DVD usa a versão 1.0. O Mecanismo de Buffer de Fluxo usa a versão 1.1.

### <a name="rate-change-version-10"></a>Alteração de taxa versão 1.0

A versão 1.0 do conjunto de propriedades De alteração de taxa define o comportamento padrão para decodificadores MPEG-2.

O filtro de origem sinaliza uma alteração de taxa definindo a [**propriedade \_ \_ SIMPLERateChange AM RATE.**](am-rate-simpleratechange-property.md) Os dados dessa propriedade são a nova taxa, além da hora de início na amostra de entrada quando a taxa entra em vigor. O decodificador mantém uma fila de alterações de taxa pendentes, classificação por hora de início.

Antes que o Navegador de DVD mude para uma velocidade não 1x, ele fornece todos os exemplos pendentes, define temporariamente a taxa como 1,0 e libera o grafo. Em seguida, ele define a nova taxa. Todas as alterações de taxa são agendadas para o final do VOBU atual (unidade de objeto de vídeo). Observe que a liberação do grafo redefine o tempo de apresentação para zero.

O Navegador de DVD opera no *modo suave ou* no modo de *verificação*. No modo suave, ele envia todos os quadros para o decodificador, incluindo quadros B e quadros P. O Navegador de DVD usa o modo suave sempre que a velocidade de reprodução é maior que zero, mas menor que a taxa de dados maxmimum do decodificador. Se a velocidade de reprodução for menor que zero (reprodução inversa) ou exceder a taxa máxima de dados do decodificador, o Navegador de DVD usará o modo de verificação, em que envia apenas os quadros I para o decodificador. Em velocidades muito altas, pode ignorar alguns quadros de I; por exemplo, ele pode enviar todos os outros quadros I.

Por padrão, o Navegador de DVD muda o fluxo de áudio para taxas diferentes de 1,0. Você pode alterar isso chamando [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) com o sinalizador \_ AUDIODuringFwdRew do DVD.

### <a name="rate-change-version-11"></a>Alteração de taxa versão 1.1

A versão 1.1 do conjunto de propriedades De alteração de taxa segue os mesmos princípios básicos da versão 1.0, com as seguintes diferenças:

-   O filtro de origem sinaliza o decodificador para usar a versão 1.1 definindo a [**propriedade AM \_ RATE \_ UseRateVersion.**](am-rate-userateversion-property.md) Caso contrário, o decodificador deverá usar o comportamento da versão 1.0.
-   O filtro de origem não libera o grafo entre as alterações de taxa. Portanto, os carimbos de data/hora aumentam monotônicamente entre os limites de alteração de taxa, em vez de redefinir para zero.
-   Em vez de enfilar uma alteração de taxa para um determinado tempo de referência, o filtro de origem pode especificar que uma alteração de taxa se aplica ao exemplo mais encaminhado do decodificador *,* definido como o exemplo no início da fila de saída do decodificador. Para fazer isso, o filtro de origem usa a [**propriedade \_ \_ SIMPLERateChange AM RATE,**](am-rate-simpleratechange-property.md) mas define a hora de início igual a -1.
-   O filtro de origem pode consultar o decodificador para a hora de início da alteração de taxa que foi en fila mais recentemente. Ele usa a [**propriedade AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) para essa finalidade.
-   O filtro de origem não solta amostras. Se a taxa exceder a taxa máxima de dados do decodificador, o decodificador deverá soltar quadros conforme necessário.
-   O filtro de origem não muda o fluxo de áudio, independentemente da taxa de dados máxima do decodificador de áudio. O decodificador de áudio poderá soltar amostras se a velocidade de reprodução exceder a taxa máxima do decodificador. No entanto, ele ainda deve manter a fila de alterações de taxa agendada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Conjuntos de propriedades](property-sets.md)
</dt> </dl>

 

 




