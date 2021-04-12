---
title: Visão geral do Windows Media Format SDK
description: Visão geral do Windows Media Format SDK
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- SDK do Windows Media Format, criação e edição de arquivos ASF
- ASF (Advanced Systems Format), criação e edição de arquivos
- ASF (formato de sistemas avançados), criação e edição de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4f58be5d377e44fc0f68c89ad580a554902c58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291874"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Visão geral do Windows Media Format SDK

O SDK do Windows Media Format contém objetos para executar tarefas em três pontos na vida de um arquivo ASF: criação, edição e reprodução. Alguns aplicativos, especialmente aqueles para edição de vídeo, usarão a ampla funcionalidade do Windows Media Format SDK para ler o conteúdo de arquivos ASF, alterar esse conteúdo e gravar os resultados em um novo arquivo. No entanto, é mais fácil considerar esse SDK nos três estágios de criação, edição e reprodução de arquivos.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Criação de arquivo ASF com o Windows Media Format SDK

O processo de gravar arquivos ASF com o Windows Media Format SDK é, em um nível alto, bastante simples. A criação do arquivo é gerenciada por um objeto do gravador. Você informa ao objeto do gravador qual tipo de arquivo você deseja criar especificando um objeto de perfil para ele usar. Cada objeto de perfil contém as configurações para um arquivo ASF. Alguns perfis estão incluídos neste SDK e o suporte à edição de perfil é fornecido por vários objetos. Quando você tiver definido um perfil para o objeto gravador a ser usado, você pode começar a passar amostras para o gravador para processamento. Na maioria dos casos, um exemplo é um pedaço de áudio ou vídeo que é descompactado, mas um exemplo pode ser qualquer tipo de dados.

Internamente, o gravador executa três tarefas principais. Primeiro, se o fluxo ao qual um exemplo pertence for compactado, o gravador se comunicará com a parte de codificação do codec (compressor/descompactador) para compactar o exemplo. Depois que os exemplos estiverem no formato especificado pelo perfil, o gravador quebrará os exemplos em pacotes de tamanho apropriado a serem transmitidos em uma rede. Por fim, os dados dos vários fluxos são multiplexados ou intercalados para que os exemplos com tempos de apresentação semelhantes em todos os fluxos estejam próximos uns dos outros na seção de dados do arquivo ASF.

O objeto do gravador não grava, na verdade, um arquivo. Ele se comunica com um ou mais objetos chamados coletores, que entregam os dados do gravador para seu destino. No caso de arquivos locais, um coletor de arquivos gerencia a gravação dos dados no arquivo. Você também pode configurar coletores de rede para entregar os dados de ASF em uma rede. Normalmente, mais de um coletor é usado. Por exemplo, um aplicativo pode transmitir um arquivo por uma rede e salvar uma cópia como um arquivo em um disco local simultaneamente. Usando um coletor de push, você pode transmitir conteúdo do seu aplicativo de gravação para um ou mais servidores que executam o Windows Media Services, que, em seguida, distribuirá o conteúdo aos usuários.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>Edição de arquivo ASF com o Windows Media Format SDK (edição de metadados)

A edição do conteúdo da seção de dados de um arquivo ASF envolve a regravação do arquivo. O Windows Media Format SDK não fornece nenhum objeto que manipule a seção de dados em vigor. Para edições simples, como concatenar dois arquivos ou cortar conteúdo de um arquivo, você pode ler amostras sem descompactá-los e, em seguida, gravá-los em um novo arquivo usando as mesmas informações de cabeçalho. As edições mais complicadas envolvem fazer alterações no perfil usado para o novo arquivo.

O SDK do Windows Media Format dá suporte à edição de partes da seção de cabeçalho sem reescrever o arquivo. O cabeçalho de um arquivo ASF contém muitos tipos diferentes de dados. Os mais comumente editados são atributos de metadados, que são pares de nome/valor que descrevem aspectos do conteúdo e das pessoas envolvidas na realização dele. Você pode editar os metadados usando o objeto editor de metadados do SDK do Windows Media Format. Esse objeto abrirá um arquivo ASF, permitirá que você altere parte do conteúdo do cabeçalho, grave as alterações no arquivo e feche o arquivo. A edição de metadados é muito simples, com chamadas de método simples para recuperar e definir valores.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Leitura de arquivo ASF com o Windows Media Format SDK

O Windows Media Format SDK fornece dois objetos distintos para ler arquivos ASF: o objeto leitor e o objeto leitor síncrono. O objeto leitor está disponível em todas as versões do SDK, enquanto o objeto leitor síncrono requer o SDK do Windows Media Format 9 Series ou uma versão posterior. A principal diferença entre os dois é que o objeto leitor fornece amostras para seu aplicativo acionando eventos para um método de retorno de chamada, enquanto o leitor síncrono fornece amostras individuais em resposta a chamadas de método.

Para usar o objeto leitor, você deve implementar vários métodos de retorno de chamada para reagir às mensagens de status e de exemplo do objeto leitor. Configure o leitor para entregar o conteúdo como desejar, inicie o leitor e aguarde as mensagens de exemplo. O processo de recuperação de amostras de um arquivo ASF é basicamente o inverso do processo de gravação. O objeto leitor se comunica com os codecs necessários para decodificar todos os fluxos compactados e entrega dados descompactados ao seu aplicativo. Você também pode configurar o objeto leitor para fornecer amostras em seu estado compactado, para que você possa incluir um fluxo codificado anteriormente em um novo arquivo.

O objeto leitor síncrono funciona praticamente da mesma forma que o objeto leitor. Mas, em vez de configurar retornos de chamada, você deve solicitar cada exemplo do leitor síncrono individualmente. O uso do leitor síncrono requer apenas um único thread, ao passo que o uso do leitor requer vários threads. O objeto leitor síncrono tem várias vantagens em relação ao objeto leitor em determinadas circunstâncias, principalmente para aplicativos de edição de conteúdo que precisam acessar rapidamente diferentes partes de um arquivo e copiar dados entre arquivos. O objeto leitor síncrono é muito mais simples de usar e torna fácil procurar locais específicos na seção de dados. No entanto, o leitor síncrono não dá suporte à leitura de arquivos em uma rede e não oferece suporte ao gerenciamento de direitos digitais.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Outras operações com o Windows Media Format SDK

Além das três principais áreas funcionais que acabamos de descrever, o SDK do Windows Media Format tem objetos para executar outras operações relacionadas a arquivos ASF. O objeto Gerenciador de perfis é usado para criar e acessar perfis e salvá-los. O objeto indexador cria objetos de índice em arquivos ASF que permitem busca em arquivos de vídeo. Por fim, o objeto de leitor e o objeto de gravador dão suporte ao gerenciamento de direitos digitais para proteger os direitos intelectuais dos criadores de conteúdo.

**Observação** A intenção da estrutura do arquivo ASF e desse SDK em geral é produzir arquivos de mídia digital contendo áudio e vídeo, e essa documentação é escrita com esse fim em mente. No entanto, a estrutura do arquivo ASF também funcionará para outros tipos de conteúdo. Você pode encontrar muitos aplicativos para arquivos ASF que não estão relacionados a áudio e vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o SDK do Windows Media Format**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




