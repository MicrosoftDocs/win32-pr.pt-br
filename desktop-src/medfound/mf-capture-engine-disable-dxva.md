---
description: Especifica se o mecanismo de captura usa a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo.
ms.assetid: 9F677E6E-0DCD-456F-8A00-1C11011BAA13
title: Atributo MF_CAPTURE_ENGINE_DISABLE_DXVA (Mfcaptureengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d2ce31ed55e151e7254168e5e6bcce0c5460e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296436"
---
# <a name="mf_capture_engine_disable_dxva-attribute"></a>\_Mecanismo de captura MF \_ \_ desabilitar \_ atributo DXVA

Especifica se o mecanismo de captura usa a DXVA (aceleração de vídeo do DirectX) para decodificação de vídeo.

## <a name="data-type"></a>Tipo de dados

**Bool** armazenado como **UINT32**

## <a name="remarks"></a>Comentários

Esse atributo se aplicará se as seguintes condições forem verdadeiras:

-   O mecanismo de captura decodifica um fluxo de vídeo compactado do dispositivo de captura (por exemplo, se o dispositivo de captura produzir o vídeo H. 264).
-   O decodificador de vídeo dá suporte à decodificação acelerada por hardware usando DXVA.
-   O aplicativo usa o atributo de [Gerenciador de D3D do \_ mecanismo de captura \_ \_ \_ MF](mf-capture-engine-d3d-manager.md) para definir o Gerenciador de dispositivos dxgi no mecanismo de captura.

Caso contrário, esse atributo será ignorado.

Esse atributo permite que o aplicativo desabilite o DXVA enquanto estiver decodificando as superfícies do Direct3D.

O valor padrão desse atributo é **false**, o que significa que a decodificação de DXVA está habilitada quando disponível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                         |
| parâmetro<br/>                   | <dl> <dt>Mfcaptureengine. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos do mecanismo de captura](capture-engine-attributes.md)
</dt> <dt>

[**IMFCaptureEngine:: Initialize**](/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize)
</dt> </dl>

 

 




