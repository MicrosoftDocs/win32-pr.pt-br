---
title: Glossário do COM
description: Página de Glossário
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9e2c56a2-0572-48b6-a2ef-650f1cf1b62e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61c12f3c021988f0349d9eaf6a2bdbd9505ca8a6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105772974"
---
# <a name="com-glossary"></a>Glossário do COM

<dl> <dt>

<span id="com.activation_gloss"></span><span id="COM.ACTIVATION_GLOSS"></span>**ativá**
</dt> <dd>

O processo de carregar um objeto na memória, que o coloca no estado de execução.

</dd> <dt>

<span id="com.active_state_gloss"></span><span id="COM.ACTIVE_STATE_GLOSS"></span>**estado ativo**
</dt> <dd>

Um objeto COM que está no estado de execução e tem uma interface do usuário visível.

</dd> <dt>

<span id="com.absolute_moniker_gloss"></span><span id="COM.ABSOLUTE_MONIKER_GLOSS"></span>**moniker absoluto**
</dt> <dd>

Um moniker que especifica o local absoluto de um objeto. Um moniker absoluto é análogo a um caminho completo.

</dd> <dt>

<span id="com.advisory_holder_gloss"></span><span id="COM.ADVISORY_HOLDER_GLOSS"></span>**titular do comunicado**
</dt> <dd>

Um objeto COM que armazena em cache, gerencia e envia notificações de alterações nos coletores de consultoria de aplicativos de contêiner.

</dd> <dt>

<span id="com.advisory_sink_gloss"></span><span id="COM.ADVISORY_SINK_GLOSS"></span>**coletor de consultoria**
</dt> <dd>

Um objeto COM que pode receber notificações de alterações em um objeto incorporado ou vinculado, pois ele implementa a interface [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) ou [**IAdviseSink2**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink2) . Contêineres que precisam ser notificados sobre alterações em objetos implementam um coletor de consultoria. As notificações são originadas no servidor, que usa um objeto de suporte de consultoria para armazenar em cache e gerenciar notificações para contêineres.

</dd> <dt>

<span id="com.aggregate_object_gloss"></span><span id="COM.AGGREGATE_OBJECT_GLOSS"></span>**objeto de agregação**
</dt> <dd>

Um objeto COM que é composto de um ou mais objetos COM. Um objeto na agregação é designado como o objeto de controle, que controla quais interfaces na agregação são expostas e que são particulares. Esse objeto de controle tem uma implementação especial de [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) chamada de controle **IUnknown**. Todos os objetos na agregação devem passar chamadas para métodos **IUnknown** por meio do **IUnknown** de controle.

</dd> <dt>

<span id="com.aggregation_gloss"></span><span id="COM.AGGREGATION_GLOSS"></span>**Aggregation**
</dt> <dd>

Uma técnica de composição para implementar objetos COM. Ele permite que você crie um novo objeto reutilizando uma ou mais implementações de interface de objetos existentes. O objeto Aggregate escolhe quais interfaces devem ser expostas aos clientes e as interfaces são expostas como se fossem implementadas pelo objeto Aggregate. Os clientes do objeto de agregação se comunicam somente com o objeto de agregação.

</dd> <dt>

<span id="com.ambient_property_gloss"></span><span id="COM.AMBIENT_PROPERTY_GLOSS"></span>**Propriedade de ambiente**
</dt> <dd>

Uma propriedade de tempo de execução que é gerenciada e exposta pelo contêiner. Normalmente, uma propriedade de ambiente representa uma característica de um formulário, como a cor do plano de fundo, que precisa ser comunicada a um controle para que o controle possa assumir a aparência de seu ambiente adjacente.

</dd> <dt>

<span id="com.anti_moniker_gloss"></span><span id="COM.ANTI_MONIKER_GLOSS"></span>**anti-moniker**
</dt> <dd>

O inverso de um arquivo, item ou moniker de ponteiro. Um anti-moniker é adicionado ao final de um arquivo, item ou moniker de ponteiro para anular. Os antimonikers são usados na construção de monikers relativos.

</dd> <dt>

<span id="com.artificial_reference_counting_gloss"></span><span id="COM.ARTIFICIAL_REFERENCE_COUNTING_GLOSS"></span>**contagem de referência artificial**
</dt> <dd>

Uma técnica usada para ajudar a proteger um objeto antes de chamar uma função ou um método que poderia destruí-lo prematuramente. Um programa chama **IUnknown:: AddRef** para incrementar a contagem de referência do objeto antes de fazer a chamada que poderia liberar o objeto. Depois que a função retorna, o programa chama **IUnknown:: Release** para diminuir a contagem.

</dd> <dt>

<span id="com.asynchronous_binding_gloss"></span><span id="COM.ASYNCHRONOUS_BINDING_GLOSS"></span>**Associação assíncrona**
</dt> <dd>

Um tipo de associação em que é necessário que o processo ocorra de forma assíncrona para evitar a degradação do desempenho do usuário final. Normalmente, a vinculação assíncrona é usada em ambientes distribuídos, como o World Wide Web. O OLE dá suporte a classes de moniker assíncronas e mecanismos de retorno de chamada que permitem que o processo de localização e inicialização de um objeto em um ambiente distribuído ocorra enquanto outras operações são executadas.

</dd> <dt>

<span id="com.asynchronous_call_gloss"></span><span id="COM.ASYNCHRONOUS_CALL_GLOSS"></span>**chamada assíncrona**
</dt> <dd>

Uma chamada para uma função que é executada separadamente para que o chamador possa continuar processando as instruções sem esperar que a função retorne.

</dd> <dt>

<span id="com.asynchronous_moniker_gloss"></span><span id="COM.ASYNCHRONOUS_MONIKER_GLOSS"></span>**moniker assíncrono**
</dt> <dd>

Um moniker que dá suporte à associação assíncrona. Por exemplo, as instâncias da classe de moniker da URL fornecida pelo sistema são monikers assíncronos.

</dd> <dt>

<span id="com.automation_gloss"></span><span id="COM.AUTOMATION_GLOSS"></span>**inicia**
</dt> <dd>

Uma maneira de manipular objetos de um aplicativo de fora do aplicativo. Normalmente, a automação é usada para criar aplicativos que expõem objetos a ferramentas de programação e linguagens de macro, criar e manipular objetos de um aplicativo a partir de outros aplicativos ou criar ferramentas para acessar e manipular objetos.

</dd> <dt>

<span id="com.bind_context_gloss"></span><span id="COM.BIND_CONTEXT_GLOSS"></span>**contexto de associação**
</dt> <dd>

Um objeto COM que implementa a interface [**IBindCtx**](/windows/desktop/api/ObjIdl/nn-objidl-ibindctx) . Os contextos de ligação são usados em operações de moniker para manter referências aos objetos ativados quando um moniker é associado. O contexto de associação contém parâmetros que se aplicam a todas as operações durante a associação de um moniker composto genérico e fornece a implementação do moniker com acesso a informações sobre seu ambiente.

</dd> <dt>

<span id="com.binding_gloss"></span><span id="COM.BINDING_GLOSS"></span>**vinculação**
</dt> <dd>

Associando um nome a seu Referent. Especificamente, localizando o objeto nomeado por um moniker, colocando-o em seu estado de execução, se ainda não estiver, e retornando um ponteiro de interface para ele. Os objetos podem ser associados em tempo de execução (também chamado de associação tardia ou vinculação dinâmica) ou em tempo de compilação (também chamado de associação estática).

</dd> <dt>

