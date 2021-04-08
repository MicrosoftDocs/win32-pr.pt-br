---
title: Visão geral técnica COM
ms.assetid: 519c87cc-b442-4187-af2a-124a1e4e8b49
description: 'Saiba mais sobre: visão geral técnica COM'
keywords:
- Visão geral técnica com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be5dc95ffae5166d86cd8110cab1a6b90e6ffa5c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089140"
---
# <a name="com-technical-overview"></a>Visão geral técnica COM

Este tópico fornece uma visão geral do Microsoft Component Object Model (COM):

-   [Introdução ao COM](#introduction-to-com)
-   [Objetos e interfaces](#objects-and-interfaces)
-   [Implementação de interface](#interface-implementation)
-   [A interface IUnknown](#the-iunknown-interface)
-   [O modelo de cliente/servidor](#the-clientserver-model)
-   [Gerenciador de Controle de Serviço](#service-control-manager)
-   [Reutilização](#reusability)
-   [Objetos de armazenamento e fluxo](#storage-and-stream-objects)
-   [Transferência de Dados](#data-transfer)
-   [Comunicação remota](#remoting)
-   [Segurança](#security)
-   [Tópicos relacionados](#related-topics)

## <a name="introduction-to-com"></a>Introdução ao COM

O Microsoft Component Object Model (COM) define um padrão de interoperabilidade binária para a criação de bibliotecas de software reutilizáveis que interagem em tempo de execução. Você pode usar bibliotecas COM sem a necessidade de compilá-las em seu aplicativo. O COM é a base para uma série de produtos e tecnologias da Microsoft, como o Windows Media Player e o Windows Server.

COM define um padrão binário que se aplica a muitos sistemas operacionais e plataformas de hardware. Para a computação em rede, COM define um formato de conexão padrão e um protocolo para interação entre objetos que são executados em diferentes plataformas de hardware. O COM é independente da linguagem de implementação, o que significa que você pode criar bibliotecas COM usando diferentes linguagens de programação, como C++ e aquelas na .NET Framework.

A especificação COM fornece todos os conceitos fundamentais que permitem a reutilização de software entre plataformas:

-   Um padrão binário para chamadas de função entre componentes.
-   Uma provisão para agrupamentos fortemente tipados de funções em interfaces.
-   Uma interface base que fornece polimorfismo, descoberta de recursos e acompanhamento do tempo de vida do objeto.
-   Um mecanismo que identifica exclusivamente os componentes e suas interfaces.
-   Um carregador de componente que cria instâncias de componente de uma implantação.

O COM tem várias partes que trabalham em conjunto para permitir a criação de aplicativos criados a partir de componentes reutilizáveis:

-   Um *sistema de host* que fornece um ambiente de tempo de execução que está em conformidade com a especificação com.
-   *Interfaces* que definem contratos de recursos e *componentes* que implementam interfaces.
-   *Servidores* que fornecem componentes para o sistema e *clientes* que usam os recursos fornecidos pelos componentes do.
-   Um *registro* que controla onde os componentes são implantados em hosts locais e remotos.
-   Um *Gerenciador de controle de serviço* que localiza componentes em hosts locais e remotos e conecta servidores a clientes.
-   Um protocolo de *armazenamento estruturado* que define como navegar o conteúdo dos arquivos no sistema de arquivos do host.

Habilitar o reuso de código em hosts e plataformas é fundamental para COM. Uma implementação de interface reutilizável é chamada de *componente*, um *objeto de componente* ou um *objeto com*. Um componente implementa uma ou mais interfaces COM.

Você define uma biblioteca COM personalizada criando as interfaces que sua biblioteca implementa. Os consumidores da sua biblioteca podem descobrir e usar seus recursos sem qualquer conhecimento dos detalhes de implantação e implementação da biblioteca.

## <a name="objects-and-interfaces"></a>Objetos e interfaces

Um objeto COM expõe seus recursos por meio de uma *interface*, que é uma coleção de funções de membro. Uma interface COM define o comportamento e as responsabilidades esperados de um componente e especifica um contrato fortemente tipado que fornece um pequeno conjunto de operações relacionadas. Toda a comunicação entre componentes COM ocorre por meio de interfaces, e todos os serviços oferecidos por um componente são expostos por meio de sua interface. Um chamador pode acessar apenas as funções de membro de interface. O estado interno não está disponível para um chamador, a menos que seja exposto na interface.

As interfaces são fortemente tipadas. Cada interface tem seu próprio identificador de interface exclusivo, chamado de IID, que elimina colisões que podem ocorrer com nomes legíveis. O IID é um GUID (identificador global exclusivo), que é o mesmo que o UUID (ID universalmente exclusivo) definido pelo DCE (ambiente de computação distribuída) do uso (Open Software Foundation). Ao criar uma nova interface, você deve criar um novo identificador para essa interface. Quando um chamador usa uma interface, ele deve usar o identificador exclusivo. Essa identificação explícita melhora a robustez ao eliminar conflitos de nomenclatura que resultariam em falha de tempo de execução.

Ao definir uma nova interface, você pode criar uma definição de interface usando o IDL (Interface Definition Language). A partir dessa definição de interface, o compilador Microsoft IDL gera arquivos de cabeçalho para uso por aplicativos usando a interface e o código-fonte para lidar com chamadas de procedimento remoto. A IDL fornecida pela Microsoft baseia-se em extensões simples para o DCE IDL, um padrão do setor para a computação distribuída baseada em RPC (chamada de procedimento remoto). IDL é uma ferramenta para a conveniência do designer de interface e não é central para a interoperabilidade COM. Com o IDL, você não precisa criar arquivos de cabeçalho manualmente para cada ambiente de programação. Para obter mais informações, consulte [definindo interfaces com](defining-com-interfaces.md).

A herança é usada COM moderação em interfaces COM. COM dá suporte à herança de interface somente para reutilizar um contrato associado a uma interface base. COM não oferece suporte à herança seletiva; Portanto, se uma interface herdar de outra, ela incluirá todas as funções que a interface base define. Além disso, as interfaces usam apenas uma única herança, em vez de várias heranças, para obter funções de uma interface base.

## <a name="interface-implementation"></a>Implementação de interface

Você não pode criar uma instância de uma interface COM por si só. Em vez disso, você cria uma instância de uma classe que implementa a interface. Em C++, uma interface COM é modelada como uma *classe base abstrata*, o que significa que a interface é uma classe C++ que contém apenas funções de membro virtual puras. Uma biblioteca C++ implementa objetos COM herdando as assinaturas de função de membro de uma ou mais interfaces, substituindo cada função de membro e fornecendo uma implementação para cada função.

Você pode usar qualquer linguagem de programação que dê suporte ao conceito de ponteiros de função para implementar uma interface COM. Por exemplo, em C, uma interface é uma estrutura que contém um ponteiro para uma tabela de ponteiros de função, uma para cada método na interface.

Quando você implementa uma interface, sua classe deve fornecer uma implementação para cada função na interface. Se a classe não tiver nenhum trabalho a ser feito em uma função de interface, a implementação poderá ser uma única instrução de retorno.

Uma classe COM é identificada usando um CLSID (ID de classe) de 128 bits exclusivo que associa uma classe a uma implantação específica no sistema de arquivos, que para o Windows é uma DLL ou um EXE. Um CLSID é um GUID, o que significa que nenhuma outra classe tem o mesmo CLSID. O uso de identificadores de classe exclusivos impede colisões de nome entre classes. Por exemplo, dois fornecedores diferentes podem escrever uma classe chamada CStack, mas ambas as classes têm um CLSID exclusivo, portanto, qualquer possibilidade de uma colisão é evitada.

Você Obtém um novo CLSID usando a função [**falha em CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) ou usando uma ferramenta de criação com, como o Visual Studio, que chama essa função internamente.

## <a name="the-iunknown-interface"></a>A interface IUnknown

Todas as interfaces COM herdam da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) . A interface **IUnknown** contém as operações com fundamentais para o gerenciamento de tempo de vida de polimorfismo e instância. A interface **IUnknown** tem três funções de membro, chamadas [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)), [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Todos os objetos COM são necessários para implementar a interface **IUnknown** .

A função de membro [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) fornece POLIMORFISMO para com. Chame **QueryInterface** para determinar em tempo de execução se um objeto com dá suporte a uma interface específica. O objeto COM retorna um ponteiro de interface no `ppvObject` parâmetro se ele implementa a interface solicitada; caso contrário, ele retorna `NULL` . A função de membro **QueryInterface** permite a navegação entre todas as interfaces às quais um objeto com dá suporte.

O tempo de vida de uma instância de objeto COM é controlado por sua *contagem de referência*. As funções de membro [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) controlam a contagem. O **AddRef** incrementa a contagem e a **versão** decrementa a contagem. Quando a contagem de referência chega a zero, a função de membro de **liberação** pode liberar a instância, pois nenhum chamador a está usando.

## <a name="the-clientserver-model"></a>O modelo de cliente/servidor

Uma classe COM implementa um número de interfaces COM. A implementação consiste em binários que são executados quando um chamador interage com uma instância da classe COM. O COM permite o uso de uma classe em aplicativos diferentes, incluindo aplicativos escritos sem conhecimento de uma classe específica. Em uma plataforma Windows, as classes existem em uma DLL (biblioteca vinculada dinâmica) ou em outro aplicativo (EXE).

Em seu sistema host, o COM mantém um banco de dados de registro de todos os CLSIDs para os objetos COM instalados no sistema. O banco de dados de registro é um mapeamento entre cada CLSID e o local da DLL ou EXE que hospeda a classe correspondente. COM consulta esse banco de dados sempre que um chamador quiser criar uma instância de uma classe COM. O chamador precisa saber apenas o CLSID para solicitar uma nova instância da classe.

A interação entre um objeto COM e seus chamadores é modelada como uma relação de cliente/servidor. O cliente é o chamador que solicita um objeto COM do sistema e o servidor é o módulo que hospeda objetos COM que fornece serviços aos clientes.

Um cliente COM é qualquer chamador que passe um CLSID para o sistema para solicitar uma instância de um objeto COM. A maneira mais simples de criar uma instância é chamar a função COM, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

A função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) cria uma instância do CLSID especificado e retorna um ponteiro de interface do tipo solicitado pelo cliente. O cliente é responsável por gerenciar o tempo de vida da instância chamando sua função de [**liberação**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) quando o cliente termina de usá-la. Para criar vários objetos com base em um único CLSID, chame a função [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) . Para se conectar a um objeto que já está criado e em execução, chame a função [**GetActiveObject**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-getactiveobject) .

Um servidor COM fornece uma implementação COM para o sistema. Um servidor associa um CLSID a uma classe COM, hospeda a implementação da classe, implementa uma fábrica de classes para criar instâncias da classe e fornece o descarregamento do servidor.

> [!Note]  
> Um servidor COM não é o mesmo que o objeto COM que ele fornece ao sistema.

 

Para habilitar a criação de um objeto COM, um servidor COM deve fornecer uma implementação da interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) . Os clientes podem chamar o método [**CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) para solicitar uma nova instância de um objeto com, mas geralmente essas solicitações são encapsuladas na função [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) .

Você pode implantar um servidor COM como uma biblioteca compartilhada que é carregada no processo do cliente em tempo de execução (DLL em plataformas Windows) ou como um módulo executável (EXE em plataformas Windows). Para obter mais informações, consulte [registrando aplicativos com](registering-com-applications.md).

## <a name="service-control-manager"></a>Gerenciador de Controle de Serviço

O SCM (Gerenciador de controle de serviço) manipula a solicitação do cliente para uma instância de um objeto COM. A lista a seguir mostra a sequência de eventos:

-   Um cliente solicita um ponteiro de interface para um objeto COM da biblioteca COM chamando uma função como [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) com o CLSID do objeto com.
-   A biblioteca COM consulta o SCM para localizar o servidor que corresponde ao CLSID solicitado.
-   O SCM localiza o servidor e solicita a criação do objeto COM da fábrica de classes fornecida pelo servidor.
-   Se for bem-sucedida, a biblioteca COM retornará um ponteiro de interface para o cliente.

Depois que o sistema COM conecta um objeto de servidor a um cliente, o cliente e o objeto se comunicam diretamente. Não há nenhuma sobrecarga adicional de chamar por meio de um tempo de execução intermediário.

Ao registrar um servidor com com o sistema host, você pode especificar diferentes maneiras para o servidor ser ativado. A lista a seguir mostra as três maneiras que o SCM pode ativar um servidor COM:

-   Em processo: o SCM retorna o caminho do arquivo da DLL que contém a implementação do servidor de objetos. A biblioteca COM carrega a DLL e a consulta para seu ponteiro de interface de fábrica de classes.
-   Local: o SCM inicia o executável local que registra uma fábrica de classes na inicialização e seu ponteiro de interface está disponível para o sistema e os clientes.
-   Remoto: o SCM local adquire um ponteiro de interface de fábrica de classe do SCM que está sendo executado em um computador remoto.

Quando um cliente solicita um objeto COM, a biblioteca COM entra em contato com o SCM no host local. O SCM localiza o servidor COM apropriado, que pode ser local ou remoto, e o servidor retorna um ponteiro de interface para a fábrica de classes do servidor. Quando a fábrica de classes estiver disponível, a biblioteca COM ou o cliente poderá usar a fábrica de classes para criar o objeto solicitado. Para obter mais informações, consulte [implementando IClassFactory](implementing-iclassfactory.md).

## <a name="reusability"></a>Capacidade de reutilização

O COM dá suporte à *reutilização de caixa preta*, o que significa que os detalhes de implementação de um componente reutilizável não são expostos aos clientes. Para obter a reutilização de caixa preta, o COM dá suporte a dois mecanismos por meio dos quais um objeto pode reutilizar outro. As duas formas de reutilização são chamadas de *contenção* e *agregação*. Por convenção, o objeto que está sendo reutilizado é chamado de *objeto interno* e o objeto que está fazendo uso do objeto interno é denominado *objeto externo*.

Em confinamento, o objeto externo se comporta como um cliente do objeto interno. O objeto externo é um contêiner lógico para o objeto interno e, quando o objeto externo usa os serviços do objeto interno, o objeto externo delega a implementação para as interfaces do objeto interno. Isso significa que o objeto externo é implementado em termos dos serviços do objeto interno. O objeto externo pode não dar suporte às mesmas interfaces que o objeto interno, e o objeto externo pode usar uma interface de objeto interno para ajudar na implementação de partes de uma interface diferente no objeto externo.

Na agregação, o objeto externo expõe interfaces do objeto interno como se elas estivessem implementadas no objeto externo. Isso é útil quando o objeto externo sempre Delega cada chamada em uma de suas interfaces para a mesma interface do objeto interno. A agregação é uma conveniência que permite que o objeto externo Evite sobrecarga de implementação extra.

Para obter mais informações, consulte [reutilizando objetos](reusing-objects.md).

## <a name="storage-and-stream-objects"></a>Objetos de armazenamento e fluxo

Objetos COM salvam o estado em um arquivo usando o *armazenamento estruturado*, que é uma forma de armazenamento persistente que permite a navegação do conteúdo de um arquivo usando a semântica do sistema de arquivos. Tratar o conteúdo de um arquivo dessa maneira habilita recursos como acesso incremental, transações e compartilhamento entre processos.

A especificação de armazenamento persistente de COM fornece dois tipos de elementos de armazenamento: objetos de armazenamento e objetos de fluxo. Esses objetos são implementados pela biblioteca COM e os aplicativos de usuário raramente implementam esses elementos de armazenamento. Os objetos de armazenamento implementam a interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) e os objetos de fluxo implementam a interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) .

Um objeto de fluxo contém dados e é conceitualmente semelhante a um único arquivo em um sistema de arquivos. Cada fluxo tem direitos de acesso e um único ponteiro de busca. Por meio da interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , você pode ler, gravar, buscar e executar outras operações nos dados subjacentes do fluxo. Um fluxo é nomeado usando uma cadeia de texto. Ele pode conter qualquer estrutura interna, pois é um fluxo simples de bytes. Além disso, as funções na interface **IStream** são semelhantes às funções baseadas em identificador de arquivo padrão, como aquelas na biblioteca de tempo de execução ANSI C.

Um objeto de armazenamento é conceitualmente semelhante a um diretório em um sistema de arquivos. Cada armazenamento pode conter qualquer número de objetos de subarmazenamento e qualquer quantidade de fluxos. Cada armazenamento tem seus próprios direitos de acesso. Por meio da interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) , você pode executar operações como enumerar, mover, copiar, renomear, criar e excluir elementos. Um objeto de armazenamento não armazena dados definidos pelo aplicativo, mas armazena implicitamente os nomes dos elementos (armazenamentos e fluxos) que ele contém.

Os objetos de armazenamento e de fluxo podem ser compartilhados entre processos quando são implementados de acordo com a especificação COM em uma plataforma de host. Isso permite que os objetos que estão executando em processo ou fora do processo tenham acesso incremental igual ao seu armazenamento de arquivos. Como o COM é carregado em cada processo separadamente, ele usa mecanismos de memória compartilhada com suporte do sistema operacional para comunicar o estado dos elementos abertos e seus modos de acesso entre os processos.

Cada objeto de armazenamento e fluxo em um arquivo estruturado tem um nome para identificá-lo. O nome é uma cadeia de caracteres que segue uma convenção específica. Para obter mais informações, consulte [convenções de nomenclatura de objeto de armazenamento](/windows/desktop/Stg/storage-object-naming-conventions). O nome é passado para funções [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) para especificar em qual elemento no armazenamento operar. Os nomes dos objetos de armazenamento raiz são os mesmos que os nomes de arquivo no sistema de arquivos subjacente, e esses nomes devem seguir as convenções e restrições do sistema de arquivos. Cadeias de caracteres passadas para funções relacionadas ao armazenamento que os arquivos de nome passam para o sistema de arquivos sem interpretação ou alterações.

Os nomes dos elementos contidos nos objetos de armazenamento são gerenciados pela implementação do objeto de armazenamento específico em questão. Todas as implementações de objetos de armazenamento devem dar suporte a nomes de elementos com 32 caracteres de comprimento e algumas implementações podem dar suporte a nomes mais longos. Os nomes são armazenados com o caso preservado, mas são comparados como não diferenciam maiúsculas de minúsculas. Os aplicativos que definem nomes de elementos de armazenamento devem escolher nomes que funcionem em qualquer situação.

Você acessa todos os elementos em um arquivo de armazenamento estruturado usando funções e interfaces implementadas pelo COM. Isso significa que outros aplicativos podem procurar o arquivo navegando com as funções da interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) que fornecem serviços do tipo diretório. Além disso, outros aplicativos podem usar os dados do arquivo, sem precisar executar o aplicativo que escreveu o arquivo. Quando um aplicativo COM acessa os arquivos de armazenamento estruturados de outro aplicativo, direitos de acesso padrão do Windows se aplicam e o aplicativo deve ter privilégios suficientes.

Um objeto COM pode ler e gravar em um armazenamento persistente. Um cliente consulta uma das interfaces relacionadas à persistência no objeto COM, dependendo do contexto da operação. Objetos COM podem implementar qualquer combinação das seguintes interfaces:

-   [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage): o objeto com lê e grava seu estado persistente em um objeto de armazenamento. O cliente fornece o objeto com um ponteiro [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) por meio desta interface. Essa é a única interface de persistência que inclui a semântica para acesso incremental.
-   [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream): o objeto com lê e grava seu estado persistente em um objeto de fluxo. O cliente fornece o objeto com um ponteiro de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) por meio desta interface.
-   [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile): o objeto com lê e grava seu estado persistente diretamente em um arquivo no sistema subjacente. Essa interface não envolve [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , a menos que o arquivo subjacente seja acessado por meio dessas interfaces, mas a interface **IPersistFile** não tem nenhuma semântica para armazenamentos e fluxos. O cliente fornece o objeto com um nome de arquivo e chama as funções [**salvar**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-save) ou [**carregar**](/windows/desktop/api/ObjIdl/nf-objidl-ipersistfile-load) .

## <a name="data-transfer"></a>Transferência de dados

O armazenamento estruturado fornece a base para troca de dados entre objetos COM e processos, que é chamada de *transferência de dados uniforme*. Antes de o COM ter sido implementado no OLE 2, a transferência de dados no Windows foi especificada por *protocolos de transferência*, como os protocolos de arrastar e soltar da área de transferência. Cada protocolo de transferência tinha seu próprio conjunto de funções que vincularam o protocolo à consulta, e o código específico era necessário para lidar com cada protocolo diferente e o procedimento do Exchange. A transferência de dados uniforme representa todas as transferências de dados usando a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) , que separa as operações de troca de dados comuns do protocolo de transferência.

A interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) encapsula as operações padrão Get e set em dados, consultas e enumerações e notificações que detectam quando os dados são alterados em um objeto. A transferência de dados uniforme permite descrições avançadas de formatos de dados, bem como o uso de diferentes mídias de armazenamento para a transferência de dados.

Durante a transferência de dados uniforme, todos os protocolos trocam um ponteiro para uma interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . O servidor é a origem dos dados e implementa um objeto de dados, que pode ser usado em qualquer protocolo de troca de dados. O cliente consome os dados e solicita dados de um objeto de dados quando recebe um ponteiro **IDataObject** de qualquer protocolo. Depois que a troca do ponteiro ocorre, ambos os lados lidam com a troca de dados de maneira uniforme, por meio da interface **IDataObject** .

COM define duas estruturas de dados que habilitam a transferência uniforme de dados. A estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) representa um formato de área de transferência generalizado e a estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) representa o meio de transferência como um identificador de memória.

O cliente cria uma estrutura [**FORMATETC**](/windows/win32/api/objidl/ns-objidl-formatetc) para indicar o tipo de dados que ele solicita de uma fonte de dados e é usado pela fonte de dados para descrever quais formatos ele fornece. O cliente consulta uma fonte de dados em busca de seus formatos disponíveis solicitando sua interface [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) . Para obter mais informações, consulte [a estrutura FORMATETC](the-formatetc-structure.md).

O cliente cria uma estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) e a passa para o método [**GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) , e o objeto de dados retorna os dados na estrutura **STGMEDIUM** fornecida.

