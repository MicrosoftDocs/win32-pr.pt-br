---
description: Define o Gerenciador de Dispositivos de infraestrutura de gráficos do Microsoft DirectX (DXGI) no mecanismo de mídia.
ms.assetid: CB952492-0ACF-4501-BD8B-133E26FCE8F7
title: Atributo MF_MEDIA_ENGINE_DXGI_MANAGER (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98e731b5aa2449ae772427c6743ec4f97b5d7601
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105810799"
---
# <a name="mf_media_engine_dxgi_manager-attribute"></a>\_Atributo de \_ Gerenciador de dxgi do mecanismo de mídia MF \_ \_

Define o Gerenciador de Dispositivos de infraestrutura de gráficos do Microsoft DirectX (DXGI) no mecanismo de mídia.

## <a name="data-type"></a>Tipo de dados

**IMFDXGIDeviceManager \* *_ armazenado como _* IUnknown\***

## <a name="getset"></a>Obter/definir

Para obter esse atributo, chame [**IMFAttributes:: getunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown).

Para definir esse atributo, chame [**IMFAttributes:: setunknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).

## <a name="remarks"></a>Comentários

O valor desse atributo é um ponteiro para a interface [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

No modo de servidor de quadro, esse atributo permite que o mecanismo de mídia use a aceleração de hardware para decodificação de vídeo e processamento de vídeo. Se o atributo não estiver definido, o mecanismo de mídia usará a decodificação e o processamento de software.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2012 \[ Desktop aplicativos \| UWP\]<br/>                                |
| parâmetro<br/>                   | <dl> <dt>Mfmediaengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaEngineClassFactory:: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance)
</dt> </dl>

 

 




