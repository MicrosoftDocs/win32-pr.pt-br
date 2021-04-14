---
title: Configurando fluxos de texto
description: Configurando fluxos de texto
ms.assetid: d99baac5-69e5-4e0a-9cd6-35b288d8181a
keywords:
- fluxos, configurando fluxos de texto
- codecs, configurando fluxos de texto
- fluxos de texto, configurando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 460369eaae02f636f8ddda8bcca4f29ecfc2e1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453611"
---
# <a name="configuring-text-streams"></a>Configurando fluxos de texto

Os fluxos de texto são essencialmente os mesmos que os fluxos arbitrários personalizados. Não há nenhuma informação de configuração associada a um fluxo de texto para identificar o tipo de codificação de texto, portanto, o objeto do gravador não pode verificar exemplos.

Para configurar um fluxo de texto, você deve garantir que a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) contenha um tipo de mídia principal de texto WMMEDIATYPE \_ . Você também deve definir uma taxa de bits e uma janela de buffer para o fluxo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Calculando valores de taxa de bits e de janela de buffer para fluxos arbitrários**](calculating-bit-rate-and-buffer-window-values-for-arbitrary-streams.md)
</dt> <dt>

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos de texto**](text-streams.md)
</dt> </dl>

 

 




