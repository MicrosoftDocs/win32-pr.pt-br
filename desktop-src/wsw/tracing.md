---
title: Rastreamento
description: O rastreamento usa o ETW (rastreamento de eventos para Windows).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Rastreando serviços Web para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c660884667cefae8067376075a30cbc41f70d4
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366935"
---
# <a name="tracing"></a>Rastreamento

O rastreamento usa o ETW (rastreamento de eventos para Windows). Para aproveitar as ferramentas de rastreamento disponíveis com o Windows Server 2008 R2, instale o SDK do Microsoft Windows no site de [downloads do MSDN](https://www.microsoft.com/download/details.aspx?id=8279) .


Há três níveis de rastreamento com suporte:

-   Detalhado (todos os rastreamentos disponíveis).
-   Informações (rastreamentos informativos).
-   Erro (rastreamentos de erro).

Os seguintes eventos são rastreados:

-   Quaisquer erros (nível = erro, nível = informações ou nível = detalhado).
-   Entrada/saída de uma API (Level = info ou level = verbose).
-   Início e conclusão de qualquer e/s (Level = info ou level = verbose)
-   Mensagens SOAP trocadas (level = verbose, disponíveis no Windows 2003 SP1 e posterior)

## <a name="generating-and-viewing-wwsapi-traces"></a>Gerando e exibindo rastreamentos de WWSAPI

O WWSAPI usa os eventos baseados no manifesto no Windows Vista e versões posteriores. Como resultado, a experiência de rastreamento tem algumas diferenças com base na versão do sistema operacional. A geração de rastreamentos de ETW pode ser feita usando as ferramentas de ETW in-box em todas as plataformas com suporte. No entanto, a exibição dos rastreamentos ETW em um ótimo formato requer ferramentas personalizadas no Windows XP SP2 e no Windows 2003 SP1. Há algumas maneiras diferentes de coletar e exibir rastreamentos de eventos do ETW WWSAPI dependendo da versão do sistema operacional.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Habilitando e exibindo rastreamentos do WWSAPI no Visualizador de Eventos (funciona no Windows Vista e superior)

-   Execute eventvwr. msc na linha de comando ou no menu executar.
-   Clique no link exibir no painel Ações à direita e habilite a opção Mostrar logs analíticos e de depuração.
-   Navegue até aplicativo e serviço logs \\ provedores do Microsoft \\ Windows \\ WebServices no painel esquerdo.
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

Os arquivos CSV criados por wstrace.bat são arquivos de texto variáveis simples e separados por vírgula. Esses arquivos podem ser abertos no Excel, no bloco de notas, etc.

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

**logman start wstrace-BS 64-pés 1-RT-p Microsoft-Windows-WebServices \[ flags \[ nível \] \] \[ -o <EtlLogFileName> \] -ETS**

para criar e iniciar a sessão de rastreamento ETW. Logman.exe é uma ferramenta de ETW na caixa disponível em todas as plataformas com suporte. Observe que você precisa usar o Microsoft \_ Windows \_ WebServices como o nome do provedor no xpsp2 e no W2K3. Você pode executar provedores de consulta logman para ver a lista de provedores registrados. O provedor Microsoft-Windows-WebServices (ou Microsoft \_ Windows \_ WebServices) deve ser listado, a menos que não esteja registrado. O provedor normalmente é registrado durante a instalação. No entanto, ele também pode ser registrado manualmente executando wevtutil.exe mensagem instantânea <ManifestFileName> (no Windows Vista e posterior) ou mofcomp.exe <MofFileName> (no xpsp2 e no W2K3).

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

para interromper a sessão de rastreamento ETW. Isso ocorre quando o ETW para de registrar os eventos. O arquivo de log de eventos do ETW (especificado no parâmetro EtlLogFileName) está pronto para consumir. Ele pode ser exibido localmente (instruções são fornecidas abaixo) ou enviado ao grupo de produtos para investigação.

Exemplo de ponta a ponta usando ferramentas de ETW:

**logman start wstrace-BS 64-FT 1-RT-p Microsoft-Windows-WebServices-o mytrace. etl-ETS**

**Echo.. Execute seu cenário..**

**logman Stop wstrace-ETS**

**Tracerpt mytrace. etl-o mytrace.xml**

**wstrace.htm**

**Echo.. Use mytrace.xml e wstrace. xsl na página aberta.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>Exibindo rastreamentos de arquivos de rastreamento ETW WWSAPI usando a ferramenta wstracedump.exe (funciona no Windows XP e versões posteriores)

Wstracedump.exe é uma ferramenta de consumidor ETW personalizada desenvolvida que processa eventos no arquivo de rastreamento ETW WWSAPI e produz saída legível humana. Ele pode produzir a saída de todas as plataformas com suporte. Veja seu uso (wstracedump.exe-?) para obter mais informações.

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>Exibindo rastreamentos de arquivos de rastreamento ETW WWSAPI usando as ferramentas de ETW (funciona no Windows Vista e versões posteriores)

Tracerpt.exe é a ferramenta para exibir o conteúdo de um arquivo de log de eventos ETW e disponível em todas as plataformas com suporte. Ele pode ser usado para gerar arquivos de despejo CSV, EVTX ou XML de um arquivo de log de eventos do ETW. No entanto, o arquivo de saída gerado tem rastreamentos legíveis somente no Windows Vista e posterior. Estas instruções descrevem como gerar o arquivo de despejo XML e usá-lo junto com um arquivo XSL para exibir os rastreamentos em um bom formato (o arquivo XSL é muito trivial e pode ser alterado se forem desejados formatos diferentes).

-   Executar

    **Tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    para criar um despejo XML a partir do arquivo ETL binário (tracerpt.exe cria o arquivo de saída em formato XML por padrão. Executar Tracerpt-? Para ver outros formatos disponíveis).

-   Neste ponto, você pode ver as informações de rastreamento no arquivo XML. Além disso, você pode abrir o arquivo de wstrace.htm e usar o arquivo de despejo XML e o arquivo wstrace. xsl para ver os rastreamentos em um formato mais interessante. Observe que os arquivos precisam estar no computador local para poderem usar esse arquivo HTML no IE.

## <a name="security"></a>Segurança

Ao habilitar o rastreamento, os administradores devem levar em conta que consome espaço em disco e capacidade de computação adicionais. Um cliente mal-intencionado ou aplicativo pode esgotar os recursos do sistema, a menos que as configurações de rastreamento sejam definidas com limites razoáveis. Ao usar o recurso de rastreamento de mensagens, as mensagens que realizam informações confidenciais, como credenciais, informações pessoais etc., podem ser mantidas no disco ou exibidas por qualquer pessoa que tenha acesso ao Visualizador de eventos do sistema. Como uma mitigação desse problema, o rastreamento pode ser habilitado por usuários do sistema ou administrador no Windows 2003 e posterior. O rastreamento de mensagens é desabilitado no Windows XP no qual qualquer usuário pode ativar o rastreamento.

A seguinte enumeração é usada com o rastreamento:

-   [**\_API de rastreamento do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