<span id="com.cache_gloss"></span><span id="COM.CACHE_GLOSS"></span>**armazenar**
</dt> <dd>

Um (geralmente temporário) armazenamento local de informações. No OLE, um cache contém informações que definem a apresentação de um objeto vinculado ou inserido quando o contêiner é aberto.

</dd> <dt>

<span id="com.cache_initialization_gloss"></span><span id="COM.CACHE_INITIALIZATION_GLOSS"></span>**inicialização do cache**
</dt> <dd>

Preenchendo o cache de um objeto vinculado ou inserido com dados de apresentação. A interface [**IOleCache**](/windows/desktop/api/OleIdl/nn-oleidl-iolecache) fornece métodos que um contêiner pode chamar para controlar os dados que são armazenados em cache para objetos vinculados ou incorporados.

</dd> <dt>

<span id="com.class_gloss"></span><span id="COM.CLASS_GLOSS"></span>**classes**
</dt> <dd>

A definição de um objeto no código. Em C++, a classe de um objeto é definida como um tipo de dados, mas esse não é o caso em outras linguagens. Como o OLE pode ser codificado em qualquer linguagem, a classe é usada para fazer referência à definição geral do objeto.

</dd> <dt>

<span id="com.class_factory_gloss"></span><span id="COM.CLASS_FACTORY_GLOSS"></span>**fábrica de classes**
</dt> <dd>

Um objeto COM que implementa a interface [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e que cria uma ou mais instâncias de um objeto identificado por um determinado identificador de classe (CLSID).

</dd> <dt>

<span id="com.class_identifier_gloss"></span><span id="COM.CLASS_IDENTIFIER_GLOSS"></span>**identificador de classe (CLSID)**
</dt> <dd>

Um GUID (identificador global exclusivo) associado a um objeto de classe OLE. Se um objeto de classe for usado para criar mais de uma instância de um objeto, o aplicativo de servidor associado deverá registrar seu CLSID no registro do sistema para que os clientes possam localizar e carregar o código executável associado aos objetos. Todo servidor OLE ou contêiner que permite vincular a seus objetos inseridos deve registrar um CLSID para cada definição de objeto com suporte.

</dd> <dt>

<span id="com.class_object_gloss"></span><span id="COM.CLASS_OBJECT_GLOSS"></span>**objeto de classe**
</dt> <dd>

Na programação orientada a objeto, um objeto cujo estado é compartilhado por todos os objetos em uma classe e cujo comportamento atua nos dados de estado classwide. No COM, os objetos de classe são chamados de fábricas de classes e normalmente não têm nenhum comportamento, exceto para criar novas instâncias da classe.

</dd> <dt>

<span id="com.client_gloss"></span><span id="COM.CLIENT_GLOSS"></span>**cliente**
</dt> <dd>

Um objeto COM que solicita serviços de outro objeto.

</dd> <dt>

<span id="com.client_site_gloss"></span><span id="COM.CLIENT_SITE_GLOSS"></span>**site do cliente**
</dt> <dd>

O site de exibição de um objeto incorporado ou vinculado em um documento composto. O site do cliente é o principal meio pelo qual um objeto solicita serviços de seu contêiner.

</dd> <dt>

<span id="com.clsid_gloss"></span><span id="COM.CLSID_GLOSS"></span>**CLSID**
</dt> <dd>

Um GUID (identificador global exclusivo) associado a um objeto de classe OLE. Se um objeto de classe for usado para criar mais de uma instância de um objeto, o aplicativo de servidor associado deverá registrar seu CLSID no registro do sistema para que os clientes possam localizar e carregar o código executável associado aos objetos. Todo servidor OLE ou contêiner que permite vincular a seus objetos inseridos deve registrar um CLSID para cada definição de objeto com suporte.

</dd> <dt>

<span id="com.commit_gloss"></span><span id="COM.COMMIT_GLOSS"></span>**compromisso**
</dt> <dd>

Para salvar de forma persistente todas as alterações feitas em um objeto de armazenamento ou de fluxo desde que ele foi aberto ou alterações foram salvas pela última vez.

</dd> <dt>

<span id="com.component_gloss"></span><span id="COM.COMPONENT_GLOSS"></span>**componente**
</dt> <dd>

Um objeto que encapsula dados e código e fornece um conjunto bem especificado de serviços publicamente disponíveis.

</dd> <dt>

<span id="com.component_object_model_gloss"></span><span id="COM.COMPONENT_OBJECT_MODEL_GLOSS"></span>**Component Object Model (COM)**
</dt> <dd>

O modelo de programação orientado a objeto OLE que define como os objetos interagem em um único processo ou entre processos. Em COM, os clientes têm acesso a um objeto por meio de interfaces implementadas no objeto.

</dd> <dt>

<span id="com.composite_menu_bar_gloss"></span><span id="COM.COMPOSITE_MENU_BAR_GLOSS"></span>**barra de menus compostas**
</dt> <dd>

Uma barra de menus compartilhada composta por grupos de menus de um aplicativo de contêiner e de um aplicativo de servidor ativado no local.

</dd> <dt>

<span id="com.composite_moniker_gloss"></span><span id="COM.COMPOSITE_MONIKER_GLOSS"></span>**moniker composto**
</dt> <dd>

Um moniker que consiste em dois ou mais monikers que são tratados como uma unidade. Um moniker composto pode ser não genérico, o que significa que seus monikers do componente têm conhecimento especial um do outro, ou genéricos, o que significa que seus monikers do componente não sabem nada sobre um do outro, exceto que eles são monikers

</dd> <dt>

<span id="com.compound_document_gloss"></span><span id="COM.COMPOUND_DOCUMENT_GLOSS"></span>**documento composto**
</dt> <dd>

Um documento que inclui objetos vinculados ou incorporados, bem como seus próprios dados nativos.

</dd> <dt>

<span id="com.compound_file_gloss"></span><span id="COM.COMPOUND_FILE_GLOSS"></span>**arquivo composto**
</dt> <dd>

Uma implementação de armazenamento estruturado fornecida por OLE.

</dd> <dt>

<span id="com.com_object_gloss"></span><span id="COM.COM_OBJECT_GLOSS"></span>**Objeto COM**
</dt> <dd>

Um objeto que está de acordo com o Component Object Model OLE (COM). Um objeto COM é uma instância de uma definição de objeto, que especifica os dados do objeto e uma ou mais implementações de interfaces no objeto. Os clientes interagem com um objeto COM somente por meio de suas interfaces.

</dd> <dt>

<span id="com.connectable_object_gloss"></span><span id="COM.CONNECTABLE_OBJECT_GLOSS"></span>**objeto conectável**
</dt> <dd>

Um objeto COM que implementa, no mínimo, a interface [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) , para o gerenciamento de objetos de ponto de conexão. Os objetos conectáveis dão suporte à comunicação do servidor para o cliente. Um objeto que pôde ser conectado cria e gerencia um ou mais subobjetos de ponto de conexão, que recebem eventos de interfaces implementadas em outros objetos e os enviam para o cliente.

</dd> <dt>

<span id="com.connection_point_object_gloss"></span><span id="COM.CONNECTION_POINT_OBJECT_GLOSS"></span>**objeto de ponto de conexão**
</dt> <dd>

Um objeto COM que é gerenciado por um objeto que pôde ser conectado e que implementa a interface [**IConnectionPoint**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpoint) . Um ou mais objetos de ponto de conexão podem ser criados e gerenciados por um objeto que pode ser conectado. Cada objeto de ponto de conexão gerencia eventos de entrada de uma interface específica em outro objeto e envia esses eventos para o cliente.

</dd> <dt>

<span id="com.container_application_gloss"></span><span id="COM.CONTAINER_APPLICATION_GLOSS"></span>**aplicativo de contêiner**
</dt> <dd>

Um aplicativo que dá suporte a documentos compostos. O aplicativo de contêiner fornece armazenamento para um objeto incorporado ou vinculado, um site para sua exibição, acesso ao site de exibição e um coletor de consultoria para receber notificações de alterações no objeto.

</dd> <dt>

<span id="com.containment_gloss"></span><span id="COM.CONTAINMENT_GLOSS"></span>**contenção**
</dt> <dd>

Uma técnica de composição para implementar objetos COM. Ele permite que um objeto reutilize algumas ou todas as implementações de interface de um ou mais objetos. O objeto externo atua como um cliente para os outros objetos, delegando a implementação quando quiser usar os serviços de um dos objetos contidos.

</dd> <dt>

<span id="com.context_gloss"></span><span id="COM.CONTEXT_GLOSS"></span>**noticioso**
</dt> <dd>

No COM+, um conjunto de propriedades de tempo de execução associadas a um ou mais objetos COM que são usados para fornecer serviços para esses objetos.

</dd> <dt>

<span id="com.control_gloss"></span><span id="COM.CONTROL_GLOSS"></span>**controlo**
</dt> <dd>

Um objeto COM que pode ser inserido e reutilizável que dá suporte ao, no mínimo, à interface [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol) . Normalmente, os controles são associados à interface do usuário. Eles também dão suporte à comunicação com um contêiner e podem ser reutilizados por vários clientes, dependendo dos critérios de licenciamento.

</dd> <dt>

<span id="com.control_container_gloss"></span><span id="COM.CONTROL_CONTAINER_GLOSS"></span>**contêiner de controle**
</dt> <dd>

Um aplicativo que dá suporte à inserção de controles implementando a interface [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite) .

</dd> <dt>

<span id="com.control_property_gloss"></span><span id="COM.CONTROL_PROPERTY_GLOSS"></span>**Propriedade de controle**
</dt> <dd>

Uma propriedade de tempo de execução que é exposta e gerenciada pelo próprio controle. Por exemplo, a fonte e o tamanho do texto usados pelo controle são propriedades de controle.

</dd> <dt>

<span id="com.controlling_object_gloss"></span><span id="COM.CONTROLLING_OBJECT_GLOSS"></span>**controlando objeto**
</dt> <dd>

O objeto dentro de um objeto de agregação que controla quais interfaces dentro do objeto de agregação são expostos e que são privados. A interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) do objeto de controle é chamada de controle **IUnknown**. As chamadas para métodos **IUnknown** de outros objetos na agregação devem ser passadas para o **IUnknown** de controle.

