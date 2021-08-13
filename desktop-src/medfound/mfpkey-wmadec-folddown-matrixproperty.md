---
description: Especifica os coeficientes de dobra fornecidos pelo autor para decodificação de áudio multicanal para menos canais do que o fluxo codificado contém.
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: Propriedade MFPKEY_WMADEC_FOLDDOWN_MATRIX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb1b9eb1259c2a8c23f7b993699e1c51f17c09636afd7d19de23ce033fd269fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119463156"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>\_Propriedade MFPKEY WMADEC \_ FOLDDOWN \_ Matrix

Especifica os coeficientes de dobra fornecidos pelo autor para decodificação de áudio multicanal para menos canais do que o fluxo codificado contém.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>Tipo de Dados

**\_I4 da matriz VT \| \_**

## <a name="remarks"></a>Comentários

um decodificador de áudio pode atuar como um objeto de mídia DirectX (DMO) ou como uma Media Foundation transformação (MFT). para obter informações sobre quando um decodificador atua como um DMO ou um MFT, consulte as páginas de referência do codec individual em [objetos de codec](codecobjects.md).

quando você usa um decodificador como um DMO, o decodificador pode executar a dobra do canal e você pode enumerar os tipos de mídia de saída dobrados, chamando [**IMediaObject:: getoutputtype**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype).

Quando você usa um decodificador como um MFT, o decodificador por padrão não executará nenhuma dobra para baixo e não oferecerá tipos de mídia de saída dobrados. Um decodificador agindo como MFT executará a dobra somente se os coeficientes de dobra personalizada forem definidos usando a propriedade de **\_ \_ \_ matriz MFPKEY WMADEC FOLDDOWN** .

Se a propriedade **MFPKEY \_ WMADEC \_ FOLDDOWN \_ Matrix** não estiver definida na MFT do decodificador de áudio e você desejar executar uma dobra, poderá usar (como MFT) o processador de sinal digital do reamostrador de áudio.

O valor dessa propriedade é uma cadeia de caracteres que contém coeficientes dobrados em uma lista separada por vírgulas de valores inteiros. A lista deve conter um número de inteiros para cada canal no conteúdo codificado igual ao número de canais no conteúdo decodificado.

Se o coeficiente for zero, o valor a ser usado na cadeia de caracteres deverá ser "-2147483648"; caso contrário, o valor será computado usando a equação: 20 \* 65536 \* log10 (x).

Os coeficientes são listados na ordem de máscara de canal, conforme definido pelas constantes de máscara de canal que são incluídas no arquivo de cabeçalho Mmreg. h. Portanto, os dois primeiros valores em uma dobra de canal de 6 para 2 representam as partes do canal de saída à esquerda e o canal de saída à direita que são compostos do canal Center esquerdo no fluxo de 6 canais.

Você deve definir essa propriedade somente se os valores de dobra fornecidos pelo autor forem persistidos com o conteúdo codificado. Caso contrário, permita que o decodificador faça seus próprios cálculos.

o codec Windows Media Audio 10 Professional atualmente dá suporte apenas à dobra para dois canais.

Se a propriedade [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) for definida como **DSSPEAKER \_ surround**, o codec ignorará os coeficientes de dobrado fornecidos pelo autor e dobrará para um sinal de 2 canais que pode ser processado pelo decodificador de matriz do receptor. Isso permite que o equipamento surround forneça quatro canais. Esse modo só terá suporte se a origem for 5,1. O codec só pode dobrar 8 canais para 2 canais.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