A estrutura [**STGMEDIUM**](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) permite que clientes e fontes de dados escolham o meio de troca mais eficiente. Por exemplo, se os dados a serem trocados forem muito grandes, a fonte de dados poderá indicar uma mídia baseada em disco como seu formato preferencial, em vez da memória principal. Essa flexibilidade permite trocas de dados eficientes que podem ser tão rápidas quanto passar um ponteiro para um [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) ou um [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Para obter mais informações, consulte [a estrutura STGMEDIUM](the-stgmedium-structure.md).

Um cliente de uma fonte de dados pode exigir notificação quando os dados são alterados. O COM manipula notificações de alteração de dados usando um objeto de *coletor de aviso* , que implementa a interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) . O objeto de coletor de aviso e a interface **IAdviseSink** são implementados pelo cliente, que passa um ponteiro **IAdviseSink** para a fonte de dados. Quando a fonte de dados detecta uma alteração nos dados subjacentes, ela chama um método **IAdviseSink** para notificar o cliente. Para obter mais informações, consulte [Data Notification](data-notification.md).

## <a name="remoting"></a>Comunicação remota

O COM permite a computação remota e distribuída. A *interface de comunicação remota* permite que uma função de membro retorne um ponteiro de interface para um objeto com que está em um processo diferente ou em um computador host diferente. A infraestrutura que executa a interface de comunicação remota é transparente para o cliente e o servidor de objetos. Nem o cliente nem o servidor precisam de um outro detalhes de implantação para se comunicar por meio de uma interface remota. Um cliente chama funções de membro na mesma interface para se comunicar com um objeto COM que está em processo, fora de processo no host local ou em um computador remoto. As chamadas locais e remotas na mesma interface são indistinguíveis para o cliente.

