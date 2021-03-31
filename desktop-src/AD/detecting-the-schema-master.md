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
# <a name="detecting-the-schema-master"></a><span data-ttu-id="c3a75-104">Detectando o mestre de esquema</span><span class="sxs-lookup"><span data-stu-id="c3a75-104">Detecting the Schema Master</span></span>

<span data-ttu-id="c3a75-105">Active Directory Domain Services ter um sistema de atualização com vários mestres; cada controlador de domínio mantém uma cópia gravável do diretório.</span><span class="sxs-lookup"><span data-stu-id="c3a75-105">Active Directory Domain Services have a multi-master update system; every domain controller holds a writable copy of the directory.</span></span> <span data-ttu-id="c3a75-106">As atualizações de esquema são propagadas para todos os domínios que pertencem à mesma árvore ou floresta.</span><span class="sxs-lookup"><span data-stu-id="c3a75-106">Schema updates are propagated to all domains that belong to the same tree or forest.</span></span> <span data-ttu-id="c3a75-107">Como é difícil reconciliar atualizações conflitantes para o esquema, as atualizações de esquema só podem ser executadas em um único servidor.</span><span class="sxs-lookup"><span data-stu-id="c3a75-107">Because it is difficult to reconcile conflicting updates to the schema, schema updates can only be performed at a single server.</span></span> <span data-ttu-id="c3a75-108">O servidor com o direito de executar atualizações pode ser alterado, mas apenas um servidor terá esse direito em um determinado momento.</span><span class="sxs-lookup"><span data-stu-id="c3a75-108">The server with the right to perform updates can change, but only one server will have that right at any given time.</span></span> <span data-ttu-id="c3a75-109">Esse servidor é chamado de mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-109">This server is called the schema master.</span></span> <span data-ttu-id="c3a75-110">O primeiro DC instalado em uma empresa é, por padrão, o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-110">The first DC installed in an enterprise is, by default, the schema master.</span></span>

<span data-ttu-id="c3a75-111">As alterações de esquema só podem ser feitas no nível do mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-111">Schema changes can only be made at the schema master level.</span></span> <span data-ttu-id="c3a75-112">Para detectar qual DC é o mestre de esquema, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c3a75-112">To detect which DC is the schema master, perform the following steps.</span></span>

<span data-ttu-id="c3a75-113">**Detectando o mestre de esquema de DC**</span><span class="sxs-lookup"><span data-stu-id="c3a75-113">**Detecting the DC Schema Master**</span></span>

1.  <span data-ttu-id="c3a75-114">Leia o atributo **fSMORoleOwner** do contêiner de esquema em qualquer DC.</span><span class="sxs-lookup"><span data-stu-id="c3a75-114">Read the **fsmoRoleOwner** attribute of the schema container on any DC.</span></span> <span data-ttu-id="c3a75-115">O atributo **fSMORoleOwner** retorna o DN (nome distinto) do objeto **nTDSDSA** para o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-115">The **fsmoRoleOwner** attribute returns the distinguished name (DN) of the **nTDSDSA** object for the schema master.</span></span>
2.  <span data-ttu-id="c3a75-116">Associe-se ao objeto **nTDSDSA** cujo DN você acabou de recuperar.</span><span class="sxs-lookup"><span data-stu-id="c3a75-116">Bind to the **nTDSDSA** object whose DN you just retrieved.</span></span> <span data-ttu-id="c3a75-117">O pai desse objeto é o objeto de servidor para o controlador de domínio que contém o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-117">The parent of this object is the server object for the DC containing the schema master.</span></span>
3.  <span data-ttu-id="c3a75-118">Obtenha o ADsPath para o pai do objeto **nTDSDSA** .</span><span class="sxs-lookup"><span data-stu-id="c3a75-118">Get the ADsPath for the parent of the **nTDSDSA** object.</span></span> <span data-ttu-id="c3a75-119">O pai é um objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="c3a75-119">The parent is a server object.</span></span>
4.  <span data-ttu-id="c3a75-120">Associar ao objeto de servidor.</span><span class="sxs-lookup"><span data-stu-id="c3a75-120">Bind to the server object.</span></span>
5.  <span data-ttu-id="c3a75-121">Obtenha o atributo **dNSHostName** do objeto Server.</span><span class="sxs-lookup"><span data-stu-id="c3a75-121">Get the **dNSHostName** attribute of the server object.</span></span> <span data-ttu-id="c3a75-122">Esse é o nome DNS do controlador de domínio que contém o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-122">This is the DNS name of the DC that contains the schema master.</span></span>
6.  <span data-ttu-id="c3a75-123">Especifique o nome DNS do mestre de esquema como o servidor e o DN como o DN do contêiner de esquema a ser associado ao mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-123">Specify the DNS name of the schema master as the server and the DN as the DN of the schema container to bind to the schema master.</span></span> <span data-ttu-id="c3a75-124">Por exemplo, se o servidor era "dc1.fabrikam.com" e o DN do contêiner de esquema era "CN = Schema, CN = Configuration, DC = Fabrikam, DC = com", o ADsPath seria o seguinte.</span><span class="sxs-lookup"><span data-stu-id="c3a75-124">For example, if the server was "dc1.fabrikam.com" and the schema container DN was "cn=schema,cn=configuration,dc=fabrikam,dc=com", the ADsPath would be as follows.</span></span>
    ```C++
    LDAP://dc1.fabrikam.com/cn=schema,cn=configuration,dc=fabrikam,dc=com
    ```

    

