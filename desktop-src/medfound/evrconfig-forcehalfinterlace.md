---
description: Força o processador de vídeo avançado (EVR) a ignorar o segundo campo de cada quadro entrelaçado.
ms.assetid: b79d9230-b127-4e9b-b73b-685ce27aefa9
title: Atributo EVRConfig_ForceHalfInterlace (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfeab4bcb3d05e615962fb8acc5f304ba3ea7e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765703"
---
# <a name="evrconfig_forcehalfinterlace-attribute"></a>\_Atributo EVRConfig ForceHalfInterlace

Força o processador de vídeo avançado (EVR) a ignorar o segundo campo de cada quadro entrelaçado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido no coletor de mídia do EVR. Para definir o atributo, use **QueryInterface** para consultar o coletor de mídia do EVR para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Definir esse atributo tem o mesmo efeito que definir o sinalizador **MFVideoMixPrefs \_ FORCEHALFINTERLACE** no EVR. Consulte [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) para obter uma descrição desse sinalizador.

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

 

 




