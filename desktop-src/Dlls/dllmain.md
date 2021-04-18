---
description: Um ponto de entrada opcional em uma DLL (biblioteca de vínculo dinâmico). Quando o sistema inicia ou termina um processo ou thread, ele chama a função de ponto de entrada para cada DLL carregada usando o primeiro thread do processo.
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: Ponto de entrada DllMain (Process. h)
ms.topic: reference
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: ee182fd54f11909e54e98f827904f1da5e46f557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753490"
---
# <a name="dllmain-entry-point"></a>Ponto de entrada DllMain

Um ponto de entrada opcional em uma DLL (biblioteca de vínculo dinâmico). Quando o sistema inicia ou termina um processo ou thread, ele chama a função de ponto de entrada para cada DLL carregada usando o primeiro thread do processo. O sistema também chama a função de ponto de entrada para uma DLL quando ela é carregada ou descarregada usando as funções [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) e [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) .

## <a name="example"></a>Exemplo

```cpp
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

Este é um exemplo da [função Entry-Point da biblioteca de vínculo dinâmico](dynamic-link-library-entry-point-function.md).


> [!WARNING]
> Há limites significativos no que você pode fazer com segurança em um ponto de entrada de DLL. Consulte [práticas recomendadas gerais](dynamic-link-library-best-practices.md) para APIs específicas do Windows que não são seguras para chamar em DllMain. Se você precisar de qualquer coisa, exceto a inicialização mais simples, faça isso em uma função de inicialização para a DLL. Você pode exigir que os aplicativos chamem a função de inicialização após a execução de DllMain e antes de chamar qualquer outra função na DLL.

 

## <a name="syntax"></a>Sintaxe


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*hInstDll* \[ no\]
</dt> <dd>

Um identificador para o módulo de DLL. O valor é o endereço base da DLL. O **HINSTANCE** de uma DLL é o mesmo que o **HMODULE** da dll, portanto, o *hInstDll* pode ser usado em chamadas para funções que exigem um identificador de módulo.

</dd> <dt>

*fdwReason* \[ no\]
</dt> <dd>

O código de motivo que indica por que a função de ponto de entrada de DLL está sendo chamada. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                                                                                | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**Dll \_ PROCESSO \_ anexado**</dt> <dt>1</dt> </dl> | A DLL está sendo carregada no espaço de endereço virtual do processo atual como resultado do processo que está sendo iniciado ou como resultado de uma chamada para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). As DLLs podem usar essa oportunidade para inicializar qualquer dado de instância ou para usar a função [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) para alocar um índice de armazenamento local de thread (TLS).<br/> O parâmetro *lpReserved* indica se a dll está sendo carregada de forma estática ou dinâmica.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**Dll \_ PROCESSO \_ desanexar**</dt> <dt>0</dt> </dl> | A DLL está sendo descarregada do espaço de endereço virtual do processo de chamada porque foi carregada sem êxito ou a contagem de referência atingiu zero (os processos foram encerrados ou chamados [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) uma vez para cada vez que ele chamou [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)).<br/> O parâmetro *lpReserved* indica se a dll está sendo descarregada como resultado de uma chamada [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) , uma falha ao carregar ou processar o encerramento.<br/> A DLL pode usar essa oportunidade para chamar a função [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) para liberar quaisquer índices TLS alocados usando [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) e para liberar quaisquer dados locais de thread.<br/> Observe que o thread que recebe a notificação de **\_ \_ desanexação do processo de dll** não é necessariamente o mesmo thread que recebeu a notificação de **\_ \_ anexação do processo de dll** .<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**Dll \_ \_Anexação de thread**</dt> <dt>2</dt> </dl>    | O processo atual está criando um novo thread. Quando isso ocorre, o sistema chama a função de ponto de entrada de todas as DLLs atualmente anexadas ao processo. A chamada é feita no contexto do novo thread. As DLLs podem usar essa oportunidade para inicializar um slot TLS para o thread. Um thread que chama a função de ponto de entrada de DLL com a **\_ \_ anexação de processo de dll** não chama a função de ponto de entrada de dll com **\_ \_ anexação de thread de dll**. <br/> Observe que a função de ponto de entrada de uma DLL é chamada com esse valor somente por threads criados depois que a DLL é carregada pelo processo. Quando uma DLL é carregada usando [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), os threads existentes não chamam a função de ponto de entrada da DLL carregada recentemente.<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**Dll \_ \_Desanexação de thread**</dt> <dt>3</dt> </dl>    | Um thread está sendo fechado corretamente. Se a DLL tiver armazenado um ponteiro para a memória alocada em um slot TLS, ela deverá usar essa oportunidade para liberar a memória. O sistema chama a função de ponto de entrada de todas as DLLs carregadas atualmente com esse valor. A chamada é feita no contexto do thread existente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvReserved* \[ no\]
</dt> <dd>

Se *fdwReason* for **o \_ processo \_ de dll Attach**, *lpvReserved* será **nulo** para cargas dinâmicas e não nulo para cargas estáticas.

Se *fdwReason* for **o \_ processo \_ de dll Detach**, *lpvReserved* será **nulo** se [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) tiver sido chamado ou o carregamento da DLL tiver falhado e não **nulo** se o processo estiver sendo encerrado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Quando o sistema chamar a função **DllMain** com o valor de **\_ \_ anexação do processo de dll** , a função retornará **true** se for bem-sucedida ou **false** se a inicialização falhar. Se o valor de retorno for **false** quando **DllMain** for chamado porque o processo usa a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) , **LoadLibrary** retornará NULL. (O sistema chama imediatamente sua função de ponto de entrada com o **processo de dll \_ \_ desanexar** e descarrega a dll.) Se o valor de retorno for **falso** quando **DllMain** for chamado durante a inicialização do processo, o processo será encerrado com um erro. Para obter informações de erro estendidas, chame [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Quando o sistema chama a função **DllMain** com qualquer valor diferente de **dll \_ processo \_ Attach**, o valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

**DllMain** é um espaço reservado para o nome da função definida pela biblioteca. Você deve especificar o nome real que você usa ao compilar sua DLL. Para obter mais informações, consulte a documentação incluída com suas ferramentas de desenvolvimento.

Durante a inicialização do processo inicial ou após uma chamada para [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), o sistema verifica a lista de DLLs carregadas para o processo. Para cada DLL que ainda não foi chamada com o valor **de \_ \_ anexação do processo de dll** , o sistema chama a função de ponto de entrada da dll. Essa chamada é feita no contexto do thread que fez com que o espaço de endereço do processo fosse alterado, como o thread principal do processo ou o thread que chamou **LoadLibrary**. O acesso ao ponto de entrada é serializado pelo sistema de acordo com todo o processo. Os threads em *DllMain* mantêm o bloqueio do carregador, portanto, nenhuma dll adicional pode ser carregada ou inicializada dinamicamente.

Se a função de ponto de entrada da DLL retornar FALSE após uma notificação de **\_ \_ anexo de processo de dll** , ela receberá uma notificação de **\_ \_ desanexação de processo de dll** e a dll será descarregada imediatamente. No entanto, se o código de **\_ \_ anexo de processo de dll** lançar uma exceção, a função de ponto de entrada não receberá a notificação de **\_ \_ desanexação do processo de dll** .

Há casos em que a função de ponto de entrada é chamada para um thread de terminação, mesmo que a função de ponto de entrada nunca tenha sido chamada com **\_ \_ anexação de thread de dll** para o thread:

-   O thread era o thread inicial no processo, portanto, o sistema chamou a função de ponto de entrada com o valor de **\_ \_ anexação do processo de dll** .
-   O thread já estava em execução quando uma chamada para a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) foi feita, portanto, o sistema nunca chamou a função de ponto de entrada para ele.

Quando uma DLL é descarregada de um processo como resultado de uma carga malsucedida da DLL, do encerramento do processo ou de uma chamada para [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary), o sistema não chama a função de ponto de entrada da dll com o valor de **\_ \_ desanexação de thread de dll** para os threads individuais do processo. A DLL só é enviada a uma notificação de **\_ \_ desanexação de processo de dll** . As DLLs podem aproveitar essa oportunidade para limpar todos os recursos de todos os threads conhecidos da DLL.

Ao manipular **a \_ \_ desanexação do processo de DLL**, uma DLL deve liberar recursos como a memória heap somente se a dll estiver sendo descarregada dinamicamente (o parâmetro *lpReserved* é **nulo**). Se o processo estiver sendo encerrado (o parâmetro *lpvReserved* é não **nulo**), todos os threads no processo, exceto o thread atual, já foram encerrados ou foram encerrados explicitamente por uma chamada para a função [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) , o que pode deixar alguns recursos de processo, como heaps em um estado inconsistente. Nesse caso, não é seguro para a DLL limpar os recursos. Em vez disso, a DLL deve permitir que o sistema operacional recupere a memória.

Se você encerrar um processo chamando [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) ou [**TerminateJobObject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject), as DLLs desse processo não receberão notificações de **\_ \_ desanexação do processo de dll** . Se você encerrar um thread chamando [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread), as DLLs desse thread não receberão notificações de **\_ \_ desanexação de thread de dll** .

A função de ponto de entrada deve executar apenas tarefas simples de inicialização ou demissão. Ele não deve chamar a função [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) ou [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (ou uma função que chama essas funções), pois isso pode criar loops de dependência na ordem de carregamento da dll. Isso pode resultar na utilização de uma DLL antes que o sistema tenha executado seu código de inicialização. Da mesma forma, a função de ponto de entrada não deve chamar a função [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (ou uma função que chama **FreeLibrary**) durante o encerramento do processo, porque isso pode resultar em uma DLL sendo usada depois que o sistema tiver executado seu código de encerramento.

Como Kernel32.dll é garantido que seja carregado no espaço de endereço do processo quando a função de ponto de entrada é chamada, a chamada de funções no Kernel32.dll não resulta na DLL que está sendo usada antes de seu código de inicialização ser executado. Portanto, a função de ponto de entrada pode chamar funções em Kernel32.dll que não carregam outras DLLs. Por exemplo, *DllMain* pode criar [objetos de sincronização](/windows/desktop/Sync/synchronization-objects) , como seções críticas e mutexes, e usar TLS. Infelizmente, não há uma lista abrangente de funções seguras no Kernel32.dll.

Chamar funções que exigem DLLs diferentes de Kernel32.dll pode resultar em problemas que são difíceis de diagnosticar. Por exemplo, a chamada a funções de usuário, Shell e COM pode causar erros de violação de acesso, pois algumas funções carregam outros componentes do sistema. Por outro lado, chamar funções como essas durante o encerramento pode causar erros de violação de acesso porque o componente correspondente pode já ter sido descarregado ou não inicializado.

Como as notificações de DLL são serializadas, as funções de ponto de entrada não devem tentar se comunicar com outros threads ou processos. Os deadlocks podem ocorrer como resultado.

Para obter informações sobre as práticas recomendadas ao gravar uma DLL, consulte https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices .

Se sua DLL estiver vinculada à biblioteca de tempo de execução C (CRT), o ponto de entrada fornecido pelo CRT chamará os construtores e destruidores para objetos C++ global e estático. Portanto, essas restrições para *DllMain* também se aplicam a construtores e destruidores e a qualquer código que seja chamado a partir deles.

Considere chamar [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) ao receber **a \_ \_ anexação do processo de dll**, a menos que sua dll esteja vinculada a CRT (biblioteca de tempo de execução) estática C.


## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                 |
| parâmetro<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Função de Entry-Point de biblioteca de vínculo dinâmico](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[Funções da biblioteca de vínculo dinâmico](dynamic-link-library-functions.md)
</dt> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[**GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
