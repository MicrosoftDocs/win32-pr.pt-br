---
description: Usando APIs de configurações de controles pais
ms.assetid: 77a239e9-1cec-4710-b673-7d0cebd502e9
title: Usando APIs de configurações de controles pais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dde4827dfe3ed5ee7eec6787744e6ff92f18775
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662573"
---
# <a name="using-parental-controls-settings-apis"></a>Usando APIs de configurações de controles pais

As configurações são discutidas antes do registro em log porque o log é condicional nas configurações do usuário.

## <a name="wmi-api-settings-writeread"></a>Gravação/leitura das configurações da API WMI

A API do WMI fornece acesso não abstrato (bruto) a todas as configurações instanciadas pela infraestrutura de controles dos pais, conforme definido no arquivo de esquema Wpcsprov. mof. O repositório de configurações existe no \\ \\ \\ namespace WindowsParentalControls de aplicativos cimv2 raiz \\ , com as seguintes definições de classe que definem um esquema. Elementos de extensibilidade são indicados.

Por computador:

-   WpcSystemSettings (uma instância)
    -   Métodos adduser () e RemoveUser () para criar e excluir configurações de controles pais para um determinado SID, respectivamente.
    -   Propriedades do sistema atual de classificações de jogos em vigor, e acompanhamento e notificação relacionadas à verificação do administrador de logs.
    -   Extensibilidade: Propriedades de aplicativo HTTP somente leitura e leitura/gravação e listas de isenção de URL para filtragem de conteúdo da Web, ID de substituição de filtro de conteúdo da Web e caminho de DLL de recurso de nome e ID e número de eventos de log personalizado e registro de nome de cabeçalho.
-   WpcRatingsSystem (uma instância por cada sistema de classificações instalada)
    -   WpcRating (uma instância por nível de classificação).
    -   WpcRatingDescriptor (uma instância por descritor de classificação).
-   Extensibilidade: WpcExtension (uma instância por cada link de extensibilidade do painel de controles pai adicionado).
    -   Propriedades de GUID, subsistema, ID, caminho de recurso de imagem, caminho de recurso de imagem de estado desabilitado, caminho executável, caminho de DLL de recurso de nome de exibição e ID, caminho de DLL de recurso de subtítulo e ID.

Usuário por controle:

-   WpcUserSettings (uma instância por usuário controlado)
    -   Propriedades para SID de propriedade, sinalizador de ativação/desativação, sinalizador de logon/desligamento, limites de tempo de ativação/desativação de sinalizador, substituições habilitadas, máscara de horário de logon e restrições gerais de aplicativo.
    -   No Windows 8, a propriedade existente representa a primeira meia hora para cada hora. Uma nova propriedade de meia hora foi adicionada para representar a segunda metade de cada hora. Uma nova propriedade adicional foi introduzida para representar a concessão de tempo diária.

        **Windows 7 e Windows Vista:** As restrições de temporizador têm suporte para uma granularidade de 1 hora.

-   WpcWebSettings (uma instância por usuário controlado)
    -   Propriedades para SID proprietário, filtro ativar/desativar sinalizador, nível de filtro, downloads de arquivo sinalizador bloqueado, sinalizadores bloqueados de sites sem classificação.
-   WpcUrlOverride (uma instância por URL explicitamente permitida ou negada na lista de substituição de URL usada como lista de permissões/bloqueios para filtragem de conteúdo da Web)
    -   Propriedades para SID proprietário, URL afetada, estado permitido/bloqueado.
-   WpcAppOverride (uma instância por caminho permitido explicitamente na lista de substituição do aplicativo de restrições de aplicativo geral)
    -   Propriedades para SID de propriedade. ID da regra mais segura, caminho para o aplicativo.
-   WpcGamesSettings (uma instância por usuário controlado)
    -   Propriedades para SID proprietário, sinalizador de jogos permitidos, GUID do sistema de classificações para essas configurações, permitir sinalizador de jogos sem classificação, ID da classificação máxima permitida no sistema atual, coleção de descritores negados.
-   WpcGameOverride (uma instância por ID de aplicativo explicitamente permitida ou negada)
    -   Propriedades para SID proprietário, ID do aplicativo identificando o jogo, estado permitido/negado.

## <a name="data-representation-notes"></a>Notas de representação de dados

Várias das configurações no esquema são restritas pelo arquivo. mof com atributo não \_ nulo. Eles não podem ser definidos como uma variante nula. Para todos os tipos que não são de matriz, o código de controles pai Inicializa os valores. Para matrizes, os Estados vazios podem ser gravados usando uma variante nula, uma variante vazia ou uma matriz variante de tamanho zero. O provedor WMI normalizará tudo isso para uma representação de estado de variante nula na leitura.

