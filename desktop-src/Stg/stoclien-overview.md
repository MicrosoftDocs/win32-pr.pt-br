---
title: Visão geral do StoClien
description: O exemplo StoClien demonstra como o cliente usa o armazenamento estruturado e como ele direciona um componente de servidor para usar esse armazenamento.
ms.assetid: 1f540e0f-2189-4f45-aad3-9b4b56732907
keywords:
- Visão geral do StoClien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee37f6f84cf981bda637abbd96ff8e8f0314d8ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105753081"
---
# <a name="stoclien-overview"></a>Visão geral do StoClien

## <a name="purpose"></a>Finalidade

O foco principal do exemplo de [StoClien](structured-storage-client-sample--stoclien-.md) é como o cliente usa o armazenamento estruturado e como ele instrui um componente de servidor a usar esse armazenamento. O exemplo StoClien demonstra um modelo de programação de serviços de armazenamento estruturados.

## <a name="functionality"></a>Funcionalidade

A funcionalidade [StoClien](structured-storage-client-sample--stoclien-.md) é semelhante aos exemplos de "rabisco" em algumas versões do Microsoft Visual C++. A diferença entre o exemplo de StoClien e o exemplo de [StoServe](structured-storage-server-sample--stoserve-.md) é uma arquitetura interna baseada em tecnologia com. Uma distinção de arquitetura clara é mantida entre o cliente COM e o servidor COM.

O [StoClien](structured-storage-client-sample--stoclien-.md) carrega e salva seus desenhos no armazenamento estruturado de arquivos compostos com.

O exemplo [StoClien](structured-storage-client-sample--stoclien-.md) cria e usa o objeto com de copapel com conexão que é fornecido como o \_ componente DllPaper do CLSID no servidor [StoServe](structured-storage-server-sample--stoserve-.md) . O cliente StoClien cria um objeto de copapel e controla-o por meio da interface IPaper que o objeto expõe. O StoClien obtém dados de desenho do usuário e os representa graficamente em uma janela que ele gerencia. O StoClien usa a interface IPaper de copapel para salvar os dados de desenho em copapel e para direcionar as operações de armazenamento de arquivos nesses dados.

Um objeto COM de copapel encapsula apenas o armazenamento baseado em servidor dos dados do papel de desenho: nenhum comportamento de GUI (interface gráfica do usuário) é fornecido no lado do servidor. Todo o comportamento da GUI é isolado no cliente. Os recursos de gerenciamento de dados e armazenamento de objetos de copapel estão disponíveis apenas por meio de uma interface personalizada COM, IPaper.

[StoClien](structured-storage-client-sample--stoclien-.md) coopera com o copaper para carregar e salvar os dados de desenho de copapel. StoClien Obtém uma interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para o objeto de armazenamento em um arquivo composto. Em suas operações de carregar e salvar, o StoClien passa um ponteiro para a interface **IStorage** para o copapel no servidor. O copaper usa o **IStorage** fornecido para criar fluxos no armazenamento. O copaper pode usar a interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) padrão para ler e gravar os dados de desenho que ele gerencia.

O copaper gerencia apenas os dados de desenho; Ele não executa ações de GUI. O [StoClien](structured-storage-client-sample--stoclien-.md) fornece a GUI para o aplicativo de desenho. Ele encapsula isso em um objeto CGuiPaper do C++ central.

O [StoClien](structured-storage-client-sample--stoclien-.md) também implementa a interface IPaperSink personalizada em um objeto com COPaperSink e conecta essa interface a um ponto de conexão apropriado no objeto de copapel do servidor. O copaper usa a interface IPaperSink conectada para enviar notificações de volta para o StoClien. O redesenho de GUI normal dos dados de desenho de copapel é feito no StoClien usando a tecnologia de objetos conectáveis de copapel.

[StoClien](structured-storage-client-sample--stoclien-.md) é um aplicativo que você pode executar diretamente da maneira normal ou da janela de prompt de comando. StoClien aceita um parâmetro de nome de arquivo opcional na linha de comando.

No exemplo a seguir, Drawing. PAP é um arquivo composto que contém o armazenamento estruturado compatível com DllPaper de dados de desenho. Se nenhum parâmetro de nome de arquivo de linha de comando for especificado, [StoClien](structured-storage-client-sample--stoclien-.md) usará o nome de arquivo padrão StoClien. PAP e tentará abri-lo no mesmo diretório que o Stoclien.exe em execução.

**StoClien c: \\ desenhos \\ Drawing. PAP**

## <a name="support-information"></a>Informações de suporte

Para obter mais informações, descrições funcionais e um tutorial de código para [StoClien](structured-storage-client-sample--stoclien-.md), consulte a seção Tour de código em Stoclien.htm. Para obter mais informações sobre a operação de usuário externo do StoClien, consulte as seções uso e operação no Stoclien.htm. Para ler Stoclient.htm, execute Tutorial.exe no diretório principal do tutorial e clique na lição StoClien na tabela de lições. Como alternativa, clique em Stoclien.htm depois de localizar o diretório principal do tutorial no Windows Explorer. Para obter mais informações sobre como o [**StoServe**](structured-storage-server-sample--stoserve-.md) funciona e expõe seus serviços para o StoClien, consulte Stoserve.htm no diretório principal do tutorial. Lembre-se de que você deve criar o Stoserve.dll antes de compilar o StoClien. O makefile para [**StoServe**](structured-storage-server-sample--stoserve-.md) registra esse servidor no registro do sistema, portanto, você deve compilar [**StoServe**](structured-storage-server-sample--stoserve-.md) antes de tentar executar o StoClien.

Para obter mais informações sobre como configurar um sistema para criar e testar os exemplos de código nesta série de tutoriais COM, consulte [como criar exemplos](how-to-build-samples.md). O makefile fornecido (MAKEFILE) é compatível com Microsoft NMAKE. Para criar uma compilação de depuração, emita o comando NMAKE na janela do prompt de comando.

Para sua conveniência, um arquivo de projeto é fornecido para cada exemplo para uso em Microsoft Visual Studio. Para carregar o projeto para o exemplo [StoClien](structured-storage-client-sample--stoclien-.md) , execute o Visual Studio no prompt de comando no diretório de exemplo da seguinte maneira:

MSDEV STOCLIEN. DSP

Você também pode clicar duas vezes no arquivo Stoclient. Dsp no Windows Explorer para carregar um projeto de exemplo no Visual Studio. No Visual Studio, você pode procurar as classes C++ da fonte de exemplo e geralmente executar as outras operações de edição-compilação-depuração. Lembre-se de que, como parte do SDK do servidor, a compilação desses exemplos de dentro do Visual Studio requer a configuração apropriada dos caminhos de diretório no Visual Studio. Para obter mais informações, consulte [como criar exemplos](how-to-build-samples.md).

## <a name="remarks"></a>Comentários

O exemplo de cliente e outros exemplos relacionados devem ser compilados antes que você possa executar o cliente. Para obter mais informações sobre como criar exemplos, consulte [como criar exemplos](how-to-build-samples.md). Se você tiver criado os exemplos apropriados, Stoclien.exe será o executável do cliente a ser executado para este exemplo.

O aplicativo Stoclien.exe fornece a interface do usuário para este tutorial. Ele exercita as Stoserve.dll associadas, mas independentes, para demonstrar o uso do cliente e do servidor do armazenamento estruturado COM em arquivos compostos.

 

 




