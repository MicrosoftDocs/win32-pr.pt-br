---
description: Força o processador de vídeo avançado (EVR) a misturar o vídeo em um retângulo menor do que o retângulo de saída e, em seguida, dimensionar o resultado.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: Atributo EVRConfig_ForceScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd85fa67af3cea27564400b86cf6c8e32e3c15645cbb4f84cc97344fbab9ef60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119346196"
---
# <a name="evrconfig_forcescaling-attribute"></a>\_Atributo EVRConfig ForceScaling

Força o processador de vídeo avançado (EVR) a misturar o vídeo em um retângulo menor do que o retângulo de saída e, em seguida, dimensionar o resultado.

## <a name="data-type"></a>Tipo de dados

**UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

Esse atributo pode ser definido no coletor de mídia do EVR. Para definir o atributo, use **QueryInterface** para consultar o coletor de mídia do EVR para a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .

Definir esse atributo tem o mesmo efeito que definir o sinalizador **MFVideoRenderPrefs \_ FORCESCALING** no EVR. Consulte [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) para obter uma descrição desse sinalizador.

A constante de GUID para esse atributo é exportada de strmiids. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| parâmetro<br/>                   | <dl> <dt>UUIDs. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos EVR](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Gerenciamento de qualidade de vídeo](video-quality-management.md)
</dt> </dl>

 

 




