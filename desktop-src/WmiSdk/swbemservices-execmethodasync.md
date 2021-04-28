---
description: SWbemServices.Exemétodo cMethodAsync – executa um método que é exportado por um provedor de método.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethodAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: fcdcd70b567a737cb8686ac841dc1ce0b55d3996
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105584"
---
# <a name="swbemservicesexecmethodasync-method"></a>SWbemServices.Exemétodo cMethodAsync

O método **ExecMethodAsync** do objeto [**SWbemServices**](swbemservices.md) executa um método que é exportado por um provedor de métodos. A chamada retorna imediatamente para o cliente enquanto os parâmetros de entrada são encaminhados para o provedor apropriado onde o método é executado. As informações e o status são retornados ao chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*. O provedor, em vez de Instrumentação de Gerenciamento do Windows (WMI), implementa o método.

O método é chamado no modo assíncrono. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter mais informações e uma explicação sobre essa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* 
</dt> <dd>

Obrigatórios. Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos. Coletor de objeto que recebe o resultado da chamada de método. Os parâmetros de saída são enviados para o evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) do coletor de objeto fornecido. Os resultados do mecanismo de chamada são enviados para o evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) do coletor de objeto fornecido. Lembre-se de que **SWbemSink. OnCompleted** não recebe o código de retorno do método WMI. No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se falhou por motivos mecânicos. O código de resultado retornado do método WMI é retornado no objeto de parâmetro de saída fornecido para **SWbemSink. OnObjectReady**. Se qualquer código de erro for retornado, o objeto [**IWbemObjectSink**](iwbemobjectsink.md) fornecido não será usado. Se a chamada for bem-sucedida, a implementação de **IWbemObjectSink** do usuário será chamada para indicar o resultado da operação.

</dd> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Uma cadeia de caracteres que contém o caminho do objeto para o qual o método é executado. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obrigatórios. O nome do método a ser executado.

</dd> <dt>

*objWbemInParams* \[ adicional\]
</dt> <dd>

Um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que é executado. Por padrão, esse parâmetro é indefinido. Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Inteiro que determina o comportamento da chamada. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus * * * * (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus * * * * (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ adicional\]
</dt> <dd>

Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) . Para obter mais informações, consulte [fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor. Se a chamada for bem-sucedida, um objeto [**Parameters**](swbemmethod-outparameters.md) , que também é um [**SWbemObject**](swbemobject.md) , é fornecido para o coletor especificado em *objWbemSink*. O objeto **Parameters** retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado. Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ExecMethodAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro listados na lista a seguir.

<dl> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidClass** -2147749904 (0x80041010)
</dt> <dd>

A classe especificada não era válida.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrInvalidMethod** -2147749934 (0x8004102E)
</dt> <dd>

O método solicitado não estava disponível.

</dd> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O usuário atual não foi autorizado a executar o método.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se o método executado tiver parâmetros de entrada, o objeto de [**inparâmetros**](swbemmethod-inparameters.md) no parâmetro *objWbemInParam* deverá ser o mesmo que a descrição nos tópicos [construindo objetos de inparâmetros e analisando objetos de subparâmetros](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .

Use **SWbemServices.ExecMethodAsync** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) quando não for possível executar um método diretamente. Por exemplo, use-o com uma linguagem de script que não ofereça suporte a parâmetros de saída, ou seja, se o seu método tiver parâmetros OUT. Caso contrário, é recomendável que você use o acesso direto para invocar um método. Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

O método **cMethodAsyncSWbemServices.Exe** requer um caminho de objeto. Se o script já contiver um objeto [**SWbemObject**](swbemobject.md) , você poderá chamar [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).

Essa chamada retorna imediatamente. As informações de status são retornadas para o chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*. Para continuar o processamento quando a chamada for concluída, implemente uma sub-rotina para o *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor. Isso representa riscos de segurança para seus scripts e aplicativos. Para obter mais informações sobre como eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Use o parâmetro *objWbemAsyncContext* para verificar a origem de uma chamada.

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra o método **ExecMethodAsync** . O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que está executando o bloco de notas. Ele mostra a configuração de um objeto de [**inparâmetros**](swbemmethod-inparameters.md) e como obter resultados de um objeto [**Parameters**](swbemmethod-outparameters.md) . Para um script que mostra as mesmas operações executadas de forma síncrona, consulte [**SWbemServices.ExecMethod**](swbemservices-execmethod.md). Para obter um exemplo de como usar o acesso direto, consulte [criar método na classe \_ processo Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obter um exemplo da mesma operação usando [**SWbemObject**](swbemobject.md), consulte [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMSERVICES CLSID<br/>                                                         |
| IID<br/>                      | ISWbemServices de IID \_<br/>                                                          |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> <dt>

[Chamando um método de provedor](calling-a-provider-method.md)
</dt> <dt>

[Manipulando informações de classe e instância](manipulating-class-and-instance-information.md)
</dt> </dl>

 

