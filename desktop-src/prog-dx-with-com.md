---
description: Programando DirectX com com.
title: Programando DirectX com com
ms.topic: article
ms.date: 01/29/2019
ms.openlocfilehash: 67fc7a35f42439e1a9eeef1b2895d88dc0dbf5d4
ms.sourcegitcommit: f712e5fed19d6afe2762a77ffcdf8b5977f85901
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/26/2021
ms.locfileid: "103923018"
---
# <a name="programming-directx-with-com"></a>Programando DirectX com com

O Microsoft Component Object Model (COM) é um modelo de programação orientado a objeto usado por várias tecnologias, incluindo a grande parte da superfície da API do DirectX. Por esse motivo, você (como um desenvolvedor do DirectX) usa inevitavelmente o COM ao programar o DirectX.

> [!NOTE]
> O tópico [consumir componentes com com C++/WinRT](/windows/uwp/cpp-and-winrt-apis/consume-com) mostra como consumir APIs do DirectX (e qualquer API com, para esse assunto) usando [C++/WinRT](/windows/uwp/cpp-and-winrt-apis/). Isso é, de longe, a tecnologia mais conveniente e recomendada para uso.

Como alternativa, você pode usar COM bruto, e é para isso que este tópico se trata. Você precisará de uma compreensão básica dos princípios e das técnicas de programação envolvidas no consumo de APIs COM. Embora o COM tenha uma reputação de ser difícil e complexo, a programação COM exigida pela maioria dos aplicativos DirectX é simples. Em parte, isso ocorre porque você consumirá os objetos COM fornecidos pelo DirectX. Não há necessidade de você criar seus próprios objetos COM, que é normalmente o local em que a complexidade surge.

## <a name="com-component-overview"></a>Visão geral do componente COM

Um objeto COM é essencialmente um componente encapsulado de funcionalidade que pode ser usado por aplicativos para executar uma ou mais tarefas. Para a implantação, um ou mais componentes COM são empacotados em um binário chamado servidor COM; com mais frequência do que não uma DLL.

Uma DLL tradicional exporta funções gratuitas. Um servidor COM pode fazer o mesmo. Mas os componentes COM dentro do servidor COM expõem interfaces COM e métodos de membro que pertencem a essas interfaces. Seu aplicativo cria instâncias de componentes COM, recupera interfaces deles e chama métodos nessas interfaces para se beneficiar dos recursos implementados nos componentes COM.

Na prática, isso parece ser semelhante à chamada de métodos em um objeto C++ regular. Mas há algumas diferenças.

- Um objeto COM impõe um encapsulamento mais estrito do que um objeto C++. Você não pode apenas criar o objeto e, em seguida, chamar qualquer método público. Em vez disso, os métodos públicos de um componente COM são agrupados em uma ou mais interfaces COM. Para chamar um método, você cria o objeto e recupera do objeto a interface que implementa o método. Uma interface normalmente implementa um conjunto relacionado de métodos que fornecem acesso a um recurso específico do objeto. Por exemplo, a interface [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) representa um adaptador gráfico virtual e contém métodos que permitem criar recursos, por exemplo, e muitas outras tarefas relacionadas ao adaptador.
- Um objeto COM não é criado da mesma maneira que um objeto C++. Há várias maneiras de criar um objeto COM, mas todos envolvem técnicas específicas de COM. A API do DirectX inclui uma variedade de funções auxiliares e métodos que simplificam a criação da maioria dos objetos COM do DirectX.
- Você deve usar técnicas específicas do COM para controlar o tempo de vida de um objeto COM.
- O servidor COM (normalmente uma DLL) não precisa ser carregado explicitamente. Não é possível vincular a uma biblioteca estática para usar um componente COM. Cada componente COM tem um identificador exclusivo registrado (um identificador global exclusivo, ou GUID), que seu aplicativo usa para identificar o objeto COM. Seu aplicativo identifica o componente e o tempo de execução COM carrega automaticamente a DLL correta do servidor COM.
- COM é uma especificação binária. Objetos COM podem ser gravados e acessados em uma variedade de idiomas. Você não precisa saber nada sobre o código-fonte do objeto. Por exemplo, Visual Basic aplicativos usam rotineiramente objetos COM que foram escritos em C++.

