---
description: Permite que o leitor de origem use transformações de Media Foundation (MFTs) que são otimizadas para transcodificação.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Atributo MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8bc5362c93138ef301ac65ace799ad64d59ac9110af349822e0efa98d410686e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119605013"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a>\_Leitor de origem MF \_ \_ habilitar \_ \_ somente \_ transformações atributo

Permite que o [leitor de origem](source-reader.md) use transformações de Media Foundation (MFTs) que são otimizadas para transcodificação.

## <a name="data-type"></a>Tipo de dados

**UINT32**

Tratar como booliano.

## <a name="remarks"></a>Comentários

Alguns MFTs, especialmente decodificadores, são otimizados para transcodificação em vez de reprodução. Por padrão, o leitor de origem não carregará essas transformações. Defina esse atributo como **true** se você quiser usar transcodificação de MFTs com o leitor de origem.

Um aplicativo poderá definir esse atributo se ele não processar os dados em tempo real (para transcodificação ou cenários semelhantes). Caso contrário, para reprodução em tempo real, use o comportamento padrão.

Internamente, esse atributo faz com que o leitor de origem inclua o sinalizador **\_ enumerador de enumeração de MFT \_ \_ \_ somente para transcodificação** ao chamar [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> </dl>

 

 