## <a name="user-interface-extensibility-link-notes"></a>Observações do link de extensibilidade da interface do usuário

O uso do WMI para registrar um link de extensibilidade da interface do usuário requer a especificação das seguintes informações:

-   GUID – vários links podem compartilhar o mesmo GUID se eles fizerem parte de um pacote ou conjunto comum.
-   Subsistema-destinado a indicar classificações de tipos de link, como pacotes ou aplicativos compatíveis autônomos
-   Nome caminho de DLL de recurso e ID-especifica o recurso para o nome de exibição a ser exibido para o link.
-   Caminho de DLL de recurso de subtítulo e ID-especifica o recurso para texto adicional abaixo do nome.
-   Caminho da imagem-caminho completo de um bitmap de 24 × 24 pixels (BMP), com profundidade de cor de 8 bits por pixel e, preferencialmente, um canal alfa. Isso é especificado de maneira consistente com extensões de Shell: <file system path> , <negative resource ID> . Por exemplo: C: \\ Windows \\ System32 \\Wpccpl.dll,-20.
-   Caminho de imagem desabilitado-o mesmo que o caminho de imagem acima, exceto a variante do bitmap que mostra o estado desabilitado. Essa imagem é mostrada quando os controles dos pais estão desativados.
-   Caminho exe-caminho completo de um executável a ser invocado usando ShellExecute (). Esse caminho deve ser especificado com barras invertidas ou o link não invocará o executável. A adição de um token% SID% após o caminho exe resultará na execução do link, substituindo a cadeia de caracteres de SID do usuário para o qual a página de Hub está sendo exibida no momento. O executável pode usar a cadeia de caracteres de SID para gerenciar a funcionalidade do usuário especificado.

A desinstalação do aplicativo deve remover um registro de link de extensibilidade.

## <a name="web-extensibility-link-and-web-content-filter-override-notes"></a>Notas de substituição de filtro de extensibilidade da Web e de conteúdo da Web

Ao definir a propriedade Filterid como o mesmo GUID de um link de extensibilidade de interface do usuário registrado existente, o link exibido será promovido de um link genérico em outras configurações para o link de restrições da Web exclusivo. Essa é uma configuração em todo o computador e, portanto, fará com que o LSP do filtro de conteúdo da Web na caixa ignore todas as filtragens de todos os usuários controlados. Um nome descritivo também deve ser definido na Propriedade FilterName, que é especificada por um caminho para DLL de recurso e ID.

O sistema de controles dos pais recomenda o seguinte de qualquer filtro da Web de substituição:

-   Honrar o estado geral de ligar/desligar dos controles dos pais para um usuário.
-   Honrar as configurações de relatório de atividades para um usuário.
-   Monitore a propriedade Filterid. Se ele mudar do GUID especificado do fornecedor, outro filtro assumirá a propriedade e o filtro do fornecedor deverá ser desabilitado. Uma interface COM foi adicionada para reduzir a sobrecarga de verificação periódica para essa alteração em relação a uma chamada WMI.
-   É altamente recomendável respeitar as entradas de lista de isenção de URL e aplicativo HTTP somente leitura e de leitura/gravação.
-   Recomendado para honrar a lista de substituição de URL por usuário (lista de permissões/bloqueios).
-   Seja robusto para a troca rápida de usuários.

Os controles dos pais não colocam nenhuma limitação sobre como um filtro de conteúdo ou da Web se conecta ao Windows para implementar a filtragem. Os fornecedores podem aproveitar seus investimentos atuais ou tecnologias preferenciais (LSP, TDI, outros).

A desinstalação do filtro do fornecedor deve cancelar o registro das entradas Filterid e FilterName. Isso é realizado pela configuração de Filterid para GUID \_ NULL e FilterName para uma variante NULL. O filtro de conteúdo da Web na caixa será habilitado novamente.

Observe que a reativação do filtro da Web na caixa só filtrará novas sessões e não as sessões ativas de antes da mudança.

## <a name="web-content-filter-allowblock-list-exportimport-format"></a>Formato de exportação/importação da lista de permissões/bloqueios do filtro de conteúdo da Web

Não há suporte para esse recurso no Windows 8.

**Windows 7 e Windows Vista:** Há suporte para esse recurso.

<WebAddresses>

<URL AllowBlock="1">https://alloweddomain.com/</URL>

