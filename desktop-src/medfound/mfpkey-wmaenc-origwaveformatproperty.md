---
description: Especifica a estrutura WAVEFORMATEX que descreve o conteúdo de áudio de entrada.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: Propriedade MFPKEY_WMAENC_ORIGWAVEFORMAT (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3475e5578124b8f0a762beddf713f701a5695110
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165298"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>\_Propriedade MFPKEY WMAENC \_ ORIGWAVEFORMAT

Especifica a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que descreve o conteúdo de áudio de entrada.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Tipo de Dados

\_ \| \_ UI1 da matriz VT ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) como uma matriz de bytes)

## <a name="remarks"></a>Comentários

Ao transcodificar o conteúdo baseado em áudio do Windows Media para uma taxa de bits inferior, você pode passar a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) do conteúdo para o codec a fim de habilitar o codec para otimizar seus algoritmos. Esse recurso, chamado de recompactação inteligente, fornece resultados melhores do que descompactar o conteúdo e, em seguida, alimentar os exemplos de PCM reconstruídos de volta pelo codec.

Ao passar a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) , inclua os bytes extras no final da estrutura especificada por **WAVEFORMATEX. cbSize**.

O codificador de áudio aceita apenas entradas e saídas para as quais o número de canais, bits por amostra e taxa de amostragem são idênticos. Você pode transcodificar o conteúdo somente para uma taxa de bits inferior dentro desses parâmetros. Em qualquer caso, você deve decodificar o conteúdo e passar os exemplos não compactados como entrada para o codificador. Definir essa propriedade fornece ao codificador algumas informações sobre o processamento que já foi realizado no conteúdo.

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

 

 
