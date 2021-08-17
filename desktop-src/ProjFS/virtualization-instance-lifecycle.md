---
title: Ciclo de vida da instância de virtualização
description: Visão geral do ciclo de vida de uma instância de virtualização projFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: bbaaf5eca5481f3959e3e5afeb36a8cf6b264c939e8eb2cc9d84ba501d3c8530
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792380"
---
# <a name="virtualization-instance-lifecycle"></a>Ciclo de vida da instância de virtualização

O aplicativo do provedor mantém uma ou mais instâncias de virtualização.  Cada instância de virtualização passa por quatro estágios em seu ciclo de vida:

1. Criação
2. Inicialização
3. Runtime
4. Shutdown

Observe que, depois de desligar uma instância de virtualização, o provedor não precisa reutilizar para reutilizar.  Ele pode simplesmente ino start-lo novamente.

> **Observação:** esta seção mostra exemplos de APIs do ProjFS.  Cada exemplo é destinado a ilustrar o uso básico da API.  Para ver a documentação das opções não usadas nesses exemplos, consulte a referência de [API do ProjFS](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Criando uma raiz de virtualização

Antes que um provedor possa iniciar a instância de virtualização que projetará itens no sistema de arquivos local, ele deve criar a raiz de virtualização.  A raiz de virtualização é o diretório no qual o provedor projeta uma árvore de diretórios e arquivos.

Para criar uma raiz de virtualização, o provedor deve:

1. Crie um diretório para servir como a raiz de virtualização.

    O provedor cria um diretório para servir como a raiz de virtualização usando, por **[exemplo, CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

    ```C++
    HRESULT hr;
    const wchar_t* rootName = LR"(C:\virtRoot)";
    if (!CreateDirectoryW(rootName, nullptr))
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
        wprintf(L"Failed to create virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

1. Crie uma ID de instância de virtualização.

    Cada instância de virtualização tem uma ID exclusiva chamada ID da instância _de virtualização_.  O sistema usa esse valor para identificar a qual instância de virtualização seu conteúdo está associado.

    ```C++
    GUID instanceId;
    hr = CoCreateGuid(&instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to create instance ID (0x%08x)\n", hr);
        return;
    }
    ```

1. Marque o novo diretório como a raiz de virtualização.

    O provedor chama **[PrjMarkDirectoryAsPlaceholder](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjmarkdirectoryasplaceholder)** para marcar o novo diretório como a raiz de virtualização e atribuí-lo à instância de virtualização.

    ```C++
    hr = PrjMarkDirectoryAsPlaceholder(rootName,
                                       nullptr,
                                       nullptr,
                                       &instanceId);
    if (FAILED(hr))
    {
        wprintf(L"Failed to mark virtualization root (0x%08x)\n", hr);
        return;
    }
    ```

O provedor só precisa criar a raiz de virtualização uma vez para cada instância de virtualização.  Depois que uma raiz tiver sido criada, sua instância associada poderá ser iniciada e interrompida repetidamente sem recriar a raiz.

## <a name="starting-a-virtualization-instance"></a>Iniciando uma instância de virtualização

Depois que a raiz de virtualização tiver sido criada, o provedor deverá iniciar a instância de virtualização.  Isso sinaliza ao ProjFS que o provedor está pronto para receber retornos de chamada e fornecer dados.

Para iniciar a instância de virtualização, o provedor deve:

1. Configurar a tabela de retorno de chamada.

    O ProjFS se comunica com o provedor invocando rotinas de retorno de chamada implementadas pelo provedor.  O provedor popula um [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) struct com ponteiros para suas rotinas de retorno de chamada.

    ```C++
    PRJ_CALLBACKS callbackTable;

    // Supply required callbacks.
    callbackTable.StartDirectoryEnumerationCallback = MyStartEnumCallback;
    callbackTable.EndDirectoryEnumerationCallback = MyEndEnumCallback;
    callbackTable.GetDirectoryEnumerationCallback = MyGetEnumCallback;
    callbackTable.GetPlaceholderInfoCallback = MyGetPlaceholderInfoCallback;
    callbackTable.GetFileDataCallback = MyGetFileDataCallback;

    // The rest of the callbacks are optional.
    callbackTable.QueryFileNameCallback = nullptr;
    callbackTable.NotificationCallback = nullptr;
    callbackTable.CancelCommandCallback = nullptr;
    ```

1. Inicie a instância .

    O provedor chama **[PrjStartVirtualizing para](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** iniciar a instância de virtualização.

    ```C++
    PRJ_NAMESPACE_VIRTUALIZATION_CONTEXT instanceHandle;
    hr = PrjStartVirtualizing(rootName,
                              &callbackTable,
                              nullptr,
                              nullptr,
                              &instanceHandle);
    if (FAILED(hr))
    {
        wprintf(L"Failed to start the virtualization instance (0x%08x)\n", hr);
        return;
    }
    ```
    O parâmetro _instanceHandle_ de **PrjStartVirtualizing** retorna um handle para a instância de virtualização.  O provedor usa esse handle ao chamar outras APIs do ProjFS.

## <a name="virtualization-instance-runtime"></a>Runtime da instância de virtualização

Depois que a chamada para **PrjStartVirtualizing** retornar, o ProjFS invocará as rotinas de retorno de chamada do provedor em resposta às operações do sistema de arquivos na instância de virtualização.  Para obter informações sobre como o provedor pode lidar com várias operações do sistema de arquivos, consulte as seguintes seções:

* [Enumerar arquivos e diretórios](enumerating-files-and-directories.md)
* [Fornecer dados de arquivo](providing-file-data.md)
* [Notificações de operação do sistema de arquivos](file-system-operation-notifications.md)
* [Manipulando alterações de exibição](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Desligando uma instância de virtualização

Para sinalizar ao ProjFS que o provedor deseja parar de receber retornos de chamada e fornecer dados, o provedor deve interromper a instância de virtualização.  Para fazer isso, o provedor chama **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passando-o para a instância de virtualização que ele recebeu da chamada para **PrjStartVirtualizing**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Observe que até que essa chamada retorne, o ProjFS pode continuar a invocar as rotinas de retorno de chamada do provedor.