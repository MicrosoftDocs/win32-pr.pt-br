---
title: Visão geral do SDK Windows Formato de Mídia
description: Visão geral do SDK Windows Formato de Mídia
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows SDK de Formato de Mídia, criação e edição de arquivo ASF
- ASF (Advanced Systems Format), criação e edição de arquivos
- ASF (Formato de Sistemas Avançados), criação e edição de arquivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80436415a6017d0429493b1d4b5be92dcb682f572796e5e9e1c3cfaa8795e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846421"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Visão geral do SDK Windows Formato de Mídia

O Windows SDK de Formato de Mídia contém objetos para executar tarefas em três pontos na vida útil de um arquivo ASF: criação, edição e reprodução. Alguns aplicativos, principalmente aqueles para edição de vídeo, usarão a ampla funcionalidade do SDK de Formato de Mídia do Windows para ler o conteúdo dos arquivos ASF, alterar esse conteúdo e gravar os resultados em um novo arquivo. No entanto, é mais fácil pensar nesse SDK nos três estágios de criação, edição e reprodução de arquivos.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Criação de arquivo ASF com o SDK Windows Formato de Mídia

O processo de escrever arquivos ASF com o SDK Windows Formato de Mídia é, em um alto nível, bastante simples. A criação de arquivo é gerenciada por um objeto de autor. Você diz ao objeto de autor que tipo de arquivo deseja criar especificando um objeto de perfil para ele usar. Cada objeto de perfil contém as configurações de um arquivo ASF. Alguns perfis são incluídos com esse SDK e o suporte à edição de perfil é fornecido por vários objetos. Quando você tiver definido um perfil para o objeto de writer a ser usado, poderá começar a passar amostras para o autor para processamento. Na maioria dos casos, um exemplo é um trecho de áudio ou vídeo descompactado, mas um exemplo pode ser qualquer tipo de dados.

Internamente, o autor executa três tarefas principais. Primeiro, se o fluxo ao que um exemplo pertence deve ser compactado, o autor se comunica com a parte de codificação do codec (itor/descompactador) para compactar o exemplo. Depois que os exemplos estão no formato especificado pelo perfil, o autor divide os exemplos em pacotes de tamanho apropriado a serem transmitidos por uma rede. Por fim, os dados dos vários fluxos são multiplexados ou intercalados para que exemplos com tempos de apresentação semelhantes em todos os fluxos sejam próximos um do outro na seção de dados do arquivo ASF.

Na verdade, o objeto writer não escreve um arquivo em si. Ele se comunica com um ou mais objetos chamados sinks, que entregam os dados do autor para seu destino. No caso de arquivos locais, um sink de arquivo gerencia a escrita dos dados no arquivo. Você também pode configurar os sinks de rede para entregar os dados do ASF em uma rede. Normalmente, mais de um sink é usado. Por exemplo, um aplicativo pode transmitir um arquivo em uma rede e salvar uma cópia como um arquivo em um disco local simultaneamente. Usando um sink push, você pode transmitir conteúdo de seu aplicativo de escrita para um ou mais servidores que executam Windows Media Services, o que distribuirá o conteúdo aos usuários.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>Edição de arquivo ASF com o SDK Windows Formato de Mídia (Edição de Metadados)

Editar o conteúdo da seção de dados de um arquivo ASF envolve reescrever o arquivo. O Windows SDK de Formato de Mídia não fornece nenhum objeto que manipule a seção de dados no local. Para edições simples, como concatenação de dois arquivos ou redução de conteúdo de um arquivo, você pode ler exemplos sem descompactá-los e, em seguida, escrevê-los em um novo arquivo usando as mesmas informações de título. Edições mais complicadas envolvem fazer alterações no perfil usado para o novo arquivo.

O Windows SDK de Formato de Mídia dá suporte à edição de partes da seção de header sem reescrever o arquivo. O header de um arquivo ASF contém muitos tipos diferentes de dados. Os mais comumente editados são atributos de metadados, que são pares de nome/valor que descrevem aspectos do conteúdo e as pessoas envolvidas na comagem. Você pode editar metadados usando o objeto do editor de metadados do SDK Windows Formato de Mídia. Esse objeto abrirá um arquivo ASF, permitirá que você altere parte do conteúdo do header, escreva as alterações no arquivo e feche o arquivo. A edição de metadados é muito simples, com chamadas de método simples para recuperar e definir valores.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Leitura de arquivo ASF com o SDK Windows Formato de Mídia

O Windows SDK de Formato de Mídia fornece dois objetos distintos para ler arquivos ASF: o objeto de leitor e o objeto de leitor síncrono. O objeto de leitor está disponível em todas as versões do SDK, enquanto o objeto de leitor síncrono requer o SDK do Windows Media Format 9 Series ou uma versão posterior. A principal diferença entre os dois é que o objeto de leitor fornece exemplos para seu aplicativo disparando eventos para um método de retorno de chamada, enquanto o leitor síncrono fornece exemplos individuais em resposta a chamadas de método.

Para usar o objeto de leitor, você deve implementar vários métodos de retorno de chamada para reagir ao status e mensagens de exemplo do objeto de leitor. Configure o leitor para entregar o conteúdo como quiser, inicie o leitor e aguarde as mensagens de exemplo. O processo de recuperação de exemplos de um arquivo ASF é basicamente o inverso do processo de escrita. O objeto leitor se comunica com os codecs necessários para decodificar quaisquer fluxos compactados e fornece dados descompactados para seu aplicativo. Você também pode configurar o objeto de leitor para fornecer exemplos em seu estado compactado, para que você possa incluir um fluxo codificado anteriormente em um novo arquivo.

O objeto de leitor síncrono funciona da mesma maneira que o objeto de leitor. Mas, em vez de configurar retornos de chamada, você deve solicitar cada amostra do leitor síncrono individualmente. O uso do leitor síncrono requer apenas um único thread, enquanto o uso do leitor requer vários threads. O objeto de leitor síncrono tem várias vantagens em relação ao objeto de leitor em determinadas circunstâncias, principalmente para aplicativos de edição de conteúdo que precisam acessar rapidamente diferentes partes de um arquivo e copiar dados entre arquivos. O objeto de leitor síncrono é muito mais simples de usar e facilita a busca por locais específicos na seção de dados. No entanto, o leitor síncrono não dá suporte à leitura de arquivos em uma rede e não dá suporte ao gerenciamento de direitos digitais.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Outras operações com o SDK Windows formato de mídia

Além das três principais áreas funcionais descritas, o SDK Windows Formato de Mídia tem objetos para executar outras operações relacionadas a arquivos ASF. O objeto do gerenciador de perfil é usado para criar e acessar perfis e salvá-los. O objeto indexador cria objetos de índice em arquivos ASF que permitem a busca em arquivos de vídeo. Por fim, o objeto leitor e o objeto de autor suportam o gerenciamento de direitos digitais para proteger os direitos intelectual dos criadores de conteúdo.

**Observação** A intenção da estrutura de arquivos ASF e desse SDK em geral é produzir arquivos de mídia digital contendo áudio e vídeo, e essa documentação é escrita com esse fim em mente. No entanto, a estrutura de arquivo ASF também funcionará para outros tipos de conteúdo. Você pode encontrar muitos aplicativos para arquivos ASF que não estão relacionados a áudio e vídeo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o SDK Windows Formato de Mídia**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




