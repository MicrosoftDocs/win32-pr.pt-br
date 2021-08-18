---
description: Especifica se o sink de mídia da DLNA (Digital Living Network Alliance) usa o MMCSS (Serviço de Agendador de Classes Multimídia).
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: MF_MP2DLNA_USE_MMCSS atributo (Mfmp2dlna.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79e824451be89bf4aca485edd2c61ce381f0cf4e0a9d5eefff82bf6c99cef2eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104752"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a>Atributo MF \_ MP2DLNA \_ USE \_ MMCSS

Especifica se o sink de mídia da DLNA (Digital Living Network Alliance) usa o MMCSS (Serviço de Agendador de Classes Multimídia).

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Para definir esse atributo no sink de mídia DLNA, consulte o sink de mídia para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) De definir o atributo antes do início do streaming.

Se esse atributo for **TRUE,** o sink de mídia DLNA se registrará no MMCSS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                             |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Mfmp2dlna.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




