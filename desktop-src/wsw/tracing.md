---
title: Rastreamento
description: O rastreamento usa o ETW (Rastreamento de Windows).
ms.assetid: b008bae2-9423-4e72-ae03-9cd50f73d812
keywords:
- Rastreamento de serviços Web para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2bcd5c07c2c5ebf3a28620e39efe3034d3c2bc024ac487caaec38e3c69fca9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707256"
---
# <a name="tracing"></a>Rastreamento

O rastreamento usa o ETW (Rastreamento de Windows). Para aproveitar as ferramentas de rastreamento disponíveis com o Windows Server 2008 R2, instale o SDK do Microsoft Windows do site downloads do [MSDN.](https://www.microsoft.com/download/details.aspx?id=8279)


Há três níveis de rastreamento com suporte:

-   Detalhado (todos os rastreamentos disponíveis).
-   Informações (rastreamentos informacionais).
-   Erro (rastreamentos de erro).

Os seguintes eventos são rastreados:

-   Erros (Level=Error, Level=Info ou Level=Verbose).
-   Entrada/saída de uma API (Level=Info ou Level=Verbose).
-   Início e conclusão de qualquer E/S (Level=Info ou Level=Verbose)
-   Mensagens SOAP trocadas (Level=Verbose, disponíveis no Windows 2003 SP1 e posterior)

## <a name="generating-and-viewing-wwsapi-traces"></a>Gerando e exibindo rastreamentos WWSAPI

O WWSAPI usa os eventos baseados em manifesto Windows Vista e superior. Como resultado, a experiência de rastreamento tem algumas diferenças com base na versão do sistema operacional. A geração de rastreamentos ETW pode ser feita usando as ferramentas etw in-box em todas as plataformas com suporte. No entanto, exibir os rastreamentos ETW em um bom formato requer ferramentas personalizadas no Windows XP SP2 e Windows 2003 SP1. Há algumas maneiras diferentes de coletar e exibir rastreamentos de eventos ETW WWSAPI dependendo da versão do sistema operacional.

## <a name="enabling-and-viewing-wwsapi-traces-in-event-viewer-works-on-windows-vista-and-above"></a>Habilitando e exibindo rastreamentos WWSAPI Visualizador de Eventos (funciona no Windows Vista e superior)

-   Execute eventvwr.msc na linha de comando ou no menu executar.
-   Clique no link exibir no painel Ações à direita e habilita a opção Mostrar logs de análise e depuração.
-   Navegue até Logs de Aplicativo e \\ Serviço Windows \\ \\ provedores WebServices no painel esquerdo.
-   Clique com o botão direito do mouse no provedor de rastreamento e selecione Habilitar log.
-   Execute seu cenário.
-   Ao atualizar a página do visualizador de eventos, você deve começar a ver as entradas de rastreamento WWSAPI.

## <a name="enabling-and-viewing-wwsapi-traces-using-wstracebat-script-works-on-xpsp2-and-above"></a>Habilitando e exibindo rastreamentos WWSAPI usando Wstrace.bat Script (funciona no XPSP2 e superior)

O wstrace.bat em lotes fornece uma maneira conveniente de:

-   Criar um log de rastreamento
-   Excluir um log de rastreamento
-   Habilitar e desabilitar o rastreamento
-   Atualizar o nível de rastreamento (informações/erro/detalhado)
-   Convertendo logs de rastreamento em arquivos CSV

O arquivo em lotes usa logman.exe para todos os comandos, com exceção de converter os logs em arquivo CSV, o que requer uma ferramenta personalizada (wstracedump.exe).

## <a name="using-tracing-commands"></a>Usando comandos de rastreamento

O comando a seguir cria um log que usa informações, erro ou nível detalhado. Esse comando requer privilégios elevados.

**wstrace.bat erro \[ de \| informações de criação \| detalhada\]**

O comando a seguir exclui o log. Esse comando requer privilégios elevados.

**wstrace.bat excluir**

O comando a seguir habilita o rastreamento. Primeiro, você deve criar um log.

**wstrace.bat em**

O nível de rastreamento (informações, erro ou detalhado) pode ser modificado da seguinte forma:

**wstrace.bat erro \[ de informações de atualização \| \| detalhado\]**

Para despejar a saída do rastreamento, use o seguinte comando:

**wstrace.bat de despejo > temp.csv**

Os eventos serão despejados no arquivo CSV até que Ctrl-C seja pressionado ou o rastreamento seja desabilitado.

## <a name="tracing-file-format"></a>Formato de arquivo de rastreamento

Os arquivos CSV criados por wstrace.bat são arquivos de texto simples de variável separada por vírgula. Esses arquivos podem ser abertos em Excel, Bloco de notas etc.

As colunas do arquivo são as seguinte:

-   Carimbo de data/hora – carimbo de data/hora de quando o evento foi registrado
-   ProcessID – ID ULONG do processo que registra o evento
-   ThreadID – ID ULONG do thread que grava o evento
-   Evento – o valor enumerado do tipo de evento pode ser ("api enter" \| "api pendente" \| "api ExitSyncSuccess" \| "api ExitSyncFailure" \| "api ExitAsyncSuccess" \| "api ExitAsyncFailure" \| "io started" \| "io \| completed" "io failed" \| "error" \| "received message start" "received message \| \| stop" "received message stop" \| "sending message start" \| "sending message" \| "sending message stop")
-   Operação – o nome da operação que está sendo invocada. Normalmente, isso é mapeada para a API que está sendo chamada.
-   Erro – número de erro HRESULT opcional
-   Informações – informações opcionais sobre o evento

## <a name="collecting-wwsapi-etw-trace-file-using-etw-tools-works-on-xpsp2-and-above"></a>Coletando o arquivo de rastreamento ETW do WWSAPI usando ferramentas ETW (funciona no XPSP2 e superior)

Habilitando o rastreamento ETW para WWSAPI

**logman start wstrace -bs 64 -ft 1 -rt -p Microsoft-Windows-WebServices \[ flags \[ level \] \] \[ -o <EtlLogFileName> \] -ets**

para criar e iniciar a sessão de rastreamento ETW. Logman.exe é uma ferramenta ETW in-box disponível em todas as plataformas com suporte. Observe que você precisa usar o Microsoft Windows WebServices como o nome do provedor \_ \_ no XPSP2 e W2K3. Você pode executar provedores de consulta logman para ver a lista de provedores registrados. O provedor Microsoft-Windows-WebServices (ou Microsoft \_ Windows WebServices) deve ser listado, a menos que não \_ esteja registrado. O provedor normalmente é registrado durante a instalação. No entanto, ele também pode ser registrado manualmente executando wevtutil.exe im (no Windows Vista e posterior) ou <ManifestFileName> mofcomp.exe <MofFileName> (no XPSP2 e W2K3).

Sinalizadores podem ser usados para filtrar os rastreamentos por seu tipo. Pode ser o valor OR'd dos seguintes tipos de rastreamento. Se não for fornecido, todos os tipos de rastreamento serão habilitados.

-   0x1 - rastreamentos de entrada/saída de API.
-   0x2 - Rastreamentos de erro.
-   0x4 - rastreamentos de E/S.
-   0x8 - rastreamentos de mensagem SOAP.
-   0x10 - rastreamentos de mensagem binária.

O nível pode ser usado para filtrar os rastreamentos por seu nível. Deve ser um dos valores a seguir. Se não for fornecido, todos os níveis de rastreamento serão habilitados.

-   0x1 - Rastreamentos fatais.
-   0x2 - Rastreamentos de erro.
-   0x3 - Rastreamentos de aviso.
-   0x4 - Rastreamentos informacionais.
-   0x5 - rastreamentos detalhados.

EtlLogFileName é o caminho para o arquivo de log de eventos ETW a ser criado (use a extensão .etl). Se não for fornecido, o ETW escolherá um nome aleatório que poderá ser consultado posteriormente. Esse arquivo não deve residir no diretório de perfil do usuário. O arquivo de log de eventos ETW (arquivo .etl) está em formato binário. Ele pode ser consumido por aplicativos ETW, mas não está no formato acessível por humanos. A próxima etapa descreve como exibir seu conteúdo.

Executar seu cenário

Coletando o arquivo de log de eventos ETW.

**logman stop wstrace -ets**

para interromper a sessão de rastreamento ETW. Isso ocorre quando o ETW para de registrar os eventos. O arquivo de log de eventos do ETW (especificado no parâmetro EtlLogFileName) está pronto para consumir. Ele pode ser exibido localmente (instruções são fornecidas abaixo) ou enviado ao grupo de produtos para investigação.

Exemplo de ponta a ponta usando ferramentas de ETW:

**logman start wstrace-bs 64-ft 1-rt-p Microsoft-Windows-webservices-o mytrace. etl-ets**

**Echo.. Execute seu cenário..**

**logman Stop wstrace-ETS**

**Tracerpt mytrace. etl-o mytrace.xml**

**wstrace.htm**

**Echo.. Use mytrace.xml e wstrace. xsl na página aberta.**

## <a name="viewing-wwsapi-etw-trace-file-traces-using-wstracedumpexe-tool-works-on-windows-xp-and-above"></a>exibindo rastreamentos de arquivos de rastreamento ETW WWSAPI usando a ferramenta wstracedump.exe (funciona no Windows XP e superior)

Wstracedump.exe é uma ferramenta de consumidor ETW personalizada desenvolvida que processa eventos no arquivo de rastreamento ETW WWSAPI e produz saída legível humana. Ele pode produzir a saída de todas as plataformas com suporte. Veja seu uso (wstracedump.exe-?) para obter mais informações.

## <a name="viewing-wwsapi-etw-trace-file-traces-using-etw-tools-works-on-windows-vista-and-above"></a>exibindo rastreamentos de arquivo de rastreamento etw WWSAPI usando ferramentas de etw (funciona no Windows Vista e superior)

Tracerpt.exe é a ferramenta para exibir o conteúdo de um arquivo de log de eventos ETW e disponível em todas as plataformas com suporte. Ele pode ser usado para gerar arquivos de despejo CSV, EVTX ou XML de um arquivo de log de eventos do ETW. no entanto, o arquivo de saída gerado tem rastreamentos legíveis somente no Windows Vista e posterior. Estas instruções descrevem como gerar o arquivo de despejo XML e usá-lo junto com um arquivo XSL para exibir os rastreamentos em um bom formato (o arquivo XSL é muito trivial e pode ser alterado se forem desejados formatos diferentes).

-   Executar

    **Tracerpt <EtlLogFileName> -o <OutputXMLFileName>**

    para criar um despejo XML a partir do arquivo ETL binário (tracerpt.exe cria o arquivo de saída em formato XML por padrão. Executar Tracerpt-? Para ver outros formatos disponíveis).

-   Neste ponto, você pode ver as informações de rastreamento no arquivo XML. Além disso, você pode abrir o arquivo de wstrace.htm e usar o arquivo de despejo XML e o arquivo wstrace. xsl para ver os rastreamentos em um formato mais interessante. Observe que os arquivos precisam estar no computador local para poderem usar esse arquivo HTML no IE.

## <a name="security"></a>Segurança

Ao habilitar o rastreamento, os administradores devem levar em conta que consome espaço em disco e capacidade de computação adicionais. Um cliente mal-intencionado ou aplicativo pode esgotar os recursos do sistema, a menos que as configurações de rastreamento sejam definidas com limites razoáveis. Ao usar o recurso de rastreamento de mensagens, as mensagens que realizam informações confidenciais, como credenciais, informações pessoais etc., podem ser mantidas no disco ou exibidas por qualquer pessoa que tenha acesso ao Visualizador de eventos do sistema. como uma mitigação desse problema, o rastreamento pode ser habilitado por usuários do sistema ou administrador no Windows 2003 e posterior. o rastreamento de mensagens é desabilitado no Windows XP no qual qualquer usuário pode ativar o rastreamento.

A seguinte enumeração é usada com o rastreamento:

-   [**\_API de rastreamento do WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_trace_api)

 

 




