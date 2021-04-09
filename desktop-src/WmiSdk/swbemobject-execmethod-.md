---
description: O \_ método ExecMethod do objeto SWbemObject executa um método exportado por um provedor de método.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Método de cMethod_ de SWbemObject.Exe(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091288"
---
# <a name="swbemobjectexecmethod_-method"></a>SWbemObject.Exe\_ método cMethod

O **método \_ ExecMethod** do objeto [**SWbemObject**](swbemobject.md) executa um método exportado por um provedor de método.

Esse método pausa enquanto o método encaminhado para o provedor apropriado é executado. Em seguida, as informações e o status são retornados. O provedor, em vez de WMI, implementa o método.

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strMethodName* \[ no\]
</dt> <dd>

Obrigatórios. Nome do método do objeto.

</dd> <dt>

*objwbemInParams* \[ em, opcional\]
</dt> <dd>

Este é um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que está sendo executado. Por padrão, esse parâmetro é indefinido. Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

</dd> <dt>

*iFlags* \[ em, opcional\]
</dt> <dd>

Reservado e deve ser definido como 0 (zero) se especificado.

</dd> <dt>

*objwbemNamedValueSet* \[ em, opcional\]
</dt> <dd>

Normalmente, ele é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem-sucedido, um objeto [**SWbemObject**](swbemobject.md) retornará. O objeto retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ExecMethod \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.

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

Esse método é semelhante a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), mas opera diretamente no objeto cujo método deve ser executado. Por exemplo, o exemplo de código a seguir chama o método de provedor [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) no [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) e usa o [acesso direto](manipulating-class-and-instance-information.md).


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



Essa versão chama **SWbemObject.ExecMethod \_** para executar o método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



Use **SWbemObject.ExecMethod \_** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) em casos em que não é possível executar um método diretamente. Por exemplo, você usaria **SWbemObject.ExecMethod \_** com uma linguagem de script que não oferece suporte a parâmetros de saída se o seu método tiver parâmetros. Caso contrário, o meio recomendado de invocar um método é usar o acesso direto.

-   O método **SWbemObject.Exe\_ cMethod** pressupõe que o objeto representado por [**SWbemObject**](swbemobject.md) contém o método a ser executado. Por outro lado, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requer um caminho de objeto. Use **SWbemObject.ExecMethod \_** se você já tiver obtido o objeto cujo método você deseja executar.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o método [**ExecMethod**](swbemservices-execmethod.md) . O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que executa o bloco de notas. Para obter mais informações sobre um script que ilustra as mesmas operações executadas de forma assíncrona, consulte [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md). Para obter um exemplo usando o acesso direto, consulte [**criar método no \_ processo Win32 da classe**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) . Para obter um exemplo da mesma operação usando um objeto [**SWbemServices**](swbemservices.md) , consulte **SWbemServices.ExecMethod**.


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
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
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
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
| CLSID<br/>                    | CLSID \_ SWbemObject<br/>                                                           |
| IID<br/>                      | ISWbemObject de IID \_<br/>                                                            |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemObject**](swbemobject.md)
</dt> <dt>

[**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md)
</dt> <dt>

[**SWbemServices.ExecMethod**](swbemservices-execmethod.md)
</dt> </dl>

 

