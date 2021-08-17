---
description: O método ExecMethodAsync \_ de SWbemObject executa de forma assíncrona um método exportado por um provedor de métodos.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: SWbemObject.ExecMethodAsync_ método (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 37d7a0ab0b2e4d1ab893619eda4b3d32b8b4e1f60791e0981125d4445bda5f98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857346"
---
# <a name="swbemobjectexecmethodasync_-method"></a>SWbemObject.Exemétodo cMethodAsync \_

O **método ExecMethodAsync \_** de [**SWbemObject**](swbemobject.md) executa de forma assíncrona um método exportado por um provedor de métodos. Esse método é semelhante [**SWbemServices.ExecMethodAsync,**](swbemservices-execmethodasync.md)mas opera diretamente no objeto do método a ser executado. Windows A Instrumentação de Gerenciamento (WMI) não implementa esse método. O provedor implementa esse método.

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*objWbemSink* \[ Em\]
</dt> <dd>

Obrigatórios. Esse é o sink de objeto que recebe os resultados da chamada de método. Os parâmetros de saída são enviados para o [**evento SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) do sink de objeto fornecido. Os resultados do mecanismo de chamada são enviados para o [**evento SWbemSink.OnCompleted**](swbemsink-oncompleted.md) do sink de objeto fornecido. Observe que **SWbemSink.OnCompleted** não recebe o código de retorno do método. No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se ela falhou por motivos mecânicos. O código de resultado retornado do método é retornado no objeto de parâmetro de saída fornecido para **SWbemSink.OnObjectReady**. Se algum código de erro retornar, o objeto [**IWbemObjectSink**](iwbemobjectsink.md) fornecido não será usado. Se a chamada for bem-sucedida, a implementação **IWbemObjectSink** do usuário será chamada para indicar o resultado da operação.

</dd> <dt>

*strMethodName* \[ Em\]
</dt> <dd>

Obrigatórios. Esse é o nome do método para o objeto .

</dd> <dt>

*objwbemInParams* \[ in, opcional\]
</dt> <dd>

Este é um [**objeto SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que está sendo executado. Por padrão, esse parâmetro é indefinido. Para obter mais informações, [consulte Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ in, opcional\]
</dt> <dd>

Inteiro que determina o comportamento da chamada. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus*** (128 (0x80))


</dt> <dd>

Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink.OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus*** (0 (0x0))


</dt> <dd>

Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o sink do objeto.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ in, opcional\]
</dt> <dd>

Normalmente, ele é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> <dt>

*objWbemAsyncContext* \[ in, opcional\]
</dt> <dd>

Este é um [**objeto SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao sink do objeto para identificar a origem da chamada assíncrona original. Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo sink de objeto. Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo. Esse **objeto SWbemNamedValueSet** é retornado ao sink do objeto e a origem da chamada pode ser extraída usando o [**método SWbemNamedValueSet.Item.**](swbemnamedvalueset-item.md) Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não tem valores de retorno. Se a chamada for bem-sucedida, um objeto [**OutParameters,**](swbemmethod-outparameters.md) que também é um objeto [**SWbemObject,**](swbemobject.md) será fornecido para o sink especificado em *objWbemSink.* O objeto **OutParameters** retornado contém os parâmetros de saída e o valor retornado para o método que está sendo executado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do **método ExecMethodAsync, \_** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidClass** – 2147749904 (0x80041010)
</dt> <dd>

A classe especificada não era válida.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Um parâmetro especificado não é válido.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrInvalidMethod** – 2147749934 (0x8004102E)
</dt> <dd>

O método solicitado não estava disponível.

</dd> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não estava autorizado a executar o método.

</dd> </dl>

## <a name="remarks"></a>Comentários

Use o **SWbemObject.ExecMethodAsync como \_** uma alternativa ao acesso direto para executar um método de provedor quando não for possível executar um método diretamente. [](gloss-p.md) Por exemplo, se o método tiver parâmetros de saída, use o método **SWbemObject.ExecMethodAsync \_** com uma linguagem de script que não dá suporte a parâmetros de saída. Caso contrário, é recomendável invocar um método usando o acesso direto. Para obter mais informações, consulte [Manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

Essa chamada retorna imediatamente. Os objetos e o status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao sink especificado em *objWbemSink.* Para processar cada objeto quando ele chegar, crie um *objWbemSink.* Sub-rotina de evento [**OnObjectReady.**](swbemsink-onobjectready.md) Depois que todos os objetos são retornados, você pode executar o processamento final em sua implementação *do objWbemSink.* [**Evento OnCompleted.**](swbemsink-oncompleted.md)

Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o sink. Isso representa riscos de segurança para seus scripts e aplicativos. Para eliminar os riscos, use comunicação síncrona ou comunicação síncrona. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Se o método que está sendo executado tiver parâmetros de entrada, o objeto [**InParameters**](swbemmethod-inparameters.md) e *o parâmetro objWbemInParam* deverão ser construídos conforme descrito em [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).

O **SWbemObject.Exemétodo \_ cMethodAsync** assume que o objeto representado por [**SWbemObject**](swbemobject.md) contém o método a ser executado. O [**SWbemServices.Exemétodo cMethodAsync**](swbemservices-execmethodasync.md) requer um caminho de objeto.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o [**método ExecMethodAsync.**](swbemservices-execmethodasync.md) O script cria um [**objeto Win32 \_ Process**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que está executando Bloco de notas. Ele mostra a configuração do [**objeto InParameters**](swbemmethod-inparameters.md) e como obter resultados de um [**objeto OutParameters.**](swbemmethod-outparameters.md)

Para um script que mostra as mesmas operações executadas de forma síncrona, [**consulteSWbemObject.ExecMethod**](swbemobject-execmethod-.md). Para ver um exemplo de como usar o acesso direto, [**consulte Criar método na classe Win32 \_ Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para ver um exemplo da mesma operação usando um [**objeto SWbemServices,**](swbemservices.md) [**consulteSWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
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
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | IID \_ ISWbemObject<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Swbemobject**](swbemobject.md)
</dt> <dt>

[**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md)
</dt> </dl>

 

