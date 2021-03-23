---
title: Associação no DirectML
description: No DirectML, a associação refere-se ao anexo de recursos para o pipeline a ser usado pela GPU durante a inicialização e execução de seus operadores de aprendizado de máquina.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: a04bf0bcc63fff810604e3db72fe507cc10040f5
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104548254"
---
# <a name="binding-in-directml"></a>Associação no DirectML

No DirectML, a *Associação* refere-se ao anexo de recursos para o pipeline a ser usado pela GPU durante a inicialização e execução de seus operadores de aprendizado de máquina. Esses recursos podem ser tempos de entrada e de saída, por exemplo, bem como quaisquer recursos temporários ou persistentes que o operador precisa.

Este tópico aborda os detalhes conceituais e de procedimento de Binding. Recomendamos que você também leia por completo a documentação das APIs que chama, incluindo os parâmetros e comentários.

## <a name="important-ideas-in-binding"></a>Ideias importantes na associação

A lista de etapas abaixo contém uma descrição de alto nível das tarefas relacionadas à associação. Você precisa seguir estas etapas sempre que você [executar um expatchable](/windows/desktop/api/directml/nn-directml-idmldispatchable)um que pode ser expedivel &mdash; é um inicializador de operador ou um operador compilado. Essas etapas apresentam as ideias, estruturas e métodos importantes envolvidos na associação DirectML.

As seções subsequentes neste tópico se aprofundam e explicam essas tarefas de vinculação com mais detalhes, com trechos de código ilustrativos extraídos do exemplo de código de [aplicativo DirectML mínimo](dml-min-app.md) .

