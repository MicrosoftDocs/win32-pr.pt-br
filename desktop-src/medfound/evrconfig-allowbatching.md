---
description: Permite que o EVR (Renderização de Vídeo Aprimorado) para chamadas em lote para o método Microsoft Direct3D IDirect3DDevice9::P resent.
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: EVRConfig_AllowBatching atributo (Uuids.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1013ca2578d8fd46ea4019035df1ba3397ad629fd27c1901cd92ac8de1bc43af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742375"
---
# <a name="evrconfig_allowbatching-attribute"></a>Atributo EVRConfig \_ AllowBatching

Permite que o EVR (Renderização de Vídeo Aprimorado) para chamadas em lote para o método Microsoft Direct3D **IDirect3DDevice9::P resent.**

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido no sink de mídia EVR. Para definir o atributo, use **QueryInterface** para consultar o sink de mídia EVR para a interface [**IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

Definir esse atributo tem o mesmo efeito que definir o **sinalizador \_ AllowBatching MFVideoRenderPrefs** no EVR. Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para ver uma descrição desse sinalizador.

A constante GUID para esse atributo é exportada de strmiids.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>Uuids.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gerenciamento de qualidade de vídeo](video-quality-management.md)
</dt> </dl>

 

 




