---
title: Detectando o mestre de esquema
description: Active Directory Domain Services ter um sistema de atualização com vários mestres; cada controlador de domínio mantém uma cópia gravável do diretório.
ms.assetid: 8e096351-43f8-48ee-acb6-681d9e38e93c
ms.tgt_platform: multiple
keywords:
- Detectando o AD mestre de esquema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6869853cba68d7155f2091e2fe4515116944a629
ms.sourcegitcommit: f730b85cc85448913e50a7f331e10b646ea7978b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/23/2019
ms.locfileid: "103823085"
---
# <a name="detecting-the-schema-master"></a>Detectando o mestre de esquema

Active Directory Domain Services ter um sistema de atualização com vários mestres; cada controlador de domínio mantém uma cópia gravável do diretório. As atualizações de esquema são propagadas para todos os domínios que pertencem à mesma árvore ou floresta. Como é difícil reconciliar atualizações conflitantes para o esquema, as atualizações de esquema só podem ser executadas em um único servidor. O servidor com o direito de executar atualizações pode ser alterado, mas apenas um servidor terá esse direito em um determinado momento. Esse servidor é chamado de mestre de esquema. O primeiro DC instalado em uma empresa é, por padrão, o mestre de esquema.

As alterações de esquema só podem ser feitas no nível do mestre de esquema. Para detectar qual DC é o mestre de esquema, execute as etapas a seguir.

**Detectando o mestre de esquema de DC**

1.  Leia o atributo **fSMORoleOwner** do contêiner de esquema em qualquer DC. O atributo **fSMORoleOwner** retorna o DN (nome distinto) do objeto **nTDSDSA** para o mestre de esquema.
2.  Associe-se ao objeto **nTDSDSA** cujo DN você acabou de recuperar. O pai desse objeto é o objeto de servidor para o controlador de domínio que contém o mestre de esquema.
3.  Obtenha o ADsPath para o pai do objeto **nTDSDSA** . O pai é um objeto de servidor.
4.  Associar ao objeto de servidor.
5.  Obtenha o atributo **dNSHostName** do objeto Server. Esse é o nome DNS do controlador de domínio que contém o mestre de esquema.
6.  Especifique o nome DNS do mestre de esquema como o servidor e o DN como o DN do contêiner de esquema a ser associado ao mestre de esquema. Por exemplo, se o servidor era "dc1.fabrikam.com" e o DN do contêiner de esquema era "CN = Schema, CN = Configuration, DC = Fabrikam, DC = com", o ADsPath seria o seguinte.
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

É recomendável que você encontre o mestre de esquema e associe-o a ele para fazer alterações de esquema. No entanto, você pode mover o mestre de esquema para outro servidor.

Para tornar outro servidor o mestre de esquema, um usuário com privilégios adequado pode:

-   Use o snap-in do MMC do Gerenciador de esquema.
    > [!Note]
    > O snap-in do MMC do esquema de Active Directory deve ser registrado manualmente. Para registrar o snap-in de esquema, você deve executar o comando a seguir no prompt de comando no diretório Windows system32.
    >
    > **regsvr32.exe schmmgmt.dll**

     

-   Use o utilitário de linha de comando NTDSUTIL.
-   Use um aplicativo de terceiros (um aplicativo que emite a gravação LDAP apropriada).

Para se tornar o mestre de esquema programaticamente, um aplicativo em execução no contexto de um usuário com privilégios adequado pode emitir uma gravação LDAP do atributo operacional **becomeSchemaMaster** para o ROOTDSE nesse DC. Isso inicia uma transferência atômica do mestre de esquema diretamente do detentor atual para o DC local.

O exemplo de código a seguir localiza o mestre de esquema. A função a seguir é associada ao contêiner de esquema no computador que é o mestre de esquema.