</dd> <dt>

<span id="com.control_site_gloss"></span><span id="COM.CONTROL_SITE_GLOSS"></span>**site de controle**
</dt> <dd>

Uma estrutura implementada por um contêiner de controle para gerenciar a exibição e o armazenamento de um controle. Dentro de um determinado contêiner, cada controle tem um site de controle correspondente.

</dd> <dt>

<span id="com.data_transfer_object_gloss"></span><span id="COM.DATA_TRANSFER_OBJECT_GLOSS"></span>**objeto de transferência de dados**
</dt> <dd>

Um objeto que implementa a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) e contém dados a serem transferidos de um objeto para outro por meio das operações de arrastar e soltar da área de transferência.

</dd> <dt>

<span id="com.default_object_handler_gloss"></span><span id="COM.DEFAULT_OBJECT_HANDLER_GLOSS"></span>**manipulador de objeto padrão**
</dt> <dd>

Uma DLL fornecida com OLE que atua como um substituto no espaço de processamento do aplicativo de contêiner para o objeto real.

Com o manipulador de objeto padrão, é possível examinar os dados armazenados de um objeto sem realmente ativar o objeto. O manipulador de objetos padrão executa outras tarefas, como a renderização de um objeto de seu estado armazenado em cache quando o objeto é carregado na memória.

</dd> <dt>

<span id="com.dependent_object_gloss"></span><span id="COM.DEPENDENT_OBJECT_GLOSS"></span>**objeto dependente**
</dt> <dd>

