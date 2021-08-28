---
title: Objeto WSMan (WSManDisp.h)
description: Fornece métodos e propriedades usados para criar uma sessão, representada por um objeto Session.
ms.assetid: 45895a4e-b7de-4469-ae78-6d1d3f9d6145
ms.tgt_platform: multiple
keywords:
- Objeto WSMan Windows Gerenciamento Remoto
- Objeto WSMan Windows Gerenciamento Remoto , descrito
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
ms.openlocfilehash: dac26be22118a320848ea227643f9c4d3857dc01
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475962"
---
# <a name="wsman-object"></a>Objeto WSMan

Fornece métodos e propriedades usados para criar uma sessão, representada por um [**objeto Session.**](session.md) As Windows de Gerenciamento Remoto exigem a criação de uma [**Sessão**](session.md) que se conecta a um computador [*remoto,*](windows-remote-management-glossary.md) ao BMC (controlador de gerenciamento base) ou ao computador local. As operações incluem obter, escrever, enumerar dados ou invocar métodos.

## <a name="members"></a>Membros

O **objeto WSMan** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto WSMan** tem esses métodos.




| Método | Descrição | 
|--------|-------------|
| <a href="wsman-createconnectionoptions.md"><strong>CreateConnectionOptions</strong></a> | Cria um <a href="connectionoptions.md"><strong>objeto ConnectionOptions</strong></a> que especifica o nome de usuário e a senha usados ao criar uma sessão remota.<br /> | 
| <a href="wsman-createresourcelocator.md"><strong>CreateResourceLocator</strong></a> | Cria um <a href="resourcelocator.md"><strong>objeto ResourceLocator</strong></a> que pode especificar:<br /><ul><li>O caminho completo para <a href="windows-remote-management-glossary.md"><em>um recurso</em></a> ou uma única parte dos dados.</li><li>Um <a href="windows-remote-management-glossary.md"><em>seletor</em></a> para uma instância específica de um recurso.</li><li>Uma <a href="windows-remote-management-glossary.md"><em>opção</em></a> que fornece dados adicionais ao provedor de recursos.</li></ul> | 
| <a href="wsman-createsession.md"><strong>Createsession</strong></a> | Cria um <a href="session.md"><strong>objeto Session</strong></a> que pode ser usado para operações de rede subsequentes.<br /> | 
| <a href="wsman-enumerationflaghierarchydeep.md"><strong>WSMan.EnumerationFlagHierarchyDeep</strong></a> | Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyDeep</strong> para uso no parâmetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflaghierarchydeepbasepropsonly.md"><strong>WSMan.EnumerationFlagHierarchyDeepBasePropsOnly</strong></a> | Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyDeepBasePropsOnly</strong> para uso no parâmetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflaghierarchyshallow.md"><strong>WSMan.EnumerationFlagHierarchyShallow</strong></a> | Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagHierarchyShallow</strong> para uso no parâmetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagnonxmltext.md"><strong>WSMan.EnumerationFlagNonXmlText</strong></a> | Retorna o valor da constante de enumeração <strong>WSManFlagNonXmlText</strong> para uso no parâmetro <em>flags</em> do <a href="session-enumerate.md"><strong>método Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflagreturnepr.md"><strong>WSMan.EnumerationFlagReturnEPR</strong></a> | Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnEPR</strong> para uso no parâmetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-enumerationflagreturnobject.md"><strong>WSMan.EnumerationFlagReturnObject</strong></a> | Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnObject</strong> para uso no parâmetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate.</strong></a><br /> | 
| <a href="wsman-enumerationflagreturnobjectandepr.md"><strong>WSMan.EnumerationFlagReturnObjectAndEPR</strong></a> | Retorna o valor do sinalizador de enumeração <strong>EnumerationFlagReturnObjectAndEPR</strong> para uso no parâmetro <em>flags</em> <a href="session-enumerate.md"><strong>de Session.Enumerate</strong></a>.<br /> | 
| <a href="wsman-geterrormessage.md"><strong>WSMan.GetErrorMessage</strong></a> | Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro.<br /> | 
| <a href="wsman-sessionflagcredusernamepassword.md"><strong>WSMan.SessionFlagCredUsernamePassword</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagCredUsernamePassword</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagenablespnserverport.md"><strong>WSMan.SessionFlagEnableSPNServerPort</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagEnableSPNServerPort</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagnoencryption.md"><strong>WSMan.SessionFlagNoEncryption</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagNoEncryption</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagskipcacheck.md"><strong>WSMan.SessionFlagSkipCACheck</strong></a> | Retorna o valor do sinalizador de autenticação <strong>WSManFlagSkipCACheck</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagskipcncheck.md"><strong>WSMan.SessionFlagSkipCNCheck</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagSkipCNCheck</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusebasic.md"><strong>WSMan.SessionFlagUseBasic</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagUseBasic</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusedigest.md"><strong>WSMan.SessionFlagUseDigest</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagUseDigest</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusekerberos.md"><strong>WSMan.SessionFlagUseKerberos</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagUseKerberos</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagusenegotiate.md"><strong>WSMan.SessionFlagUseNegotiate</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagUseNegotiate</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession.</strong></a><br /> | 
| <a href="wsman-sessionflagusenoauthentication.md"><strong>WSMan.SessionFlagUseNoAuthentication</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagUseNoAuthentication</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 
| <a href="wsman-sessionflagutf8.md"><strong>WSMan.SessionFlagUTF8</strong></a> | Retorna o valor do sinalizador de <strong>autenticação WSManFlagUTF8</strong> para uso no parâmetro <em>flags</em> <a href="wsman-createsession.md"><strong>de WSMan.CreateSession</strong></a>.<br /> | 




 

### <a name="properties"></a>Propriedades

O **objeto WSMan** tem essas propriedades.



| Propriedade                                            | Tipo de acesso          | Descrição                                                                   |
|:----------------------------------------------------|:---------------------|:------------------------------------------------------------------------------|
| [**Commandline**](wsman-commandline.md)<br/> | Somente leitura<br/> | Obtém a linha de comando não processada para o processo de hospedagem atual.<br/> |
| [**Erro do**](wsman-error.md)<br/>             | Somente leitura<br/> | Obtém informações de erro.<br/>                                            |



 

## <a name="remarks"></a>Comentários

O **objeto WSMan** corresponde às interfaces [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) [**e IWSManEx.**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex) **O WSMan** é o único objeto que pode ser criado diretamente usando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).

## <a name="examples"></a>Exemplos

O exemplo de código a seguir mostra como insinuar um **objeto WSMan.**


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
| Cabeçalho<br/>                   | <dl> <dt>WSManDisp.h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WSManDisp.idl</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>WSManDisp.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[API de Script WinRM](winrm-scripting-api.md)
</dt> <dt>

[Sobre Windows gerenciamento remoto](about-windows-remote-management.md)
</dt> <dt>

[Usando Windows gerenciamento remoto](using-windows-remote-management.md)
</dt> <dt>

[Scripts em Windows Gerenciamento Remoto](scripting-in-windows-remote-management.md)
</dt> <dt>

[Obtendo dados do computador local](obtaining-data-from-the-local-computer.md)
</dt> <dt>

[Obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md)
</dt> </dl>

 

