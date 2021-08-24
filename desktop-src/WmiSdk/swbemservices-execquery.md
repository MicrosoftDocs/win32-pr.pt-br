---
description: SWbemServices.Exemétodo cQuery – executa uma consulta para recuperar objetos.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cQuery (Wbemdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9e827b1297a2bdd3bac39a22efa7f80e0d4723ded689e691423c6945a88bb729
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119897476"
---
# <a name="swbemservicesexecquery-method"></a>SWbemServices.Exemétodo cQuery

O **método ExecQuery** do [**objeto SWbemServices**](swbemservices.md) executa uma consulta para recuperar objetos. Esses objetos estão disponíveis por meio da coleção [**SWbemObjectSet**](swbemobjectset.md) retornada.

Esse método é chamado no modo semissíncrono. Para obter mais informações, consulte [Chamando um método](calling-a-method.md).

Para uma explicação dessa sintaxe, consulte [Convenções de documento para a API de Script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strQuery* 
</dt> <dd>

Obrigatórios. Cadeia de caracteres que contém o texto da consulta. Esse parâmetro não pode estar em branco. Para obter mais informações sobre como criar cadeias de caracteres de consulta WMI, consulte Consultando com [WQL](querying-with-wql.md) e a [referência WQL.](wql-sql-for-wmi.md)

</dd> <dt>

*strQueryLanguage* \[ Opcional\]
</dt> <dd>

Cadeia de caracteres que contém a linguagem de consulta a ser usada. Se especificado, esse valor deve ser "WQL".

</dd> <dt>

*iFlags* \[ Opcional\]
</dt> <dd>

Inteiro que determina o comportamento da consulta e determina se essa chamada retorna imediatamente. O valor padrão para esse parâmetro é **wbemFlagReturnImmediately**. Esse parâmetro pode aceitar os valores a seguir.

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly*** (32 (0x20))


</dt> <dd>

Faz com que um enumerador somente de avanço seja retornado. Enumeradores somente avanço geralmente são muito mais rápidos e usam menos memória do que enumeradores convencionais, mas não permitem chamadas para [**SWbemObject.Clone \_**](swbemobject-clone-.md).

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional*** (0 (0x0))


</dt> <dd>

Faz com que o WMI mantenha ponteiros para objetos da enumeração até que o cliente libere o enumerador.

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately*** (16 (0x10))


</dt> <dd>

Faz com que a chamada retorne imediatamente.

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete*** (0 (0x0))


</dt> <dd>

Faz com que essa chamada bloqueie até que a consulta seja concluída. Esse sinalizador chama o método no modo síncrono.

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype*** (2 (0x2))


</dt> <dd>

Usado para criação de protótipos. Esse sinalizador impede que a consulta ocorra e retorna um objeto que se parece com um objeto de resultado típico.

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers*** (131072 (0x20000))


</dt> <dd>

Faz com que o WMI retorne dados de alteração de classe com a definição de classe base. Para obter mais informações, consulte [Localizando informações de classe WMI](localizing-wmi-class-information.md).

</dd> </dl> </dd> <dt>

*objWbemNamedValueSet* \[ Opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é [**um objeto SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou requer essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se nenhum erro ocorrer, esse método retornará um [**objeto SWbemObjectSet.**](swbemobjectset.md) Essa é uma coleção de objetos que contém o conjunto de resultados da consulta. O chamador pode examinar a coleção usando a implementação de coleções para a linguagem de programação que você está usando. Para obter mais informações, [consulte Acessando uma coleção](accessing-a-collection.md).

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ExecQuery,** o [objeto Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** – 2147749891 (0x80041003)
</dt> <dd>

O usuário atual não tem a permissão para exibir o conjunto de resultados.

</dd> <dt>

**wbemErrFailed** – 2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidParameter** – 2147749896 (0x80041008)
</dt> <dd>

Parâmetro inválido foi especificado.

</dd> <dt>

**wbemErrInvalidQuery** – 2147749911 (0x80041017)
</dt> <dd>

A sintaxe de consulta não é válida.

</dd> <dt>

**wbemErrInvalidQueryType** – 2147749912 (0x80041018)
</dt> <dd>

Não há suporte para a linguagem de consulta solicitada.

</dd> <dt>

**wbemErrOutOfMemory** – 2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> </dl>

## <a name="remarks"></a>Comentários

**ExecQuery** é uma das chamadas mais usadas para recuperar informações de WMI. Uma chamada padrão para **ExecQuery** é parecida com a seguinte:


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



Observe que você cria o objeto [**SWbemServices**](swbemservices.md) com um moniker que representa o namespace e a segurança apropriados e, em seguida, faz a chamada **ExecQuery** por meio do serviço. Para obter uma discussão mais completa, consulte [Criando um script WMI e](creating-a-wmi-script.md) [Enumerando wmi](enumerating-wmi.md).

Assim como [**o método InstancesOf,**](swbemservices-instancesof.md) o **método ExecQuery** sempre retorna uma [**coleção SWbemObjectSet.**](swbemobjectset.md) Portanto, o script WMI deve enumerar os retornos da coleção ExecQuery para acessar cada instância de recurso gerenciado na coleção, conforme mostrado aqui:


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



Outros [**métodos SWbemServices**](swbemservices.md) que retornam [**um SWbemObjectSet**](swbemobjectset.md) incluem [**AssociatorsOf,**](swbemservices-associatorsof.md) [**ReferencesTo**](swbemservices-referencesto.md)e [**SubclassesOf**](swbemservices-subclassesof.md).

Não é um erro para a consulta retornar um conjunto de resultados vazio. O **método ExecQuery retorna** propriedades de chave, independentemente de a propriedade de chave ser solicitada ou não no argumento *strQuery.* Se ocorrer um erro ao executar esse método e você não usar o sinalizador **wbemFlagReturnImmediately,** o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) não será definido até que você tente acessar o conjunto de objetos retornado. No entanto, se você usar o **sinalizador wbemFlagReturnWhenComplete,** o objeto Err será definido quando o **método ExecQuery** for chamado.

Há limites para o número de palavras-chave **AND** e **OR** que podem ser usadas em consultas WQL. Um grande número de palavras-chave WQL usadas em uma consulta complexa pode fazer com que o WMI retorne o código de erro **WBEM \_ E \_ QUOTA \_ VIOLATION** como **um valor HRESULT.** O limite de palavras-chave WQL depende de quão complexa a consulta é.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir localiza todas as unidades de disco no computador local e exibe a ID do dispositivo e o tipo da unidade de disco.


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Wbemdisp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemServices<br/>                                                         |
| IID<br/>                      | IID \_ ISWbemServices<br/>                                                          |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[**SWbemServices.Get**](swbemservices-get.md)
</dt> <dt>

[Consultando com o WQL](querying-with-wql.md)
</dt> <dt>

[Criando um script WMI](creating-a-wmi-script.md)
</dt> <dt>

[Enumerando WMI](enumerating-wmi.md)
</dt> </dl>

 

