---
description: Assim como acontece com todos os aplicativos, o WMI recebe códigos de erro do sistema operacional Windows.
ms.assetid: f54b8e7c-c531-47d5-bab8-780652b94555
ms.tgt_platform: multiple
title: Recuperando um código de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c42dbd160ef6412c332e2da2c01f6590e10966
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780325"
---
# <a name="retrieving-an-error-code"></a>Recuperando um código de erro

Assim como acontece com todos os aplicativos, o WMI recebe códigos de erro do sistema operacional Windows.

Ao receber um código de erro, você tem as seguintes opções:

-   Examine o log de eventos.

    O WMI envia mensagens de erro para o serviço log de eventos que verifica os logs de eventos para ajudar a determinar a causa de um erro. Você pode usar as classes que o provedor de [log de eventos](/previous-versions/windows/desktop/eventlogprov/event-log-provider) dá suporte para acessar logs de eventos programaticamente.

-   Recupere o código de erro normalmente.

    O WMI dá suporte às técnicas padrão para recuperar códigos de erro, que são códigos de erro COM para C++ e objetos de erro nativos, como o [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85))ou [**SWbemLastError**](swbemlasterror.md) , se o provedor fornecer informações de erro.

Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

As seções a seguir são discutidas neste tópico:

-   [Tratamento de um erro com o VBScript](#handling-an-error-with-vbscript)
-   [Tratando um erro usando C++](#handling-an-error-using-c)

## <a name="handling-an-error-with-vbscript"></a>Tratamento de um erro com o VBScript

Se uma chamada para o WMI por meio da API de script para WMI causar um erro, você terá as seguintes opções para acessar as informações de erro:

-   Use mecanismos de erro nativos da linguagem de script, por exemplo, no VBScript, use o [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) para dar suporte ao tratamento de erros.
-   Crie um objeto [**SWbemLastError**](swbemlasterror.md) para obter um relatório de erros.

O script a seguir mostra o uso do [objeto de erro nativo (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)). Quando um valor incorreto para o identificador de processo é fornecido, um erro é gerado.


```VB
On Error Resume Next
Set objProcess = GetObject( _
    "winmgmts:root\cimv2:Win32_Process.Handle='one'")
Wscript.Echo Err.Number
```



> [!Note]
>
> A propriedade **Description** do [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)) está vazia ao se conectar ao WMI por meio do moniker "winmgmts:". No entanto, se você se conectar usando [**SWbemLocator**](swbemlocator.md), a descrição estará disponível.
>
> A tabela a seguir lista as propriedades de [objeto Err (VBScript)](/previous-versions//sbf5ze0e(v=vs.85)).
>
> 
>
> | Propriedade                   | Contém                                                       |
> |----------------------------|----------------------------------------------------------------|
> | **Descrição**<br/> | Descrição de erro localizada e legível pelo homem.<br/> |
> | **Número**<br/>      | **HRESULT** RETORNADO pela API de script para WMI.<br/>  |
> | **Origem**<br/>      | Identifica o objeto que gerou o erro.<br/>        |
>
> 
>
>  

 

O script a seguir mostra o uso de um objeto [**SWbemLastError**](swbemlasterror.md) para obter informações de erro detalhadas. Observe que nem todos os provedores fornecem informações para **SWbemLastError**. Para obter mais informações sobre códigos de erro no script, consulte [WbemErrorEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemerrorenum).


```VB
On Error Resume Next
Set obj = GetObject("winmgmts:root\cimv2:Win32_Process.Handle='one'")
Set LastError = createobject("wbemscripting.swbemlasterror")
Wscript.Echo "Operation = " & LastError.operation & VBCRLF & "ParameterInfo = " _
            & LastError.ParameterInfo & VBCRLF & "ProviderName = " & LastError.ProviderName
```



## <a name="handling-an-error-using-c"></a>Tratando um erro usando C++

Um aplicativo cliente WMI pode receber erros específicos de COM ou WMI. Os erros de COM estão em conformidade com a estrutura de códigos de erro COM. Todas as interfaces WMI podem retornar um erro específico COM, exceto as interfaces [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext), [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject)e [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) . Para obter mais informações sobre códigos de erro COM, consulte [tratamento de erros](../com/error-handling-in-com.md). As páginas de referência das interfaces WMI listam os códigos de erro WMI apropriados na seção códigos de erro.

Um aplicativo cliente deve seguir os padrões COM para verificar o status e os códigos de retorno de erro. A principal diferença que você deve escolher é se deseja recuperar o código de erro de uma chamada síncrona, semisynchronous ou assíncrona.

**Para acessar mensagens de erro síncronas e semisynchronouss usando C++**

1.  Recupere as informações de erro com uma chamada para a função com [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) .

    Certifique-se de chamar [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) imediatamente após um método de interface indicar um erro. Isso inclui qualquer um dos métodos [**IWbemCallResult**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemcallresult) que você chama ao processar um processo semisynchronous.

2.  Examine o objeto de erro COM retornado com uma chamada para o método [**IErrorInterface:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) .

    Certifique-se de especificar \_ o WbemClassObject de IID para o parâmetro *riid* na chamada [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) . O método **QueryInterface** retorna uma instância de uma classe WMI, normalmente [**\_ \_ ExtendedStatus**](--extendedstatus.md).

O WMI não entrega o objeto de erro por meio do [GetErrorInfo]( /windows/win32/api/oleauto/nf-oleauto-geterrorinfo) para uma chamada assíncrona porque não há como saber quando ou em qual thread a chamada assíncrona ocorreu. Portanto, o código só pode tratar erros específicos ou passar a falha de chamada por meio de COM.

> [!Note]  
> Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

 

**Para acessar mensagens de erro assíncronas usando C++**

-   Recupere o objeto de erro COM de sua implementação de [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus).

    O pseudocódigo a seguir mostra uma implementação típica de tratamento de erros para um aplicativo cliente.

    ```C++
    HRESULT hRes = SomeMethod;

    // Check for specific error and status codes.
    if (hRes == WBEM_E_NOT_FOUND)
    {
    // Processing to handle specific error code
    }
    else if hRes == WBEM_S_DUPLICATE_OBJECTS
    {
    // All other cases, including errors specific to COM
    }
    else if (FAILED(hRes))
    {

    }
    ```

    

 

