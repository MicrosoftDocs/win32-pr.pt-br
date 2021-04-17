---
description: Conecta-se ao namespace no computador especificado no parâmetro strServer.
ms.assetid: 31364c68-b031-4cf0-851f-b4e302f077e0
ms.tgt_platform: multiple
title: Método SWbemLocator. ConnectServer (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
- ISWbemLocator.ConnectServer
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 31c2e6de8cf1504543727cad056a3616a51182d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761235"
---
# <a name="swbemlocatorconnectserver-method"></a>Método SWbemLocator. ConnectServer

O método **ConnectServer** do objeto [**SWbemLocator**](swbemlocator.md) se conecta ao namespace no computador especificado no parâmetro *strServer* . O computador de destino pode ser local ou remoto, mas ele deve ter o WMI instalado. Para obter exemplos e uma comparação com o tipo de moniker de conexão, consulte [criando um script WMI](creating-a-wmi-script.md).

A partir do Windows Vista, o **SWbemLocator. ConnectServer** pode se conectar a computadores que executam o IPv6 usando um endereço IPv6 no parâmetro *strServer* . Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](ipv6-and-ipv4-support-in-wmi.md).

Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Sintaxe


```VB
objwbemServices = .ConnectServer( _
  [ ByVal strServer ], _
  [ ByVal strNamespace ], _
  [ ByVal strUser ], _
  [ ByVal strPassword ], _
  [ ByVal strLocale ], _
  [ ByVal strAuthority ], _
  [ ByVal iSecurityFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*strServer* \[ em, opcional\]
</dt> <dd>

Nome do computador ao qual você está se conectando. Se o computador remoto estiver em um domínio diferente da conta de usuário sob a qual você faz logon, use o nome do computador totalmente qualificado. Se você não fornecer esse parâmetro, a chamada usa como padrão o computador local.

Exemplo: `server1.network.fabrikam`

Você também pode usar um endereço IP nesse parâmetro. Se o endereço IP estiver no formato IPv6, o computador de destino deverá estar executando o IPv6. Um endereço em IPv4 é semelhante a `123.123.123.123`

Um endereço IP no formato IPv6 é semelhante a `2010:836B:4179::836B:4179`

Para obter mais informações sobre DNS e IPv4, consulte a seção comentários.

</dd> <dt>

*strNamespace* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que especifica o namespace no qual você faz logon. Por exemplo, para fazer logon no namespace raiz \\ padrão, use o \\ padrão raiz. Se você não especificar esse parâmetro, o padrão será o namespace configurado como o namespace padrão para scripts. Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).

Exemplo: "raiz \\ cimv2"

</dd> <dt>

*strUser* \[ em, opcional\]
</dt> <dd>

Nome de usuário a ser usado para se conectar. A cadeia de caracteres pode estar na forma de um nome de usuário ou de um domínio de \\ usuário. Deixe esse parâmetro em branco para usar o contexto de segurança atual. O parâmetro *strUser* só deve ser usado com conexões com servidores WMI remotos. Se você tentar especificar *strUser* para uma conexão WMI local, a tentativa de conexão falhará. Se a autenticação Kerberos estiver em uso, o nome de usuário e a senha especificados em *strUser* e *strPassword* não poderão ser interceptados em uma rede. Você pode usar o formato UPN para especificar o *strUser*.

Exemplo: "nome_do_domínio nome de \\ usuário"

> [!Note]  
> Se um domínio for especificado em *strAuthority*, o domínio não deverá ser especificado aqui. A especificação do domínio em ambos os parâmetros resulta em um erro de parâmetro inválido.

 

</dd> <dt>

*strPassword* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que especifica a senha a ser usada ao tentar se conectar. Deixe o parâmetro em branco para usar o contexto de segurança atual. O parâmetro *strPassword* só deve ser usado com conexões com servidores WMI remotos. Se você tentar especificar *strPassword* para uma conexão WMI local, a tentativa de conexão falhará. Se a autenticação Kerberos estiver em uso, o nome de usuário e a senha especificados em *strUser* e *strPassword* não poderão ser interceptados na rede.

</dd> <dt>

*strLocale* \[ em, opcional\]
</dt> <dd>

Cadeia de caracteres que especifica o código de localização. Se você quiser usar a localidade atual, deixe em branco. Se não estiver em branco, esse parâmetro deverá ser uma cadeia de caracteres que indica a localidade desejada onde as informações devem ser recuperadas. Para identificadores de localidade da Microsoft, o formato da cadeia de caracteres é "MS \_ xxxx", onde xxxx é uma cadeia de caracteres no formato hexadecimal que indica o LCID. Por exemplo, inglês americano apareceria como "MS \_ 409".

</dd> <dt>

*strAuthority* \[ em, opcional\]
</dt> <dd>

<dt>

""
</dt> <dd>

Esse parâmetro é opcional. No entanto, se for especificado, somente Kerberos ou NTLMDomain poderão ser usados.

</dd> <dt>

Kerberos
</dt> <dd>

Se o parâmetro *strAuthority* começar com a cadeia de caracteres "Kerberos:", a autenticação Kerberos será usada e esse parâmetro deverá conter um nome de entidade de segurança Kerberos. O nome da entidade de segurança Kerberos é especificado como Kerberos:*Domain*, por exemplo, `Kerberos:fabrikam` onde `fabrikam` é o servidor ao qual você está tentando se conectar.

Exemplo: "Kerberos: DOMAIN"

</dd> <dt>

NTLMDomain:
</dt> <dd>

Para usar a autenticação NTLM (NT LAN Manager), você deve especificá-la como NTLMDomain:*Domain*, por exemplo, `NTLMDomain:fabrikam` onde `fabrikam` é o nome do domínio.

Exemplo: "NTLMDomain: DOMAIN"

</dd> </dl>

Se você deixar esse parâmetro em branco, o sistema operacional negociará com com para determinar se a autenticação NTLM ou Kerberos será usada. Esse parâmetro só deve ser usado com conexões com servidores WMI remotos. Se você tentar definir a autoridade para uma conexão WMI local, a tentativa de conexão falhará.

> [!Note]  
> Se o domínio for especificado em *strUser*, que é o local preferido, ele não deverá ser especificado aqui. A especificação do domínio em ambos os parâmetros resulta em um erro de parâmetro inválido.

 

</dd> <dt>

*iSecurityFlags* \[ em, opcional\]
</dt> <dd>

Usado para passar valores de sinalizador para **ConnectServer**.

<dt>

0 (0x0)
</dt> <dd>

Um valor de 0 para esse parâmetro faz com que a chamada para **ConnectServer** seja retornada somente depois que a conexão com o servidor é estabelecida. Isso pode fazer com que o programa pare de responder indefinidamente se não for possível estabelecer a conexão.

</dd> <dt>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>

<span id="wbemConnectFlagUseMaxWait"></span><span id="wbemconnectflagusemaxwait"></span><span id="WBEMCONNECTFLAGUSEMAXWAIT"></span>wbemConnectFlagUseMaxWait * * * * (128 (0x80))


</dt> <dd>

A chamada **ConnectServer** é garantida para retornar em 2 minutos ou menos. Use esse sinalizador para impedir que o programa deixar responda indefinidamente se não for possível estabelecer a conexão.

</dd> </dl> </dd> <dt>

*objwbemNamedValueSet* \[ em, opcional\]
</dt> <dd>

Normalmente, isso é indefinido. Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação. Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, o WMI retornará um objeto [**SWbemServices**](swbemservices.md) que está associado ao namespace especificado em *strNamespace* no computador especificado em *strServer*.

## <a name="error-codes"></a>Códigos do Erro

Após a conclusão do método **ConnectServer** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.

<dl> <dt>

**wbemErrAccessDenied** -2147749891 (0x80041003)
</dt> <dd>

O nome de usuário e a senha atuais ou especificados não eram válidos ou autorizados a estabelecer a conexão.

</dd> <dt>

**wbemErrFailed** -2147749889 (0x80041001)
</dt> <dd>

Erro não especificado.

</dd> <dt>

**wbemErrInvalidNamespace** -2147749902 (0x8004100E)
</dt> <dd>

O namespace especificado não existia no servidor.

</dd> <dt>

**wbemErrInvalidParameter** -2147749896 (0x80041008)
</dt> <dd>

Um parâmetro inválido foi especificado ou o namespace não pôde ser analisado.

</dd> <dt>

**wbemErrOutOfMemory** -2147749894 (0x80041006)
</dt> <dd>

Não há memória suficiente para concluir a operação.

</dd> <dt>

**wbemErrTransportFailure** -2147749909
</dt> <dd>

Ocorreu um erro de rede, impedindo A operação normal.

</dd> </dl>

## <a name="remarks"></a>Comentários

O método **ConnectServer** geralmente é usado ao se conectar a uma conta com credenciais de nome de usuário e senha diferentes em um computador remoto porque você não pode especificar uma senha diferente em uma cadeia de caracteres de [moniker](constructing-a-moniker-string.md) . Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).

Usar um endereço IPv4 para se conectar a um servidor remoto pode resultar em um comportamento inesperado. A causa provável é as entradas DNS obsoletas em seu ambiente. Nessas circunstâncias, a entrada PTR obsoleta para o computador será usada, com resultados imprevisíveis. Para evitar esse comportamento, você pode acrescentar um ponto (".") ao endereço IP antes de chamar ConnectServer. Isso faz com que a pesquisa de DNS reverso falhe, mas pode permitir que a chamada **ConnectServer** seja bem-sucedida no computador correto.

## <a name="examples"></a>Exemplos

O exemplo de código VBScript a seguir descreve como se conectar a um computador remoto para obter dados do [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) . O nome de domínio especificado em *strDomain* é usado em *strAuthority*.


```VB
Const intMin = 3600
strComputer = "RemoteComputer" 
strDomain = "DomainName"  
Wscript.StdOut.Write "Please enter your user name:"
strUser = Wscript.StdIn.ReadLine 
Set objPassword = CreateObject("ScriptPW.Password")
Wscript.StdOut.Write "Please enter your password:"
strPassword = objPassword.GetPassword()
Wscript.Echo

