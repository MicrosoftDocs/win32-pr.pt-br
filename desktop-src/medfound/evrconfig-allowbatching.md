---
description: Permite que o processador de vídeo avançado (EVR) chame em lote o método Microsoft Direct3D IDirect3DDevice9::P reenviado.
ms.assetid: 6dbb2839-97ea-4881-8f22-0f8e943a3071
title: Atributo EVRConfig_AllowBatching (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 191c3c0f0ea4ad18e7bb711ae6d37c21f75cd478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501169"
---
# <a name="evrconfig_allowbatching-attribute"></a>\_Atributo EVRConfig AllowBatching

Permite que o processador de vídeo avançado (EVR) chame em lote o método Microsoft Direct3D **IDirect3DDevice9::P reenviado** .

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido no coletor de mídia do EVR. Para definir o atributo, use **QueryInterface** para consultar o coletor de mídia do EVR para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Definir esse atributo tem o mesmo efeito que definir o sinalizador **MFVideoRenderPrefs \_ ALLOWBATCHING** no EVR. Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obter uma descrição desse sinalizador.

A constante de GUID para esse atributo é exportada de strmiids. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gerenciamento de qualidade de vídeo](video-quality-management.md)
</dt> </dl>

 

 




