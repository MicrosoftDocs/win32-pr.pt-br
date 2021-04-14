---
description: Obtém estatísticas do coletor de mídia de rede de vida digital (DLNA).
ms.assetid: 1fa6ea9f-fd30-4fa2-a0e6-1647273bcc35
title: Atributo MF_MP2DLNA_STATISTICS (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a51620c1ca093a422a5e4657edcfbfaa66ae6cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502390"
---
# <a name="mf_mp2dlna_statistics-attribute"></a>\_Atributo de \_ estatísticas MF MP2DLNA

Obtém estatísticas do coletor de mídia de rede de vida digital (DLNA).

## <a name="data-type"></a>Tipo de dados

**[**MFMPEG2DLNASINKSTATS**](/windows/desktop/api/mfmp2dlna/ns-mfmp2dlna-mfmpeg2dlnasinkstats)** armazenado como **byte \[ \]**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).

## <a name="remarks"></a>Comentários

Durante o streaming, o coletor de mídia DLNA atualiza esse atributo com estatísticas sobre a codificação e a multiplexação dos fluxos MPEG-2. O aplicativo pode consultar esse atributo a qualquer momento para obter os valores mais recentes.

A definição desse atributo no coletor de mídia DLNA não tem efeito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Mfmp2dlna. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