Um objeto COM que é normalmente inicializado por outro objeto (o objeto de host). Embora o tempo de vida do objeto dependente possa fazer sentido apenas durante o tempo de vida do objeto de host, o objeto de host não funciona como o [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle para o objeto dependente. Por outro lado, um objeto é um objeto agregado quando seu tempo de vida (por meio de sua contagem de referência) é totalmente controlado pelo objeto de gerenciamento.

</dd> <dt>

<span id="com.direct_access_mode_gloss"></span><span id="COM.DIRECT_ACCESS_MODE_GLOSS"></span>**modo de acesso direto**
</dt> <dd>

Um dos dois modos de acesso nos quais um objeto de armazenamento pode ser aberto. No modo direto, todas as alterações são imediatamente confirmadas no objeto de armazenamento raiz.

</dd> <dt>

<span id="com.document_object_gloss"></span><span id="COM.DOCUMENT_OBJECT_GLOSS"></span>**objeto Document**
</dt> <dd>

Um documento OLE que pode exibir uma ou mais exibições ativadas no local de seus dados em um quadro nativo ou estrangeiro, como um navegador, mantendo o controle total sobre a interface do usuário. Além de implementar o documento OLE comum e as interfaces de ativação in-loco, um objeto de documento deve implementar [**IOleDocument**](/windows/desktop/api/DocObj/nn-docobj-ioledocument)e cada uma de suas exibições (na forma de um objeto de exibição de documento) deve implementar [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview).

</dd> <dt>

<span id="com.document_object_container_gloss"></span><span id="COM.DOCUMENT_OBJECT_CONTAINER_GLOSS"></span>**contêiner de objeto de documento**
</dt> <dd>

Um aplicativo de contêiner capaz de exibir uma ou mais exibições de um ou mais objetos de documento e gerenciar todos os objetos de documento contidos em um arquivo. Cada objeto de documento é associado a um site de documento, e cada site de documento contém um ou mais sites de exibição de documento correspondentes às exibições com suporte pelo objeto Document. Um contêiner de objeto de documento também inclui um quadro de contêiner, que manipula a negociação de menus e barras de ferramentas e a enumeração de objetos contidos.

</dd> <dt>

<span id="com.document_object_server_gloss"></span><span id="COM.DOCUMENT_OBJECT_SERVER_GLOSS"></span>**servidor de objeto de documento**
</dt> <dd>

Um aplicativo de servidor capaz de fornecer objetos de documento.

</dd> <dt>

<span id="com.document_site_gloss"></span><span id="COM.DOCUMENT_SITE_GLOSS"></span>**site do documento**
</dt> <dd>

Um site do cliente implementado por um contêiner de objeto de documento para gerenciar a exibição e o armazenamento de um objeto de documento. Cada objeto de documento em um contêiner tem um site de documento correspondente.

</dd> <dt>

<span id="com.document_site_object_gloss"></span><span id="COM.DOCUMENT_SITE_OBJECT_GLOSS"></span>**objeto do site do documento**
</dt> <dd>

Um objeto COM que implementa a interface [**IOleDocumentSite**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentsite) , além das interfaces de cliente-site usuais (como [**IOleClientSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleclientsite)).

</dd> <dt>

<span id="com.document_view_gloss"></span><span id="COM.DOCUMENT_VIEW_GLOSS"></span>**exibição de documento**
</dt> <dd>

Uma apresentação específica dos dados de um documento. Um único objeto de documento pode ter uma ou mais exibições, mas uma única exibição de documento pode pertencer a um único objeto de documento.

</dd> <dt>

<span id="com.document_view_object_gloss"></span><span id="COM.DOCUMENT_VIEW_OBJECT_GLOSS"></span>**objeto de exibição de documento**
</dt> <dd>

Um objeto COM que implementa a interface [**IOleDocumentView**](/windows/desktop/api/DocObj/nn-docobj-ioledocumentview) e corresponde a uma determinada exibição de documento. Um objeto com várias exibições de documento agrega um objeto de exibição de documento separado para cada exibição.

</dd> <dt>

<span id="com.document_view_site_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_GLOSS"></span>**site de exibição de documentos**
</dt> <dd>

Um objeto agregado por um objeto de site de documento para gerenciar o espaço de exibição para uma exibição específica de um objeto de documento. Em um determinado site de documento, cada exibição de documento tem um site de exibição de documento correspondente.

</dd> <dt>

<span id="com.document_view_site_object_gloss"></span><span id="COM.DOCUMENT_VIEW_SITE_OBJECT_GLOSS"></span>**objeto de site de exibição de documento**
</dt> <dd>

Um objeto COM que é agregado em um objeto de site de documento e implementa a interface [**IOleInPlaceSite**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplacesite) e, opcionalmente, a interface [**IContinueCallback**](/windows/desktop/api/DocObj/nn-docobj-icontinuecallback) .

</dd> <dt>

<span id="com.drag_and_drop_gloss"></span><span id="COM.DRAG_AND_DROP_GLOSS"></span>**arrastar e soltar**
</dt> <dd>

Uma operação na qual o usuário final usa o mouse ou outro dispositivo apontador para mover dados para outro local na mesma janela ou em outra janela.

</dd> <dt>

<span id="com.embed_gloss"></span><span id="COM.EMBED_GLOSS"></span>**Incorporar**
</dt> <dd>

Para inserir um objeto em um documento composto de forma a preservar os formatos de dados nativos a esse objeto e habilitá-lo a ser editado de dentro de seu contêiner usando as ferramentas expostas por seu servidor.

</dd> <dt>

<span id="com.embedded_object_gloss"></span><span id="COM.EMBEDDED_OBJECT_GLOSS"></span>**objeto inserido**
</dt> <dd>

Um objeto cujos dados são armazenados em um documento composto, mas o objeto é executado no espaço de processo de seu servidor. O manipulador de objetos padrão fornece um substituto no espaço de processamento do aplicativo de contêiner para o objeto real.

</dd> <dt>

<span id="com.extended_property_gloss"></span><span id="COM.EXTENDED_PROPERTY_GLOSS"></span>**Propriedade estendida**
</dt> <dd>

Uma propriedade de tempo de execução, como a posição e o tamanho de um controle, que um usuário presumiria ser exposto pelo controle, mas é exposto e gerenciado pelo contêiner.

</dd> <dt>

<span id="com.file_moniker_gloss"></span><span id="COM.FILE_MONIKER_GLOSS"></span>**moniker do arquivo**
</dt> <dd>

Um moniker com base em um caminho no sistema de arquivos. Os identificadores de arquivo podem ser usados para identificar objetos que são salvos em seus próprios arquivos. Um moniker de arquivo é um objeto COM que dá suporte à implementação fornecida pelo sistema da interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) para a classe File moniker.

</dd> <dt>

<span id="com.font_object_gloss"></span><span id="COM.FONT_OBJECT_GLOSS"></span>**objeto de fonte**
</dt> <dd>

Um objeto COM que fornece acesso a fontes Graphics Device Interface (GDI) implementando a interface [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .

</dd> <dt>

<span id="com.format_identifier_gloss"></span><span id="COM.FORMAT_IDENTIFIER_GLOSS"></span>**identificador de formato**
</dt> <dd>

Um GUID que identifica uma propriedade persistente definida. Também conhecido como FMTID.

</dd> <dt>

<span id="com.frame_gloss"></span><span id="COM.FRAME_GLOSS"></span>**quadro**
</dt> <dd>

A parte de um aplicativo de contêiner responsável por negociar menus, teclas de aceleração, barras de ferramentas e outros elementos de interface do usuário compartilhados com um objeto COM inserido ou um objeto de documento.

</dd> <dt>

<span id="com.frame_object_gloss"></span><span id="COM.FRAME_OBJECT_GLOSS"></span>**objeto de quadro**
</dt> <dd>

Um objeto COM que implementa a interface [**IOleInPlaceFrame**](/windows/desktop/api/OleIdl/nn-oleidl-ioleinplaceframe) e, opcionalmente, a interface [**IOleCommandTarget**](/windows/desktop/api/DocObj/nn-docobj-iolecommandtarget) .

</dd> <dt>

<span id="com.generic_composite_moniker_gloss"></span><span id="COM.GENERIC_COMPOSITE_MONIKER_GLOSS"></span>**moniker composto genérico**
</dt> <dd>

Uma coleção sequenciada de monikers, começando com um moniker de arquivo para fornecer o caminho de nível de documento e continuando com um ou mais monikers de item que, como um todo, identifica exclusivamente um objeto.

</dd> <dt>

<span id="com.helper_function_gloss"></span><span id="COM.HELPER_FUNCTION_GLOSS"></span>**função auxiliar**
</dt> <dd>

Uma função que encapsula chamadas para outras funções e métodos de interface publicamente disponíveis no SDK do OLE. As funções auxiliares são uma maneira conveniente de chamar sequências usadas com frequência de chamadas de função e de método que realizam tarefas comuns.

</dd> <dt>

<span id="com.host_object_gloss"></span><span id="COM.HOST_OBJECT_GLOSS"></span>**objeto de host**
</dt> <dd>

Um objeto COM que forma uma relação hierárquica com um ou mais objetos COM, conhecidos como objetos dependentes. Normalmente, o objeto de host instancia os objetos dependentes e sua existência faz sentido dentro do tempo de vida do objeto de host. No entanto, o objeto de host não funciona como o [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) de controle para os objetos dependentes, nem é delegado diretamente às implementações de interface desses objetos.

</dd> <dt>

<span id="com.hresult_gloss"></span><span id="COM.HRESULT_GLOSS"></span>**RESULTADO**
</dt> <dd>

Um identificador de resultado opaco definido como zero para um retorno bem-sucedido de uma função e diferente de zero se as informações de erro ou de status forem retornadas.

</dd> <dt>

<span id="com.hyperlink_object_gloss"></span><span id="COM.HYPERLINK_OBJECT_GLOSS"></span>**objeto de hiperlink**
</dt> <dd>

Um objeto COM que implementa, no mínimo, a interface [**IHlink**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767974(v=vs.85)) e atua como um link para um objeto em outro local (o destino). Um hiperlink é composto de quatro partes: um moniker que identifica o local do destino; uma cadeia de caracteres para o local dentro do destino; um nome amigável, ou exibível, para o destino; e uma cadeia de caracteres que pode conter parâmetros adicionais.

</dd> <dt>

<span id="com.hyperlink_browse_context_gloss"></span><span id="COM.HYPERLINK_BROWSE_CONTEXT_GLOSS"></span>**contexto de procura de hiperlink**
</dt> <dd>

Um objeto COM que implementa a interface [**IHlinkBrowseContext**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767949(v=vs.85)) e mantém a pilha de navegação de hiperlink. O objeto de contexto de procura gerencia a janela do quadro do hiperlink e a janela do objeto de destino do hiperlink.

</dd> <dt>

<span id="com.hyperlink_container_gloss"></span><span id="COM.HYPERLINK_CONTAINER_GLOSS"></span>**contêiner de hiperlink**
</dt> <dd>

Um aplicativo de contêiner que dá suporte a hiperlinks implementando a interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e, se os objetos do contêiner podem ser destinos de outros hiperlinks, a interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) .

