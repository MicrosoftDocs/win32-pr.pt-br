---
title: Ciclo de vida da instância de virtualização
description: Visão geral do ciclo de vida de uma instância de virtualização ProjFS.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/17/2018
ms.topic: article
ms.openlocfilehash: 567eff1f7b8acf330dba7c652e2e12b724072b9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499066"
---
# <a name="virtualization-instance-lifecycle"></a>Ciclo de vida da instância de virtualização

O aplicativo do provedor mantém uma ou mais instâncias de virtualização.  Cada instância de virtualização passa por quatro estágios em seu ciclo de vida:

1. Criação
2. Inicialização
3. Runtime
4. Desligar

Observe que, depois de desligar uma instância de virtualização, o provedor não precisa recriá-la para reutilizá-la.  Ele pode simplesmente iniciá-lo novamente.

> **Observação**: Esta seção mostra exemplos de APIs ProjFS.  Cada exemplo destina-se a ilustrar o uso básico da API.  Para obter a documentação das opções não utilizadas nesses exemplos, consulte a [referência da API do ProjFS](/windows/desktop/api/_projfs).

## <a name="creating-a-virtualization-root"></a>Criando uma raiz de virtualização

Antes que um provedor possa iniciar a instância de virtualização que irá projetar itens no sistema de arquivos local, ele deve criar a raiz de virtualização.  A raiz de virtualização é o diretório no qual o provedor projeta uma árvore de diretórios e arquivos.

Para criar uma raiz de virtualização, o provedor deve:

1. Crie um diretório para servir como a raiz de virtualização.

    O provedor cria um diretório para servir como a raiz de virtualização usando, por exemplo, **[CreateDirectory](/windows/desktop/api/fileapi/nf-fileapi-createdirectoryw)**:

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

    Cada instância de virtualização tem uma ID exclusiva chamada de _ID de instância de virtualização_.  O sistema usa esse valor para identificar a qual instância de virtualização seu conteúdo está associado.

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

O provedor só precisa criar a raiz de virtualização uma vez para cada instância de virtualização.  Depois que uma raiz tiver sido criada, sua instância associada poderá ser iniciada repetidamente e interrompida sem recriar a raiz.

## <a name="starting-a-virtualization-instance"></a>Iniciando uma instância de virtualização

Depois que a raiz de virtualização tiver sido criada, o provedor deverá iniciar a instância de virtualização.  Isso sinaliza ProjFS que o provedor está pronto para receber retornos de chamada e fornecer dados.

Para iniciar a instância de virtualização, o provedor deve:

1. Configure a tabela de retorno de chamada.

    O ProjFS se comunica com o provedor invocando rotinas de retorno de chamada implementadas pelo provedor.  O provedor popula um struct [PRJ_CALLBACKS](/windows/desktop/api/projectedfslib/ns-projectedfslib-prj_callbacks) com ponteiros para suas rotinas de retorno de chamada.

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

1. Inicie a instância.

    O provedor chama **[PrjStartVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstartvirtualizing)** para iniciar a instância de virtualização.

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
    O parâmetro _instanceHandle_ do **PrjStartVirtualizing** retorna um identificador para a instância de virtualização.  O provedor usa esse identificador ao chamar outras APIs ProjFS.

## <a name="virtualization-instance-runtime"></a>Tempo de execução da instância de virtualização

Depois que a chamada para **PrjStartVirtualizing** retorna, ProjFS invocará as rotinas de retorno de chamada do provedor em resposta às operações do sistema de arquivos na instância de virtualização.  Para obter informações sobre como o provedor pode lidar com várias operações do sistema de arquivos, consulte as seguintes seções:

* [Enumerar arquivos e diretórios](enumerating-files-and-directories.md)
* [Fornecer dados de arquivo](providing-file-data.md)
* [Notificações de operação do sistema de arquivos](file-system-operation-notifications.md)
* [Manipulando alterações de exibição](handling-view-changes.md)

## <a name="shutting-down-a-virtualization-instance"></a>Desligando uma instância de virtualização

Para sinalizar ProjFS que o provedor deseja parar de receber retornos de chamada e fornecer dados, o provedor deve parar a instância de virtualização.  Para fazer isso, o provedor chama **[PrjStopVirtualizing](/windows/desktop/api/projectedfslib/nf-projectedfslib-prjstopvirtualizing)**, passando o identificador para a instância de virtualização recebida da chamada para **PrjStartVirtualizing**.

```C++
PrjStopVirtualizing(instanceHandle);
```

Observe que até que essa chamada retorne, ProjFS pode continuar invocando as rotinas de retorno de chamada do provedor.