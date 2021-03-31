---
title: Para definir as configurações de entrada
description: Para definir as configurações de entrada
ms.assetid: 288801a7-793f-43bd-9c5a-f9e1bd86ecc3
keywords:
- ASF (Advanced Systems Format), configurações de entrada
- ASF (formato de sistemas avançados), configurações de entrada
- perfis, configurações de entrada
- codecs, configurações de entrada
- fluxos, configurações de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e7b2db64a7346cc8b9d46c48f0add79dafcac95
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103917001"
---
# <a name="to-set-input-settings"></a>Para definir as configurações de entrada

As propriedades básicas de mídia de entrada e mídia de fluxo são definidas pela estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) . Para formatos de entrada, as informações de tipo de mídia são definidas pelo seu aplicativo. Para formatos de fluxo, as informações de tipo de mídia são definidas no perfil que você atribui ao gravador. Algumas propriedades são independentes do tipo de mídia e devem ser definidas para uma entrada antes do início da gravação. Essas propriedades são recursos de codec e gravador que são independentes do tipo de fluxo e devem ser definidas após o perfil ser atribuído no gravador, mas antes do início da gravação.

A definição de uma configuração de entrada requer uma chamada para [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting). Você também pode verificar o valor atual de uma configuração com uma chamada para [**IWMWriterAdvanced2:: GetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-getinputsetting).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usar perfis com o gravador**](to-use-profiles-with-the-writer.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> <dt>

[**Gravando fluxos de imagem**](writing-image-streams.md)
</dt> </dl>

 

 




