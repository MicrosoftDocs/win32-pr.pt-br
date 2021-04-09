---
description: Especifica o número máximo de amostras de saída que uma Microsoft Media Foundation transformação (MFT) terá pendente no pipeline a qualquer momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Atributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cf168158fd6a5f9a173d4d5d25dda3fa5b16d2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164761"
---
# <a name="mf_sa_minimum_output_sample_count-attribute"></a>\_Atributo de \_ \_ contagem de amostras de saída mínima \_ \_ de

Especifica o número máximo de amostras de saída que uma Microsoft Media Foundation transformação (MFT) terá pendente no pipeline a qualquer momento.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="remarks"></a>Comentários

Esse atributo aplica-se somente a MFTs que usam um buffer circular para alocar seus próprios exemplos de saída. Outros MFTs ignoram esse atributo.

Para definir este atributo:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no decodificador para obter um ponteiro [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .
2.  Chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) para adicionar o atributo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                              |
| parâmetro<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




