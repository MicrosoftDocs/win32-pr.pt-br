---
title: LDIF Scripts
description: O LDIF (Formato de Intercâmbio de Dados LDAP) é um padrão IETF (Internet Engineering Task Force) que define como importar e exportar dados de diretório entre servidores de diretório que usam provedores de serviços LDAP.
ms.assetid: a87d0d34-96c0-4cef-a38e-30a7e2291a7a
ms.tgt_platform: multiple
keywords:
- LDIF Scripts Active Directory
- Scripts LDIF do Active Directory, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad45c51fc16b3c19c3e59f4cfba2e006d4df900c20ce7ddc1b801478a22982c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118187080"
---
# <a name="ldif-scripts"></a>LDIF Scripts

O LDIF (Formato de Intercâmbio de Dados LDAP) é um padrão IETF (Internet Engineering Task Force) que define como importar e exportar dados de diretório entre servidores de diretório que usam provedores de serviços LDAP. Windows 2000 e Windows Server 2003 incluem um utilitário de linha de comando, LDIFDE, que pode ser usado para importar objetos de diretório para Active Directory Domain Services usando arquivos LDIF. O LDIFDE permite definir um filtro para uma cadeia de caracteres específica para pesquisar e listar objetos de diretório no Active Directory Domain Services como arquivos LDIF que podem ser lidos facilmente por administradores de esquema.

Ao importar um arquivo Unicode, o LDIFDE importa o arquivo como Unicode se ele contém o identificador Unicode no início do arquivo. Se você quiser importar um arquivo como Unicode quando ele não contém o identificador Unicode no início do arquivo, poderá usar a opção -u para forçá-lo a ser importado como Unicode.

O modo padrão para exportar arquivos é ANSI. Se houver entradas Unicode, elas serão convertidas no formato base 64. Para exportar um arquivo para o formato Unicode, use a opção -u.

Um arquivo LDIF deve aplicar alterações de esquema quando há dependências entre os atributos que são adicionados. Por exemplo, atributos de link de encaminhamento devem ser adicionados antes do atributo de link voltar correspondente. Você também deve atualizar o cache de esquema antes de adicionar classes que dependem de atributos ou classes adicionadas anteriormente no script LDIF. Para obter mais informações, consulte o exemplo de código a seguir.

Esteja ciente de que, para valores binários, você deve codificar os valores como base64. A codificação Base64 é definida no IETF RFC 2045, Seção 6.8.

