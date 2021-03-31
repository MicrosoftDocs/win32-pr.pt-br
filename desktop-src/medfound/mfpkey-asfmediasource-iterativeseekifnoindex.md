---
description: Configura a fonte de mídia do ASF para usar a busca iterativa se o arquivo de origem não tiver nenhum índice.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Propriedade MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663805"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Propriedades de Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




