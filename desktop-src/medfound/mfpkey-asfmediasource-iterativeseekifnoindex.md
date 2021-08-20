---
description: Configura a fonte de mídia do ASF para usar a busca iterativa se o arquivo de origem não tiver nenhum índice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Propriedade MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb56a9b063d2bf30a0f6e48f25becb61d585751439f103ca26aa06d1d3c69727
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117874100"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a>\_Propriedade MFPKEY ASFMediaSource \_ IterativeSeekIfNoIndex

Configura a fonte de mídia do ASF para usar a busca iterativa se o arquivo de origem não tiver nenhum índice.



Tipo de dados

Tipo PROPVARIANT (VT)

Membro PROPVARIANT

**BOOL de variante \_**

BOOL do VT \_

**boolVal**



## <a name="remarks"></a>Comentários

Use essa propriedade para configurar a origem da mídia ASF. Para definir a propriedade, passe um ponteiro **IPropertyStore** para o *resolvedor de origem*. Para obter mais informações, consulte [Configurando uma origem de mídia](configuring-a-media-source.md).

A *busca iterativa* é um algoritmo para localizar uma posição em um arquivo ASF sem índice. Ele usa uma série de aproximações, com base na taxa média de bits, para ficar progressivamente mais próximo do tempo de busca de destino. (O algoritmo é semelhante a uma pesquisa binária.) A busca iterativa pode levar mais tempo do que procurar por índice, portanto, ela está desabilitada por padrão.

Se você definir essa propriedade, use as seguintes propriedades para definir os parâmetros de pesquisa:

-   [Contagem máxima de MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ \_](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [MFPKEY \_ ASFMediaSource \_ IterativeSeek \_ tolerância \_ a \_ milissegundos](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

Essas propriedades definem o número máximo de iterações e a tolerância, respectivamente. O algoritmo é interrompido quando atinge o número máximo de iterações ou quando encontra um pacote cuja distância do tempo de busca está dentro da tolerância especificada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[aplicativos UWP para aplicativos de área de trabalho Windows 7 \|\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos de aplicativos de área de trabalho do servidor 2008 R2 \[ \| UWP\]<br/>                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




