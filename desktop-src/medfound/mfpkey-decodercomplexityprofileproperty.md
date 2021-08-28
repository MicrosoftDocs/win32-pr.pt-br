---
description: Especifica o perfil de complexidade do conteúdo codificado.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: MFPKEY_DECODERCOMPLEXITYPROFILE propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca206357a3f3a396ac6d07ea16a1b72bc245c641095a5523e46139dfd6af7f76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119604216"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>Propriedade MFPKEY \_ DECODERCOMPLEXITYPROFILE

Especifica o perfil de complexidade do conteúdo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityProfile

## <a name="data-type"></a>Tipo de Dados

**VT \_ BSTR**

## <a name="remarks"></a>Comentários

Você pode ler esse valor somente depois que a codificação for concluída.

Para áudio, essa propriedade tem um dos valores a seguir.



| Valor | Descrição                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| "L1"  | Codificação padrão com uma taxa de amostragem de 44,1 KHz e uma taxa de bits máxima de 161 Kbps.         |
| "L2"  | Codificação padrão com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 161 Kbps.         |
| "L3"  | Codificação padrão com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 385 Kbps.         |
| "M0a" | Professional codificação com taxas de amostragem de até 48 KHz e taxas de bits entre 48 e 192 Kbps.  |
| "M0b" | Professional codificação com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 192 Kbps.      |
| "M1"  | Professional codificação com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 384 Kbps.      |
| "M2"  | Professional codificação com taxas de amostragem de até 96 KHz e uma taxa de bits máxima de 768 Kbps.      |
| "M3"  | Professional codificação com taxas de amostragem de até 96 KHz e uma taxa de bits máxima de 1,5 Mbps.      |
| "N1"  | Codificação sem perda com taxas de amostragem de até 48 KHz e um máximo de 2 canais.                |
| "N2"  | Codificação sem perda com taxas de amostragem de até 96 KHz e um máximo de 6 canais (cerca de 5,1). |
| "N3"  | Codificação sem perda com taxas de amostragem de até 96 KHz e um máximo de 8 canais (cerca de 7,1). |



 

Para vídeo, essa propriedade tem um dos seguintes valores:



| Valor | Descrição                                                                       |
|-------|-----------------------------------------------------------------------------------|
| "AP"  | perfil avançado (disponível somente no codec Windows Perfil Avançado do Vídeo de Mídia 9) |
| "CP"  | não há mais suporte para                                                               |
| "MP"  | perfil principal                                                                      |
| "SP"  | perfil simples                                                                    |



 

Para conteúdo de vídeo, você pode solicitar um nível de perfil definindo [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) antes de começar a codificação. O codec tentará codificar dentro dos parâmetros do nível de complexidade solicitado, mas as outras configurações que você configurar terão precedência. Você sempre deve verificar o valor real do perfil de complexidade após a codificação, caso sua solicitação não possa ser a mesma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation propriedades](media-foundation-properties.md)
</dt> </dl>

 

 