Para se comunicar com um objeto COM, um cliente sempre chama uma implementação em processo. Se o objeto COM estiver em processo, a chamada será direta. Se o objeto COM estiver fora do processo ou remoto, COM fornecerá uma implementação de *proxy* que encaminha a chamada para o objeto usando o Protocolo RPC (chamada de procedimento remoto).

Um objeto COM sempre recebe chamadas de um cliente por meio de uma implementação em processo. Se o chamador estiver em processo, a chamada será direta. Se o chamador estiver fora do processo ou remoto, o COM fornecerá uma implementação de *stub* que recebe a chamada de procedimento remoto do proxy no processo do cliente.

O *marshaling* é o procedimento para empacotar a pilha de chamadas para transmissão de proxy para stub. O *desempacotamento* é o desempacotamento que ocorre na extremidade de recebimento. Os valores de retorno são empacotados e desempacotados do stub para o proxy. Esse tipo de comunicação também é conhecido como enviar uma chamada *pela conexão*.

Cada tipo de dados diferente tem regras para marshaling. Os ponteiros de interface também têm um protocolo de marshaling, que é encapsulado na função [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface) . Na maioria dos casos, o *empacotamento de interface padrão*, que é fornecido pelo sistema, é suficiente, mas um objeto com, opcionalmente, pode implementar o *empacotamento de interface personalizada* para controlar a criação de proxies de objeto remoto para si mesmo. Para obter mais informações, consulte [comunicação entre objetos](inter-object-communication.md).

