---
title: Visão geral do StoServe
description: O exemplo de código StoServe mostra como usar serviços de armazenamento estruturados conforme fornecido na implementação de arquivos compostos. O uso das interfaces IStorage e IStream padrão é descrito.
ms.assetid: 41ccd333-15c8-46b2-91c6-3e1929f7198c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0c8325fbc20d4917785d0b83ca70bffa996824
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294325"
---
# <a name="stoserve-overview"></a>Visão geral do StoServe

## <a name="purpose"></a>Finalidade

O foco principal deste exemplo de código é o uso de serviços de armazenamento estruturado, conforme fornecido na implementação dos arquivos compostos. O uso das interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) e [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) padrão é descrito. **StoServe** trabalha com o exemplo de código [StoClien](structured-storage-client-sample--stoclien-.md) para ilustrar o uso conjunto de armazenamento de arquivos compostos por cliente e servidor.

## <a name="functionality"></a>Funcionalidade

O exemplo de **StoServe** apresenta o objeto com de copapel, que representa praticamente uma folha em branco de desenho de papel.

Os objetos de copapel expõem um conjunto de recursos para desenho de forma livre na superfície do papel usando a "tinta" de cor e largura especificadas. A funcionalidade é muito semelhante ao exemplo de tutorial "rabisco" em muitas versões do Microsoft Visual C++. A diferença no **StoServe** / **StoClien** Samples é uma arquitetura baseada principalmente em tecnologia com. Os recursos de papel de desenho eletrônico de objetos de copapel estão disponíveis para clientes por meio de uma interface [**IPaper**](ipaper-methods.md) personalizada. O copaper implementa a interface **IPaper** . Uma distinção clara da arquitetura é mantida entre o cliente e o servidor. Nenhuma GUI (interface gráfica do usuário) é fornecida por copaper. O design do objeto de copapel depende do cliente para todo o comportamento da GUI. O copaper encapsula apenas a captura baseada em servidor e o armazenamento dos dados de tinta desenhados.

Os dados de tinta que são desenhados na superfície de copapel podem ser armazenados e carregados de arquivos compostos. Os métodos [**IPaper**](ipaper-methods.md), [**Save**](ipaper--save.md) e [**Load**](ipaper--load.md) aceitam um ponteiro de interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . O copaper usa essa interface **IStorage** fornecida pelo cliente para armazenar os dados de desenho.

O copaper é hospedado em um servidor em processo e disponibilizado publicamente como um componente COM personalizado. Semelhante a outros servidores nesta série de tutoriais, o StoServe é um servidor COM de registro automático. Ele torna o tipo de objeto de copapel disponível para clientes como o componente DllPaper usando um \_ registro DllPaper de CLSID no registro.

Como no servidor do conservar anterior, há suporte para recursos de objeto conectáveis no copaper. A interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) é exposta e um ponto de conexão apropriado é implementado. Nesse contexto, uma interface IPaperSink personalizada de saída é declarada para uso no envio de notificações para o cliente.

As duas interfaces personalizadas [**IPaper**](ipaper-methods.md) e [**IPaperSink**](ipapersink-methods.md) são declaradas em IPaper. O H localizado no diretório irmão \\ Ltda comum. Os GUIDs para as interfaces e objetos são definidos em PAPGUIDS. O H localizado no mesmo diretório de inclusão comum.

O recurso CThreaded no APPUTIL é usado pelo **StoServe** para obter a segurança do thread, como ele estava no exemplo de FRESERVE. Os objetos de copapel são derivados da classe CThreaded e herdam seus métodos OwnThis e UnOwnThis. Esses métodos permitem que apenas um thread de cada vez tenha acesso ao servidor **StoServe** e a objetos de copapel gerenciados pelo servidor.

## <a name="copaper-com-object"></a>Objeto COM de copapel

O objeto COM de copapel é o tipo de objeto único gerenciado por esse servidor **StoServe** em processo. O copaper é construído como um objeto COM conectável com uma implementação da interface [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) padrão e uma implementação da interface [**IPaper**](ipaper-methods.md) personalizada. O copaper expõe a interface **IPaper** para que os clientes possam executar um pequeno conjunto de operações de papel eletrônico em uma instância do copaper. As operações essenciais estão iniciando uma sequência de desenho de tinta, desenhando os dados de tinta na superfície de papel virtual de copapel e encerrando a sequência de desenho de tinta. Neste esquema, supõe-se que o cliente seja um aplicativo de GUI controlado por um mouse ou dispositivo de Tablet. O cliente é responsável por converter os movimentos do mouse em solicitações para o copaper, o que salva essas solicitações como dados de tinta.

