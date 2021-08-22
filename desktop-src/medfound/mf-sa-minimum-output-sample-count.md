---
description: Especifica o número máximo de amostras de saída que uma Microsoft Media Foundation transformação (MFT) terá pendente no pipeline a qualquer momento.
ms.assetid: 53D393B4-BFF1-430F-9CD1-5071336E6F04
title: Atributo MF_SA_MINIMUM_OUTPUT_SAMPLE_COUNT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a7d00fcb5a11d756ed4848e3e600a6fd1cca32203ff7234cb01963dfcb5149
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663906"
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
| Cliente mínimo com suporte<br/> | Windows 8 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ aplicativos UWP de aplicativos de desktop \|\]<br/>                              |
| Cabeçalho<br/>                   | <dl> <dt>Mftransform. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de transformação](transform-attributes.md)
</dt> </dl>

 

 




