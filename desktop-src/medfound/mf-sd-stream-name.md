---
description: Contém o nome de um fluxo.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: Atributo MF_SD_STREAM_NAME (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297473"
---
# <a name="mf_sd_stream_name-attribute"></a>\_Atributo de \_ nome de fluxo SD MF \_

Contém o nome de um fluxo.

## <a name="data-type"></a>Tipo de dados

**WCHAR \** _

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [_ *IMFAttributes:: GetString* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes:: SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Aplica-se a

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Comentários

A fonte de mídia AVI define esse atributo se o arquivo AVI contiver um bloco ' strn '.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 7 \| UWP\]<br/>                                  |
| Servidor mínimo com suporte<br/> | \[Aplicativos UWP para aplicativos da área de trabalho do Windows Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> </dl>

 

 