<URL AllowBlock="1">https://allowedurl.com/allowed/default.html</URL>

<URL AllowBlock="2">https://blockeddomain.com/</URL>

<URL AllowBlock="2">https://blockedurl.com/blocked/default.html</URL>

</WebAddresses>

## <a name="application-restrictions-override-notes"></a>Notas de substituição de restrições de aplicativo

As substituições de restrições de aplicativo são definidas por usuário para permitir binários ou caminhos específicos. Se um novo usuário com controle pai for configurado e as substituições de restrições de aplicativo forem necessárias para esse usuário, é recomendável que a chave de execução do Windows no registro seja usada com um aplicativo pequeno marcado como exigindo a elevação implantada para gravar as substituições. Isso resultará em um prompt de credenciais de uso único para configurar as substituições para o usuário, após o qual os binários de destino das substituições não serão um incômodo para os usuários devido a solicitações de substituição de administrador adicionais.

## <a name="actions-required-for-settings-changes-to-become-effective"></a>Ações necessárias para que as alterações nas configurações se tornem efetivas

Se um administrador alterar as configurações de um usuário padrão conectado, uma mensagem de aviso será gerada. Isso indica que as alterações nas configurações podem não entrar em vigor até que o usuário controlado Faça logoff e logon novamente. Esse é um design conservador. A maioria das configurações entrará em vigor quase imediatamente enquanto o usuário controlado estiver conectado. Uma exceção é para jogos, em que as configurações entrarão em vigor na próxima vez que o explorador de jogos for executado ou invocar o jogo for tentado.

## <a name="sample-code"></a>Código de exemplo

Exemplos de C++ são fornecidos no SDK que demonstra o uso dos recursos de extensibilidade de configurações. Consulte a seção de exemplos de controles dos pais.

## <a name="independent-test-tools"></a>Ferramentas de teste independentes

A inspeção de classes e instâncias é facilitada pelo plug-in wmimgmt. msc e pela ferramenta de Wbemtest.exe.

## <a name="64-bit-considerations"></a>Considerações de 64 bits

as versões do sistema operacional Windows de 64 bits atualmente têm um provedor WMI de 32 bits e um provedor de 64 bits instalado.

## <a name="general-code-development-and-debugging"></a>Desenvolvimento e depuração de código geral

Se o Visual Studio for usado para o desenvolvimento de código de gerenciamento de configurações, a depuração local exigirá a execução do Visual Studio com direitos de administrador (chamando com executar como administrador usando a linha de comando ou a opção de clique com o botão direito do mouse) Isso se deve ao isolamento do processo e da mensagem implementado pelo UAC.

## <a name="minimum-compliance-api-settings-read"></a>Configurações de API de conformidade mínimas lidas

### <a name="interfaces-and-methods"></a>Interfaces e métodos

A API de conformidade controlada pelo arquivo de cabeçalho Wpcapi. h fornece acesso simplificado somente leitura para as seguintes configurações usando interfaces COM.

Os métodos de interface raiz [**IWindowsParentalControls**](/windows/desktop/api/Wpcapi/nn-wpcapi-iwindowsparentalcontrols) fornecem acesso a:

-   Métodos de IWPCSettings:
    -   IsLoggingRequired () — o relatório de atividades é configurado como ativado para o usuário?
    -   GetLastSettingsChangeTime () — o aplicativo pode estar ciente se as políticas de configurações foram alteradas desde uma verificação anterior.
    -   Getrestrictions () — Leia se restrições da Web, limites de tempo, restrições de jogo ou restrições de aplicativo estão definidas como on.
-   Métodos de IWPCWebSettings:
    -   GetSettings () – recupera sinalizadores para ativar ou desativar o filtro e downloads bloqueados.
    -   RequestURLOverride () — Insira uma solicitação no mecanismo de substituição do administrador (aprovação over-tiracolo) que apresentará uma caixa de diálogo que contém as URLs a serem aprovadas.
-   Métodos de IWPCGamesSettings:
    -   IsBlocked () – para uma determinada ID de aplicativo do jogo, é o jogo bloqueado pelos controles dos pais e por qual motivo.
-   Getvisibility () — fornece informações sobre se a interface do usuário de controles pai está oculta no momento.
-   GetWebFilterInfo () — fornece uma interface para obter a ID do filtro de conteúdo da Web ativo no momento.

### <a name="sample-code"></a>Código de exemplo

Exemplos de C++ são fornecidos no SDK que demonstra o uso da API de conformidade. Consulte a seção de exemplos de controles dos pais.

 

 



