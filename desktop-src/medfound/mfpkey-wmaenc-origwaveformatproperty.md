---
description: Especifica a estrutura WAVEFORMATEX que descreve o conteúdo de áudio de entrada.
ms.assetid: d424f243-5ad6-46f2-b99b-9bb780715e8a
title: MFPKEY_WMAENC_ORIGWAVEFORMAT propriedade (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df477daa61e39eb6b2a86aa26c27de4088e943d41f40ac9b708a0201698088c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113136"
---
# <a name="mfpkey_wmaenc_origwaveformat-property"></a>Propriedade \_ ORIGWAVEFORMAT MFPKEY WMAENC \_

Especifica a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) que descreve o conteúdo de áudio de entrada.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACOriginalWaveFormat

## <a name="data-type"></a>Tipo de Dados

VT \_ ARRAY \| VT \_ UI1 ([**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) como uma matriz de bytes)

## <a name="remarks"></a>Comentários

Ao transcodificar Windows conteúdo baseado em Áudio de Mídia para uma taxa de bits mais baixa, você pode passar a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) do conteúdo para o codec para permitir que o codec otimize seus algoritmos. Esse recurso, chamado de recompactação inteligente, fornece melhores resultados do que descompactar o conteúdo e, em seguida, alimentar os exemplos de PCM reconstruídos por meio do codec.

Ao passar a [**estrutura WAVEFORMATEX,**](/previous-versions/dd757713(v=vs.85)) inclua quaisquer bytes extras no final da estrutura especificada por **WAVEFORMATEX.cbSize**.

O codificador de áudio aceita apenas entradas e saídas para as quais o número de canais, bits por exemplo e taxa de amostra são idênticos. Você pode transcodificar o conteúdo apenas para uma taxa de bits inferior dentro desses parâmetros. Em qualquer caso, você deve decodificar o conteúdo e passar os exemplos descompactados como entrada para o codificador. Definir essa propriedade fornece ao codificador algumas informações sobre o processamento que já foi executado no conteúdo.

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

 

 
