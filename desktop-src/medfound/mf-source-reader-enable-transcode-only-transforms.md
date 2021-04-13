---
description: Permite que o leitor de origem use transformações de Media Foundation (MFTs) que são otimizadas para transcodificação.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Atributo MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Mfreadwrite. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501635"
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
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mfreadwrite. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> </dl>

 

 




