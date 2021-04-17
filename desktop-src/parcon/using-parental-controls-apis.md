---
description: Usando APIs de controles dos pais
ms.assetid: 3d0bb750-0882-4b95-a595-38611f161ca9
title: Usando APIs de controles dos pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4ed69815bc04e00a3cae07f16530f8ea837f24a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812106"
---
# <a name="using-parental-controls-apis"></a>Usando APIs de controles dos pais

## <a name="api-selection"></a>Seleção de API

Conforme observado na seção de visão geral, o desenvolvimento envolve o uso de até três APIs:

-   Acesso às configurações básicas: a API de COM de conformidade mínima do controla os pais (API de conformidade) definida em Wpcapi. h para acesso simples a um subconjunto de chaves do estado dos controles dos pais.
-   Configurações completas acesso de gravação/leitura: o uso de um pequeno subconjunto da API COM do WMI para acesso completo só será necessário se o ISV precisar modificar as configurações. A adição de um link de extensibilidade da interface do usuário, a substituição do filtro de conteúdo da Web ou adições ao aplicativo HTTP em todo o computador ou às listas de isenção de filtragem de URL são as principais razões para usar a API. Como o uso do namespace de controles pai do WMI fornece acesso bruto ao armazenamento de configurações subjacentes, os ISVs devem prosseguir com cuidado ao interpretar o estado de configurações individuais que, de fato, podem ter dependências em outras configurações. Portanto, é recomendável usar a API de conformidade para o estado de leitura de todos os valores expostos por essa API.
-   Registro em log: o rastreamento de eventos do Windows Vista e a API do sistema de relatórios (também conhecida como ETW) para publicar eventos de atividade nos logs de controles dos pais, em conjunto com descritores de eventos e enumerações de matriz definidas em WpcEvent. h.

Todas as APIs são chamáveis como usuário padrão. Para registro em log, qualquer usuário pode registrar eventos de log. A chamada para recuperar ou alterar as configurações de outro usuário falhará se o chamador não tiver privilégios de administrador. Em outras palavras, um usuário padrão pode acessar suas próprias configurações apenas e apenas para leitura.

As configurações e o uso de API de registro em log são discutidos mais detalhadamente nestas seções

-   [Usando APIs de configurações de controles pais](using-parental-controls-settings-apis.md)
-   [Usando APIs de log para controles dos pais](using-logging-apis-for-parental-controls.md)

## <a name="development-environment"></a>Ambiente de desenvolvimento

O desenvolvimento para controles dos pais requer acesso a três arquivos de cabeçalho: WPC. h, WpcApi. h e WpcEvent. h. WPC. h é um coletor que inclui as configurações de API de conformidade pública e cabeçalhos de eventos, portanto, é suficiente incluir WPC. h no código do aplicativo.

Permissões de leitura/gravação para a API do WMI são especificadas pelo arquivo Wpcsprov. mof. Esse arquivo é instalado no subdiretório WBEM no diretório system32 do Windows.

O SDK (Software Development Kit) do Microsoft Windows contém um código de exemplo para reforçar o código de exemplo mostrado aqui e fornecer ferramentas simples orientadas por linha de comando para exploração de API ou testes de integração.

 

 