```C++
HRESULT BindToSchemaMaster(IADsContainer **ppSchemaMaster)
{
HRESULT hr = E_FAIL;
// Get rootDSE and the schema container DN.
IADs *pObject = NULL;
IADs *pTempSchema = NULL;
IADs *pNTDS = NULL;
IADs *pServer = NULL;
BSTR bstrParent;
LPOLESTR szPath = new OLECHAR[MAX_PATH];
VARIANT var, varRole,varComputer;
hr = ADsOpenObject(L"LDAP://rootDSE",
         NULL,
         NULL,
         ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
         IID_IADs,
         (void**)&pObject);
if (hr == S_OK)
{
  hr = pObject->Get(CComBSTR("schemaNamingContext"), &var);
  if (hr == S_OK)
  {
    wcscpy_s(szPath,L"LDAP://");
    wcscat_s(szPath,var.bstrVal);
    hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION, // Use Secure Authentication.
             IID_IADs,
             (void**)&pTempSchema);
 
    if (hr == S_OK)
    {
      /*
      Read the fsmoRoleOwner attribute to identify which server is 
      the schema master.
      */  
      hr = pTempSchema->Get(CComBSTR("fsmoRoleOwner"), &varRole);
      if (hr == S_OK)
      {
        // The fsmoRoleOwner attribute returns the nTDSDSA object.
        // The parent is the server object.
        // Bind to NTDSDSA object and get parent.
        wcscpy_s(szPath,L"LDAP://");
        wcscat_s(szPath,varRole.bstrVal);
        hr = ADsOpenObject(szPath,
             NULL,
             NULL,
             ADS_SECURE_AUTHENTICATION,
             IID_IADs,
             (void**)&pNTDS);
        if (hr == S_OK)
        {
          hr = pNTDS->get_Parent(&bstrParent);
          if (hr == S_OK)
          {
            /*
            Bind to server object and get the DNS name of 
            the server.
            */
            wcscpy_s(szPath,bstrParent);
            hr = ADsOpenObject(szPath,
               NULL,
               NULL,
               ADS_SECURE_AUTHENTICATION,
               IID_IADs,
               (void**)&pServer);
            if (hr == S_OK)
            {
              // Get the dns name of the server.
              hr = pServer->Get(CComBSTR("dNSHostName"), 
                  &varComputer);
              if (hr == S_OK)
              {
                    wcscpy_s(szPath,L"LDAP://");
                    wcscat_s(szPath,varComputer.bstrVal);
                    wcscat_s(szPath,L"/");
                    wcscat_s(szPath,var.bstrVal);
                    hr = ADsOpenObject(szPath,
                         NULL,
                         NULL,
                         ADS_SECURE_AUTHENTICATION,
                         IID_IADs,
                         (void**)ppSchemaMaster);
                    if (FAILED(hr))
                    {
                      if (*ppSchemaMaster)
                      {
                        (*ppSchemaMaster)->Release();
                        (*ppSchemaMaster) = NULL;
                      }
                    }
              }
              VariantClear(&varComputer);
            }
            if (pServer)
              pServer->Release();
          }
          SysFreeString(bstrParent);
        }
        if (pNTDS)
          pNTDS->Release();
      }
      VariantClear(&varRole);
    }
    if (pTempSchema)
      pTempSchema->Release();
  }
  VariantClear(&var);
}
if (pObject)
    pObject->Release();
 
return hr;
}
```



O exemplo de código a seguir exibe o nome DNS para o computador que é o mestre de esquema.


```VB
On Error Resume Next
 
'''''''''''''''''''
' Bind to the rootDSE
''''''''''''''''''''
sPrefix = "LDAP://"
Set root= GetObject(sPrefix & "rootDSE")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method"
End If
 
'''''''''''''''''''
' Get the DN for the schema
''''''''''''''''''''
sSchema = root.Get("schemaNamingContext")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on Get method"
End If
 
'''''''''''''''''''
' Bind to the schema container
''''''''''''''''''''
Set Schema= GetObject(sPrefix & sSchema )
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method to bind to schema"
End If
''''''''''''''''''''
' Read the fsmoRoleOwner attribute to see which server is the 
' schema master.
''''''''''''''''''''
sMaster = Schema.Get("fsmoRoleOwner")
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on IADs::Get method for fsmoRoleOwner"
End If
''''''''''''''''''''
' The fsmoRoleOwner attribute returns the nTDSDSA object.
' The parent is the server object.
' Bind to NTDSDSA object and get the parent object.
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
' Bind to server object
' and get the reference to the computer object.
''''''''''''''''''''
Set Server = GetObject(sServer)
If (Err.Number <> 0) Then
   BailOnFailure Err.Number, "on GetObject method for " & sServer
End If
sComputer = Server.Get("dNSHostName")
''''''''''''''''''''
' Display the DNS name for the computer.
''''''''''''''''''''
strText = "Schema master has the following DNS name: "& sComputer
WScript.echo strText
 
 
 
''''''''''''''''''''
' Display subroutines
''''''''''''''''''''
 
Sub BailOnFailure(ErrNum, ErrText)
    strText = "Error 0x" & Hex(ErrNum) & " " & ErrText
    MsgBox strText, vbInformation, "ADSI Error"
    WScript.Quit
End Sub
```



 

 