Para obter mais informações sobre o formato de arquivos LDIF, consulte O LDIF (Formato de Intercâmbio de Dados [LDAP) –](https://www.ietf.org/rfc/rfc2849.txt) Especificação Técnica (RFC 2849) no site da Força de Tarefa de Engenharia da Internet.

## <a name="ntds-specific-ldif-changetypes"></a>Tipos de alteração LDIF específicos do NTDS

É melhor usar ntdsSchema changetypes em vez de \* chamar ldifde -k. A opção -k de ldifde ignora um conjunto maior de erros LDAP. A lista completa de erros ignorados é a seguinte:

-   O objeto já é um membro do grupo.
-   Uma violação de classe de objeto (o que significa que a classe de objeto especificada não existe), se o objeto que está sendo importado não tiver outros atributos.
-   O objeto já existe (**LDAP \_ JÁ \_ EXISTE**)
-   violação de restrição (**LDAP \_ CONSTRAINT \_ VIOLATION**)
-   atributo ou valor já existe (**LDAP \_ ATTRIBUTE OR VALUE \_ \_ \_ EXISTS**)
-   nenhum objeto (**LDAP \_ NO SUCH \_ \_ OBJECT**)

Os tipos de alteração a seguir são projetados especificamente para operações de atualização de esquema.



| Changetype                      | Descrição                                                                                                                                                                                                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ntdsSchemaAdd**<br/>    | **ntdsSchemaAdd** corresponde a **adicionar** em um arquivo LDIF. A única diferença é que **ntdsSchemaAdd** faria com que ldifde ignorasse uma operação **de** adoção se o objeto já existir no esquema. (**LDAP \_ ALREADY \_ EXISTS** é ignorado.)<br/>                                   |
| **ntdsSchemaModify**<br/> | **ntdsSchemaModify** corresponde a **modificar em** um arquivo LDIF. A única diferença é que **ntdsSchemaModify** faria com que ldifde ignorasse uma operação **de** modificação se o objeto não fosse encontrado no esquema. (**LDAP \_ NO SUCH \_ \_ OBJECT** é ignorado.)<br/>                        |
| **ntdsSchemaDelete**<br/> | **ntdsSchemaDelete corresponde** à **exclusão em** um arquivo LDIF. A única diferença é que **ntdsSchemaDelete** faria com  que ldifde ignorasse uma operação de exclusão se o objeto não fosse encontrado no esquema. (**LDAP \_ NO SUCH \_ \_ OBJECT** é ignorado.)<br/>                        |
| **ntdsSchemaModRdn**<br/> | **ntdsSchemaModRdn** corresponde a **modrdn em** um arquivo LDIF. A única diferença é que **ntdsSchemaModRdn** faria com que ldifde ignorasse uma operação modify-relative-distinguished-name se o objeto não fosse encontrado no esquema. (**LDAP \_ NO SUCH \_ \_ OBJECT** é ignorado.)<br/> |



 

## <a name="example"></a>Exemplo

O exemplo de código a seguir inclui:

-   Myschemaext.ldf é um script LDIF que contém novos atributos e classes. Esteja ciente de que esse arquivo é uma versão modificada do arquivo gerado de Lgetattcls.vbs. Além disso, esteja ciente de que o atributo **My-Test-Attribute-DN-FL** foi movido à frente de **My-Test-Attribute-DN-BL** porque o link de fundo (**My-Test-Attribute-DN-BL**) depende do link de avanço (**My-Test-Attribute-DN-FL**). Além disso, o atributo **operacional schemaUpdateNow** é definido em dois locais para disparar atualizações do cache de esquema para que atributos e classes dependentes estarão disponíveis para adicionar as duas classes no script.
    > [!Note]  
    > Consulte o tópico [Obtendo uma ID de](obtaining-a-link-id.md) link para obter informações sobre a origem da ID nas instruções linkID:.

     

-   Lgetattcls.vbs é um arquivo VBScript que gera o script LDIF usado como o ponto de partida para Myschemaext.ldf. Esteja ciente de que o caminho do esquema atual é substituído por CN=Schema,CN=Configuration,DC=myorg,DC=com. Você pode substituir DC=myorg,DC=com para refletir o DN (nome diferenciado) a ser publicado no script LDIF para garantir que LSETATTCLS.VBS reflita a alteração em **seu sFromDN** para que o DN correto seja substituído quando o script LDIF for aplicado. Também esteja ciente de que o script usa um prefixo para encontrar as classes e atributos que você também deve definir e usar um prefixo para todas as suas classes e atributos. Para obter mais informações, consulte [Nomeando atributos e classes](naming-attributes-and-classes.md). Além disso, o script só saída os atributos necessários para os **objetos attributeSchema** e **classSchema** para o arquivo LDIF.
-   Lsetattcls.vbs é um arquivo VBScript que usa o script Myschemaext.ldf para adicionar os novos atributos e classes no script. Verifique se o mestre de esquema é capaz de ser gravado antes de executar o script.

## <a name="myschemaextldf"></a>MYSCHEMAEXT. Ldf

``` syntax
dn: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-CaseExactString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.65
attributeSyntax: 2.5.5.3
cn: My-Test-Attribute-CaseExactString
description: Test attribute of syntax CaseExactString used to show how to add a CaseExactString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeCaseExactString
distinguishedName: CN=My-Test-Attribute-CaseExactString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMSyntax: 27
name: My-Test-Attribute-CaseExactString
schemaIDGUID:: 6ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-FL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.614
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-FL
description: Test forward link attribute of syntax DN used to show how to add a forward link attribute. Back link is My-Test-Attribute-DN-BL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNFL
linkID: 1.2.840.113556.1.2.50
distinguishedName: CN=My-Test-Attribute-DN-FL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-FL
schemaIDGUID:: YGLudffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-BL
attributeID: 1.2.840.113556.1.4.7000.159.24.10.615
attributeSyntax: 2.5.5.1
cn: My-Test-Attribute-DN-BL
description: Test back link attribute of syntax DN used to show how to add a back link attribute. Forward link is My-Test-Attribute-DN-FL.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNBL
linkID: 1.2.840.113556.6.1234
distinguishedName: CN=My-Test-Attribute-DN-BL,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 127
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-BL
schemaIDGUID:: jFfbhffa0hGLEwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DN-Regular
attributeID: 1.2.840.113556.1.4.7000.159.24.10.613
attributeSyntax: 2.5.5.12
cn: My-Test-Attribute-DN-Regular
description: Test attribute of syntax DN used to show how to add a DN attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNRegular
distinguishedName: CN=My-Test-Attribute-DN-Regular,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KwwCh3McAIVK
oMSyntax: 64
rangeLower: 0
rangeUpper: 257
name: My-Test-Attribute-DN-Regular
schemaIDGUID:: 5QSznA3W0hGBpwDAT7mMGg==
searchFlags: 0
 
dn: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
changetype: add
adminDisplayName: My-Test-Attribute-DNString
attributeID: 1.2.840.113556.1.4.7000.159.24.10.611
attributeSyntax: 2.5.5.14
cn: My-Test-Attribute-DNString
description: Test attribute of syntax DNString used to show how to add a DNString attribute.
isMemberOfPartialAttributeSet: FALSE
isSingleValued: TRUE
lDAPDisplayName: myTestAttributeDNString
distinguishedName: CN=My-Test-Attribute-DNString,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectCategory: CN=Attribute-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=com
objectClass: attributeSchema
oMObjectClass:: KoZIhvcUAQEBDA==
oMSyntax: 127
rangeLower: 1
rangeUpper: 64
name: My-Test-Attribute-DNString
schemaIDGUID:: 5ASznA3W0hGBpwDAT7mMGg==
searchFlags: 0

DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Auxiliary-Class1
description: Test class used to show how to add an auxiliary class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestAuxiliaryClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.11
instanceType: 4
objectClassCategory: 3
schemaIDGUID:: mmsxdsXb0hGL0AAA+HW2YA==
subClassOf: Top
mayContain: my-Test-Attribute-DNString
mustContain: description
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
 
dn: CN=My-Test-Structural-Class1,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
changetype: add
adminDisplayName: My-Test-Structural-Class1
auxiliaryClass: myTestAuxiliaryClass1
defaultHidingValue: FALSE
defaultObjectCategory: CN=Organizational-Unit,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
defaultSecurityDescriptor: D:(A;;RPWPCRCCDCLCLOLORCWOWDSDDTDTSW;;;DA)(A;;RPWPCRCCDCLCLORCWOWDSDDTSW;;;SY)(A;;RPLCLORC;;;AU)
admindescription: Test class used to show how to add a structure class.
objectCategory: CN=Class-Schema,CN=Schema,CN=Configuration,DC=Fabrikam,DC=com
objectClass: classSchema
lDAPDisplayName: myTestStructuralClass1
governsID: 1.2.840.113556.1.4.7000.159.24.10.611.12
mayContain: myTestAttributeDNFL
mayContain: wWWHomePage
mustContain: url
instanceType: 4
objectClassCategory: 1
possSuperiors: organizationalUnit
rDNAttID: ou
schemaIDGUID:: 1HsnsL7b0hGL0AAA+HW2YA==
subClassOf: organizationalUnit
 
DN:
changetype: modify
add: schemaUpdateNow
schemaUpdateNow: 1
-
```

## <a name="lgetattclsvbs"></a>LGETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''
' Bind to server object and get the
' reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext1.ldf"
sFromDN = sSchema
sToDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sAttrPrefix = "My-Test"
sFilter = "(&((cn=" & sAttrPrefix & "*)(|(objectCategory=classSchema)_
(objectCategory=attributeSchema))))"
sRetAttr = "dn,adminDescription,adminDisplayName,governsID,cn,mayContain,_
mustContain,systemMayContain,systemMustContain,lDAPDisplayName,_
objectClassCategory,distinguishedName,objectCategory,objectClass,_
possSuperiors,systemPossSuperiors,subClassOf,defaultObjectCategory,_
name,schemaIDGUID,auxiliaryClass,auxiliaryClass,systemAuxiliaryClass,_
description,defaultHidingValue,rDNAttId,defaultSecurityDescriptor,_
attributeID,attributeSecurityGUID,attributeSyntax,_
isMemberOfPartialAttributeSet,isSingleValued,mAPIID,oMSyntax,rangeLower,_
rangeUpper,searchFlags,oMObjectClass,linkID"
 
