---
title: Rastreamento
description: o rastreamento usa o rastreamento de eventos para Windows (ETW).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Rastreando serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ace571c2639ddd1eb55ed1e4afd70bcef7318b44
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882302"
---
# <a name="tracing"></a>Rastreamento

o rastreamento usa o rastreamento de eventos para Windows (ETW). para aproveitar as ferramentas de rastreamento disponíveis com o Windows Server 2008 R2, instale o SDK do Microsoft Windows do site de [Downloads do MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .


Há três níveis de rastreamento com suporte:

-   Detalhado (todos os rastreamentos disponíveis).
-   Informações (rastreamentos informativos).
-   Erro (rastreamentos de erro).

Os seguintes eventos são rastreados:

-   Quaisquer erros (nível = erro, nível = informações ou nível = detalhado).
-   Entrada/saída de uma API (Level = info ou level = verbose).
-   Início e conclusão de qualquer e/s (Level = info ou level = verbose)
-   mensagens SOAP trocadas (Level = verbose, disponíveis em Windows 2003 SP1 e posterior)

## <a name="generating-and-viewing-wwsapi-traces"></a>Gerando e exibindo rastreamentos de WWSAPI

o WWSAPI usa os eventos baseados em manifesto no Windows Vista e superior. Como resultado, a experiência de rastreamento tem algumas diferenças com base na versão do sistema operacional. A geração de rastreamentos de ETW pode ser feita usando as ferramentas de ETW in-box em todas as plataformas com suporte. no entanto, a exibição dos rastreamentos ETW em um ótimo formato requer ferramentas personalizadas no Windows XP SP2 e Windows 2003 SP1. Há algumas maneiras diferentes de coletar e exibir rastreamentos de eventos do ETW WWSAPI dependendo da versão do sistema operacional.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>habilitando e exibindo rastreamentos do WWSAPI no Visualizador de Eventos (funciona no Windows Vista e superior)

-   Execute eventvwr. msc na linha de comando ou no menu executar.
-   Clique no link exibir no painel Ações à direita e habilite a opção Mostrar logs analíticos e de depuração.
-   navegue até aplicativo e serviço Logs \\ Microsoft \\ Windows \\ provedores do webservices no painel esquerdo.
-   Clique com o botão direito do mouse no provedor de rastreamento e selecione habilitar log.
-   Execute seu cenário.
-   Ao atualizar a página do Visualizador de eventos, você deve começar a ver as entradas de rastreamento do WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Habilitando e exibindo rastreamentos de WWSAPI usando o script Wstrace.bat (funciona no XPSP2 e acima)

O arquivo em lotes wstrace.bat fornece uma maneira conveniente para:

-   Criar um log de rastreamento
-   Excluir um log de rastreamento
-   Habilitar e desabilitar o rastreamento
-   Atualizar o nível de rastreamento (info/Error/verbose)
-   Convertendo logs de rastreamento em arquivos CSV

O arquivo em lotes usa logman.exe para todos os comandos, com exceção da conversão dos logs para o arquivo CSV, que requer uma ferramenta personalizada (wstracedump.exe).

## <a name="using-tracing-commands"></a>Usando comandos de rastreamento

O comando a seguir cria um log que usa informações, o nível de erro ou detalhado. Este comando requer privilégios elevados.

**wstrace.bat criar \[ erro de informações \| \| detalhadas\]**

O comando a seguir exclui o log. Este comando requer privilégios elevados.

**wstrace.bat excluir**

O comando a seguir habilita o rastreamento. Primeiro, você deve criar um log.

**wstrace.bat em**

O nível de rastreamento (info, Error ou verbose) pode ser modificado da seguinte maneira:

**\[ \| Erro detalhado de informações de atualização dewstrace.bat \|\]**

Para despejar a saída de rastreamento, use o seguinte comando:

**> de despejo dewstrace.bat temp.csv**

Os eventos serão despejados no arquivo CSV até que CTRL-C seja pressionado ou o rastreamento seja desabilitado.

## <a name="tracing-file-format"></a>Formato de arquivo de rastreamento

Os arquivos CSV criados por wstrace.bat são arquivos de texto variáveis simples e separados por vírgula. esses arquivos podem ser abertos em Excel, Bloco de notas, etc.

As colunas do arquivo são as seguintes:

-   TimeStamp-carimbo de data/hora de quando o evento foi registrado
-   ProcessID-ID ULONG do processo que registra o evento
-   ID ThreadID-ULONG do thread que está registrando o evento
-   O valor enumerado de evento do tipo de evento pode ser ("API Enter" "API \| pendente" "API \| ExitSyncSuccess" \| "API ExitSyncFailure" \| "API ExitAsyncSuccess" \| "API ExitAsyncFailure" " \| e/s iniciada" \| "e/s concluído" \| "falha de e/s" " \| erro" \| "mensagem recebida iniciada" "mensagem recebida" "mensagem recebida \| \| parada" \| "enviando mensagem iniciada" \| "enviando mensagem" \| "enviando mensagem parada")
-   Operation-o nome da operação que está sendo invocada. Normalmente, isso é mapeado para a API que está sendo chamada.
-   Erro-número de erro HRESULT opcional
-   Informações-informações opcionais sobre o evento

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Coletando arquivo de rastreamento ETW WWSAPI usando ferramentas de ETW (funciona no XPSP2 e superior)

Habilitando o rastreamento ETW para WWSAPI

**logman start wstrace-bs 64-pés 1-rt-p Microsoft-Windows-webservices \[ flags \[ nível \] \] \[ -o &lt; EtlLogFileName &gt; \] -ets**

para criar e iniciar a sessão de rastreamento ETW. Logman.exe é uma ferramenta de ETW na caixa disponível em todas as plataformas com suporte. observe que você precisa usar o Microsoft \_ Windows \_ webservices como o nome do provedor no XPSP2 e no W2K3. Você pode executar provedores de consulta logman para ver a lista de provedores registrados. o provedor microsoft-Windows-webservices (ou microsoft \_ Windows \_ webservices) deve ser listado, a menos que não esteja registrado. O provedor normalmente é registrado durante a instalação. no entanto, ele também pode ser registrado manualmente executando wevtutil.exe im &lt; ManifestFileName &gt; (no Windows Vista e posterior) ou mofcomp.exe &lt; MofFileName &gt; (no XPSP2 e no W2K3).

Os sinalizadores podem ser usados para filtrar os rastreamentos por seu tipo. Pode ser ou um valor para os seguintes tipos de rastreamento. Se não for fornecido, todos os tipos de rastreamento serão habilitados.

-   0x1-rastreamentos de entrada/saída da API.
-   0x2-rastreamentos de erro.
-   0x4-rastreamentos de e/s.
-   os rastreamentos de mensagens 0x8-SOAP.
-   0x10-rastreamentos de mensagens binários.

O nível pode ser usado para filtrar os rastreamentos por seu nível. Deve ser um dos valores a seguir. Se não for fornecido, todos os níveis de rastreamento serão habilitados.

-   0x1-rastreamentos fatais.
-   0x2-rastreamentos de erro.
-   0x3-rastreamentos de aviso.
-   0x4-rastreamentos informativos.
-   0x5-rastreamentos detalhados.

EtlLogFileName é o caminho para o arquivo de log de eventos do ETW a ser criado (use a extensão. ETL). Se não for fornecido, o ETW escolherá um nome aleatório que poderá ser consultado posteriormente. Esse arquivo não deve residir no diretório de perfil do usuário. O arquivo de log de eventos do ETW (arquivo. ETL) está em formato binário. Ele pode ser consumido por aplicativos ETW, mas não está no formato legível humana. A próxima etapa descreve como exibir seu conteúdo.

Execute seu cenário

Coletando arquivo de log de eventos ETW.

**logman Stop wstrace-ETS**

para interromper a sessão de rastreamento ETW. Isso ocorre quando o ETW para de registrar os eventos em log. O arquivo de log de eventos ETW (especificado no parâmetro EtlLogFileName) está pronto para ser consumido. Ele pode ser exibido localmente (as instruções são fornecidas abaixo) ou enviado ao grupo de produtos para investigação.

Exemplo de ponta a ponta usando ferramentas ETW:

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices -o mytrace.etl -ets**

**Eco.. execute seu cenário..**

**logman stop wstrace -ets**

**tracerpt mytrace.etl -o mytrace.xml**

**wstrace.htm**

**Eco.. use mytrace.xml e wstrace.xsl na página aberta ..**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Exibindo rastreamentos de arquivo de rastreamento ETW do WWSAPI usando wstracedump.exe ferramenta (funciona Windows XP e superior)

Wstracedump.exe é uma ferramenta de consumidor ETW desenvolvida personalizada que processa eventos no arquivo de rastreamento ETW WWSAPI e produz uma saída acessível por humanos. Ele pode produzir a saída de todas as plataformas com suporte. Consulte seu uso (wstracedump.exe -?) para obter mais informações.

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Exibindo rastreamentos de arquivo de rastreamento ETW do WWSAPI usando ferramentas ETW (funciona no Windows Vista e superior)

Tracerpt.exe é a ferramenta para exibir o conteúdo de um arquivo de log de eventos ETW e disponível em todas as plataformas com suporte. Ele pode ser usado para gerar arquivos de despejo CSV, EVTX ou XML de um arquivo de log de eventos ETW. No entanto, o arquivo de saída gerado tem rastreamentos íveis humanos somente Windows Vista e posterior. Essas instruções descrevem como gerar o arquivo de despejo XML e usá-lo junto com um arquivo xsl para exibir os rastreamentos em um formato interessante (o arquivo xsl é muito trivial e pode ser alterado se formatos diferentes são desejados).

-   Executar

    **tracerpt &lt; EtlLogFileName &gt; -o &lt; OutputXMLFileName&gt;**

    para criar um despejo XML do arquivo ETL binário (tracerpt.exe cria o arquivo de saída no formato XML por padrão. Executar tracerpt -? Para ver outros formatos disponíveis).

-   Neste ponto, você pode ver as informações de rastreamento no arquivo XML. Além disso, você pode abrir o arquivo wstrace.htm e usar o arquivo de despejo xml e o arquivo wstrace.xsl para ver os rastreamentos em um formato melhor. Observe que os arquivos precisam estar no computador local para poder usar esse arquivo HTML no IE.

## <a name="security"></a>Segurança

Ao habilenciar o rastreamento, os administradores devem levar em conta que ele consome espaço em disco adicional e potência de computação. Um cliente ou aplicativo mal-intencionado pode esgotar os recursos do sistema, a menos que as configurações de rastreamento sejam configuradas com limites razoáveis. Ao usar o recurso de rastreamento de mensagens, as mensagens que carregam informações confidenciais, como credenciais, informações pessoais etc. podem ser persistida no disco ou exibidas por qualquer pessoa que tenha acesso ao visualizador de eventos do sistema. Como uma mitigação para esse problema, o rastreamento pode ser habilitado por usuários do sistema ou administrador no Windows 2003 e posterior. O rastreamento de mensagens está desabilitado Windows XP no qual qualquer usuário pode ativar o rastreamento.

A enumeração a seguir é usada com rastreamento:

-   [**API de RASTREAMENTO do WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




