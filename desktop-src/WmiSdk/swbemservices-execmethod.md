---
description: Executa um método que é exportado por um provedor de método.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethod (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011124"
---
# <a name="swbemservicesexecmethod-method"></a>SWbemServices.Exemétodo cMethod

O método **ExecMethod** do objeto [**SWbemServices**](swbemservices.md) executa um método que é exportado por um provedor de método. Esse método é bloqueado enquanto o método encaminhado para o provedor apropriado é executado. Em seguida, as informações e o status são retornados. O provedor, em vez do WMI, implementa o método.

Esse método é chamado no modo síncrono. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strObjectPath* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o caminho do objeto do objeto para o qual o método é executado. Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).

</dd> <dt>

*strMethodName* 
</dt> <dd>

Obrigatórios. Nome do método do objeto.

</dd> <dt>

*objWbemInParams* \[ adicional\]
</dt> <dd>

Um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que está sendo executado. Por padrão, esse parâmetro é indefinido. Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ adicional\]
</dt> <dd>

Reservado. Esse valor precisa ser zero.

</dd> <dt>

*objWbemNamedValueSet* \[ adicional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se o método for bem-sucedido, um objeto [**SWbemObject**](swbemobject.md) será retornado. O objeto retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ExecMethod** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

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

Use **SWbemServices.ExecMethod** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) em casos em que não é possível executar um método diretamente. O método **ExecMethod** permite que você obtenha parâmetros de saída, se o provedor fornecer, com uma linguagem de script que não ofereça suporte a parâmetros de saída. Caso contrário, o meio recomendado de invocar um método é usar o acesso direto. Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).

Por exemplo, o exemplo de código a seguir que chama o método de provedor [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) no [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) usa o acesso direto.


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Este exemplo chama **SWbemServices.ExecMethod** para executar o método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) . Observe que um caminho de objeto é necessário porque **SWbemServices.ExecMethod** ainda não está operando no objeto, ao contrário de [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



O método **cMethodSWbemServices.Exe** requer um caminho de objeto. Se o script já mantiver um objeto [**SWbemObject**](swbemobject.md) , use o método [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o método **ExecMethod** . O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que está executando o bloco de notas. Ele mostra a configuração de um objeto de [**inparâmetros**](swbemmethod-inparameters.md) e como obter resultados de um objeto [**Parameters**](swbemmethod-outparameters.md) . Para um script que mostra as mesmas operações executadas de forma assíncrona, consulte [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md). Para obter um exemplo de como usar o acesso direto, consulte [criar método na classe \_ processo Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process). Para obter um exemplo da mesma operação usando um [**SWbemObject**](swbemobject.md), consulte [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md)
</dt> <dt>

[Chamando um método de provedor](calling-a-provider-method.md)
</dt> <dt>

[Manipulando informações de classe e instância](manipulating-class-and-instance-information.md)
</dt> </dl>

 