## <a name="security"></a>Segurança

O COM fornece duas formas de segurança de aplicativo. Uma é a *segurança de ativação*, que especifica como novos objetos são criados, como os clientes se conectam a objetos novos e existentes e como determinados serviços públicos, como a tabela de classes e a tabela de objetos em execução, são protegidos. A outra é *chamar segurança*, que especifica como a segurança opera em uma conexão estabelecida entre um cliente para um objeto com.

A segurança de ativação é aplicada automaticamente pelo SCM (Gerenciador de controle de serviço). Quando o SCM recebe uma solicitação para recuperar um objeto COM, ele verifica a solicitação em relação às informações de segurança armazenadas no registro.

As implementações do SCM geralmente oferecem configuração controlada pelo registro para administrar classes implantadas e para contas de usuário específicas no host. Para obter mais informações, consulte [Activation Security](activation-security.md).

A segurança da chamada é aplicada automaticamente ou imposta pelo aplicativo. Se o aplicativo fornecer informações de instalação, o COM executará as verificações necessárias para proteger o aplicativo.

O mecanismo automático verifica a segurança para o processo, mas não para objetos ou métodos individuais. Se um aplicativo exigir segurança mais refinada, o COM fornecerá funções que os aplicativos podem usar para fazer sua própria verificação de segurança.

