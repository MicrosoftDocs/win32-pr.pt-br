---
title: Barreiras de UAV e barreiras de estado de recursos no DirectML
description: Descreve os benefícios de correção das barreiras e como você pode trabalhar com elas no DirectML.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 9bfc93d4fb28cff5d7d196287c6573e3e494d1d5
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548255"
---
# <a name="uav-barriers-and-resource-state-barriers-in-directml"></a>Barreiras de UAV e barreiras de estado de recursos no DirectML

## <a name="unordered-access-view-uav-barrier-requirements"></a>Requisitos de barreira de UAV (exibição de acesso não ordenado)

### <a name="uav-barriers-in-direct3d-12"></a>Barreiras de UAV no Direct3D 12

No Direct3D 12, os despachos de sombreador de computação adjacentes na mesma lista de comandos têm permissão para serem executados em paralelo na GPU, a menos que sejam sincronizados com uma barreira de UAV (exibição de acesso não ordenado) intermediária. Isso pode melhorar o desempenho aumentando a utilização do hardware de GPU. No entanto, por padrão, sem o uso de uma barreira UAV, a execução paralela de dois expedimentos adjacentes poderá causar uma condição de corrida se existir uma dependência de dados entre os dois despachos; ou se ambos os despachos executam gravações UAV nas mesmas regiões de memória.

Uma barreira UAV força todos os despachos enviados anteriormente para concluir o execução na GPU antes que os despachos subsequentes possam começar. As barreiras de UAV são usadas para sincronizar entre expatches na mesma lista de comandos para evitar corridas de dados. Você pode emitir uma barreira UAV usando o método [ **ID3D12GraphicsCommandList:: ResourceBarrier**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier).

### <a name="uav-barriers-in-directml"></a>UAV barreiras no DirectML

No DirectML, os operadores são expedidos de uma maneira semelhante à forma como os sombreadores de computação são expedidos no Direct3D 12. Ou seja, os expedimentos adjacentes de operadores têm permissão para serem executados em paralelo na GPU, a menos que exista uma barreira de UAV intermediária entre eles. Um modelo de aprendizado de máquina típico contém dependências de dados entre seus operadores; por exemplo, a saída de um operador alimenta a entrada de outro. Portanto, é importante usar barreiras UAV para sincronizar os expedimentos corretamente.

O DirectML garante que ele nunca lerá (e nunca gravará) os tempos de entrada. Ele também garante que nunca fabricará gravações para um tensor de saída fora do intervalo do membro [**DML_BUFFER_TENSOR_DESC:: TotalTensorSizeInBytes**](/windows/desktop/api/directml/ns-directml-dml_buffer_tensor_desc) do tensor. Isso significa que as dependências de dados entre operadores em DirectML podem ser geradas observando apenas as associações de entrada e saída de um operador.

Por exemplo, essas garantias permitem que você despache dois operadores que associam a mesma região de um recurso como uma entrada, sem a necessidade de emitir uma barreira de UAV intermediária. Isso é sempre seguro porque DirectML nunca grava em dezenases de entrada. Como outro exemplo, é sempre seguro associar os tempos de saída de dois despachos de operador simultâneos ao mesmo recurso do Direct3D 12 (desde que seus grandes prazos não se sobreponham), porque DirectML nunca grava fora dos limites de um tensor (conforme definido pelo DML_BUFFER_TENSOR_DESC da tensor **:: TotalTensorSizeInBytes**).

Como as barreiras de UAV são uma forma de sincronização, o uso desnecessário de barreiras de UAV pode afetar negativamente o desempenho. Portanto, é melhor usar o número mínimo de barreiras UAV necessárias para sincronizar corretamente os despachos dentro de uma lista de comandos.

### <a name="example-1"></a>Exemplo 1

No exemplo a seguir, a saída de um operador de convolução é inserida em uma ativação do ReLU, seguida por uma normalização do lote.

```console
    CONVOLUTION (conv1)
         |
  ACTIVATION_RELU (relu1)
         |
BATCH_NORMALIZATION (batch1)
```

Como existe uma dependência de dados entre todos os três operadores, você precisará de uma barreira UAV entre cada expedição sucessiva (consulte [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch)).

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barreira UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**relu1**`)`
4. `d3d12CommandList->ResourceBarrier(`**Barreira UAV**`)`
5. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**batch1**`)`

### <a name="example-2"></a>Exemplo 2

```console
     MAX_POOLING (pool1)
        /    \
CONVOLUTION  CONVOLUTION
  (conv1)      (conv2)
        \    /
         JOIN (join1)
```

Aqui, a saída do pooling é inserida em duas convolução, cujas saídas são concatenadas em conjunto usando o operador JOIN. Existe uma dependência de dados entre `pool1` e `conv1` e `conv2` ; bem como entre `conv1` e `conv2` e e `join1` . Aqui está uma maneira válida de executar esse grafo.

1. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**pool1**`)`
2. `d3d12CommandList->ResourceBarrier(`**Barreira UAV**`)`
3. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv1**`)`
4. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**conv2**`)`
5. `d3d12CommandList->ResourceBarrier(`**Barreira UAV**`)`
6. `dmlCommandRecorder->RecordDispatch(d3d12CommandList, `**join1**`)`

Nesse caso, `conv1` e `conv2` são capazes de executar simultaneamente na GPU, o que pode melhorar o desempenho.

## <a name="resource-barrier-state-requirements"></a>Requisitos de estado de barreira de recurso

Como o chamador, é sua responsabilidade garantir que todos os recursos do Direct3D 12 estejam no estado de barreira do recurso correto antes de executar expedimentos do DirectML na GPU. O DirectML não realiza nenhuma barreiras de transição em seu nome.

Antes da execução de [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) na GPU, você deve fazer a transição de todos os recursos associados para o estado **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** ou para um estado implicitamente passível de promoção para **D3D12_RESOURCE_STATE_UNORDERED_ACCESS**, como **D3D12_RESOURCE_STATE_COMMON**. Depois que essa chamada for concluída, os recursos permanecerão no estado de **D3D12_RESOURCE_STATE_UNORDERED_ACCESS** . Para obter mais detalhes, consulte [Binding in DirectML](dml-binding.md).

## <a name="see-also"></a>Confira também

* [Usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)
* [Associação no DirectML](dml-binding.md)
