---
title: configurando Fluxos arbitrários personalizados
description: configurando Fluxos arbitrários personalizados
ms.assetid: 09b28fd3-a0a3-44d9-b664-7421290abf02
keywords:
- fluxos, configurando fluxos arbitrários personalizados
- codecs, configurando fluxos arbitrários personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b9b98b25ae9f973682ee3987ed8b590d485288e72e0b5ef7977eb7f3da0d1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119809806"
---
# <a name="configuring-custom-arbitrary-streams"></a>configurando Fluxos arbitrários personalizados

Ao usar seu próprio tipo de dados arbitrário, você deve criar um valor de GUID para servir como o identificador de tipo de mídia principal para ele. Quando o gravador encontra um fluxo em um perfil com um tipo principal que ele não reconhece, ele pressupõe que o fluxo é dados arbitrários personalizados. Ele aceitará seus exemplos, os atualizará e os combinará com exemplos de outros fluxos no arquivo sem verificar os dados de qualquer forma.

Você também pode criar seus próprios identificadores GUID de subtipo para definir subcategorias de dados personalizados. O gravador irá ignorar esses subtipos completamente, mas eles serão preservados na seção de cabeçalho do arquivo ASF, para que seu aplicativo de leitura possa recuperá-los e tomar decisões com base neles.

Um fluxo arbitrário requer uma taxa de bits e uma janela de buffer e deve ter uma estrutura de [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) com os valores limpos, exceto o tipo de mídia principal e subtipo (se estiver usando um).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**configuração comum a todos os Fluxos**](configuration-common-to-all-streams.md)
</dt> <dt>

[**Configurando tipos de fluxo arbitrários**](configuring-arbitrary-stream-types.md)
</dt> <dt>

[**Fluxos de dados arbitrários personalizados**](custom-arbitrary-data-streams.md)
</dt> </dl>

 

 