</dd> <dt>

<span id="com.hyperlink_frame_object_gloss"></span><span id="COM.HYPERLINK_FRAME_OBJECT_GLOSS"></span>**objeto de moldura de hiperlink**
</dt> <dd>

Um objeto COM que implementa a interface [**IHlinkFrame**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767938(v=vs.85)) e controla a navegação de nível superior e a exibição de hiperlinks para o contêiner do quadro e o servidor do destino do hiperlink.

</dd> <dt>

<span id="com.hyperlink_site_object_gloss"></span><span id="COM.HYPERLINK_SITE_OBJECT_GLOSS"></span>**objeto do site de hiperlink**
</dt> <dd>

Um objeto COM que implementa a interface [**IHlinkSite**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767933(v=vs.85)) e fornece o moniker ou o identificador de interface do seu contêiner de hiperlink. Um site de hiperlink pode atender a vários hiperlinks.

</dd> <dt>

<span id="com.hyperlink_target_object_gloss"></span><span id="COM.HYPERLINK_TARGET_OBJECT_GLOSS"></span>**objeto de destino do hiperlink**
</dt> <dd>

Um objeto COM que implementa a interface [**IHlinkTarget**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767929(v=vs.85)) e fornece seu moniker, nome amigável e outras informações que outros objetos de hiperlink usarão para navegar até ele.

</dd> <dt>

<span id="com.in_parameter_gloss"></span><span id="COM.IN_PARAMETER_GLOSS"></span>**parâmetro in**
</dt> <dd>

Um parâmetro que é alocado, definido e liberado pelo chamador de um método de função ou de interface. Um parâmetro in não é modificado pela função chamada.

</dd> <dt>

<span id="com.in_out_parameter_gloss"></span><span id="COM.IN_OUT_PARAMETER_GLOSS"></span>**parâmetro in/out**
</dt> <dd>

Um parâmetro que é inicialmente alocado pelo chamador de um método de função ou de interface e definido, liberado e realocado, se necessário, pelo processo que é chamado.

</dd> <dt>

<span id="com.in_place_activation_gloss"></span><span id="COM.IN_PLACE_ACTIVATION_GLOSS"></span>**ativação in-loco**
</dt> <dd>

Editar um objeto inserido dentro da janela de seu contêiner, usando as ferramentas fornecidas pelo servidor. Objetos vinculados não dão suporte à ativação in-loco; Eles são sempre editados na janela do servidor.

</dd> <dt>

<span id="com.in_process_server_gloss"></span><span id="COM.IN_PROCESS_SERVER_GLOSS"></span>**servidor em processo**
</dt> <dd>

Um servidor implementado como uma DLL que é executada no espaço de processo do cliente.

</dd> <dt>

<span id="com.instance_gloss"></span><span id="COM.INSTANCE_GLOSS"></span>**cópia**
</dt> <dd>

Um objeto para o qual a memória é alocada ou que é persistente.

</dd> <dt>

<span id="com.interface_gloss"></span><span id="COM.INTERFACE_GLOSS"></span>**interface**
</dt> <dd>

Um grupo de funções relacionadas semanticamente que fornecem acesso a um objeto COM. Cada interface OLE define um contrato que permite que os objetos interajam de acordo com o Component Object Model (COM). Embora o OLE forneça muitas implementações de interface, a maioria das interfaces também pode ser implementada por desenvolvedores que projetam aplicativos OLE.

</dd> <dt>

<span id="com.interface_identifier_iid_gloss"></span><span id="COM.INTERFACE_IDENTIFIER_IID_GLOSS"></span>**identificador de interface (IID)**
</dt> <dd>

Um GUID (identificador global exclusivo) associado a uma interface. Algumas funções usam IIDs como parâmetros para permitir que o chamador especifique qual ponteiro de interface deve ser retornado.

</dd> <dt>

<span id="com.item_moniker_gloss"></span><span id="COM.ITEM_MONIKER_GLOSS"></span>**moniker do item**
</dt> <dd>

Um moniker com base em uma cadeia de caracteres que identifica um objeto em um contêiner. Os monikers de item podem identificar objetos menores do que um arquivo, incluindo objetos incorporados em um documento composto ou um pseudo objeto (como um intervalo de células em uma planilha).

</dd> <dt>

<span id="com.licensing_gloss"></span><span id="COM.LICENSING_GLOSS"></span>**licença**
</dt> <dd>

Um recurso do COM que fornece controle sobre a criação de objetos. Os objetos licenciados podem ser criados somente por clientes que estão autorizados a usá-los. O licenciamento é implementado em COM por meio da interface [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) e por suporte para uma chave de licença que pode ser passada em tempo de execução.

</dd> <dt>

<span id="com.link_object_gloss"></span><span id="COM.LINK_OBJECT_GLOSS"></span>**vincular objeto**
</dt> <dd>

Um objeto COM que é criado quando um objeto COM vinculado é criado ou carregado. O objeto link é fornecido pelo OLE e implementa a interface [**IOleLink**](/windows/desktop/api/OleIdl/nn-oleidl-iolelink) .

</dd> <dt>

<span id="com.linked_object_gloss"></span><span id="COM.LINKED_OBJECT_GLOSS"></span>**objeto vinculado**
</dt> <dd>

Um objeto COM cujos dados de origem residem fisicamente onde ele foi inicialmente criado. Somente um moniker que representa os dados de origem e os dados de apresentação apropriados são mantidos com o documento composto. As alterações feitas na origem do link são refletidas automaticamente no objeto vinculado.

</dd> <dt>

<span id="com.link_source_gloss"></span><span id="COM.LINK_SOURCE_GLOSS"></span>**origem do link**
</dt> <dd>

Os dados que são a origem de um objeto vinculado. Uma fonte de link pode ser um arquivo ou uma parte de um arquivo, como um intervalo selecionado de células dentro de um arquivo (também chamado de pseudo objeto).

</dd> <dt>

<span id="com.loaded_state_gloss"></span><span id="COM.LOADED_STATE_GLOSS"></span>**estado carregado**
</dt> <dd>

O estado de um objeto depois que suas estruturas de dados são carregadas na memória e estão acessíveis para o processo do cliente.

</dd> <dt>

<span id="com.local_server_gloss"></span><span id="COM.LOCAL_SERVER_GLOSS"></span>**servidor local**
</dt> <dd>

Um servidor fora do processo implementado como um. Aplicativo EXE em execução no mesmo computador que o aplicativo cliente.

</dd> <dt>

<span id="com.lock_gloss"></span><span id="COM.LOCK_GLOSS"></span>**proprietário**
</dt> <dd>

Um ponteiro mantido para-e, possivelmente, uma contagem de referência incrementada em um objeto em execução. O OLE define dois tipos de bloqueios que podem ser mantidos em um objeto: forte e fraca. Para implementar um bloqueio forte, um servidor deve manter um ponteiro e uma contagem de referência, para que o objeto permaneça "bloqueado" na memória pelo menos até que o servidor chame [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release). Para implementar um bloqueio fraco, o servidor mantém apenas um ponteiro para o objeto, para que o objeto possa ser destruído por outro processo.