Há dois níveis de economia de dados de tinta em copapel. O copaper salva os dados de tinta em uma matriz baseada em RAM que representa o desenho atual, e o copapel de forma persistente salva um desenho inteiro em um arquivo composto. Os métodos na interface [**IPaper**](ipaper-methods.md) executam ambos.

Como o cliente não gerencia os dados de papel desenhados, mas é responsável por renderizá-lo como uma imagem na tela, a implementação de [**IPaper**](ipaper-methods.md) no copaper deve expor um método que permita que o cliente obtenha os dados de desenho. A tecnologia de objetos conectáveis no copaper é usada para essa finalidade. Um ponto de conexão do CONNPOINT \_ PAPERSINK é implementado por copaper para que um cliente possa se conectar ao copaper para receber os dados de tinta para desenho. Primeiro, o cliente chama o método [IPaper:: redesenhar](ipaper--redraw.md) no objeto de copapel para solicitar todos os dados de tinta do desenho atual. A implementação de copapel de redesenhar usa então a implementação de cliente do [**IPaperSink**](ipapersink-methods.md) para passar os dados para o cliente.

À medida que o usuário desenha interativamente no cliente, ele pinta os dados imediatamente para a tela e também o envia para o copapel para salvar. Quando o cliente requer que a tela seja redesenhada, ele chama o método [redesenhar](ipaper--redraw.md) de copapel. Essa repintura é comum em aplicativos. Por exemplo, o redesenho ocorre quando a janela do cliente é sobreposta por outra janela do aplicativo. O cliente tem uma renderização de bitmap da imagem desenhada, mas o bitmap é facilmente perdido e, muitas vezes, deve ser redesenhado. O cliente depende do copapel no servidor para os dados de tinta necessários para repintura.

Essa é uma divisão de trabalho do cliente/servidor comum. É especialmente apropriado quando há um requisito para que vários clientes compartilhem os dados. O copapel é codificado para habilitar isso. Ele usa o recurso APPUTIL CThreaded para obter segurança de thread. Um aplicativo que pode explorar esse design é um aplicativo de quadro de comunicações compartilhado, em que vários clientes podem contribuir para um desenho normalmente exibido. O suporte COM para DCOM (Distributed COM) dá suporte a esse tipo de uso de aplicativo de grupo de trabalho na rede. Para obter mais informações, consulte o exemplo anterior de REMCLIEN.

Um uso mais modesto do esquema de cliente/servidor de copapel é integrar o comportamento para objetos implementados em diferentes aplicativos no mesmo computador. Nesse caso, os clientes podem ser um contêiner do ActiveX em aplicativos separados que compartilham dados gerenciados pelo mesmo objeto. Esses dados podem não ser os dados de desenho de tinta aos quais o componente DllPaper dá suporte. **StoServe** pode ser usado como uma estrutura inicial para componentes de programação que gerenciam outros tipos de dados compartilhados.

## <a name="support-information"></a>Informações de suporte

O makefile **StoServe** registra o componente com do **StoServe** DllPaper no registro. Esse componente deve ser registrado antes que **StoServe** esteja disponível para fora de clientes com como um servidor para esse componente. Esse registro automático é feito usando o utilitário de Register.exe interno do exemplo de registro. Para compilar ou executar o **StoServe**, primeiro crie o exemplo de código de registro.

Para obter mais informações sobre como configurar seu sistema para criar e testar os exemplos de código nesta série de tutoriais COM, consulte [como criar exemplos](how-to-build-samples.md). O makefile fornecido (MAKEFILE) é compatível com Microsoft NMAKE. Para criar uma compilação de depuração, emita o comando NMAKE na janela do prompt de comando.

Para uso conveniente no Microsoft Visual Studio, um arquivo de projeto é fornecido para cada exemplo. Para carregar o projeto para o exemplo **StoServe** , você pode executar o Visual Studio no prompt de comando no diretório samples da seguinte maneira:

MSDEV STOSERVE. DSP

Você também pode clicar duas vezes no arquivo Stoserve. Dsp no Windows Explorer para carregar um projeto de exemplo no Visual Studio. No Visual Studio, você pode procurar as classes C++ da fonte de exemplo e geralmente executar as outras operações de edição-compilação-depuração.

> [!Note]  
> Como parte do SDK (Kit de desenvolvimento de software) da plataforma, a compilação desses exemplos de dentro do Visual Studio requer a configuração apropriada dos caminhos de diretório no Visual Studio. Para obter mais informações, consulte [como criar exemplos](how-to-build-samples.md).

 

 

 