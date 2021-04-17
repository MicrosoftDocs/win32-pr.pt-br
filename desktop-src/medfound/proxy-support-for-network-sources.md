---
description: Suporte de proxy para fontes de rede
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Suporte de proxy para fontes de rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813302"
---
# <a name="proxy-support-for-network-sources"></a>Suporte de proxy para fontes de rede

Um servidor proxy é um servidor intermediário entre a intranet e a Internet, que roteia solicitações do aplicativo cliente para o servidor de mídia e recupera arquivos do servidor de mídia.

Media Foundation Cria implicitamente um objeto de *localizador de proxy* quando um aplicativo cliente tenta acessar uma URL de origem. O objeto de localizador de proxy expõe a interface [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) . Durante a resolução da origem, Media Foundation verifica se o repositório de propriedades foi passado para o método do resolvedor de origem.

Se o repositório de propriedades contiver o conjunto de propriedades [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) para um objeto de fábrica localizador de proxy implementado pelo aplicativo, ele invocará o método [**IMFNetProxyLocatorFactory:: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) para criar um localizador de proxy com definições de configuração personalizadas.

Se o repositório de propriedades não estiver definido, Media Foundation criará o localizador de proxy com a configuração padrão. Essas configurações são as seguintes:

-   Se a política de usuário estiver definida, o localizador de proxy usará as configurações especificadas no registro.

-   Para HTTP, o localizador de proxy usa as configurações de proxy do navegador.

-   Para RTSP, o localizador de proxy é configurado para ignorar servidores proxy ao se conectar ao servidor de mídia.

Essa configuração padrão pode ser alterada pelo aplicativo. Os tópicos a seguir contêm informações sobre as definições de configuração para um localizador de proxy:

-   [Definições de configuração do localizador de proxy](proxy-locator-configuration-settings.md)

-   [Como configurar o localizador de proxy](how-to-configure-the-proxy-locator.md)

Media Foundation Inicializa o localizador de proxy para a URL de origem especificada para o [resolvedor de origem](source-resolver.md). O localizador de proxy detecta um servidor proxy a ser usado com base nas definições de configuração. Quando o localizador de proxy tenta definir um servidor proxy, ele registra o resultado de êxito ou falha no registro. Esse valor é verificado durante o próximo processo de detecção de proxy. Se um determinado servidor proxy for conhecido por ter causado falhas no passado, o localizador de proxy o ignorará.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos e propriedades](attributes-and-properties.md)
</dt> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



