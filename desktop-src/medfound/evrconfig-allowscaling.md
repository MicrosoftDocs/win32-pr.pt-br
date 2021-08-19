---
description: Permite que o EVR (Renderador de Vídeo Aprimorado) misture o vídeo dentro de um retângulo menor que o retângulo de saída e, em seguida, dimensione o resultado.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: EVRConfig_AllowScaling atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83323c42ac81d4cce0bb42733bd4246959cf0fc9a58b5705579a86aee9b2bd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879420"
---
# <a name="evrconfig_allowscaling-attribute"></a>Atributo EVRConfig \_ AllowScaling

Permite que o EVR (Renderador de Vídeo Aprimorado) misture o vídeo dentro de um retângulo menor que o retângulo de saída e, em seguida, dimensione o resultado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido no sink de mídia EVR. Para definir o atributo, use **QueryInterface** para consultar o sink de mídia EVR para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Definir esse atributo tem o mesmo efeito que definir o **sinalizador MFVideoRenderPrefs \_ AllowScaling** no EVR. Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para ver uma descrição desse sinalizador.

A constante GUID para esse atributo é exportada de strmiids.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gerenciamento de qualidade de vídeo](video-quality-management.md)
</dt> </dl>

 

 




