---
title: Suporte de associação antecipada
description: O exemplo de código a seguir apresenta um cenário com suporte de associação antecipada em vigor.
ms.assetid: 3ca955cc-a9cd-4309-8617-89fe50b65c3d
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, suporte de ligação antecipada
- Associação de anúncio, suporte de associação antecipada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be6980edb0395ad0139f9cf2e4a1f9cde3ff6077
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104084893"
---
# <a name="early-binding-support"></a><span data-ttu-id="84024-105">Suporte de associação antecipada</span><span class="sxs-lookup"><span data-stu-id="84024-105">Early Binding Support</span></span>

<span data-ttu-id="84024-106">O exemplo de código a seguir apresenta um cenário com suporte de associação antecipada em vigor.</span><span class="sxs-lookup"><span data-stu-id="84024-106">The following code example presents a scenario with early binding support in place.</span></span>


```VB
Dim x as IADsUser
Dim y as IADsExt1
Dim z as IADsExt2
 
Set x = GetObject("LDAP://CN=JeffSmith, OU=Sales, 
                   DC=Fabrikam,DC=COM")
x.SetPassword("newPassword")
 
Set y = x
y.MyNewMethod( "\\srv\public")
y.MyProperty = "Hello World"
 
Set z = y
z.OtherMethod()
z.OtherProperty = 4362
 
Debug.Print x.LastName
 
Set z = GetObject("LDAP://CN=Jeff,OU=Engr, 
                   DC=Fabrikam,DC=COM")
z.OtherProperty = 5323
```



