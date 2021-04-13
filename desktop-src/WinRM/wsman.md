---
title: Objeto WSMan (WSManDisp. h)
description: Fornece métodos e propriedades usados para criar uma sessão, representada por um objeto de sessão.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows de objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, descrito
topic_type:
- apiref
api_name:
- WSMan
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02cb92b2d72d657791d4a16bd1e999b77645a67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369288"
---
# <a name="wsman-object"></a>Objeto WSMan

Fornece métodos e propriedades usados para criar uma sessão, representada por um objeto de [**sessão**](session.md) . Todas as operações de Gerenciamento Remoto do Windows exigem a criação de uma [**sessão**](session.md) que se conecta a um computador remoto, BMC ( [*controlador de gerenciamento base*](windows-remote-management-glossary.md) ) ou o computador local. As operações incluem obter, gravar, enumerar dados ou invocar métodos.

## <a name="members"></a>Membros

O objeto **WSMan** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **WSMan** tem esses métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createconnectionoptions.md"><strong>Createconnectoptions</strong></a></td>
<td style="text-align: left;">Cria um objeto <a href="connectionoptions.md"><strong>ConnectionOptions</strong></a> que especifica o nome de usuário e a senha usados ao criar uma sessão remota.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a></td>
<td style="text-align: left;">Cria um objeto <a href="resourcelocator.md"><strong>ResourceLocator</strong></a> que pode especificar:<br/>
<ul>
<li>O caminho completo para um <a href="windows-remote-management-glossary.md"><em>recurso</em></a> ou um único dado.</li>
<li>Um <a href="windows-remote-management-glossary.md"><em>seletor</em></a> para uma instância específica de um recurso.</li>
<li>Uma <a href="windows-remote-management-glossary.md"><em>opção</em></a> que fornece dados adicionais para o provedor de recursos.</li>
</ul></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-createsession.md"><strong>CreateSession</strong></a></td>
<td style="text-align: left;">Cria um objeto de <a href="session.md"><strong>sessão</strong></a> que pode ser usado para operações de rede subsequentes.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan. EnumerationFlagHierarchyDeep</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyDeep</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan. EnumerationFlagHierarchyDeepBasePropsOnly</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan. EnumerationFlagHierarchyShallow</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyShallow</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan. EnumerationFlagNonXmlText</strong></a></td>
<td style="text-align: left;">Retorna o valor da constante de enumeração <strong>WSManFlagNonXmlText</strong> para uso no parâmetro <em>flags</em> do método <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a> .<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnepr.md"><strong>WSMan. EnumerationFlagReturnEPR</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnEPR</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobject.md"><strong>WSMan. EnumerationFlagReturnObject</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnObject</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan. EnumerationFlagReturnObjectAndEPR</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnObjectAndEPR</strong> para uso no parâmetro <em>flags</em> de <a href="session-enumerate.md"><strong>Session. Enumerate</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-geterrormessage.md"><strong>WSMan. GetErrorMessage</strong></a></td>
<td style="text-align: left;">Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan. SessionFlagCredUsernamePassword</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagCredUsernamePassword</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan. SessionFlagEnableSPNServerPort</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagEnableSPNServerPort</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagnoencryption.md"><strong>WSMan. SessionFlagNoEncryption</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagNoEncryption</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagskipcacheck.md"><strong>WSMan. SessionFlagSkipCACheck</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagSkipCACheck</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagskipcncheck.md"><strong>WSMan. SessionFlagSkipCNCheck</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagSkipCNCheck</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusebasic.md"><strong>WSMan. SessionFlagUseBasic</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseBasic</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusedigest.md"><strong>WSMan. SessionFlagUseDigest</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseDigest</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusekerberos.md"><strong>WSMan. SessionFlagUseKerberos</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseKerberos</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagusenegotiate.md"><strong>WSMan. SessionFlagUseNegotiate</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseNegotiate</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan. SessionFlagUseNoAuthentication</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUseNoAuthentication</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="wsman-sessionflagutf8.md"><strong>WSMan. SessionFlagUTF8</strong></a></td>
<td style="text-align: left;">Retorna o valor do sinalizador de autenticação <strong>WSManFlagUTF8</strong> para uso no parâmetro <em>flags</em> de <a href="wsman-createsession.md"><strong>WSMan. CreateSession</strong></a>.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="properties"></a>Propriedades

O objeto **WSMan** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**CommandLine**](wsman-commandline.md)<br/> | Somente leitura<br/> | Obtém a linha de comando não processada para o processo de hospedagem atual.<br/> |
| [**Erro**](wsman-error.md)<br/>             | Somente leitura<br/> | Obtém informações de erro.<br/>                                            |



 

## <a name="remarks"></a>Comentários

O objeto **WSMan** corresponde às interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) . **WSMan** é o único objeto que pode ser criado diretamente usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como criar uma instância de um objeto **WSMan** .


```VB
Dim objWsman
Dim Session, Resource 
Set objWsman = CreateObject( "WSMAN.Automation" )
Set Session = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/wmi/Root/CIMv2/Win32_OperatingSystem"
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API de script do WinRM](winrm-scripting-api.md)
</dt> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[Usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[Criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtendo dados do computador local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

