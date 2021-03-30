---
title: Configurando fluxos arbitrários personalizados
description: Configurando fluxos arbitrários personalizados
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- fluxos, configurando fluxos arbitrários personalizados
- codecs, configurando fluxos arbitrários personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29d5cf3e95a5514ddeede9eb3c25df01ed4cd2ae
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635789"
---
# <a name="configuring-custom-arbitrary-streams"></a>Configurando fluxos arbitrários personalizados

Ao usar seu próprio tipo de dados arbitrário, você deve criar um valor de GUID para servir como o identificador de tipo de mídia principal para ele. Quando o gravador encontra um fluxo em um perfil com um tipo principal que ele não reconhece, ele pressupõe que o fluxo é dados arbitrários personalizados. Ele aceitará seus exemplos, os atualizará e os combinará com exemplos de outros fluxos no arquivo sem verificar os dados de qualquer forma.

Você também pode criar seus próprios identificadores GUID de subtipo para definir subcategorias de dados personalizados. O gravador irá ignorar esses subtipos completamente, mas eles serão preservados na seção de cabeçalho do arquivo ASF, para que seu aplicativo de leitura possa recuperá-los e tomar decisões com base neles.

Um fluxo arbitrário requer uma taxa de bits e uma janela de buffer e deve ter uma estrutura de [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) com os valores limpos, exceto o tipo de mídia principal e subtipo (se estiver usando um).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Configuração comum a todos os fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos de dados arbitrários personalizados**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