' Add flag rootDN.
sCommand = "ldifde -d " & sSchema 
sCommand = sCommand & " -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
' Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for attributes.
sCommand = sCommand & " -r " & sFilter
' Add flag for attributes to return.
sCommand = sCommand & " -l " & sRetAttr
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText) strText = "Error 0x"_
 & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



## <a name="lsetattclsvbs"></a>LSETATTCLS.VBS


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
'''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the Schema
'''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the Schema container
'''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to Schema"
End If
''''''''''''''''''''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the schema master.
''''''''''''''''''''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
'''''''''''''''''''''''''''
' fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get parent
'''''''''''''''''''''''''''
Set NTDS = GetObject(sPrefix & sMaster)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for NTDS"
End If
sServer = NTDS.Parent
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::get_Parent method"
End If
''''''''''''''''''''''''
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("serverReference")
'''''''''''''''''''''
' Display the DN for the computer object.
'''''''''''''''''''''
sComputerDNSName = Server.Get("DNSHostName")
' strText = "Schema Master has the following DN: "& sComputer
strText = "Schema Master has the following DNS Name: "& sComputerDNSName
WScript.echo strText
 
sFile = "myschemaext.ldf"
sFromDN = "CN=Schema,CN=Configuration,DC=myorg,DC=com"
sToDN = sSchema
' Add flag replace fromDN with ToDN.
sCommand = "ldifde -i -k -c " & sFromDN & " " & sToDN
' Add flag schema master.
sCommand = sCommand & " -s " & sComputerDNSName
'Add flag filename.
sCommand = sCommand & " -f " & sFile
' Add flag filter to search for my attributes.
 
WScript.echo sCommand
Set WshShell = Wscript.CreateObject("Wscript.Shell")
WshShell.Run (sCommand)
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 





