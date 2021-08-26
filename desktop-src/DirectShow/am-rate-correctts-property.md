---
description: O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.
ms.assetid: f04e8291-734f-483e-b756-5362beb68d9c
title: Propriedade AM_RATE_CorrectTS (DVDMedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5858195ee6366be385a0d192a73b4375d43cae58cb574da2795efc87f78651ca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052916"
---
# <a name="am_rate_correctts-property"></a>Propriedade de CorrectTS da \_ taxa de am \_

O navegador de DVD usa essa propriedade para informar ao decodificador que o navegador está definindo os carimbos de data/hora corretos nos exemplos que ele fornece ao decodificador.



| Rótulo | Valor |
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

 

 