- Chame [**IDMLDispatchable:: Getbindproperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) no expedible para determinar quantos descritores ele precisa e também suas necessidades de recursos temporário/persistente.
- Crie um heap de descritor do Direct3D 12 grande o suficiente para os descritores e associe-o ao pipeline.
- Chame [**IDMLDevice:: Createbindtable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) para criar uma tabela de associação DirectML para representar os recursos associados ao pipeline. Use a estrutura [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) para descrever sua tabela de associação, incluindo o subconjunto dos descritores que aponta para o heap do descritor.
- Crie recursos temporários/persistentes como recursos de buffer do Direct3D 12, descreva-os com estruturas [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) e [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) e adicione-os à tabela de associação.
- Se o expatchable for um operador compilado, crie um buffer de elementos tensor como um recurso de buffer do Direct3D 12. Preencha/carregue-o, descreva-o com estruturas **DML_BUFFER_BINDING** e **DML_BINDING_DESC** e adicione-o à tabela de associação.
- Passe sua tabela de associação como um parâmetro ao chamar [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

## <a name="retrieve-the-binding-properties-of-a-dispatchable"></a>Recuperar as propriedades de associação de um impedible

A estrutura de [**DML_BINDING_PROPERTIES**](/windows/desktop/api/directml/ns-directml-dml_binding_properties) descreve as necessidades de associação de um expatchable (inicializador de operador ou operador compilado). Essas propriedades relacionadas à associação incluem o número de descritores que você deve associar ao expatchable, bem como o tamanho em bytes de qualquer recurso temporário e/ou persistente necessário.

> [!NOTE]
> Mesmo para vários operadores do mesmo tipo, não faça suposições sobre eles com os mesmos requisitos de ligação. Consulte as propriedades de associação para cada inicializador e operador que você criar.

Chame [**IDMLDispatchable:: Getbindproperties**](/windows/desktop/api/directml/nf-directml-idmldispatchable-getbindingproperties) para recuperar um **DML_BINDING_PROPERTIES**.

```cppwinrt
winrt::com_ptr<::IDMLCompiledOperator> dmlCompiledOperator;
// Code to create and compile a DirectML operator goes here.

DML_BINDING_PROPERTIES executeDmlBindingProperties{
    dmlCompiledOperator->GetBindingProperties()
};

winrt::com_ptr<::IDMLOperatorInitializer> dmlOperatorInitializer;
// Code to create a DirectML operator initializer goes here.

DML_BINDING_PROPERTIES initializeDmlBindingProperties{
    dmlOperatorInitializer->GetBindingProperties()
};

UINT descriptorCount = ...
```

O `descriptorCount` valor que você recupera aqui determina o tamanho (mínimo) do heap do descritor e da tabela de associação que você cria nas próximas duas etapas.

**DML_BINDING_PROPERTIES** também contém um `TemporaryResourceSize` membro, que é o tamanho mínimo em bytes do recurso temporário que deve ser associado à tabela de associação para esse objeto que pode ser expedido. Um valor de zero significa que um recurso temporário não é necessário.

E um `PersistentResourceSize` membro, que é o tamanho mínimo em bytes do recurso persistente que deve ser associado à tabela de associação para esse objeto que pode ser expedido. Um valor de zero significa que um recurso persistente não é necessário. Um recurso persistente, se for necessário, deve ser fornecido durante a inicialização de um operador compilado (onde está associado como uma saída do inicializador do operador), bem como durante a execução. Há mais informações sobre isso posteriormente neste tópico. Somente operadores compilados têm recursos persistentes – inicializadores de operador sempre retornam um valor de 0 para esse membro.

Se você chamar **IDMLDispatchable:: Getbindproperties** em um inicializador de operador antes e depois de uma chamada para [**IDMLOperatorInitializer:: Reset**](/windows/desktop/api/directml/nf-directml-idmloperatorinitializer-reset), os dois conjuntos de propriedades de associação recuperados não terão a garantia de serem idênticos.

## <a name="describe-create-and-bind-a-descriptor-heap"></a>Descrever, criar e associar um heap de descritor

Em termos de descritores, sua responsabilidade começa e termina com o próprio heap de descritor. O próprio DirectML cuida da criação e do gerenciamento dos descritores dentro do heap que você fornece.

Portanto, use uma estrutura de [**D3D12_DESCRIPTOR_HEAP_DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_heap_desc) para descrever um heap grande o suficiente para o número de descritores que o expedible precisa. Em seguida, crie-o com [**ID3D12Device:: CreateDescriptorHeap**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createdescriptorheap). E, por fim, chame [**ID3D12GraphicsCommandList:: SetDescriptorHeaps**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps) para associar o heap de descritor ao pipeline.

```cppwinrt
winrt::com_ptr<::ID3D12DescriptorHeap> d3D12DescriptorHeap;

D3D12_DESCRIPTOR_HEAP_DESC descriptorHeapDescription{};
descriptorHeapDescription.Type = D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV;
descriptorHeapDescription.NumDescriptors = descriptorCount;
descriptorHeapDescription.Flags = D3D12_DESCRIPTOR_HEAP_FLAG_SHADER_VISIBLE;

winrt::check_hresult(
    d3D12Device->CreateDescriptorHeap(
        &descriptorHeapDescription,
        _uuidof(d3D12DescriptorHeap),
        d3D12DescriptorHeap.put_void()
    )
);

std::array<ID3D12DescriptorHeap*, 1> d3D12DescriptorHeaps{ d3D12DescriptorHeap.get() };
d3D12GraphicsCommandList->SetDescriptorHeaps(
    static_cast<UINT>(d3D12DescriptorHeaps.size()),
    d3D12DescriptorHeaps.data()
);
```

## <a name="describe-and-create-a-binding-table"></a>Descrever e criar uma tabela de associação

Uma tabela de associação DirectML representa os recursos que você associa ao pipeline para que um seja impedido de usar. Esses recursos podem ser de entrada e de saída (ou outros parâmetros) para um operador, ou podem ser vários recursos persistentes e temporários com os quais um impedible funciona.

Use a estrutura [**DML_BINDING_TABLE_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_table_desc) para descrever sua tabela de associação, incluindo o expatchable para o qual a tabela de associação representará as associações e o intervalo de descritores (do heap de descrição que você acabou de criar) ao qual você deseja que a tabela de associação se refira (e em que DirectML pode gravar descritores). O `descriptorCount` valor (uma das propriedades de associação que recuperamos na primeira etapa) nos informa qual tamanho mínimo é, em descritores, da tabela de associação necessária para o objeto que pode ser expedido. Aqui, usamos esse valor para indicar o número máximo de descritores que o DirectML tem permissão para gravar em nosso heap, desde o início dos identificadores de CPU e de descritores de GPU fornecidos.

Em seguida, chame [**IDMLDevice:: Createbindtable**](/windows/desktop/api/directml/nf-directml-idmldevice-createbindingtable) para criar a tabela de associação DirectML. Em etapas posteriores, depois de criarmos outros recursos para o que pode ser expedido, adicionaremos esses recursos à tabela de associação.

Em vez de passar um **DML_BINDING_TABLE_DESC** para essa chamada, você pode passar `nullptr` , indicando uma tabela de associação vazia.

```cppwinrt
DML_BINDING_TABLE_DESC dmlBindingTableDesc{};
dmlBindingTableDesc.Dispatchable = dmlOperatorInitializer.get();
dmlBindingTableDesc.CPUDescriptorHandle = d3D12DescriptorHeap->GetCPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.GPUDescriptorHandle = d3D12DescriptorHeap->GetGPUDescriptorHandleForHeapStart();
dmlBindingTableDesc.SizeInDescriptors = descriptorCount;

winrt::com_ptr<::IDMLBindingTable> dmlBindingTable;
winrt::check_hresult(
    dmlDevice->CreateBindingTable(
        &dmlBindingTableDesc,
        __uuidof(dmlBindingTable),
        dmlBindingTable.put_void()
    )
);
```

A ordem na qual o DirectML grava os descritores no heap não é especificado, de modo que seu aplicativo deve tomar cuidado para não substituir os descritores encapsulados pela tabela de associação. Os identificadores de CPU e de descritores de GPU fornecidos podem vir de heaps diferentes. no entanto, é responsabilidade do seu aplicativo garantir que todo o intervalo de descritores referido pelo identificador do descritor de CPU seja copiado para o intervalo referido pelo identificador do descritor de GPU antes da execução usando essa tabela de associação. O heap de descritor do qual os identificadores são fornecidos deve ter o tipo **D3D12_DESCRIPTOR_HEAP_TYPE_CBV_SRV_UAV**. Além disso, o heap referido pelo `GPUDescriptorHandle` deve ser um heap de descritor visível para sombreador.

Você pode redefinir uma tabela de associação para remover todos os recursos que você adicionou a ela, enquanto, ao mesmo tempo, altera qualquer propriedade definida em seu **DML_BINDING_TABLE_DESC** inicial (para encapsular um novo intervalo de descritores ou para reutilizá-lo para um distribuidor diferente). Basta fazer as alterações na estrutura de descrição e chamar [**IDMLBindingTable:: Reset**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-reset).

```cppwinrt
dmlBindingTableDesc.Dispatchable = pIDMLCompiledOperator.get();

winrt::check_hresult(
    pIDMLBindingTable->Reset(
        &dmlBindingTableDesc
    )
);
```

## <a name="describe-and-bind-any-temporarypersistent-resources"></a>Descrever e associar qualquer recurso temporário/persistente

A estrutura de **DML_BINDING_PROPERTIES** que populamos quando [recuperamos as propriedades de associação](#retrieve-the-binding-properties-of-a-dispatchable) de nosso expedible contém o tamanho em bytes de qualquer recurso temporário e/ou persistente que o expedible precisa. Se um desses tamanhos for diferente de zero, crie um recurso de buffer do Direct3D 12 e adicione-o à tabela de associação.

No exemplo de código abaixo, criamos um recurso temporário ( `temporaryResourceSize` bytes de tamanho) para o que pode ser expedido. Descrevemos como desejamos associar o recurso e, em seguida, adicionamos essa associação à tabela de associação.

Como estamos ligando um único recurso de buffer, descrevemos nossa associação com uma estrutura de [**DML_BUFFER_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_binding) . Nessa estrutura, especificamos o recurso de buffer do Direct3D 12 (o recurso deve ter a dimensão [**D3D12_RESOURCE_DIMENSION_BUFFER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_dimension)), bem como um deslocamento e um tamanho no buffer. Também é possível descrever uma associação para uma matriz de buffers (em vez de para um único buffer) e a estrutura de [**DML_BUFFER_ARRAY_BINDING**](/windows/desktop/api/directml/ns-directml-dml_buffer_array_binding) existe para essa finalidade.

Para abstrair a distinção entre uma associação de buffer e uma associação de matriz de buffer, usamos a estrutura de  [**DML_BINDING_DESC**](/windows/desktop/api/directml/ns-directml-dml_binding_desc) . Você pode definir o `Type` membro do **DML_BINDING_DESC** como [**DML_BINDING_TYPE_BUFFER**](/windows/desktop/api/directml/ne-directml-dml_binding_type) ou **DML_BINDING_TYPE_BUFFER_ARRAY**. E, em seguida, você pode definir o `Desc` membro para apontar para um **DML_BUFFER_BINDING** ou para um **DML_BUFFER_ARRAY_BINDING**, dependendo de `Type` .

Estamos lidando com o recurso temporário neste exemplo, portanto, o adicionamos à tabela de associação com uma chamada para [**IDMLBindingTable:: BindTemporaryResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindtemporaryresource).

```cppwinrt
D3D12_HEAP_PROPERTIES defaultHeapProperties{ CD3DX12_HEAP_PROPERTIES(D3D12_HEAP_TYPE_DEFAULT) };
winrt::com_ptr<::ID3D12Resource> temporaryBuffer;

D3D12_RESOURCE_DESC temporaryBufferDesc{ CD3DX12_RESOURCE_DESC::Buffer(temporaryResourceSize) };
winrt::check_hresult(
    d3D12Device->CreateCommittedResource(
        &defaultHeapProperties,
        D3D12_HEAP_FLAG_NONE,
        &temporaryBufferDesc,
        D3D12_RESOURCE_STATE_COMMON,
        nullptr,
        __uuidof(temporaryBuffer),
        temporaryBuffer.put_void()
    )
);

DML_BUFFER_BINDING bufferBinding{ temporaryBuffer.get(), 0, temporaryResourceSize };
DML_BINDING_DESC bindingDesc{ DML_BINDING_TYPE_BUFFER, &bufferBinding };
dmlBindingTable->BindTemporaryResource(&bindingDesc);
```

Um recurso temporário (se necessário) é a memória temporária que é usada internamente durante a execução do operador, para que você não precise se preocupar com seu conteúdo. Nem você precisa mantê-lo depois que sua chamada para [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) foi concluída na GPU. Isso significa que seu aplicativo pode liberar ou substituir o recurso temporário entre expatches do operador compilado. O intervalo de buffer fornecido a ser associado como o recurso temporário deve ter seu deslocamento de início alinhado com [**DML_TEMPORARY_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). O tipo do heap subjacente ao buffer deve ser **D3D12_HEAP_TYPE_DEFAULT**.

No entanto, se o expedivel relatar um tamanho diferente de zero para seu recurso persistente de vida mais longa, o procedimento será um pouco diferente. Você deve criar um buffer e descrever uma associação seguindo o mesmo padrão, conforme mostrado acima. Mas adicione-o à tabela de associação do inicializador do operador com uma chamada para [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs), porque é o trabalho do inicializador do operador para inicializar o recurso persistente. Em seguida, adicione-o à tabela de associação do operador compilado com uma chamada para [**IDMLBindingTable:: BindPersistentResource**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindpersistentresource). Consulte o exemplo de código do [aplicativo DirectML mínimo](dml-min-app.md) para ver esse fluxo de trabalho em ação. O conteúdo e o tempo de vida do recurso persistente devem persistir desde que o operador compilado faça. Ou seja, se um operador exigir um recurso persistente, seu aplicativo deverá fornecê-lo durante a inicialização e, posteriormente, também fornecê-lo a todas as futuras realizações do operador sem modificar seu conteúdo. Normalmente, o recurso persistente é usado pelo DirectML para armazenar tabelas de pesquisa ou outros dados de longa duração que são computados durante a inicialização de um operador e reutilizados em execuções futuras desse operador. O intervalo de buffer fornecido a ser associado como o buffer persistente deve ter seu deslocamento de início alinhado com [**DML_PERSISTENT_BUFFER_ALIGNMENT**](./direct3d-directml-constants.md). O tipo do heap subjacente ao buffer deve ser **D3D12_HEAP_TYPE_DEFAULT**.

## <a name="describe-and-bind-any-tensors"></a>Descrever e associar quaisquer tempos

Se você estiver lidando com um operador compilado (em vez de um inicializador de operador), você precisará associar recursos de entrada e saída (para dezenases e outros parâmetros) à tabela de associação do operador. O número de associações deve corresponder exatamente ao número de entradas do operador, incluindo os tempos opcionais. Os tempos de entrada e saída específicos e outros parâmetros que um operador usa são documentados no tópico para esse operador (por exemplo, [**DML_ELEMENT_WISE_IDENTITY_OPERATOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_element_wise_identity_operator_desc)).

Um recurso tensor é um buffer que contém os valores de elemento individuais de tensor. Você carrega e lê esse buffer de/para a GPU usando as técnicas regulares do Direct3D 12 ([carregar recursos](/windows/desktop/direct3d12/uploading-resources) e [ler dados por meio de um buffer](/windows/desktop/direct3d12/readback-data-using-heaps)). Consulte o exemplo de código do [aplicativo DirectML mínimo](dml-min-app.md) para ver essas técnicas em ação.

Por fim, descreva as associações de recursos de entrada e saída com estruturas **DML_BUFFER_BINDING** e **DML_BINDING_DESC** e, em seguida, adicione-as à tabela de associação do operador compilado com chamadas para [**IDMLBindingTable:: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) e [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs). Quando você chama um método **IDMLBindingTable:: \* BIND* _, o DirectML grava um ou mais descritores no intervalo de descritores de CPU.

```cppwinrt
DML_BUFFER_BINDING inputBufferBinding{ inputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC inputBindingDesc{ DML_BINDING_TYPE_BUFFER, &inputBufferBinding };
dmlBindingTable->BindInputs(1, &inputBindingDesc);

DML_BUFFER_BINDING outputBufferBinding{ outputBuffer.get(), 0, tensorBufferSize };
DML_BINDING_DESC outputBindingDesc{ DML_BINDING_TYPE_BUFFER, &outputBufferBinding };
dmlBindingTable->BindOutputs(1, &outputBindingDesc);
```

Uma das etapas na criação de um operador DirectML (consulte [_ *IDMLDevice:: createoperator* *](/windows/desktop/api/directml/nf-directml-idmldevice-createoperator)) é declarar uma ou mais estruturas de [**DML_BUFFER_TENSOR_DESC**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) para descrever os buffers de dados do tensor que o operador usa e retorna. Assim como o tipo e o tamanho do buffer tensor, você pode opcionalmente especificar o sinalizador [**DML_TENSOR_FLAG_OWNED_BY_DML**](/windows/desktop/api/directml/ne-directml-dml_tensor_flags) .

**DML_TENSOR_FLAG_OWNED_BY_DML** indica que os dados de tensor devem ser de propriedade e gerenciados pelo DirectML. O DirectML faz uma cópia dos dados do tensor durante a inicialização do operador e o armazena no recurso persistente. Isso permite que o DirectML realize a reformatação dos dados do tensor para outras formas mais eficientes. Definir esse sinalizador pode aumentar o desempenho, mas geralmente é útil apenas para os dezenases cujos dados não são alterados durante o tempo de vida do operador (por exemplo, tempos de peso). E o sinalizador só pode ser usado em tempos de entrada. Quando o sinalizador é definido em uma descrição tensor específica, o tensor correspondente deve ser associado à tabela de associação durante a inicialização do operador e não durante a execução (o que resultará em um erro). Esse é o oposto do comportamento padrão (o comportamento sem o sinalizador DML_TENSOR_FLAG_OWNED_BY_DML), em que o tensor deve ser associado durante a execução, e não durante a inicialização. Quando você fornece os dados de tensor para um inicializador de operador, é legal associar um UPLOAD em vez de um heap padrão, pois o DirectML faz uma cópia dos dados. Em todos os outros casos, todos os recursos associados a DirectML devem ser recursos de heap padrão.

Para obter mais informações, consulte [**IDMLBindingTable:: BindInputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindinputs) e [**IDMLBindingTable:: BindOutputs**](/windows/desktop/api/directml/nf-directml-idmlbindingtable-bindoutputs).

## <a name="execute-the-dispatchable"></a>Executar o impedible

Passe sua tabela de associação como um parâmetro ao chamar [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch).

Quando você usa a tabela de associação durante uma chamada para **IDMLCommandRecorder:: RecordDispatch**, DirectML associa os descritores de GPU correspondentes ao pipeline. Os identificadores de CPU e de descritores de GPU não precisam apontar para as mesmas entradas em um heap de descritor, no entanto, é responsabilidade do seu aplicativo garantir que todo o intervalo de descritor referido pelo identificador do descritor de CPU seja copiado para o intervalo referido pelo identificador do descritor de GPU antes da execução usando essa tabela de associação.

```cppwinrt
winrt::com_ptr<::ID3D12GraphicsCommandList> d3D12GraphicsCommandList;
// Code to create a Direct3D 12 command list goes here.

winrt::com_ptr<::IDMLCommandRecorder> dmlCommandRecorder;
// Code to create a DirectML command recorder goes here.

dmlCommandRecorder->RecordDispatch(
    d3D12GraphicsCommandList.get(),
    dmlOperatorInitializer.get(),
    dmlBindingTable.get()
);
```

Por fim, feche a lista de comandos do Direct3D 12 e envie-a para execução como faria com qualquer outra lista de comandos.

Antes da execução de **RecordDispatch** na GPU, você deve fazer a transição de todos os recursos associados para o estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** ou para um estado implicitamente passível de promoção para **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, como **D3D12_RESOURCE_STATE_COMMON**. Depois que essa chamada for concluída, os recursos permanecerão no estado de **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . A única exceção a isso é para o carregamento de heaps vinculados ao executar um inicializador de operador e enquanto um ou mais dezenasrs tem o sinalizador de **DML_TENSOR_FLAG_OWNED_BY_DML** definido. Nesse caso, qualquer heap de carregamento associado à entrada deve estar no estado **D3D12_RESOURCE_STATE_GENERIC_READ** e permanecerá nesse estado, conforme exigido por todos os heaps de carregamento. Se **DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE** não foi definido durante a compilação do operador, todas as associações deverão ser definidas na tabela de associação antes de **RecordDispatch** ser chamada, caso contrário, o comportamento será indefinido. Caso contrário, se um operador oferecer suporte à [associação tardia](#optionally-specify-late-bound-operator-bindings), a associação de recursos poderá ser adiada até que a lista de comandos do Direct3D 12 seja enviada para a fila de comandos para execução.

**RecordDispatch** age logicamente como uma chamada para [**ID3D12GraphicsCommandList::D ispatch**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch). Assim, as barreiras de UAV (exibição de acesso não ordenado) são necessárias para garantir a ordenação correta se houver dependências de dados entre expedimentos. Esse método não insere barreiras de UAV em recursos de entrada e saída. Seu aplicativo deve garantir que as barreiras de UAV corretas sejam executadas em qualquer entrada se seu conteúdo depender de um despacho upstream e em qualquer saída se houver despachos downstream que dependem dessas saídas.

## <a name="lifetime-and-synchronization-of-descriptors-and-binding-table"></a>Tempo de vida e sincronização de descritores e tabela de associação

Um bom modelo mental de associação em DirectML é que, por trás dos bastidores, a própria tabela de associação DirectML está criando e gerenciando descritores UAV (modo de exibição de acesso não ordenado) dentro do heap de descritor que você fornece. Portanto, todas as regras comuns do Direct3D 12 se aplicam ao sincronizar o acesso a esse heap e a seus descritores. É responsabilidade do seu aplicativo executar a sincronização correta entre o trabalho de CPU e a GPU que usa uma tabela de associação.

Uma tabela de associação não pode substituir um descritor enquanto o descritor está em uso (por um quadro anterior, por exemplo). Portanto, se você quiser reutilizar um heap de descritor já associado (por exemplo, chamando BIND * novamente em uma tabela de associação que aponta para ele ou substituindo manualmente o heap do descritor), deverá aguardar o Despatch que está usando o heap do descritor para concluir a execução na GPU. Uma tabela de associação não mantém uma referência forte no heap do descritor que ele grava, de modo que você não deve liberar o heap de descritor visível do sombreador até que todo o trabalho que usa essa tabela de associação tenha concluído a execução na GPU.

Por outro lado, enquanto uma tabela de associação especifica e gerencia um heap de descritor, a tabela não *contém* a mesma memória. Portanto, você pode liberar ou redefinir uma tabela de associação a qualquer momento depois de ter chamado [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) com ela (você não precisa esperar que essa chamada seja concluída na GPU, desde que os descritores subjacentes permaneçam válidos).

A tabela de associação não mantém referências fortes em todos os recursos associados usando ti &mdash; seu aplicativo deve garantir que os recursos não sejam excluídos enquanto ainda estiverem em uso pela GPU. Além disso, uma tabela de associação não é thread-safe &mdash; seu aplicativo não deve chamar métodos em uma tabela de associação simultaneamente de threads diferentes sem sincronização.

E considere que, em qualquer caso, a reassociação é necessária somente quando você altera quais recursos estão associados. Se você não precisar alterar os recursos associados, poderá associar uma vez na inicialização e passar a mesma tabela de ligação sempre que chamar **RecordDispatch**.

Para intercalar as cargas de trabalho de aprendizado de máquina e renderização, apenas verifique se as tabelas de associação de cada quadro apontam para os intervalos do heap de descritores que ainda não estão em uso na GPU.

## <a name="optionally-specify-late-bound-operator-bindings"></a>Opcionalmente, especificar associações de operador de associação tardia

Se você estiver lidando com um operador compilado (em vez de um inicializador de operador), terá a opção de especificar a associação tardia para o operador. Sem associação tardia, você deve definir todas as associações na tabela de associação antes de gravar um operador em uma lista de comandos. Com a associação tardia, você pode definir (ou alterar) associações em operadores que você já registrou em uma lista de comandos, antes que ele seja enviado para a fila de comandos.

Para especificar a associação tardia, chame [**IDMLDevice:: CompileOperator**](/windows/win32/api/directml/nf-directml-idmldevice-compileoperator) com um `flags` argumento de [**DML_EXECUTION_FLAG_DESCRIPTORS_VOLATILE**](/windows/desktop/api/directml/ne-directml-dml_execution_flags).