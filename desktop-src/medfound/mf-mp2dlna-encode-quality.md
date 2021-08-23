---
description: Especifica a qualidade de codificação para o coletor de mídia do DLNA (digital telenetwork Alliance).
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: Atributo MF_MP2DLNA_ENCODE_QUALITY (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a612dae32aabe4276ece76e7edff1aef431cc5d93f8aeaae0dbc9087620374c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973655"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a>\_Atributo de \_ qualidade de codificação MP2DLNA MF \_

Especifica a qualidade de codificação para o coletor de mídia do DLNA (digital telenetwork Alliance).

## <a name="data-type"></a>Tipo de dados

**UINT32**

Intervalo: 0 a 18

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Números mais altos indicam melhor qualidade de codificação. Números mais baixos indicam codificação mais rápida, mas baixa qualidade de codificação. O valor padrão é 9.

Para definir esse atributo no coletor de mídia DLNA, consulte o coletor de mídia para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) . Defina o atributo antes de o streaming começar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




