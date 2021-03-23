---
title: Tempo de vida e sincronização de recursos
description: Para evitar um comportamento indefinido, seu aplicativo DirectML deve gerenciar corretamente os tempos de vida de objeto e a sincronização entre a CPU e a GPU.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 6e8ab30c5c87c135ef3bdac0c1bc2a3d64040787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103771"
---
# <a name="resource-lifetime-and-synchronization"></a>Tempo de vida e sincronização de recursos

Assim como ocorre com o Direct3D 12, seu aplicativo DirectML deve (para evitar o comportamento indefinido) gerenciar corretamente os tempos de vida de objetos e a sincronização entre a CPU e a GPU. DirectML segue um modelo de tempo de vida de recurso idêntico ao do Direct3D 12.

- As dependências de tempo de vida entre dois objetos de CPU são mantidas pelo DirectML usando contagens de referência forte. Seu aplicativo não é possível gerenciar manualmente dependências de tempo de vida da CPU. Por exemplo, cada dispositivo filho mantém uma referência forte ao seu dispositivo pai.
- As dependências de tempo de vida entre objetos GPU &mdash; ou dependências que abrangem entre CPU e GPU &mdash; não são gerenciadas automaticamente. É responsabilidade do seu aplicativo garantir que os recursos de GPU estejam ao menos até que todo o trabalho usando esse recurso tenha concluído a execução na GPU.

## <a name="directml-devices"></a>Dispositivos DirectML

O dispositivo DirectML é um objeto de fábrica sem monitoração de estado thread-safe. Cada dispositivo filho (consulte [**IDMLDeviceChild**](/windows/desktop/api/directml/nn-directml-idmldevicechild)) mantém uma referência forte ao seu dispositivo DirectML pai (consulte [**IDMLDevice**](/windows/desktop/api/directml/nn-directml-idmldevice)). Isso significa que você sempre pode recuperar a interface do dispositivo pai de qualquer interface filho do dispositivo.

Um dispositivo DirectML, por sua vez, mantém uma referência forte ao dispositivo Direct3D 12 que foi usado para criá-lo (consulte [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)e interfaces derivadas).

Como o dispositivo DirectML é sem monitoração de estado, ele é implicitamente seguro para thread. Você pode chamar métodos no dispositivo DirectML de vários threads simultaneamente sem a necessidade de sincronização externa.

No entanto, ao contrário do dispositivo Direct3D 12, o dispositivo DirectML não é um objeto singleton. Você tem a liberdade de criar quantos dispositivos DirectML desejar. No entanto, você não pode misturar e corresponder a filhos do dispositivo que pertencem a dispositivos diferentes. Por exemplo, [**IDMLBindingTable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) e [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) são dois tipos de filhos de dispositivo (ambas as interfaces derivam direta ou indiretamente do **IDMLDeviceChild**). E você não poderá usar uma tabela de associação (**IDMLBindingTable**) para associar um operador (**IDMLCompiledOperator**) se o operador e a tabela de associação pertencerem a diferentes instâncias de dispositivo DirectML.

Como o dispositivo DirectML não é um singleton, a remoção do dispositivo ocorre em uma base por dispositivo, em vez de ser um evento de todo o processo como é para um dispositivo Direct3D 12. Para obter mais informações, consulte [tratamento de erros e remoção de dispositivo no DirectML](dml-errors.md).

## <a name="lifetime-requirements-of-gpu-resources"></a>Requisitos de tempo de vida de recursos de GPU

Como o Direct3D 12, o DirectML não sincroniza automaticamente entre a CPU e a GPU; nem mantém os recursos ativos automaticamente enquanto eles estão em uso pela GPU. Em vez disso, essas são as responsabilidades de seu aplicativo.

Ao executar uma lista de comandos que contém expedições de DirectML, seu aplicativo deve garantir que os recursos de GPU sejam mantidos ativos até que todo o trabalho que usa esses recursos tenha concluído a execução na GPU.

No caso de [**IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) para um operador DirectML, que inclui os objetos a seguir.

- O [**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) que está sendo executado (ou [**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) em vez disso, se estiver executando a inicialização do operador).
- O **IDMLCompiledOperator** fazendo backup da tabela de associação que está sendo usada para associar o operador.
- Os objetos [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) associados como entradas/saídas do operador.
- Os objetos **ID3D12Resource** associados como recursos persistentes e temporários, se aplicável.
- O [**ID3D12CommandAllocator**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator) fazendo o backup da lista de comandos em si.

Nem todas as interfaces DirectML representam recursos de GPU. Por exemplo, uma tabela de associação *não* precisa ser mantida ativa até que todos os expedimentos que o utilizam tenham concluído a execução na GPU. Isso ocorre porque a própria tabela de associação não possui nenhum recurso de GPU. Em vez disso, o heap de descritor faz. Portanto, o *heap de descritor* subjacente é o objeto que deve ser mantido ativo até que a execução seja concluída e não a própria tabela de associação.

Existe um conceito semelhante no Direct3D 12. Um *alocador* de comando deve ser mantido ativo até que todas as execuções que o utilizam tenham sido concluídas na GPU; Pois ela possui memória de GPU. Mas, uma *lista* de comandos não possui memória de GPU, portanto, ela pode ser redefinida ou liberada assim que foi enviada para execução.

No DirectML, os operadores compilados ([**IDMLCompiledOperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)) e os inicializadores de operador ([**IDMLOperatorInitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)) têm os próprios recursos de GPU diretamente, portanto, eles devem ser mantidos ativos até que todos os despachos que o utilizam tenham concluído a execução na GPU. Além disso, qualquer recurso do Direct3D 12 que está sendo usado (alocadores de comando, heaps de descritores, buffers, como exemplos) deve ser mantido de forma semelhante ao seu aplicativo.

Se você lançar prematuramente um objeto enquanto ele ainda estiver em uso pela GPU, o resultado será um comportamento indefinido, que tem o potencial de causar a remoção do dispositivo ou outros erros.

## <a name="cpu-and-gpu-synchronization"></a>Sincronização de CPU e GPU

O DirectML não envia nenhum trabalho para execução na GPU. Em vez disso, o [método **IDMLCommandRecorder:: RecordDispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) *registra* a expedição desse trabalho em uma lista de comandos para execução posterior. Seu aplicativo deve fechar e enviar sua lista de comandos para execução chamando [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists), como com qualquer lista de comandos do Direct3D 12.

Como o DirectML não envia nenhum trabalho para execução na GPU, ele também não cria nenhum limite nem executa qualquer forma de sincronização de CPU/GPU em seu nome. É responsabilidade do seu aplicativo usar os primitivos do Direct3D 12 apropriados para aguardar o trabalho enviado para concluir a execução na GPU, se necessário. Para obter mais informações, consulte [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) e [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal).

## <a name="see-also"></a>Confira também

* [Executando e sincronizando listas de comandos](/windows/desktop/direct3d12/executing-and-synchronizing-command-lists)
* [Tratamento de erros e remoção de dispositivo no DirectML](dml-errors.md)