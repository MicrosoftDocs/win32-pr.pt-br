---
description: Especifica o perfil de complexidade do conteúdo codificado.
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: Propriedade MFPKEY_DECODERCOMPLEXITYPROFILE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827917"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>\_Propriedade MFPKEY DECODERCOMPLEXITYPROFILE

Especifica o perfil de complexidade do conteúdo codificado.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCDecoderComplexityProfile

## <a name="data-type"></a>Tipo de Dados

**VT \_ BSTR**

## <a name="remarks"></a>Comentários

Você pode ler esse valor somente após a conclusão da codificação.

Para áudio, essa propriedade tem um dos valores a seguir.



| Valor | Descrição                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| L1  | Codificação padrão com uma taxa de amostragem de 44,1 KHz e uma taxa de bits máxima de 161 kbps.         |
| Cache  | Codificação padrão com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 161 kbps.         |
| MB  | Codificação padrão com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 385 kbps.         |
| "M0a" | Codificação profissional com taxas de amostragem de até 48 KHz e taxas de bits entre 48 e 192 kbps.  |
| "M0b" | Codificação profissional com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 192 kbps.      |
| M1  | Codificação profissional com taxas de amostragem de até 48 KHz e uma taxa de bits máxima de 384 kbps.      |
| M2  | Codificação profissional com taxas de amostragem de até 96 KHz e uma taxa de bits máxima de 768 Kbps.      |
| M3  | Codificação profissional com taxas de amostragem de até 96 KHz e uma taxa de bits máxima de 1,5 Mbps.      |
| Múltiplos  | Codificação sem perdas com taxas de amostragem de até 48 KHz e um máximo de 2 canais.                |
| N2  | Codificação sem perdas com taxas de amostragem de até 96 KHz e um máximo de 6 canais (5,1 surround). |
| N3  | Codificação sem perdas com taxas de amostragem de até 96 KHz e um máximo de 8 canais (7,1 surround). |



 

Para vídeo, essa propriedade tem um dos seguintes valores:



| Valor | Descrição                                                                       |
|-------|-----------------------------------------------------------------------------------|
| PONTOS  | perfil avançado (disponível somente no codec de perfil avançado do vídeo do Windows Media 9) |
| CP  | Não tem mais suporte                                                               |
| MP  | Perfil principal                                                                      |
| SP3  | Perfil simples                                                                    |



 

Para conteúdo de vídeo, você pode solicitar um nível de perfil definindo [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) antes de começar a codificação. O codec tentará codificar dentro dos parâmetros do nível de complexidade solicitado, mas as outras configurações que você configurar terão precedência. Você sempre deve verificar o valor do perfil de complexidade real após a codificação, caso sua solicitação não possa ser respeitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