<span data-ttu-id="c3a75-125">É recomendável que você encontre o mestre de esquema e associe-o a ele para fazer alterações de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-125">It is recommended that you find the schema master and bind to it to make schema changes.</span></span> <span data-ttu-id="c3a75-126">No entanto, você pode mover o mestre de esquema para outro servidor.</span><span class="sxs-lookup"><span data-stu-id="c3a75-126">However, you can move the schema master to another server.</span></span>

<span data-ttu-id="c3a75-127">Para tornar outro servidor o mestre de esquema, um usuário com privilégios adequado pode:</span><span class="sxs-lookup"><span data-stu-id="c3a75-127">To make another server the schema master, a suitably privileged user can:</span></span>

-   <span data-ttu-id="c3a75-128">Use o snap-in do MMC do Gerenciador de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-128">Use the Schema Manager MMC snap-in.</span></span>
    > [!Note]
    > <span data-ttu-id="c3a75-129">O snap-in do MMC do esquema de Active Directory deve ser registrado manualmente.</span><span class="sxs-lookup"><span data-stu-id="c3a75-129">The Active Directory Schema MMC snap-in must be registered manually.</span></span> <span data-ttu-id="c3a75-130">Para registrar o snap-in de esquema, você deve executar o comando a seguir no prompt de comando no diretório Windows system32.</span><span class="sxs-lookup"><span data-stu-id="c3a75-130">To register the Schema snap-in, you must run the following command from the command prompt in the Windows System32 directory.</span></span>
    >
    > <span data-ttu-id="c3a75-131">**regsvr32.exe schmmgmt.dll**</span><span class="sxs-lookup"><span data-stu-id="c3a75-131">**regsvr32.exe schmmgmt.dll**</span></span>

     

-   <span data-ttu-id="c3a75-132">Use o utilitário de linha de comando NTDSUTIL.</span><span class="sxs-lookup"><span data-stu-id="c3a75-132">Use the NTDSUTIL command-line utility.</span></span>
-   <span data-ttu-id="c3a75-133">Use um aplicativo de terceiros (um aplicativo que emite a gravação LDAP apropriada).</span><span class="sxs-lookup"><span data-stu-id="c3a75-133">Use a third-party application (an application that issues the appropriate LDAP write).</span></span>

<span data-ttu-id="c3a75-134">Para se tornar o mestre de esquema programaticamente, um aplicativo em execução no contexto de um usuário com privilégios adequado pode emitir uma gravação LDAP do atributo operacional **becomeSchemaMaster** para o ROOTDSE nesse DC.</span><span class="sxs-lookup"><span data-stu-id="c3a75-134">To become the schema master programmatically, an application running in the context of a suitably privileged user can issue an LDAP write of the operational attribute **becomeSchemaMaster** to the rootDSE on that DC.</span></span> <span data-ttu-id="c3a75-135">Isso inicia uma transferência atômica do mestre de esquema diretamente do detentor atual para o DC local.</span><span class="sxs-lookup"><span data-stu-id="c3a75-135">This initiates an atomic transfer of the schema master right from the current holder to the local DC.</span></span>

<span data-ttu-id="c3a75-136">O exemplo de código a seguir localiza o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-136">The following code example finds the schema master.</span></span> <span data-ttu-id="c3a75-137">A função a seguir é associada ao contêiner de esquema no computador que é o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-137">The following function binds to the schema container on the computer that is the schema master.</span></span>


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



<span data-ttu-id="c3a75-138">O exemplo de código a seguir exibe o nome DNS para o computador que é o mestre de esquema.</span><span class="sxs-lookup"><span data-stu-id="c3a75-138">The following code example displays the DNS name for the computer that is the schema master.</span></span>


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



 

 