</dd> <dt>

<span id="com.marshaling_gloss"></span><span id="COM.MARSHALING_GLOSS"></span>**marshaling**
</dt> <dd>

Empacotamento e envio de chamadas de método de interface entre limites de thread ou processo.

</dd> <dt>

<span id="com.media_type_gloss"></span><span id="COM.MEDIA_TYPE_GLOSS"></span>**tipo de mídia**
</dt> <dd>

Uma extensão de MIME que permite a negociação de formato de dados entre um cliente e um objeto.

</dd> <dt>

<span id="com.mime_content_type_gloss"></span><span id="COM.MIME_CONTENT_TYPE_GLOSS"></span>**Tipo de conteúdo MIME**
</dt> <dd>

Uma extensão de MIME que permite a negociação de formato de dados entre um cliente e um objeto.

</dd> <dt>

<span id="com.multipurpose_internet_mail_extension_gloss"></span><span id="COM.MULTIPURPOSE_INTERNET_MAIL_EXTENSION_GLOSS"></span>**MIME (Multipurpose Internet Mail Extension)**
</dt> <dd>

Um protocolo de Internet originalmente desenvolvido para permitir o intercâmbio de mensagens de email com conteúdo rico em ambientes de rede, computador e email heterogêneos. Na prática, o MIME também foi adotado e estendido por aplicativos que não são de email.

</dd> <dt>

<span id="com.moniker_gloss"></span><span id="COM.MONIKER_GLOSS"></span>**moniker**
</dt> <dd>

Um objeto que implementa a interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . Um moniker atua como um nome que identifica exclusivamente um objeto COM. Da mesma forma que um caminho identifica um arquivo no sistema de arquivos, um moniker identifica um objeto COM no namespace do diretório.

</dd> <dt>

<span id="com.moniker_class_gloss"></span><span id="COM.MONIKER_CLASS_GLOSS"></span>**classe de moniker**
</dt> <dd>

Uma implementação da interface [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) . As classes de moniker fornecidas pelo sistema incluem moniker de arquivo, monikers de item, monikers compostos genéricos, antimonikers, monikers de ponteiro e identificadores de URL.

</dd> <dt>

<span id="com.moniker_client_gloss"></span><span id="COM.MONIKER_CLIENT_GLOSS"></span>**cliente de moniker**
</dt> <dd>

Um aplicativo que usa monikers para adquirir ponteiros de interface para objetos gerenciados por outro aplicativo.

</dd> <dt>

<span id="com.moniker_provider_gloss"></span><span id="COM.MONIKER_PROVIDER_GLOSS"></span>**provedor de moniker**
</dt> <dd>

Um aplicativo que torna os monikers disponíveis que identificam os objetos que ele gerencia, para que os objetos estejam acessíveis a outros aplicativos.

</dd> <dt>

<span id="com.namespace_extension_gloss"></span><span id="COM.NAMESPACE_EXTENSION_GLOSS"></span>**extensão do namespace**
</dt> <dd>

Um objeto COM em processo que implementa [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder), [**IPersistFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipersistfolder)e [**IShellView**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellview), que às vezes são chamados de interfaces de extensão de namespace. Uma extensão de namespace é usada para estender o namespace do Shell ou para criar um namespace separado. Os usuários primários são as caixas de diálogo do Windows Explorer e arquivo comum.

</dd> <dt>

<span id="com.native_data_gloss"></span><span id="COM.NATIVE_DATA_GLOSS"></span>**dados nativos**
</dt> <dd>

Os dados usados por um aplicativo de servidor OLE ao editar um objeto inserido.

</dd> <dt>

<span id="com.object_gloss"></span><span id="COM.OBJECT_GLOSS"></span>**objeto**
</dt> <dd>

No OLE, uma estrutura de programação que encapsula os dados e a funcionalidade que são definidos e alocados como uma única unidade e para o qual o único acesso público é por meio das interfaces da estrutura de programação. Um objeto COM deve dar suporte a, no mínimo, a interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , que mantém a existência do objeto enquanto ele está sendo usado e fornece acesso às outras interfaces do objeto.

</dd> <dt>

<span id="com.object_state_gloss"></span><span id="COM.OBJECT_STATE_GLOSS"></span>**Estado do objeto** 
</dt> <dd>

A relação entre um objeto de documento composto em seu contêiner e o aplicativo responsável pela criação do objeto: ativo, passivo, carregado ou em execução. Os objetos passivos são armazenados em disco ou em um banco de dados, e o objeto não é selecionado ou ativo. No estado Loaded, as estruturas de dados do objeto foram carregadas na memória, mas não estão disponíveis para operações como edição. Os objetos em execução são carregados e estão disponíveis para todas as operações. Os objetos ativos estão executando objetos que têm uma interface do usuário visível.

</dd> <dt>

<span id="com.object_type_name_gloss"></span><span id="COM.OBJECT_TYPE_NAME_GLOSS"></span>**nome do tipo de objeto**
</dt> <dd>

Uma cadeia de caracteres de identificação exclusiva que é armazenada como parte das informações disponíveis para um objeto no banco de dados de registro.

</dd> <dt>

<span id="com.ole_gloss"></span><span id="COM.OLE_GLOSS"></span>**OleDb**
</dt> <dd>

A tecnologia baseada em objeto da Microsoft para compartilhar informações e serviços entre os limites do processo e do computador.

</dd> <dt>

<span id="com.out_of_process_server_gloss"></span><span id="COM.OUT_OF_PROCESS_SERVER_GLOSS"></span>**servidor fora do processo**
</dt> <dd>

Um servidor, implementado como um. EXE, que é executado fora do processo de seu cliente, seja no mesmo computador ou em um computador remoto.

</dd> <dt>

<span id="com.out_parameter_gloss"></span><span id="COM.OUT_PARAMETER_GLOSS"></span>**parâmetro out**
</dt> <dd>

Um parâmetro out é alocado pela função que está sendo chamada e liberada pelo chamador.

</dd> <dt>

<span id="com.passive_state_gloss"></span><span id="COM.PASSIVE_STATE_GLOSS"></span>**estado passivo**
</dt> <dd>

O estado de um objeto COM quando ele é armazenado (em disco ou em um banco de dados). O objeto não está selecionado ou ativo.

</dd> <dt>

<span id="com.persistent_property_gloss"></span><span id="COM.PERSISTENT_PROPERTY_GLOSS"></span>**Propriedade persistente**
</dt> <dd>

Informações que podem ser armazenadas de forma persistente como parte de um objeto de armazenamento, como um arquivo ou diretório. As propriedades persistentes são agrupadas em conjuntos de propriedades, que podem ser exibidas e editadas.

Uma propriedade persistente é diferente das propriedades de tempo de execução de objetos criados com controles OLE e tecnologias de automação, que podem ser usadas para afetar o comportamento do sistema. A estrutura [**PROPVARIANT**](/windows/win32/api/propidl/ns-propidl-propvariant) define todos os tipos válidos de propriedades persistentes, enquanto a estrutura **variante** define todos os tipos válidos de propriedades de tempo de execução.

</dd> <dt>

<span id="com.persistent_storage_gloss"></span><span id="COM.PERSISTENT_STORAGE_GLOSS"></span>**armazenamento persistente**
</dt> <dd>