## <a name="component-object-and-interface"></a>Componente, objeto e interface

É importante entender a distinção entre componentes, objetos e interfaces. Em uso casual, você pode ouvir um componente ou objeto referido pelo nome de sua interface principal. Mas os termos não são intercambiáveis. Um componente pode implementar qualquer número de interfaces; e um objeto é uma instância de um componente. Por exemplo, embora todos os componentes devam implementar a [**interface IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown), normalmente implementam pelo menos uma interface adicional e podem implementar muitos.

Para usar um método de interface específico, você não deve apenas criar uma instância de um objeto. você também deve obter a interface correta a partir dele.

Além disso, mais de um componente pode implementar a mesma interface. Uma interface é um grupo de métodos que executam um conjunto de operações logicamente relacionadas. A definição de interface especifica apenas a sintaxe dos métodos e sua funcionalidade geral. Qualquer componente COM que precise dar suporte a um determinado conjunto de operações pode fazer isso implementando uma interface adequada. Algumas interfaces são altamente especializadas e são implementadas somente por um único componente; outras são úteis em várias circunstâncias e são implementadas por vários componentes.

Se um componente implementa uma interface, ele deve dar suporte a todos os métodos na definição de interface. Em outras palavras, você deve ser capaz de chamar qualquer método e ter certeza de que ele existe. No entanto, os detalhes de como um método específico é implementado podem variar de um componente para outro. Por exemplo, componentes diferentes podem usar algoritmos diferentes para chegar ao resultado final. Também não há nenhuma garantia de que um método terá suporte de forma não trivial. Às vezes, um componente implementa uma interface comumente usada, mas precisa dar suporte a apenas um subconjunto dos métodos. Você ainda poderá chamar os métodos restantes com êxito, mas retornará um [**HRESULT**](#hresult-values) (que é um tipo com padrão que representa um código de resultado) que contém o valor **E_NOTIMPL**. Você deve consultar sua documentação para ver como uma interface é implementada por qualquer componente específico.

O padrão COM requer que uma definição de interface não deva ser alterada depois de ser publicada. O autor não pode, por exemplo, adicionar um novo método a uma interface existente. O autor deve, em vez disso, criar uma nova interface. Embora não haja restrições quanto aos métodos que devem estar nessa interface, uma prática comum é fazer com que a interface de próxima geração inclua todos os métodos da interface antiga, além de quaisquer novos métodos.

Não é incomum que uma interface tenha várias gerações. Normalmente, todas as gerações executam essencialmente a mesma tarefa geral, mas elas são diferentes em termos específicos. Geralmente, um componente COM implementa todas as gerações atuais e anteriores de uma linhagem de interface específica. Isso permite que os aplicativos mais antigos continuem usando as interfaces mais antigas do objeto, enquanto os aplicativos mais recentes podem aproveitar os recursos das interfaces mais recentes. Normalmente, um grupo descendente de interfaces tem o mesmo nome, mais um inteiro que indica a geração. Por exemplo, se a interface original fosse nomeada **IMinhaInterface** (implicando a geração 1), as duas próximas gerações seriam chamadas **IMyInterface2** e **IMyInterface3**. No caso de interfaces DirectX, gerações sucessivas são normalmente nomeadas para o número de versão do DirectX.

## <a name="guids"></a>GUIDs

GUIDs são uma parte fundamental do modelo de programação COM. Em seu mais básico, um GUID é uma estrutura de 128 bits. No entanto, os GUIDs são criados de forma a garantir que dois GUIDs sejam os mesmos. O COM usa os GUIDs extensivamente para duas finalidades principais.

- Para identificar exclusivamente um componente COM específico. Um GUID atribuído para identificar um componente COM é chamado de identificador de classe (CLSID) e você usa um CLSID quando deseja criar uma instância do componente COM associado.
- Para identificar exclusivamente uma interface COM específica. Um GUID atribuído para identificar uma interface COM é chamado de IID (identificador de interface) e você usa um IID quando solicita uma interface específica de uma instância de um componente (um objeto). O IID de uma interface será o mesmo, independentemente de qual componente implemente a interface.

Para sua conveniência, a documentação do DirectX normalmente se refere a componentes e interfaces por seus nomes descritivos (por exemplo, **ID3D12Device**) em vez de seus GUIDs. No contexto da documentação do DirectX, não há nenhuma ambiguidade. É tecnicamente possível que uma terceira parte crie uma interface com o nome descritivo **ID3D12Device** (ela precisaria ter um IID diferente para ser válido). No entanto, para fins de clareza, não recomendamos isso.

Portanto, a única maneira não ambígua de se referir a um objeto ou interface específica é por seu GUID.

Embora um GUID seja uma estrutura, um GUID geralmente é expresso em forma de cadeia de caracteres equivalente. O formato geral da forma de cadeia de caracteres de um GUID é de 32 dígitos hexadecimais, no formato 8-4-4-4-12. Ou seja, {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}, em que cada x corresponde a um dígito hexadecimal. Por exemplo, a forma de cadeia de caracteres do IID para a interface **ID3D12Device** é {189819F1-1DB6-4B57-BE54-1821339B85F7}.

Como o GUID real é um pouco atarefado para uso e fácil de digitar, um nome equivalente geralmente é fornecido também. No seu código, você pode usar esse nome em vez da estrutura real ao chamar funções, por exemplo, quando você passa um argumento para o `riid` parâmetro para [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice). A Convenção de nomenclatura personalizada é preceder IID_ ou CLSID_ ao nome descritivo da interface ou do objeto, respectivamente. Por exemplo, o nome do IID da interface **ID3D12Device** é IID_ID3D12Device.

> [!NOTE]
> Os aplicativos DirectX devem ser vinculados com ``dxguid.lib`` e ``uuid.lib`` para fornecer definições para os vários GUIDs de interface e de classe. Visual C++ e outros compiladores dão suporte à extensão de linguagem do operador de **__uuidof** , mas o vínculo C-Style explícito com essas bibliotecas de links também tem suporte e é totalmente portátil.

## <a name="hresult-values"></a>Valores HRESULT

A maioria dos métodos COM retorna um inteiro de 32 bits chamado **HRESULT**. Com a maioria dos métodos, o HRESULT é essencialmente uma estrutura que contém duas partes principais de informações.
- Se o método teve êxito ou falhou.
- Informações mais detalhadas sobre o resultado da operação executada pelo método.

Alguns métodos retornam um valor **HRESULT** do conjunto padrão definido em `Winerror.h` . No entanto, um método é gratuito para retornar um valor de **HRESULT** personalizado com informações mais especializadas. Esses valores normalmente estão documentados na página de referência do método.

A lista de valores **HRESULT** que você encontra na página de referência de um método é geralmente apenas um subconjunto dos possíveis valores que podem ser retornados. A lista normalmente aborda apenas os valores que são específicos para o método, bem como os valores padrão que têm algum significado específico do método. Você deve assumir que um método pode retornar uma variedade de valores **HRESULT** padrão, mesmo que eles não estejam documentados explicitamente.

Embora os valores **HRESULT** geralmente sejam usados para retornar informações de erro, você não deve considerá-los como códigos de erro. O fato de que o bit que indica êxito ou falha é armazenado separadamente dos bits que contêm as informações detalhadas permite que os valores de **HRESULT** tenham qualquer número de códigos de êxito e de falha. Por convenção, os nomes de códigos de êxito são prefixados por S_ e códigos de falha por E_. Por exemplo, os dois códigos mais comumente usados são S_OK e E_FAIL, que indicam êxito ou falha simples, respectivamente.

O fato de que os métodos COM podem retornar uma variedade de códigos de êxito ou de falha significam que você precisa ter cuidado ao testar o valor **HRESULT** . Por exemplo, considere um método hipotético com valores de retorno documentados de S_OK se for bem-sucedido e E_FAIL se não for. No entanto, lembre-se de que o método também pode retornar outros códigos de falha ou êxito. O fragmento de código a seguir ilustra o perigo de usar um teste simples, em que `hr` contém o valor **HRESULT** retornado pelo método.

```cpp
if (hr == E_FAIL)
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Desde que, no caso de falha, esse método apenas retorne E_FAIL (e não algum outro código de falha), esse teste funciona. No entanto, é mais realista que um determinado método seja implementado para retornar um conjunto de códigos de falha específicos, talvez E_NOTIMPL ou E_INVALIDARG. Com o código acima, esses valores seriam interpretados incorretamente como um sucesso.

Se precisar de informações detalhadas sobre o resultado da chamada do método, você precisará testar cada valor **HRESULT** relevante. No entanto, você pode se interessar apenas se o método teve êxito ou falhou. Uma maneira robusta de testar se um valor **HRESULT** indica êxito ou falha é passar o valor para uma das macros a seguir, definida em Winerror. h.

- A `SUCCEEDED` macro retorna true para um código de êxito e false para um código de falha.
- A `FAILED` macro retorna true para um código de falha e false para um código de êxito.

Portanto, você pode corrigir o fragmento de código anterior usando a `FAILED` macro, conforme mostrado no código a seguir.

```cpp
if (FAILED(hr))
{
    // Handle the failure case.
}
else
{
    // Handle the success case.
}  
```

Esse fragmento de código corrigido trata corretamente E_NOTIMPL e E_INVALIDARG como falhas.

Embora a maioria dos métodos COM retorne valores de **HRESULT** estruturados, um pequeno número usa **HRESULT** para retornar um inteiro simples. Implicitamente, esses métodos sempre são bem-sucedidos. Se você passar um **HRESULT** desse tipo para a macro SUCCEEDED, a macro sempre retornará true. Um exemplo de um método chamado comumente que não retorna um **HRESULT** é o método **IUnknown:: Release** , que retorna um ULONG. Esse método decrementa a contagem de referência de um objeto em um e retorna a contagem de referência atual. Consulte [Gerenciando um tempo de vida de um objeto com](#managing-a-com-objects-lifetime) para uma discussão de contagem de referência.

## <a name="the-address-of-a-pointer"></a>O endereço de um ponteiro

Se você exibir algumas páginas de referência de método COM, provavelmente será executado em algo semelhante ao seguinte.

```cpp
HRESULT D3D12CreateDevice(
  IUnknown          *pAdapter,
  D3D_FEATURE_LEVEL MinimumFeatureLevel,
  REFIID            riid,
  void              **ppDevice
);
```

Embora um ponteiro normal seja bastante familiar para qualquer desenvolvedor de C/C++, COM geralmente usa um nível adicional de indireção. Esse segundo nível de indireção é indicado por dois asteriscos, `**` , após a declaração de tipo, e o nome da variável normalmente tem um prefixo de `pp` . Para a função acima, o `ppDevice` parâmetro é normalmente referido como o endereço de um ponteiro para um void. Na prática, neste exemplo, `ppDevice` é o endereço de um ponteiro para uma interface **ID3D12Device** .

Ao contrário de um objeto C++, você não acessa diretamente os métodos de um objeto COM. Em vez disso, você deve obter um ponteiro para uma interface que expõe o método. Para invocar o método, você usa essencialmente a mesma sintaxe que faria para invocar um ponteiro para um método C++. Por exemplo, para invocar o método **IMinhaInterface::D osomething** , você usaria a sintaxe a seguir.

```cpp
IMyInterface * pMyIface = nullptr;
...
pMyIface->DoSomething(...);
```

A necessidade de um segundo nível de indireção é o fato de que você não cria ponteiros de interface diretamente. Você deve chamar um de vários métodos, como o método **D3D12CreateDevice** mostrado acima. Para usar esse método para obter um ponteiro de interface, você declara uma variável como um ponteiro para a interface desejada e, em seguida, passa o endereço dessa variável para o método. Em outras palavras, você passa o endereço de um ponteiro para o método. Quando o método retorna, a variável aponta para a interface solicitada e você pode usar esse ponteiro para chamar qualquer um dos métodos da interface.

```cpp
IDXGIAdapter * pIDXGIAdapter = nullptr;
...
ID3D12Device * pD3D12Device = nullptr;
HRESULT hr = ::D3D12CreateDevice(
    pIDXGIAdapter,
    D3D_FEATURE_LEVEL_11_0,
    IID_ID3D12Device,
    &pD3D12Device);
if (FAILED(hr)) return E_FAIL;

// Now use pD3D12Device in the form pD3D12Device->MethodName(...);
```

## <a name="creating-a-com-object"></a>Criando um objeto COM

Há várias maneiras de criar um objeto COM. Esses são os dois mais comumente usados na programação do DirectX.

- Indiretamente, chamando um método ou função DirectX que cria o objeto para você. O método cria o objeto e retorna uma interface no objeto. Quando você cria um objeto dessa forma, às vezes você pode especificar qual interface deve ser retornada, outras vezes a interface é implícita. O exemplo de código acima mostra como criar indiretamente um objeto COM de dispositivo Direct3D 12.
- Diretamente, passando o CLSID do objeto para a [**função CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). A função cria uma instância do objeto e retorna um ponteiro para uma interface que você especifica.

Uma vez, antes de criar qualquer objeto COM, você deve inicializar COM chamando a [**função CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Se você estiver criando objetos indiretamente, o método de criação de objeto tratará essa tarefa. Mas, se você precisar criar um objeto com **CoCreateInstance**, deverá chamar **CoInitializeEx** explicitamente. Quando tiver terminado, o COM deve ser não inicializado chamando [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize). Se você fizer uma chamada para **CoInitializeEx** , deverá fazer a correspondência com uma chamada para **CoUninitialize**. Normalmente, os aplicativos que precisam inicializar explicitamente o COM fazem isso em sua rotina de inicialização e não inicializam COM em sua rotina de limpeza.

Para criar uma nova instância de um objeto com com **CoCreateInstance**, você deve ter o CLSID do objeto. Se esse CLSID estiver disponível publicamente, você o encontrará na documentação de referência ou no arquivo de cabeçalho apropriado. Se o CLSID não estiver disponível publicamente, você não poderá criar o objeto diretamente.

A função **CoCreateInstance** tem cinco parâmetros. Para os objetos COM que você usará com o DirectX, você pode normalmente definir os parâmetros da seguinte maneira.

*rclsid* Defina isso para o CLSID do objeto que você deseja criar.

*pUnkOuter* Defina como `nullptr` . Esse parâmetro será usado somente se você estiver agregando objetos. Uma discussão sobre a agregação COM está fora do escopo deste tópico.

*dwClsContext* Defina como CLSCTX_INPROC_SERVER. Essa configuração indica que o objeto é implementado como uma DLL e é executado como parte do processo do seu aplicativo.

*riid* Defina como o IID da interface que você deseja que tenha retornado. A função criará o objeto e retornará o ponteiro de interface solicitado no parâmetro PPV.

*PPV* Defina isso para o endereço de um ponteiro que será definido para a interface especificada por `riid` quando a função retornar. Essa variável deve ser declarada como um ponteiro para a interface solicitada, e a referência ao ponteiro na lista de parâmetros deve ser convertida como (LPVOID *).

Criar um objeto indiretamente geralmente é muito mais simples, como vimos no exemplo de código acima. Você passa o método de criação de objeto o endereço de um ponteiro de interface, e o método cria o objeto e retorna um ponteiro de interface. Quando você cria um objeto indiretamente, mesmo que não possa escolher qual interface o método retorna, geralmente você ainda pode especificar uma variedade de coisas sobre como o objeto deve ser criado.

Por exemplo, você pode passar para **D3D12CreateDevice** um valor especificando o nível mínimo de recurso do D3D ao qual o dispositivo retornado deve dar suporte, conforme mostrado no exemplo de código acima.

## <a name="using-com-interfaces"></a>Usando interfaces COM

Quando você cria um objeto COM, o método de criação retorna um ponteiro de interface. Em seguida, você pode usar esse ponteiro para acessar qualquer um dos métodos da interface. A sintaxe é idêntica à usada com um ponteiro para um método C++.

## <a name="requesting-additional-interfaces"></a>Solicitando interfaces adicionais

Em muitos casos, o ponteiro de interface que você recebe do método de criação pode ser o único que você precisa. Na verdade, é relativamente comum que um objeto exporte apenas uma interface diferente de **IUnknown**. No entanto, muitos objetos exportam várias interfaces e você pode precisar de ponteiros para vários deles. Se você precisar de mais interfaces do que aquela retornada pelo método de criação, não será necessário criar um novo objeto. Em vez disso, solicite outro ponteiro de interface usando o [**método IUnknown:: QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(refiid_void))do objeto.

Se você criar o objeto com **CoCreateInstance**, poderá solicitar um ponteiro de interface **IUnknown** e, em seguida, chamar **IUnknown:: QueryInterface** para solicitar todas as interfaces necessárias. No entanto, essa abordagem não é conveniente se você precisar apenas de uma interface única, e ela não funcionará se você usar um método de criação de objeto que não permita que você especifique qual ponteiro de interface deve ser retornado. Na prática, normalmente você não precisa obter um ponteiro **IUnknown** explícito, pois todas as interfaces com estendem a interface **IUnknown** .

Estender uma interface é conceitualmente semelhante à herança de uma classe C++. A interface filho expõe todos os métodos da interface pai, além de um ou mais de seus próprios. Na verdade, você verá com frequência "herda de" usado em vez de "extends". O que você precisa lembrar é que a herança é interna ao objeto. Seu aplicativo não pode herdar de ou estender a interface de um objeto. No entanto, você pode usar a interface filho para chamar qualquer um dos métodos do filho ou pai.

Como todas as interfaces são filhas de **IUnknown**, você pode chamar **QueryInterface** em qualquer um dos ponteiros de interface que você já tem para o objeto. Ao fazer isso, você deve fornecer o IID da interface que você está solicitando e o endereço de um ponteiro que conterá o ponteiro de interface quando o método retornar.

Por exemplo, o fragmento de código a seguir chama **IDXGIFactory2:: CreateSwapChainForHwnd** para criar um objeto de cadeia de permuta primário. Esse objeto expõe várias interfaces. O método **CreateSwapChainForHwnd** retorna uma interface **IDXGISwapChain1** . Em seguida, o código subsequente usa a interface **IDXGISwapChain1** para chamar **QueryInterface** para solicitar uma interface **IDXGISwapChain3** .

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;
```

> [!NOTE]
> Em C++, você pode fazer uso da ``IID_PPV_ARGS`` macro em vez do IID explícito e do ponteiro de conversão: ``pDXGISwapChain1->QueryInterface(IID_PPV_ARGS(&pDXGISwapChain3));`` .
> Isso geralmente é usado para métodos de criação, bem como para **QueryInterface**. Consulte [combaseapi. h](/windows/win32/api/combaseapi/nf-combaseapi-iid_ppv_args) para obter mais informações.

## <a name="managing-a-com-objects-lifetime"></a>Gerenciando o tempo de vida de um objeto COM

Quando um objeto é criado, o sistema aloca os recursos de memória necessários. Quando um objeto não for mais necessário, ele deverá ser destruído. O sistema pode usar essa memória para outras finalidades. Com objetos C++, você pode controlar o tempo de vida do objeto diretamente com os `new` `delete` operadores e nos casos em que você está operando nesse nível ou apenas usando a pilha e o tempo de vida do escopo. O COM não permite que você crie ou destrua objetos diretamente. O motivo para esse design é que o mesmo objeto pode ser usado por mais de uma parte do seu aplicativo ou, em alguns casos, por mais de um aplicativo. Se uma dessas referências fosse destruir o objeto, as outras referências se tornarão inválidas. Em vez disso, COM usa um sistema de contagem de referência para controlar o tempo de vida de um objeto.

A contagem de referência de um objeto é o número de vezes que uma de suas interfaces foi solicitada. Cada vez que uma interface é solicitada, a contagem de referência é incrementada. Um aplicativo libera uma interface quando essa interface não é mais necessária, decrementando a contagem de referência. Desde que a contagem de referência seja maior que zero, o objeto permanecerá na memória. Quando a contagem de referência chega a zero, o objeto se destrói. Você não precisa saber nada sobre a contagem de referência de um objeto. Desde que você obtenha e libere as interfaces de um objeto corretamente, o objeto terá o tempo de vida apropriado.

Lidar corretamente com a contagem de referência é uma parte crucial da programação COM. A falha em fazer isso pode criar facilmente um vazamento de memória ou uma falha. Um dos erros mais comuns que os programadores do COM faz é falhar ao liberar uma interface. Quando isso acontece, a contagem de referência nunca chega a zero e o objeto permanece na memória indefinidamente.

> [!NOTE]
> O Direct3D 10 ou posterior tem regras de tempo de vida ligeiramente modificadas para objetos. Em particular, os objetos que derivam de **ID3DxxDeviceChild** nunca sobreviver Alémm seu dispositivo pai (ou seja, se o **ID3DxxDevice** proprietário chegar a 0 Refcount, todos os objetos filho também serão inválidos imediatamente). Além disso, quando você usa métodos **set** para associar objetos ao pipeline de renderização, essas referências não aumentam a contagem de referência (ou seja, são referências fracas). Na prática, isso é melhor tratado ao garantir que você libere todos os objetos filho do dispositivo completamente antes de liberar o dispositivo.

## <a name="incrementing-and-decrementing-the-reference-count"></a>Incrementando e decrementando a contagem de referência

Sempre que você obtém um novo ponteiro de interface, a contagem de referência deve ser incrementada por uma chamada para [**IUnknown:: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref). No entanto, o aplicativo geralmente não precisa chamar esse método. Se você obtiver um ponteiro de interface chamando um método de criação de objeto ou chamando **IUnknown:: QueryInterface**, o objeto incrementará automaticamente a contagem de referência. No entanto, se você criar um ponteiro de interface de alguma outra forma, como copiar um ponteiro existente, deverá chamar explicitamente **IUnknown:: AddRef**. Caso contrário, quando você liberar o ponteiro de interface original, o objeto poderá ser destruído, mesmo que ainda seja necessário usar a cópia do ponteiro.

Você deve liberar todos os ponteiros de interface, independentemente se você ou o objeto incrementou a contagem de referência. Quando você não precisar mais de um ponteiro de interface, chame [**IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) para diminuir a contagem de referência. Uma prática comum é inicializar todos os ponteiros de interface para `nullptr` e, em seguida, defini-los de volta para `nullptr` quando eles são liberados. Essa Convenção permite testar todos os ponteiros de interface em seu código de limpeza. Aqueles que ainda não `nullptr` estão ativos, e você precisa liberá-los antes de encerrar o aplicativo.

O fragmento de código a seguir estende o exemplo mostrado anteriormente para ilustrar como tratar a contagem de referência.

```cpp
HRESULT hr = S_OK;

IDXGISwapChain1 * pDXGISwapChain1 = nullptr;
hr = pIDXGIFactory->CreateSwapChainForHwnd(
    pCommandQueue, // For D3D12, this is a pointer to a direct command queue.
    hWnd,
    &swapChainDesc,
    nullptr,
    nullptr,
    &pDXGISwapChain1));
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3 = nullptr;
hr = pDXGISwapChain1->QueryInterface(IID_IDXGISwapChain3, (LPVOID*)&pDXGISwapChain3);
if (FAILED(hr)) return hr;

IDXGISwapChain3 * pDXGISwapChain3Copy = nullptr;

// Make a copy of the IDXGISwapChain3 interface pointer.
// Call AddRef to increment the reference count and to ensure that
// the object is not destroyed prematurely.
pDXGISwapChain3Copy = pDXGISwapChain3;
pDXGISwapChain3Copy->AddRef();
...
// Cleanup code. Check to see whether the pointers are still active.
// If they are, then call Release to release the interface.
if (pDXGISwapChain1 != nullptr)
{
    pDXGISwapChain1->Release();
    pDXGISwapChain1 = nullptr;
}
if (pDXGISwapChain3 != nullptr)
{
    pDXGISwapChain3->Release();
    pDXGISwapChain3 = nullptr;
}
if (pDXGISwapChain3Copy != nullptr)
{
    pDXGISwapChain3Copy->Release();
    pDXGISwapChain3Copy = nullptr;
}
```

## <a name="com-smart-pointers"></a>Ponteiros inteligentes COM

O código até agora foi chamado explicitamente ``Release`` e ``AddRef`` para manter as contagens de referência usando métodos **IUnknown** . Esse padrão exige que o programador seja cuidadoso para se lembrar de manter a contagem corretamente em todos os caminhos possíveis. Isso pode resultar em tratamento de erros complicado, e com a manipulação de exceção do C++ habilitada pode ser particularmente difícil de implementar. Uma solução melhor com o C++ é usar um [ponteiro inteligente](/cpp/cpp/smart-pointers-modern-cpp).

* **winrt:: com_ptr** é um ponteiro inteligente fornecido pelas [projeções de linguagem C++/WinRT](/uwp/cpp-ref-for-winrt/com-ptr). Este é o ponteiro inteligente COM recomendado a ser usado para aplicativos UWP. Observe que C++/WinRT requer C++ 17.

* **Microsoft:: WRL:: ComPtr** é um ponteiro inteligente fornecido pela [Windows Runtime biblioteca de modelos do C++ (WRL)](/cpp/cppcx/wrl/comptr-class). Essa biblioteca é "pura" C++ para que possa ser utilizada para aplicativos Windows Runtime (via C++/CX ou C++/WinRT), bem como aplicativos de área de trabalho Win32 clássicos. Esse ponteiro inteligente também funciona em versões anteriores do Windows que não dão suporte às APIs de Windows Runtime. Para aplicativos de área de trabalho Win32, você pode usar ``#include <wrl/client.h>`` para incluir apenas essa classe e, opcionalmente, definir o símbolo de pré-processador ``__WRL_CLASSIC_COM_STRICT__`` também. Para obter mais informações, consulte [apontadores inteligentes com revisitados](/archive/msdn-magazine/2015/february/windows-with-c-com-smart-pointers-revisited).

* **CComPtr** é um ponteiro inteligente fornecido pelo [Active Template Library (ATL)](/cpp/atl/reference/ccomptr-class). O **Microsoft:: WRL:: ComPtr** é uma versão mais recente dessa implementação que aborda vários problemas de uso sutis, portanto, o uso desse ponteiro inteligente não é recomendado para novos projetos. Para obter mais informações, consulte [como criar e usar CComPtr e CComQIPtr](/cpp/cpp/how-to-create-and-use-ccomptr-and-ccomqiptr-instances).


## <a name="using-atl-with-directx-9"></a>Usando a ATL com o DirectX 9

Para usar o Active Template Library (ATL) com o DirectX 9, você deve redefinir as interfaces para compatibilidade com ATL. Isso permite que você use corretamente a classe **CComQIPtr** para obter um ponteiro para uma interface.

Você saberá se não redefinir as interfaces para ATL, porque verá a seguinte mensagem de erro.

```
[...]\atlmfc\include\atlbase.h(4704) :   error C2787: 'IDirectXFileData' : no GUID has been associated with this object
```

O exemplo de código a seguir mostra como definir a interface IDirectXFileData.

```cpp
// Explicit declaration
struct __declspec(uuid("{3D82AB44-62DA-11CF-AB39-0020AF71E433}")) IDirectXFileData;

// Macro method
#define RT_IID(iid_, name_) struct __declspec(uuid(iid_)) name_
RT_IID("{1DD9E8DA-1C77-4D40-B0CF-98FEFDFF9512}", IDirectXFileData);
```

Depois de redefinir a interface, você deve usar o método **Attach** para anexar a interface ao ponteiro de interface retornado por **::D irect3dcreate9**. Caso contrário, a interface **IDirect3D9** não será liberada corretamente pela classe de ponteiro inteligente.

A classe **CComPtr** internamente chama **IUnknown:: AddRef** no ponteiro de interface quando o objeto é criado e quando uma interface é atribuída à classe **CComPtr** . Para evitar o vazamento do ponteiro de interface, não chame * * IUnknown:: AddRef na interface retornada de **::D irect3dcreate9**.

O código a seguir libera corretamente a interface sem chamar **IUnknown:: AddRef**.

```cpp
CComPtr<IDirect3D9> d3d;
d3d.Attach(::Direct3DCreate9(D3D_SDK_VERSION));
```

Use o código anterior. Não use o código a seguir, que chama **IUnknown:: AddRef** seguido por **IUnknown:: Release** e não libera a referência adicionada por **::D irect3dcreate9**.

```cpp
CComPtr<IDirect3D9> d3d = ::Direct3DCreate9(D3D_SDK_VERSION);
```

Observe que esse é o único lugar no Direct3D 9, no qual você terá que usar o método **Attach** dessa maneira.

Para obter mais informações sobre as classes **CComPTR** e **CComQIPtr** , consulte suas definições no `Atlbase.h` arquivo de cabeçalho.
