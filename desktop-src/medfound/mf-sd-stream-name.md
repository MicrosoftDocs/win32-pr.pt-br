---
description: Contém o nome de um fluxo.
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: MF_SD_STREAM_NAME atributo (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 312ca788b03c3bef075c2c51d06df921d258e7372c091c5ccb43ec248444fcfc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474045"
---
# <a name="mf_sd_stream_name-attribute"></a>Atributo MF \_ SD \_ STREAM \_ NAME

Contém o nome de um fluxo.

## <a name="data-type"></a>Tipo de dados

**Wchar\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).

Para definir esse atributo, chame [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).

## <a name="applies-to"></a>Aplica-se a

[**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a>Comentários

A fonte de mídia AVI define esse atributo se o arquivo AVI contiver uma parte 'strn'.

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows aplicativos UWP de 7 \[ \| áreas de trabalho\]<br/>                                  |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP de aplicativos da área de trabalho do Server 2008 R2 \|\]<br/>                     |
| parâmetro<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do descritor de fluxo](stream-descriptor-attributes.md)
</dt> </dl>

 

 




