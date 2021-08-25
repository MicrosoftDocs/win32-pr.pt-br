---
description: Especifica se o mecanismo de captura usa a DXVA (Aceleração de Vídeo) do DirectX para decodificação de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: MF_CAPTURE_ENGINE_DISABLE_DXVA atributo (Mfcaptureengine.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c722b70e1707e6ad5d14b7afca0da2c8d1a63b3a132345e727de1f37023916a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941006"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>Atributo \_ \_ \_ DXVA DISABLE DO MECANISMO DE CAPTURA DE \_ MF

Especifica se o mecanismo de captura usa a DXVA (Aceleração de Vídeo) do DirectX para decodificação de vídeo.

## <a name="data-type"></a>Tipo de dados

**BOOL** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplica se as seguintes condições são verdadeiras:

-   O mecanismo de captura decodifica um fluxo de vídeo compactado do dispositivo de captura (por exemplo, se o dispositivo de captura saída de vídeo H.264).
-   O decodificador de vídeo dá suporte à decodificação acelerada por hardware usando DXVA.
-   O aplicativo usa o [atributo MF \_ CAPTURE ENGINE \_ \_ D3D \_ MANAGER](mf-capture-engine-d3d-manager.md) para definir o Gerenciador de Dispositivos DXGI no mecanismo de captura.

Caso contrário, esse atributo será ignorado.

Esse atributo permite que o aplicativo desabilite o DXVA enquanto ainda decodifica as superfícies do Direct3D.

O valor padrão desse atributo é **FALSE,** o que significa que a decodificação DXVA está habilitada quando disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                         |
| Cabeçalho<br/>                   | <dl> <dt>Mfcaptureengine.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do Mecanismo de Captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine::Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




