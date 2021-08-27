---
description: Especifica o grau para o qual o codec deve reduzir o intervalo de cores efetivo do vídeo.
ms.assetid: 7227957b-59c9-4dd9-ad2b-a383e888cd46
title: Propriedade MFPKEY_RANGEREDUX (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b3a186522cdc328ab7b6f8e11154ae605673d2cca9d988e0e07c0d159e71589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113306"
---
# <a name="mfpkey_rangeredux-property"></a>\_Propriedade MFPKEY RANGEREDUX

Especifica o grau para o qual o codec deve reduzir o intervalo de cores efetivo do vídeo.

## <a name="constant-for-ipropertybag"></a>Constante para IPropertyBag

g \_ wszWMVCRangeRedux

## <a name="data-type"></a>Tipo de Dados

\_I4 VT

## <a name="default-value"></a>Valor padrão

0

## <a name="remarks"></a>Comentários

A redução de intervalo especifica o grau até o qual o codec deve reduzir o intervalo de Luma e croma do vídeo. Reduzir o intervalo reduz o tamanho dos quadros de vídeo codificados, mas também reduz os detalhes de cores do vídeo.

A redução de intervalo consiste em redução durante a codificação e a expansão durante a decodificação. É possível tornar os fatores de expansão diferentes dos fatores de redução, mas isso não é recomendado na maioria dos cenários em que o remapeamento de intervalo é útil.

A redução e a expansão do intervalo são executadas separadamente nos canais Luma e croma. A redução do intervalo pode ser uma maneira eficiente de reduzir a complexidade do vídeo de taxa de bits baixa sem sacrificar os detalhes da imagem. Definir todos os quatro valores como 8 reduz a quantidade de informações de Luma e croma pela metade, deixando mais bits a serem direcionados para preservar os detalhes da imagem.

O codec pode optar por usar automaticamente a redução de intervalo ao codificar o vídeo em taxas de bits muito baixas. Definir todos os quatro valores como 0 desabilita completamente a redução de intervalo, mesmo em cenários de taxa de bits baixa.

A redução do intervalo de cores reduz o tamanho codificado dos quadros de vídeo, mas pode introduzir desfoque nos quadros decodificados.

Se essa propriedade não for definida, o codec determinará se a redução de intervalo deve ser usada no momento da codificação. Normalmente, essa opção é selecionada pelo codec somente em taxas de bits baixas.

O valor dessa propriedade é uma combinação de quatro componentes, separados por zeros, formatados como 0x0M0m0N0n, em que:

-   M é o fator de redução do intervalo de codificação para o componente Y.
-   m é o fator de expansão do intervalo de decodificação para o componente Y (geralmente o mesmo que M).
-   N é o fator de redução do intervalo de codificação para o componente UV.
-   n é o fator de expansão do intervalo de decodificação para o componente UV (geralmente o mesmo que N).

Cada fator é um dígito de 0 a 8, em que 0 não é uma redução ou expansão e 8 é a redução ou expansão máxima.

Se você definir o valor como 0x00000000, a redução de intervalo será completamente desabilitada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho XP\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




