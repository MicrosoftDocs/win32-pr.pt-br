---
description: Especifica a função de dispositivo para um dispositivo de captura de áudio.
ms.assetid: 4f2885b6-c771-4577-880d-5feea671432e
title: Atributo MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_AUDCAP_ROLE (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebe0aecb12a7831218fceb3c480c6c4e2a20a1ffa330675a642feefc14ecbe39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060730"
---
# <a name="mf_devsource_attribute_source_type_audcap_role-attribute"></a>\_Tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP atributo de \_ função

Especifica a função de dispositivo para um dispositivo de captura de áudio.

## <a name="data-type"></a>Tipo de dados

**ERole** armazenado como **UINT32**

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Para definir esse atributo, chame [**IMFAttributes:: setuint32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="remarks"></a>Comentários

O tipo de enumeração **eRole** está documentado na documentação da API de áudio principal.

O valor do atributo especifica uma função de dispositivo. Esse atributo é usado com as funções a seguir.

Esse atributo pode ser usado como entrada para as funções [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource) e [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate) . Se o atributo for especificado, a função criará uma fonte de mídia que usa o dispositivo de captura de áudio padrão para a função de dispositivo especificada.

Esse atributo também pode ser usado como entrada para a função [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources) . Se o atributo for especificado, a enumeração será restrita à função de dispositivo especificada. Além disso, cada objeto de ativação retornado pela função **MFEnumDeviceSources** contém esse atributo. O atributo é então usado internamente pelo objeto de ativação quando cria a origem da mídia.

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                            |
| Cabeçalho<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Captura de áudio/vídeo](audio-video-capture.md)
</dt> <dt>

[Capturar atributos de dispositivo](capture-device-attributes.md)
</dt> </dl>

 

 




