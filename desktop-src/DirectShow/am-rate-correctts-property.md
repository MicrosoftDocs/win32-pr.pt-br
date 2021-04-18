---
description: O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Propriedade AM_RATE_CorrectTS (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa410b079d3de63de364662c7d5465c82814d24a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810956"
---
# <a name="am_rate_correctts-property"></a>Propriedade de CorrectTS da \_ taxa de am \_

O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.



|                   |                               |
|-------------------|-------------------------------|
| GUID do Conjunto de Propriedades | \_KSPROPSETID \_ TSRateChange |
| ID da propriedade       | \_CorrectTS de taxa de am \_           |
| Tipo de Dados         | **LONG**                      |



 

## <a name="remarks"></a>Comentários

As versões anteriores do navegador de DVD não definiram os carimbos de data/hora corretos quando a taxa de reprodução era algo diferente de 1,0. Muitos decodificadores configuram esse problema ignorando os carimbos de data/hora durante o retrocesso ou avanço rápido e Estimando os tempos de apresentação corretos.

Esses problemas foram corrigidos na versão atual do navegador de DVD. Para compatibilidade com versões anteriores com decodificadores existentes, o navegador de DVD indica que os carimbos de data/hora estão corretos, definindo a \_ Propriedade CorrectTS da taxa de am \_ no decodificador com o valor **true**. Quando essa propriedade é definida, o decodificador deve usar os carimbos de data/hora reais, em vez de estimar os tempos de apresentação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>DVDMedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Conjunto de propriedades de alteração de taxa**](rate-change-property-set.md)
</dt> </dl>

 

 