Os mecanismos automáticos e personalizados podem ser usados juntos, de modo que um aplicativo pode pedir ao COM para executar a verificação de segurança automática e, em seguida, executar seu próprio.

Os serviços de segurança de chamada COM são divididos nas seguintes categorias:

-   Funções gerais que são chamadas por clientes e servidores, que permitem que o mecanismo de segurança automática seja inicializado e os serviços de autenticação automática sejam registrados. As APIs de segurança de chamada geral são as funções [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) .
-   Interfaces em proxies de cliente, que permitem que o cliente controle a segurança em chamadas para interfaces individuais. A interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) e as funções [**CoQueryProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryproxyblanket), [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket)e [**CoCopyProxy**](/windows/desktop/api/combaseapi/nf-combaseapi-cocopyproxy) fornecem segurança de chamada em um objeto remoto.
-   Funções do lado do servidor e interfaces de contexto de chamada, que permitem que o servidor recupere informações de segurança sobre uma chamada e represente o chamador. A interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) e as funções [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext), [**CoImpersonateClient**](/windows/desktop/api/combaseapi/nf-combaseapi-coimpersonateclient)e [**CoRevertToSelf**](/windows/desktop/api/combaseapi/nf-combaseapi-coreverttoself) fornecem segurança de chamada no lado do servidor.