<span data-ttu-id="84024-107">Neste exemplo de código, dois componentes de extensão estendem um objeto de **usuário** .</span><span class="sxs-lookup"><span data-stu-id="84024-107">In this code example, two extension components extend a **user** object.</span></span> <span data-ttu-id="84024-108">Cada extensão publica sua própria interface.</span><span class="sxs-lookup"><span data-stu-id="84024-108">Each extension publishes its own interface.</span></span> <span data-ttu-id="84024-109">Cada extensão não reconhece a outra interface de extensão; somente ADSI reconhece a existência de ambas as extensões.</span><span class="sxs-lookup"><span data-stu-id="84024-109">Each extension does not recognize the other extension interface; only ADSI recognizes the existence of both extensions.</span></span> <span data-ttu-id="84024-110">Cada extensão Delega seu [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) a ADSI.</span><span class="sxs-lookup"><span data-stu-id="84024-110">Each extension delegates its [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to ADSI.</span></span> <span data-ttu-id="84024-111">A ADSI atua como um agregador para ambas as extensões e outras extensões futuras.</span><span class="sxs-lookup"><span data-stu-id="84024-111">ADSI acts as an aggregator for both extensions, and any other future extensions.</span></span> <span data-ttu-id="84024-112">Consultar uma interface de qualquer extensão ou de ADSI, produz o mesmo resultado consistente.</span><span class="sxs-lookup"><span data-stu-id="84024-112">Querying an interface from any extension, or from ADSI, yields the same consistent result.</span></span>

<span data-ttu-id="84024-113">O procedimento a seguir descreve como criar uma extensão.</span><span class="sxs-lookup"><span data-stu-id="84024-113">The following procedure describes how to create an extension.</span></span>

## <a name="step-1-add-aggregation-to-your-component"></a><span data-ttu-id="84024-114">Etapa 1: Adicionar agregação ao seu componente</span><span class="sxs-lookup"><span data-stu-id="84024-114">Step 1: Add Aggregation to Your Component</span></span>

<span data-ttu-id="84024-115">Siga a especificação COM para adicionar agregação ao seu componente.</span><span class="sxs-lookup"><span data-stu-id="84024-115">Follow the COM specification for adding aggregation to your component.</span></span> <span data-ttu-id="84024-116">Em resumo, você deve aceitar as solicitações *pUnknown* para o componente durante **CreateInstance** e delegar o *pUnknown* ao [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) do agregador se o componente for agregado.</span><span class="sxs-lookup"><span data-stu-id="84024-116">In summary, you must accept the *pUnknown* requests to your component during **CreateInstance**, and delegate the *pUnknown* to the aggregator's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) if the component is aggregated.</span></span>

## <a name="step-2-register-your-extension"></a><span data-ttu-id="84024-117">Etapa 2: registrar sua extensão</span><span class="sxs-lookup"><span data-stu-id="84024-117">Step 2: Register Your Extension</span></span>

<span data-ttu-id="84024-118">Agora você deve decidir qual classe de diretório estender.</span><span class="sxs-lookup"><span data-stu-id="84024-118">Now you must decide which directory class to extend.</span></span> <span data-ttu-id="84024-119">Não é possível usar as mesmas interfaces para fazer isso que você usaria para uma interface ADSI, por exemplo, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span><span class="sxs-lookup"><span data-stu-id="84024-119">You cannot use the same interfaces to accomplish this that you would use for an ADSI interface, for example, [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser), [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer).</span></span> <span data-ttu-id="84024-120">Os objetos de diretório são mantidos no diretório, enquanto a extensão e a ADSI estão em execução no computador cliente.</span><span class="sxs-lookup"><span data-stu-id="84024-120">Directory objects are persisted in the directory, while your extension and ADSI are running on the client computer.</span></span> <span data-ttu-id="84024-121">Os exemplos de objeto de diretório são **User**, **Computer**, **PrintQueue**, **serviceConnectionPoint** e **nTDSService**.</span><span class="sxs-lookup"><span data-stu-id="84024-121">Directory object examples are **user**, **computer**, **printQueue**, **serviceConnectionPoint**, and **nTDSService**.</span></span> <span data-ttu-id="84024-122">Você pode adicionar uma nova classe em Active Directory e criar uma nova extensão para essa nova classe também.</span><span class="sxs-lookup"><span data-stu-id="84024-122">You can add a new class in Active Directory and create a new extension for this new class as well.</span></span>

<span data-ttu-id="84024-123">Você usa chaves do registro para associar um nome de classe de diretório com os componentes de extensão ADSI.</span><span class="sxs-lookup"><span data-stu-id="84024-123">You use registry keys to associate a directory class name with the ADSI extension components.</span></span> <span data-ttu-id="84024-124">A figura a seguir representa o layout de registro existente, bem como novas chaves.</span><span class="sxs-lookup"><span data-stu-id="84024-124">The following figure represents the existing registry layout, as a well as new keys.</span></span>

-   <span data-ttu-id="84024-125">Uma nova chave, chamada **extensões**, contém uma lista de chaves, cada uma representando uma classe no diretório.</span><span class="sxs-lookup"><span data-stu-id="84024-125">A new key, called **Extensions**, contains a list of keys, each of which represents a class in the directory.</span></span> <span data-ttu-id="84024-126">Cada classe, por exemplo, **User**, **PrintQueue** ou **Computer**, mantém uma lista de subchaves.</span><span class="sxs-lookup"><span data-stu-id="84024-126">Each class, for example, **user**, **printQueue**, or **computer**, maintains a list of subkeys.</span></span>
-   <span data-ttu-id="84024-127">Cada subchave contém o CLSID do componente de extensão ADSI.</span><span class="sxs-lookup"><span data-stu-id="84024-127">Each subkey contains the CLSID of the ADSI extension component.</span></span>
-   <span data-ttu-id="84024-128">Cada subchave CLSID contém uma entrada de cadeia de caracteres que permite vários valores.</span><span class="sxs-lookup"><span data-stu-id="84024-128">Each CLSID subkey contains a string entry that allows multiple values.</span></span> <span data-ttu-id="84024-129">Você só deve listar as interfaces que participam da agregação.</span><span class="sxs-lookup"><span data-stu-id="84024-129">You should only list the interfaces that participate in the aggregation.</span></span>

> [!Note]  
> <span data-ttu-id="84024-130">Os objetos de extensão ainda são necessários para registrar chaves COM padrão.</span><span class="sxs-lookup"><span data-stu-id="84024-130">Extension objects are still required to register standard COM keys.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         ADS
            Providers
               LDAP
                  Extensions
                     ClassNameA
                        CLSID of ExtensionA1
                           Interfaces = List of interfaces
                        CLSID of ExtensionA2
                           Interfaces = List of interfaces
                     ClassNameB
                        CLSID of ExtensionB1
                           Interfaces = List of interfaces
                        CLSID of ExtensionB2
                           Interfaces = List of interfaces
```

## <a name="example"></a><span data-ttu-id="84024-131">Exemplo</span><span class="sxs-lookup"><span data-stu-id="84024-131">Example</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         ADs
            Providers
               LDAP
                  Extensions
                     printQueue
                        {9f37f39c-6f49-11d1-8c18-00c04fd8d503}
                           Interfaces = {466841B0-E531-11d1-8718-00C04FD44407}
                                        {466841B1-E531-11d1-8718-00C04FD44407}
```

<span data-ttu-id="84024-132">A lista de interfaces do Extension1 pode ser diferente da do Extension2.</span><span class="sxs-lookup"><span data-stu-id="84024-132">The list of interfaces from Extension1 can be different from that of Extension2.</span></span> <span data-ttu-id="84024-133">O objeto, quando ativo, dá suporte às interfaces do agregador (ADSI) e a todas as interfaces fornecidas pelo Extension1 e Extension2 da agregação.</span><span class="sxs-lookup"><span data-stu-id="84024-133">The object, when active, supports the interfaces of the aggregator (ADSI) and all the interfaces provided by the aggregate's Extension1 and Extension2.</span></span> <span data-ttu-id="84024-134">A resolução de interfaces conflitantes (a mesma interface com suporte tanto pelo agregador quanto pelas agregações ou por várias agregações) é determinada pelas prioridades das extensões.</span><span class="sxs-lookup"><span data-stu-id="84024-134">Resolution of conflicting interfaces (the same interface supported by both the aggregator and the aggregates or by multiple aggregates) is determined by priorities of the extensions.</span></span>

<span data-ttu-id="84024-135">Você também pode associar sua extensão CLSID a vários nomes de classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="84024-135">You can also associate your CLSID extension with multiple object class names.</span></span> <span data-ttu-id="84024-136">Por exemplo, sua extensão pode estender os objetos de **usuário** e de **contato** .</span><span class="sxs-lookup"><span data-stu-id="84024-136">For example, your extension can extend both the **user** and **contact** objects.</span></span>

> [!Note]  
> <span data-ttu-id="84024-137">O comportamento da extensão é adicionado em uma classe por objeto, não em uma instância por objeto.</span><span class="sxs-lookup"><span data-stu-id="84024-137">Extension behavior is added on a per-object class, not on a per-object instance.</span></span>

 

<span data-ttu-id="84024-138">Como prática recomendada, registre suas extensões, como você faria com qualquer outro componente COM, com uma chamada para a função **DllRegisterSvr** .</span><span class="sxs-lookup"><span data-stu-id="84024-138">As a best practice, register your extensions, as you would any other COM components, with a call to the **DllRegisterSvr** function.</span></span> <span data-ttu-id="84024-139">Além disso, forneça um recurso para cancelar o registro de sua extensão com a função **DllUnregisterServer** .</span><span class="sxs-lookup"><span data-stu-id="84024-139">Also provide a facility to unregister your extension with the **DllUnregisterServer** function.</span></span>

<span data-ttu-id="84024-140">O exemplo de código a seguir mostra como registrar uma extensão.</span><span class="sxs-lookup"><span data-stu-id="84024-140">The following code example shows how to register an extension.</span></span>


```C++
/////
// Register the class.
///////////////////////
hr = RegCreateKeyEx( HKEY_LOCAL_MACHINE,
                 _T("SOFTWARE\\Microsoft\\ADs\\Providers\\LDAP\\Extensions\\User\\{E1E3EDF8-48D1-11D2-B22B-0000F87A6B50}"),
 0,
 NULL,
 REG_OPTION_NON_VOLATILE,
 KEY_WRITE,
 NULL,
 &hKey,
 &dwDisposition );
 
///////////////////////////
// Register the Interface.
///////////////////////////
const TCHAR szIf[] = _T("{E1E3EDF7-48D1-11D2-B22B-0000F87A6B50}");
 
hr = RegSetValueEx( hKey, _T("Interfaces"), 0, REG_BINARY, (const BYTE *) szIf, sizeof(szIf) );
 
RegCloseKey(hKey);
return S_OK;
 
}
```



 

 