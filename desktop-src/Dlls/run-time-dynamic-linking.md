---
description: Quando o aplicativo chama as funções LoadLibrary ou LoadLibraryEx, o sistema tenta localizar a DLL (para obter detalhes, consulte Dynamic-Link ordem de pesquisa da biblioteca).
ms.assetid: 81e237a9-3c32-46a5-88d3-c978f43dad54
title: Run-Time vinculação dinâmica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9e215ac83ecdc0615b8030e2e215857c67fe6e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766920"
---
# <a name="run-time-dynamic-linking"></a>Run-Time vinculação dinâmica

Quando o aplicativo chama as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) , o sistema tenta localizar a dll (para obter detalhes, consulte [ordem de pesquisa da biblioteca de vínculo dinâmico](dynamic-link-library-search-order.md)). Se a pesquisa for bem sucedido, o sistema mapeará o módulo DLL para o espaço de endereço virtual do processo e incrementará a contagem de referência. Se a chamada para **LoadLibrary** ou **LOADLIBRARYEX** especificar uma dll cujo código já esteja mapeado no espaço de endereço virtual do processo de chamada, a função simplesmente retornará um identificador para a dll e incrementará a contagem de referência de dll. Observe que duas DLLs que têm o mesmo nome de arquivo base e extensão, mas que são encontradas em diretórios diferentes, não são consideradas a mesma DLL.

O sistema chama a função de ponto de entrada no contexto do thread que chamou [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). A função de ponto de entrada não será chamada se a DLL já tiver sido carregada pelo processo por meio de uma chamada para **LoadLibrary** ou **LoadLibraryEx** sem nenhuma chamada correspondente à função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

Se o sistema não puder localizar a DLL ou se a função de ponto de entrada retornar FALSE, [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) retornará NULL. Se **LoadLibrary** ou **LoadLibraryEx** tiver sucesso, ele retornará um identificador para o módulo de dll. O processo pode usar esse identificador para identificar a DLL em uma chamada para a função [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)ou [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread) .

A função [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) retorna um identificador usado em [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress), [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)ou [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). A função **GetModuleHandle** só terá sucesso se o módulo DLL já estiver mapeado para o espaço de endereço do processo por vinculação de tempo de carregamento ou por uma chamada anterior para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa). Ao contrário de **LoadLibrary** ou **LoadLibraryEx**, **GetModuleHandle** não incrementa a contagem de referência do módulo. A função [**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) recupera o caminho completo do módulo associado a um identificador retornado por **GetModuleHandle**, **LoadLibrary** ou **LoadLibraryEx**.

O processo pode usar [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) para obter o endereço de uma função exportada na DLL usando um identificador de módulo de dll retornado por [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea).

Quando o módulo DLL não é mais necessário, o processo pode chamar [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) ou [**FreeLibraryAndExitThread**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibraryandexitthread). Essas funções decrementam a contagem de referência de módulo e desmapeam o código de DLL do espaço de endereço virtual do processo se a contagem de referência for zero.

A vinculação dinâmica em tempo de execução permite que o processo continue em execução mesmo se uma DLL não estiver disponível. O processo pode, então, usar um método alternativo para atingir seu objetivo. Por exemplo, se um processo não puder localizar uma DLL, ele poderá tentar usar outra ou poderá notificar o usuário sobre um erro. Se o usuário puder fornecer o caminho completo da DLL ausente, o processo poderá usar essas informações para carregar a DLL, mesmo que ela não esteja no caminho de pesquisa normal. Essa situação contrasta com a vinculação de tempo de carregamento, na qual o sistema simplesmente encerra o processo se não conseguir encontrar a DLL.

A vinculação dinâmica em tempo de execução pode causar problemas se a DLL usa a função [**DllMain**](dllmain.md) para executar a inicialização para cada thread de um processo, porque o ponto de entrada não é chamado para threads que existiam antes de [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) ser chamado. Para obter um exemplo que mostra como lidar com esse problema, consulte [usando o armazenamento local de thread em uma biblioteca de Dynamic-Link](using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando vinculação dinâmica em tempo de execução](using-run-time-dynamic-linking.md)
</dt> </dl>

 

 