Geralmente, o cliente consulta o objeto COM para a interface [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) , que é implementada localmente pela camada de comunicação remota. O cliente usa essa interface para controlar a segurança de proxies de interface individuais no objeto COM antes de fazer uma chamada em uma das interfaces.

Quando uma chamada chega ao servidor, o servidor pode chamar a função [**CoGetCallContext**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetcallcontext) para recuperar uma interface [**IServerSecurity**](/windows/win32/api/objidlbase/nn-objidlbase-iserversecurity) , que permite que o servidor Verifique a autenticação do cliente e represente o cliente, se necessário. O objeto **IServerSecurity** é válido para a duração da chamada.

Chame a função [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) para inicializar a camada de segurança e defina os valores especificados como o padrão de segurança. Se um processo não chamar **CoInitializeSecurity**, o com o chamará automaticamente na primeira vez que uma interface for empacotada ou desempacotada, registrando a segurança padrão do sistema. A função **CoInitializeSecurity** permite que o cliente estabeleça a segurança de chamada padrão para o processo, o que evita o uso de [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) em proxies individuais. A função **CoInitializeSecurity** permite que um servidor Registre serviços de autenticação automática para o processo. Para obter mais informações, consulte [definindo Process-Wide segurança com CoInitializeSecurity](setting-processwide-security-with-coinitializesecurity.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes e servidores COM](com-clients-and-servers.md)
</dt> <dt>

[Definição de interfaces COM](defining-com-interfaces.md)
</dt> <dt>

[Registrando aplicativos COM](registering-com-applications.md)
</dt> <dt>

[Segurança em COM](security-in-com.md)
</dt> <dt>

[Processos, threads e Apartments](processes--threads--and-apartments.md)
</dt> </dl>

 

 