Set objSWbemLocator = CreateObject("WbemScripting.SWbemLocator") 
Set objWMIService = objSWbemLocator.ConnectServer(strComputer, _ 
                                                  "root\CIMV2", _ 
                                                  strUser, _ 
                                                  strPassword, _ 
                                                  "MS_409", _ 
                                                  "NTLMDomain:" + strDomain) 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_IP4RouteTable",,48) 
For Each objItem in colItems
    WScript.Echo "Age in Minutes: " & int(objItem.Age/intMin) & VBNewLine _
               & "Description:    " & objItem.Description & VBNewLine _
               & "Destination:    " & objItem.Destination & VBNewLine _
               & "InterfaceIndex: " & objItem.InterfaceIndex & VBNewLine _
               & "Mask:           " & objItem.Mask & VBNewLine _
               & "Metric1:        " & objItem.Metric1 & VBNewLine _
               & "Metric2:        " & objItem.Metric2 & VBNewLine _
               & "Metric3:        " & objItem.Metric3 & VBNewLine _
               & "Metric4:        " & objItem.Metric4 & VBNewLine _
               & "Metric5:        " & objItem.Metric5 & VBNewLine _
               & "Name:           " & objItem.Name & VBNewLine _
               & "NextHop:        " & objItem.NextHop & VBNewLine _
               & "Protocol:       " & objItem.Protocol & VBNewLine _
               & "Type: " & objItem.Type
    WScript.Echo
   </example>
Next
```



O trecho do PowerShell a seguir acessa um servidor remoto e lista as classes WMI disponíveis.


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMLOCATOR CLSID<br/>                                                          |
| IID<br/>                      | ISWbemLocator de IID \_<br/>                                                           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**SWbemLocator**](swbemlocator.md)
</dt> <dt>

[**SWbemServices**](swbemservices.md)
</dt> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[Criando um script WMI](creating-a-wmi-script.md)
</dt> </dl>

 

