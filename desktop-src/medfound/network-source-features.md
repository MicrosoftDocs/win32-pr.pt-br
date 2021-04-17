---
description: Recursos de origem da rede
ms.assetid: a4e20ecb-c145-4823-ae59-f6fc88593d86
title: Recursos de origem da rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e937a97cf743740d9cebf84ad477c52cdee5083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553489"
---
# <a name="network-source-features"></a>Recursos de origem da rede

A fonte de rede fornece a implementação base para streaming de arquivos de mídia e expõe a interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) . A implementação de origem de rede específica depende do protocolo usado para abrir a fonte, como RTSP ou HTTP. As fontes de rede específicas de protocolo estendem a funcionalidade de rede básica. Para obter informações sobre os esquemas e protocolos com suporte, consulte [protocolos com suporte](supported-protocols.md).

A origem da rede:

-   Implementa recursos como cache, detecção de proxy e reconexão automática.
-   Converte chamadas independentes de protocolo do resolvedor de origem para chamadas específicas de protocolo.
-   Interage com a camada de soquete e o sistema operacional. Analisa a descrição de SDP e a usa como dados de configuração e lê os dados de fluxo da camada de soquetes subjacentes. Ao receber, a fonte de rede é responsável por reordenar e solicitar retransmissões de pacotes.

## <a name="network-source-creation"></a>Criação de origem de rede

A criação de uma fonte de mídia para uma origem da rede não é diferente de uma origem de mídia para um arquivo local. O aplicativo passa a URL para os métodos de origem para o [resolvedor de origem](source-resolver.md) , como [**IMFSourceResolver:: CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) ou [**IMFSourceResolver:: BeginCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfromurl) e especifica o \_ \_ sinalizador Mediate de resolução MF. Para obter mais informações sobre como usar esse sinalizador, consulte [usando o resolvedor de origem](using-the-source-resolver.md).