Armazenamento de um arquivo ou objeto em uma mídia, como um sistema de arquivos ou um banco de dados, de forma que o objeto e os seus próprios arquivos persistam quando o arquivo é fechado e, em seguida, reaberto posteriormente.

</dd> <dt>

<span id="com.picture_object_gloss"></span><span id="COM.PICTURE_OBJECT_GLOSS"></span>**objeto de imagem**
</dt> <dd>

Um objeto COM que fornece acesso a imagens GDI implementando a interface [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .

</dd> <dt>

<span id="com.pointer_moniker_gloss"></span><span id="COM.POINTER_MONIKER_GLOSS"></span>**moniker do ponteiro**
</dt> <dd>

Um moniker que mapeia um ponteiro de interface para um objeto na memória. Enquanto a maioria dos monikers identifica objetos que podem ser armazenados de forma persistente, os moniker do ponteiro identificam objetos que não podem. Eles permitem que esses objetos participem de uma operação de associação de moniker.

</dd> <dt>

<span id="com.presentation_data_gloss"></span><span id="COM.PRESENTATION_DATA_GLOSS"></span>**dados da apresentação**
</dt> <dd>

Os dados usados por um contêiner para exibir objetos inseridos ou vinculados.

</dd> <dt>

<span id="com.primary_verb_gloss"></span><span id="COM.PRIMARY_VERB_GLOSS"></span>**verbo primário**
</dt> <dd>

A ação associada aos usuários de operação mais comuns ou preferenciais que o executa em um objeto. O verbo primário é sempre definido como verbo zero no banco de dados de registro do sistema. Um verbo primário do objeto é executado clicando duas vezes no objeto.

</dd> <dt>

<span id="com.property_gloss"></span><span id="COM.PROPERTY_GLOSS"></span>**Propriedade**
</dt> <dd>

Informações associadas a um objeto. No OLE, as propriedades se enquadram em duas categorias: Propriedades de tempo de execução e propriedades persistentes. As propriedades de tempo de execução geralmente são associadas a objetos de controle ou seus contêineres. Por exemplo, cor do plano de fundo é uma propriedade de tempo de execução definida pelo contêiner de um controle. As propriedades persistentes são associadas a objetos armazenados.

</dd> <dt>

<span id="com.property_frame_gloss"></span><span id="COM.PROPERTY_FRAME_GLOSS"></span>**quadro de propriedade**
</dt> <dd>

O mecanismo de interface do usuário que exibe uma ou mais páginas de propriedades para um controle. O sistema de tempo de execução dos controles OLE fornece uma implementação padrão de um quadro de propriedade que pode ser acessado usando a função auxiliar [**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe) .

</dd> <dt>

<span id="com.property_identifier_gloss"></span><span id="COM.PROPERTY_IDENTIFIER_GLOSS"></span>**identificador de propriedade**
</dt> <dd>

Um inteiro assinado de quatro bytes que identifica uma propriedade persistente dentro de um conjunto de propriedades.

</dd> <dt>

<span id="com.property_page_gloss"></span><span id="COM.PROPERTY_PAGE_GLOSS"></span>**página de propriedades**
</dt> <dd>

Um objeto com com seu próprio CLSID que faz parte de uma interface do usuário, implementado por um controle e permite que as propriedades do controle sejam exibidas e definidas. Os objetos da página de propriedades implementam a interface [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) .

</dd> <dt>

<span id="com.property_page_site_gloss"></span><span id="COM.PROPERTY_PAGE_SITE_GLOSS"></span>**site da página de propriedades**
</dt> <dd>

O local dentro de um quadro de propriedades onde uma página de propriedades é exibida. O quadro de propriedades implementa a interface [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite) , que contém métodos para gerenciar os sites de cada uma das páginas de propriedades fornecidas por um controle.

</dd> <dt>

<span id="com.property_set_gloss"></span><span id="COM.PROPERTY_SET_GLOSS"></span>**conjunto de propriedades**
</dt> <dd>

Um grupo de propriedades relacionado logicamente que está associado a um objeto armazenado persistente. Para criar, abrir, excluir ou enumerar um ou mais conjuntos de propriedades, implemente a interface [**IPropertySetStorage**](/windows/desktop/api/propidl/nn-propidl-ipropertysetstorage) . Se você estiver usando arquivos compostos, poderá usar a implementação do OLE dessa interface em vez de implementar seu próprio.

</dd> <dt>

<span id="com.property_set_storage_gloss"></span><span id="COM.PROPERTY_SET_STORAGE_GLOSS"></span>**armazenamento de conjunto de propriedades**
</dt> <dd>

Um objeto de armazenamento COM que mantém um conjunto de propriedades. Um armazenamento de conjunto de propriedades é um objeto dependente associado e gerenciado por um objeto de armazenamento.

</dd> <dt>

<span id="com.property_sheet_gloss"></span><span id="COM.PROPERTY_SHEET_GLOSS"></span>**folha de propriedades**
</dt> <dd>

Um conjunto de páginas de propriedades para um ou mais objetos.

</dd> <dt>

<span id="com.proxy_gloss"></span><span id="COM.PROXY_GLOSS"></span>**acionista**
</dt> <dd>

Um objeto específico de interface que empacota parâmetros para essa interface em preparação para uma chamada de método remoto. Um proxy é executado no espaço de endereço do remetente e se comunica com um stub correspondente no espaço de endereço do destinatário.

</dd> <dt>

<span id="com.proxy_manager_gloss"></span><span id="COM.PROXY_MANAGER_GLOSS"></span>**Gerenciador de proxy**
</dt> <dd>

No empacotamento padrão, um proxy que gerencia todos os proxies de interface para um único objeto.

</dd> <dt>

<span id="com.pseudo_object_gloss"></span><span id="COM.PSEUDO_OBJECT_GLOSS"></span>**pseudo objeto**
</dt> <dd>

Uma parte de um documento ou objeto inserido, como um intervalo de células em uma planilha, que pode ser a origem de um objeto COM.

</dd> <dt>

<span id="com.reference_counting_gloss"></span><span id="COM.REFERENCE_COUNTING_GLOSS"></span>**contagem de referência**
</dt> <dd>

Manter uma contagem de cada ponteiro de interface mantido em um objeto para garantir que o objeto não seja destruído antes que todas as referências a ele sejam liberadas.

</dd> <dt>

<span id="com.relative_moniker_gloss"></span><span id="COM.RELATIVE_MONIKER_GLOSS"></span>**moniker relativo**
</dt> <dd>

Um moniker que especifica o local de um objeto relativo ao local de outro objeto. Um moniker relativo é análogo a um caminho relativo, como.. \\ relatório de backup \\ . old.

</dd> <dt>

<span id="com.remote_server_gloss"></span><span id="COM.REMOTE_SERVER_GLOSS"></span>**servidor remoto**
</dt> <dd>

Um aplicativo de servidor, implementado como um EXE, em execução em um computador diferente do aplicativo cliente que o está usando.

</dd> <dt>

<span id="com.revert_gloss"></span><span id="COM.REVERT_GLOSS"></span>**voltar**
</dt> <dd>

Para descartar as alterações feitas em um objeto desde a última vez em que as alterações foram confirmadas ou o armazenamento do objeto foi aberto.

</dd> <dt>

<span id="com.root_storage_object_gloss"></span><span id="COM.ROOT_STORAGE_OBJECT_GLOSS"></span>**objeto de armazenamento raiz**
</dt> <dd>

O objeto de armazenamento mais externo em um documento. Um objeto de armazenamento raiz pode conter outros objetos de armazenamento e fluxo aninhados. Por exemplo, um documento composto é salvo em disco como uma série de objetos de armazenamento e fluxo dentro de um objeto de armazenamento raiz.

</dd> <dt>

<span id="com.running_state_gloss"></span><span id="COM.RUNNING_STATE_GLOSS"></span>**Estado de execução**
</dt> <dd>

O estado de um objeto COM quando seu aplicativo de servidor está em execução e é possível acessar suas interfaces e receber notificações de alterações.

</dd> <dt>

<span id="com.running_object_table_gloss"></span><span id="COM.RUNNING_OBJECT_TABLE_GLOSS"></span>**executando a tabela de objetos (corrompidos)**
</dt> <dd>

Uma tabela acessível globalmente em cada computador que controla todos os objetos COM no estado em execução que podem ser identificados por um moniker. Os provedores de moniker registram um objeto na tabela, que incrementa a contagem de referência do objeto. Antes que o objeto possa ser destruído, seu moniker deve ser liberado da tabela.

</dd> <dt>

<span id="com.run_time_property_gloss"></span><span id="COM.RUN_TIME_PROPERTY_GLOSS"></span>**Propriedade de tempo de execução**
</dt> <dd>

Informações de estado discreta associadas a um objeto de controle ou a seu contêiner. Há três tipos de propriedades de tempo de execução: Propriedades de ambiente, propriedades de controle e propriedades estendidas.

</dd> <dt>

<span id="com.self_registration_gloss"></span><span id="COM.SELF_REGISTRATION_GLOSS"></span>**registro automático**
</dt> <dd>

O processo pelo qual um servidor pode executar suas próprias operações de registro.

</dd> <dt>

<span id="com.server_application_gloss"></span><span id="COM.SERVER_APPLICATION_GLOSS"></span>**aplicativo de servidor**
</dt> <dd>

Um aplicativo que pode criar objetos COM. Os aplicativos de contêiner podem então ser inseridos ou vinculados a esses objetos.

</dd> <dt>

<span id="com.static_object_gloss"></span><span id="COM.STATIC_OBJECT_GLOSS"></span>**objeto estático**
</dt> <dd>

Um objeto que contém apenas uma apresentação, sem dados nativos. Um contêiner pode tratar um objeto estático como se fosse um objeto vinculado ou incorporado, exceto que não é possível editar um objeto estático.

Um objeto estático pode resultar, por exemplo, da interrupção de um link em um objeto vinculado, ou seja, o aplicativo do servidor não está disponível ou o usuário não quer que o objeto vinculado seja mais atualizado.

</dd> <dt>

<span id="com.storage_object_gloss"></span><span id="COM.STORAGE_OBJECT_GLOSS"></span>**objeto de armazenamento**
</dt> <dd>

Um objeto COM que implementa a interface [**IStorage**](/windows/desktop/api/objidl/nn-objidl-istorage) . Um objeto de armazenamento contém objetos de armazenamento aninhados ou objetos de fluxo, resultando no equivalente de uma estrutura de diretório/arquivo em um único arquivo.

</dd> <dt>

<span id="com.stream_object_gloss"></span><span id="COM.STREAM_OBJECT_GLOSS"></span>**objeto Stream**
</dt> <dd>

Um objeto COM que implementa a interface [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) . Um objeto Stream é análogo a um arquivo em um diretório/sistema de arquivos.

</dd> <dt>

<span id="com.structured_storage_gloss"></span><span id="COM.STRUCTURED_STORAGE_GLOSS"></span>**Armazenamento estruturado**
</dt> <dd>

Tecnologia do OLE para armazenar arquivos compostos em sistemas de arquivos nativos.

</dd> <dt>

<span id="com.stub_gloss"></span><span id="COM.STUB_GLOSS"></span>**Gerenciador**
</dt> <dd>

Quando os parâmetros de um método de interface ou de uma função são empacotados em um limite de processo, o stub é um objeto específico de interface que desempacota os parâmetros de marshaling e chama o método necessário. O stub é executado no espaço de endereço do destinatário e se comunica com um proxy correspondente no espaço de endereço do remetente.

</dd> <dt>

<span id="com.stub_manager_gloss"></span><span id="COM.STUB_MANAGER_GLOSS"></span>**Gerenciador de stub**
</dt> <dd>

Gerencia todos os stubs de interface para um único objeto.

</dd> <dt>

<span id="com.synchronous_call_gloss"></span><span id="COM.SYNCHRONOUS_CALL_GLOSS"></span>**chamada síncrona**
</dt> <dd>

Uma chamada de função que não permite que mais instruções no processo de chamada sejam executadas até que a função retorne.

</dd> <dt>

<span id="com.system_registry_gloss"></span><span id="COM.SYSTEM_REGISTRY_GLOSS"></span>**registro do sistema**
</dt> <dd>

Um repositório de informações em todo o sistema com suporte no Windows, que contém informações sobre o sistema e seus aplicativos, incluindo clientes e servidores OLE.

</dd> <dt>

<span id="com.transacted_access_mode_gloss"></span><span id="COM.TRANSACTED_ACCESS_MODE_GLOSS"></span>**modo de acesso transacionado**
</dt> <dd>

Um dos dois modos de acesso nos quais um objeto de armazenamento pode ser aberto. Quando aberto no modo transacionado, as alterações são armazenadas em buffers até que o objeto de armazenamento raiz confirme suas alterações.

</dd> <dt>

<span id="com.type_information_gloss"></span><span id="COM.TYPE_INFORMATION_GLOSS"></span>**informações de tipo**
</dt> <dd>

Informações sobre a classe de um objeto fornecida por uma biblioteca de tipos. Para fornecer informações de tipo, um objeto COM implementa a interface [**IProvideClassInfo**](/windows/desktop/api/OCIdl/nn-ocidl-iprovideclassinfo) .

</dd> <dt>

<span id="com.uniform_data_transfer_gloss"></span><span id="COM.UNIFORM_DATA_TRANSFER_GLOSS"></span>**transferência de dados uniforme**
</dt> <dd>

Um modelo para transferir dados por meio da área de transferência, arrastar e soltar ou automação. Os objetos que estão em conformidade com esse modelo implementam a interface [**IDataObject**](/windows/desktop/api/ObjIdl/nn-objidl-idataobject) . Esse modelo substitui o DDE (Dynamic Data Exchange).

</dd> <dt>

<span id="com.unmarshaling_gloss"></span><span id="COM.UNMARSHALING_GLOSS"></span>**desempacotamento**
</dt> <dd>

Desempacotamento de parâmetros que foram enviados a um proxy entre limites de processo.

</dd> <dt>

<span id="com.universal_resource_locator_gloss"></span><span id="COM.UNIVERSAL_RESOURCE_LOCATOR_GLOSS"></span>**localizador de recursos universal (URL)**
</dt> <dd>

O identificador usado pelo World Wide Web para os nomes e locais de objetos na Internet. O OLE fornece uma classe de moniker, moniker de URL, cuja implementação pode ser usada para associar um cliente a objetos identificados por uma URL.

</dd> <dt>

<span id="com.url_moniker_gloss"></span><span id="COM.URL_MONIKER_GLOSS"></span>**Moniker da URL**
</dt> <dd>

Um moniker com base em um localizador de recursos universal (URL). Um cliente pode usar identificadores de URL para associar a objetos que residem na Internet. A classe de moniker da URL fornecida pelo sistema dá suporte à associação síncrona e assíncrona.

</dd> </dl>

 

 