Dependendo do esquema fornecido pelo aplicativo, o resolvedor de origem carrega o objeto manipulador de esquema apropriado, que expõe a interface [**IMFSchemeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler) . O aplicativo também pode usar o manipulador de esquema diretamente para criar a origem da rede chamando [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

Para obter mais informações, consulte [manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md).

Media Foundation não dá suporte a fluxos de bytes para fontes de rede. O objeto de fluxo de bytes só tem suporte no cenário de conteúdo baixado. Todos os dados são transmitidos o mais rapidamente possível para que possam ser salvos como um arquivo no computador local. os servidores Web fornecem dados baixados. Não há comunicação entre o cliente e o servidor após o início do download. Nesse caso, o protocolo de download HTTP é usado.

Se o aplicativo solicitar o resolvedor de origem para criar um objeto de fluxo de bytes para esquemas "http:", "MMS:" ou "RTSP:", a chamada falhará com o \_ erro de esquema MF E \_ sem suporte \_ .

> [!Note]  
> No Windows 7, a fonte de rede dá suporte aos arquivos de estação de mídia do Windows (. NSC). Esses arquivos são usados no streaming multicast do conteúdo de mídia em uma rede. Para criar a origem de rede para um especificado. Arquivo NSC, o aplicativo deve usar o resolvedor de origem.

 

Se o aplicativo estiver usando o manipulador de esquema, a chamada assíncrona ignorará o parâmetro *dwFlags* e retornará um ponteiro para a origem da rede na conclusão.

A ilustração a seguir mostra o fluxo de dados para streaming de mídia usando a fonte de rede.

![fluxograma mostrando caminhos do aplicativo para o servidor de streaming, com um loop entre a origem da rede e a sessão de mídia](images/3f9186ea-53ed-4a31-a097-92f39fa08624.gif)

## <a name="network-source-configuration"></a>Configuração de origem da rede

Este tópico descreve os recursos com suporte da fonte de rede e as opções de configuração associadas. Um aplicativo pode configurar a origem da rede ao criar o objeto de origem da rede. Essas opções são armazenadas em um objeto **IPropertyStore** , que o aplicativo deve passar no parâmetro *pProps* dos métodos do resolvedor de origem ou [**IMFSchemeHandler:: BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject).

### <a name="auto-reconnect"></a>Reconexão automática

O recurso de reconexão automática da fonte de rede permite que um cliente se reconecte ao servidor de mídia automaticamente quando a conexão TCP com o servidor falhar ou o cliente não receber pacotes. Quando a conexão falha, a origem da rede tenta se reconectar ao servidor de mídia usando a mesma configuração que foi usada na conexão anterior. O processo de reconexão é assíncrono. A origem da rede gera o evento [MEReconnectStart](mereconnectstart.md) quando ele começa a reconexão e o evento [MEReconnectEnd](mereconnectend.md) quando a reconexão é bem-sucedida ou falha.

Se o número de tentativas de reconexão exceder o valor máximo especificado pela propriedade [**MFNETSOURCE \_ AUTORECONNECTLIMIT**](mfnetsource-autoreconnectlimit-property.md) , a operação de reconexão será cancelada. O número de tentativas de reconexão é armazenado na propriedade [**MFNETSOURCE \_ AUTORECONNECTPROGRESS**](mfnetsource-autoreconnectprogress-property.md) .

A reconexão automática permite a reprodução suave de conteúdo de mídia mesmo quando a conexão TCP com o servidor de mídia falha. Para uma experiência de reprodução suave, o cliente deve ter dados suficientes, pelo menos de 1 a 2 minutos, em seu cache para continuar a reprodução até a reconexão. A quantidade máxima de dados que a fonte de rede pode armazenar em buffer pode ser definida na propriedade [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) .

### <a name="fast-streaming"></a>Transmissão rápida

O cliente de origem de rede solicita que o servidor transmita alguns dos dados no início do conteúdo a uma taxa mais rápida do que a especificada pela taxa de bits do conteúdo. Se a *inicialização rápida* estiver habilitada no servidor, o servidor enviará um fluxo de taxa de bits acelerada para que o cliente possa armazenar em buffer uma quantidade suficiente de dados mais rápido do que em tempo real. Isso melhora a experiência do usuário, minimizando os atrasos iniciais de buffer, que podem ser causados por vários fatores, como baixa velocidade do computador cliente ou da rede, e largura de banda disponível.

Para especificar a quantidade de dados de streaming rápido que o cliente pode solicitar, defina a propriedade [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) . Se a fonte de rede estiver usando UDP como o protocolo de transporte, especifique a quantidade máxima de dados de streaming rápido definindo a propriedade [**MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION**](mfnetsource-maxudpacceleratedstreamingduration-property.md) em vez disso.

O streaming rápido no cliente também é possível por meio do recurso de *cache rápido* — streaming sob demanda de conteúdo mais rápido do que em tempo real e cache de dados no cache local do cliente. Para usar esse tipo de streaming rápido, o cache rápido deve ser habilitado na fonte de rede e o servidor deve dar suporte a ele. Quando o cliente solicita o conteúdo do servidor, a fonte de rede primeiro verifica se o conteúdo já está no cache do cliente. Se o conteúdo estiver no cache local do cliente e não tiver expirado, ele será renderizado. Se o conteúdo não estiver no cache local ou já tiver expirado, o conteúdo será transmitido e armazenado em cache, e a origem da rede o reproduzirá do cache local. Nas solicitações subsequentes, para listas de reprodução, somente as entradas ausentes são armazenadas em cache e, em seguida, reproduzidas. Se uma entrada de playlist já estiver no cache local do cliente, ela será reproduzida a partir daí e não será armazenada em cache novamente.

Por padrão, o cache rápido é habilitado no cliente de origem de rede. No entanto, os seguintes fatores também determinam se o recurso é usado:

-   O cliente deve ter largura de banda extra disponível para baixar e armazenar o conteúdo em cache mais rápido do que a velocidade normal.
-   O cliente deve ter espaço em disco suficiente. Se o cliente tiver menos de 100 MB de espaço livre em disco depois de armazenar em cache o conteúdo solicitado sob demanda, ele não será armazenado em cache, mas será transmitido e renderizado simultaneamente.

O recurso de cache rápido é controlado pela propriedade [**MFNETSOURCE \_ CACHEENABLED**](mfnetsource-cacheenabled-property.md) .

### <a name="buffer-management"></a>Gerenciamento de buffer

A fonte de rede fornece um gerenciamento de buffer eficiente que monitora o estado do buffer no cliente. Por padrão, a origem de rede armazena cinco segundos de dados na inicialização. Esse valor pode ser configurado definindo a propriedade [**MFNETSOURCE \_ BUFFERINGTIME**](mfnetsource-bufferingtime-property.md) . Com base nesse valor de propriedade, a origem da rede computa o tamanho do buffer que é suficiente para garantir a reprodução tranqüila e ininterrupta do conteúdo de mídia. Se essa propriedade for definida como 0, o gerenciamento de buffer será desabilitado. Quando a quantidade de conteúdo no buffer é baixa, a origem da rede começa a armazenar em buffer e gera o evento [MEBufferingStarted](mebufferingstarted.md) para indicar que o buffer foi iniciado. Após o recebimento desse evento, o pipeline parará de renderizar. Quando o buffer é concluído, a origem da rede gera o evento [MEBufferingStopped](mebufferingstopped.md) e o cliente pode iniciar a renderização novamente.

O cliente começa a renderizar o conteúdo depois de ter acumulado a quantidade de dados indicada pelo tamanho do buffer do primeiro exemplo. Se esse valor for inferior ao tamanho do buffer calculado, a reprodução será iniciada imediatamente. Esse comportamento é muito semelhante ao recurso de inicialização rápida.

A propriedade [**MFNETSOURCE \_ MAXBUFFERTIMEMS**](mfnetsource-maxbuffertimems-property.md) armazena a quantidade máxima de dados que podem ser armazenados em buffer.

### <a name="bandwidth-selection"></a>Seleção de largura de banda

Quando um cliente se conecta ao servidor de mídia, como parte da configuração da conexão, a origem da rede executa uma medida de *par de pacotes estáticos* para estimar a largura de banda de link inicial entre o cliente e o servidor. Com base no resultado dessa medição, o cliente pode selecionar fluxos de áudio e vídeo que se enquadram na largura de banda estimada. Isso garante a reprodução suave do conteúdo de streaming de mídia.

Durante o estágio de inicialização rápida, a medida de *pares de pacotes dinâmicos* é executada. Nesse processo, o cliente recebe grandes quantidades de dados, que podem ser vários pacotes ou amostras.

O resultado da medição de pares de pacotes dinâmicos é mais preciso do que a estimativa de largura de banda de link retornada por uma medida de par de pacotes estáticos porque o processo de par de pacotes estático envia um único pacote de tamanho fixo, o que pode não gerar resultados precisos para redes de largura de banda alta.

O aplicativo pode obter a largura de banda estimada usando a propriedade [**MFNETSOURCE \_ PPBANDWIDTH**](mfnetsource-ppbandwidth-property.md) .

As condições de rede podem ser alteradas dinamicamente, causando problemas na reprodução da origem da rede. A origem da rede pode alterar a seleção de fluxo inicial do cliente com base na taxa de recebimento e no estado do buffer. Por exemplo, o cliente pode mudar para uma taxa de bits inferior durante o congestionamento da rede e voltar para uma taxa de bits mais alta quando o tráfego de rede tiver melhorado e o cliente tiver acumulado uma quantidade suficiente de conteúdo em buffer.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Rede em Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 



