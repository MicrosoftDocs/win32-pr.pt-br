---
description: Uma recuperação de instância parcial é quando o WMI recupera apenas um subconjunto das propriedades de uma instância.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Recuperando parte de uma instância do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d9d547ec2bbb7e3b53e22177cc0c48794dff22a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165214"
---
# <a name="retrieving-part-of-a-wmi-instance"></a><span data-ttu-id="dac3d-103">Recuperando parte de uma instância do WMI</span><span class="sxs-lookup"><span data-stu-id="dac3d-103">Retrieving Part of a WMI Instance</span></span>

<span data-ttu-id="dac3d-104">Uma recuperação de instância parcial é quando o WMI recupera apenas um subconjunto das propriedades de uma instância.</span><span class="sxs-lookup"><span data-stu-id="dac3d-104">A partial-instance retrieval is when WMI retrieves only a subset of the properties of an instance.</span></span> <span data-ttu-id="dac3d-105">Por exemplo, o WMI pode recuperar apenas as propriedades **Name** e **Key** .</span><span class="sxs-lookup"><span data-stu-id="dac3d-105">For example, WMI could retrieve only the **Name** and **Key** properties.</span></span> <span data-ttu-id="dac3d-106">O uso mais comum da recuperação de instância parcial é em enumerações grandes que têm várias propriedades.</span><span class="sxs-lookup"><span data-stu-id="dac3d-106">The most common use of partial-instance retrieval is on large enumerations that have multiple properties.</span></span>

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a><span data-ttu-id="dac3d-107">Recuperando parte de uma instância do WMI usando o PowerShell</span><span class="sxs-lookup"><span data-stu-id="dac3d-107">Retrieving Part of a WMI Instance Using PowerShell</span></span>

<span data-ttu-id="dac3d-108">Você pode recuperar uma propriedade individual de uma instância usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); a própria propriedade pode ser recuperada e exibida de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="dac3d-108">You can retrieve an individual property of an instance by using [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); the property itself can be retrieved and displayed a number of ways.</span></span> <span data-ttu-id="dac3d-109">Assim como na recuperação de uma instância, o PowerShell retornará, por padrão, todas as instâncias de uma determinada classe; Você deve especificar um valor específico se desejar recuperar apenas uma única instância.</span><span class="sxs-lookup"><span data-stu-id="dac3d-109">As with retrieving an instance, PowerShell will by default return all instances of a given class; you must specify a specific value if you wish to retrieve only a single instance.</span></span>

<span data-ttu-id="dac3d-110">O exemplo de código a seguir exibe o número de série do volume para uma instância da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="dac3d-110">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a><span data-ttu-id="dac3d-111">Recuperando parte de uma instância do WMI usando C# (System. Management)</span><span class="sxs-lookup"><span data-stu-id="dac3d-111">Retrieving Part of a WMI Instance Using C# (System.Management)</span></span>

<span data-ttu-id="dac3d-112">Você pode recuperar uma propriedade individual de uma instância criando um novo [ManagementObject](/dotnet/api/system.management.managementobject) usando os detalhes de uma instância específica.</span><span class="sxs-lookup"><span data-stu-id="dac3d-112">You can retrieve an individual property of an instance by creating a new [ManagementObject](/dotnet/api/system.management.managementobject) using the details of a specific instance.</span></span> <span data-ttu-id="dac3d-113">Em seguida, você pode recuperar implicitamente uma ou mais propriedades da instância com o método [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) .</span><span class="sxs-lookup"><span data-stu-id="dac3d-113">You can then implicitly retrieve one or more properties of the instance with the [GetPropertyValue](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_) method.</span></span>

> [!Note]  
> <span data-ttu-id="dac3d-114">**System. Management** foi o namespace .net original usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são dimensionadas em relação às suas contrapartes mais modernas de **Microsoft. Management. Infrastructure** .</span><span class="sxs-lookup"><span data-stu-id="dac3d-114">**System.Management** was the original .NET namespace used to access WMI; however, the APIs in this namespace generally are slower and do not scale as well relative to their more modern **Microsoft.Management.Infrastructure** counterparts.</span></span>

 

<span data-ttu-id="dac3d-115">O exemplo de código a seguir exibe o número de série do volume para uma instância da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="dac3d-115">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a><span data-ttu-id="dac3d-116">Recuperando parte de uma instância do WMI usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="dac3d-116">Retrieving Part of a WMI Instance Using VBScript</span></span>

<span data-ttu-id="dac3d-117">Você pode recuperar uma propriedade individual de uma instância usando [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span><span class="sxs-lookup"><span data-stu-id="dac3d-117">You can retrieve an individual property of an instance by using [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).</span></span>

<span data-ttu-id="dac3d-118">O exemplo de código a seguir exibe o número de série do volume para uma instância da classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="dac3d-118">The following code example displays the volume serial number for an instance of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a><span data-ttu-id="dac3d-119">Recuperando parte de uma instância do WMI usando C++</span><span class="sxs-lookup"><span data-stu-id="dac3d-119">Retrieving Part of a WMI Instance Using C++</span></span>

<span data-ttu-id="dac3d-120">O procedimento a seguir é usado para solicitar uma recuperação de instância parcial usando C++.</span><span class="sxs-lookup"><span data-stu-id="dac3d-120">The following procedure is used to request a partial-instance retrieval using C++.</span></span>

<span data-ttu-id="dac3d-121">**Para solicitar uma recuperação de instância parcial usando C++**</span><span class="sxs-lookup"><span data-stu-id="dac3d-121">**To request a partial-instance retrieval using C++**</span></span>

1.  <span data-ttu-id="dac3d-122">Crie um objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="dac3d-122">Create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    <span data-ttu-id="dac3d-123">Um objeto de contexto é um objeto que o WMI usa para passar mais informações para um provedor WMI.</span><span class="sxs-lookup"><span data-stu-id="dac3d-123">A context object is an object that WMI uses to pass in more information to a WMI provider.</span></span> <span data-ttu-id="dac3d-124">Nesse caso, você está usando o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para instruir o provedor a processar uma recuperação de instância parcial.</span><span class="sxs-lookup"><span data-stu-id="dac3d-124">In this case, you are using the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object to instruct the provider to process a partial-instance retrieval.</span></span>

2.  <span data-ttu-id="dac3d-125">Adicione \_ \_ obter \_ extensões, \_ \_ obter \_ \_ solicitação de cliente ext \_ e quaisquer outros valores nomeados que descrevam as propriedades que você deseja recuperar para o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) .</span><span class="sxs-lookup"><span data-stu-id="dac3d-125">Add \_\_GET\_EXTENSIONS, \_\_GET\_EXT\_CLIENT\_REQUEST, and any other named values that describe the properties you want to retrieve to the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object.</span></span>

    <span data-ttu-id="dac3d-126">A tabela a seguir lista os valores nomeados diferentes usados na sua chamada de recuperação.</span><span class="sxs-lookup"><span data-stu-id="dac3d-126">The following table lists the different named values use in your retrieval call.</span></span>

    

    | <span data-ttu-id="dac3d-127">Valor nomeado</span><span class="sxs-lookup"><span data-stu-id="dac3d-127">Named value</span></span>                              | <span data-ttu-id="dac3d-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="dac3d-128">Description</span></span>                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="dac3d-129">\_\_OBTER \_ extensões</span><span class="sxs-lookup"><span data-stu-id="dac3d-129">\_\_GET\_EXTENSIONS</span></span><br/>           | <span data-ttu-id="dac3d-130">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="dac3d-130">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="dac3d-131">Usado para sinalizar que as operações de recuperação de instância parcial estão sendo usadas.</span><span class="sxs-lookup"><span data-stu-id="dac3d-131">Used to signal that partial-instance retrieval operations are being used.</span></span> <span data-ttu-id="dac3d-132">Isso permite uma verificação rápida e única sem a necessidade de enumerar o objeto de contexto inteiro.</span><span class="sxs-lookup"><span data-stu-id="dac3d-132">This allows a quick, single check without having to enumerate the entire context object.</span></span> <span data-ttu-id="dac3d-133">Se qualquer um dos outros valores for usado, este deverá ser.</span><span class="sxs-lookup"><span data-stu-id="dac3d-133">If any of the other values are used, this one must be.</span></span><br/> |
    | <span data-ttu-id="dac3d-134">\_\_OBTER \_ Propriedades ext. \_</span><span class="sxs-lookup"><span data-stu-id="dac3d-134">\_\_GET\_EXT\_PROPERTIES</span></span><br/>      | <span data-ttu-id="dac3d-135">[**SafeArray**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadeias de caracteres que listam as propriedades a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="dac3d-135">[**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) of strings listing the properties to be retrieved.</span></span> <span data-ttu-id="dac3d-136">Não pode ser especificado simultaneamente \_ \_ \_ somente com \_ as chaves Get ext \_ .</span><span class="sxs-lookup"><span data-stu-id="dac3d-136">Cannot be simultaneously specified with \_\_GET\_EXT\_KEYS\_ONLY.</span></span><br/> <span data-ttu-id="dac3d-137">Um asterisco " \* " é um nome de propriedade inválido para \_ \_ Propriedades de get \_ ext \_ .</span><span class="sxs-lookup"><span data-stu-id="dac3d-137">An asterisk "\*" is an invalid property name for \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                    |
    | <span data-ttu-id="dac3d-138">\_\_OBTER \_ \_ chaves ext \_ somente</span><span class="sxs-lookup"><span data-stu-id="dac3d-138">\_\_GET\_EXT\_KEYS\_ONLY</span></span><br/>      | <span data-ttu-id="dac3d-139">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="dac3d-139">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="dac3d-140">Indica que somente as chaves devem ser fornecidas no objeto retornado.</span><span class="sxs-lookup"><span data-stu-id="dac3d-140">Indicates that only keys should be provided in the returned object.</span></span> <span data-ttu-id="dac3d-141">Não pode ser especificado simultaneamente com \_ \_ \_ \_ as propriedades Get ext.</span><span class="sxs-lookup"><span data-stu-id="dac3d-141">Cannot be simultaneously specified with \_\_GET\_EXT\_PROPERTIES.</span></span> <span data-ttu-id="dac3d-142">Em vez disso, tem precedência sobre \_ \_ obter \_ \_ Propriedades ext.</span><span class="sxs-lookup"><span data-stu-id="dac3d-142">Instead, takes precedence over \_\_GET\_EXT\_PROPERTIES.</span></span><br/>                            |
    | <span data-ttu-id="dac3d-143">\_\_OBTER \_ \_ solicitação de cliente ext \_</span><span class="sxs-lookup"><span data-stu-id="dac3d-143">\_\_GET\_EXT\_CLIENT\_REQUEST</span></span><br/> | <span data-ttu-id="dac3d-144">**VT \_ BOOL** definido como **Variant \_ true**.</span><span class="sxs-lookup"><span data-stu-id="dac3d-144">**VT\_BOOL** set to **VARIANT\_TRUE**.</span></span> <span data-ttu-id="dac3d-145">Indica que o chamador foi aquele que escreveu o valor no objeto de contexto e que ele não foi propagado de outra operação dependente.</span><span class="sxs-lookup"><span data-stu-id="dac3d-145">Indicates that the caller was the one who wrote the value into the context object and that it was not propagated from another dependent operation.</span></span><br/>                                                                        |

    

     

3.  <span data-ttu-id="dac3d-146">Passe o objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) em qualquer chamada para [**IWbemServices:: GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices:: GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices:: CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum)ou [**IWbemServices:: CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) por meio do parâmetro *pCtx* .</span><span class="sxs-lookup"><span data-stu-id="dac3d-146">Pass the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) context object into any calls to [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum), or [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) through the *pCtx* parameter.</span></span>

    <span data-ttu-id="dac3d-147">Passar o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) instrui o provedor para permitir recuperações de instância parcial.</span><span class="sxs-lookup"><span data-stu-id="dac3d-147">Passing the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object instructs the provider to allow partial-instance retrievals.</span></span> <span data-ttu-id="dac3d-148">Em uma recuperação de instância completa, você definiria *pCtx* como um valor **nulo** .</span><span class="sxs-lookup"><span data-stu-id="dac3d-148">In a full-instance retrieval, you would set *pCtx* to a **null** value.</span></span> <span data-ttu-id="dac3d-149">Se o provedor não oferecer suporte à recuperação de instância parcial, você receberá uma mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="dac3d-149">If the provider does not support partial-instance retrieval, you will receive an error message.</span></span>

<span data-ttu-id="dac3d-150">Se o provedor não puder cumprir a operação de instância parcial, o provedor continuará como se você não inseriu o objeto de contexto ou, caso contrário, retornará o **\_ \_ \_ parâmetro WBEM E sem suporte**.</span><span class="sxs-lookup"><span data-stu-id="dac3d-150">If the provider cannot comply with the partial-instance operation, the provider either proceeds as if you did not enter the context object, or else returns **WBEM\_E\_UNSUPPORTED\_PARAMETER**.</span></span>

<span data-ttu-id="dac3d-151">O exemplo a seguir descreve como executar uma recuperação de instância completa do [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)e, em seguida, executa uma recuperação de instância parcial da propriedade **Win32 \_ LogicalDisk. Caption** .</span><span class="sxs-lookup"><span data-stu-id="dac3d-151">The following example describes how to perform a full instance retrieval of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), and then performs a partial-instance retrieval of the **Win32\_LogicalDisk.Caption** property.</span></span>


```C++
#include <stdio.h>
#define _WIN32_DCOM
#include <wbemidl.h>
#pragma comment(lib, "wbemuuid.lib")
#include <iostream>
using namespace std;
#include <comdef.h>


void main(void)
{
    HRESULT hr;
    _bstr_t bstrNamespace;
    IWbemLocator *pWbemLocator = NULL;
    IWbemServices *pServices = NULL;
    IWbemClassObject *pDrive = NULL;
    

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);

    hr = CoInitializeSecurity(NULL, -1, NULL, NULL,
                         RPC_C_AUTHN_LEVEL_CONNECT,
                         RPC_C_IMP_LEVEL_IMPERSONATE,
                         NULL, EOAC_NONE, 0);
 
    if (FAILED(hr))
    {
       CoUninitialize();
       cout << "Failed to initialize security. Error code = 0x" 
            << hex << hr << endl;
       return;
    }

    hr = CoCreateInstance(CLSID_WbemLocator, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemLocator, 
                          (void**) &pWbemLocator);
    if( FAILED(hr) ) 
    {
        CoUninitialize();
        printf("failed CoCreateInstance\n");
        return;
    }
    
    bstrNamespace = L"root\\cimv2";
    hr = pWbemLocator->ConnectServer(bstrNamespace, 
              NULL, NULL, NULL, 0, NULL, NULL, &pServices);
    if( FAILED(hr) ) 
    {
        pWbemLocator->Release();
        CoUninitialize();
        printf("failed ConnectServer\n");
        return;
    }
    pWbemLocator->Release();
    printf("Successfully connected to namespace.\n");

    
    BSTR bstrPath = 
         SysAllocString(L"Win32_LogicalDisk.DeviceID=\"C:\"");
   // *******************************************************//
   // Perform a full-instance retrieval. 
   // *******************************************************//
    hr = pServices->GetObject(bstrPath,
                              0,0, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed GetObject\n");
        return;
    }    
    // Display the object
    BSTR  bstrDriveObj;
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    pDrive->Release();
    pDrive = NULL;

   // *****************************************************//
   // Perform a partial-instance retrieval. 
   // *****************************************************//
    
    IWbemContext  *pctxDrive; // Create context object
    hr = CoCreateInstance(CLSID_WbemContext, NULL, 
                          CLSCTX_INPROC_SERVER, IID_IWbemContext, 
                          (void**) &pctxDrive);
    if (FAILED(hr))
    {
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("create instance failed for context object.\n");
        return;
    }
    
    VARIANT  vExtensions;
    VARIANT  vClient;
    VARIANT  vPropertyList;
    VARIANT  vProperty;
    SAFEARRAY  *psaProperties;
    SAFEARRAYBOUND saBounds;
    LONG  lArrayIndex = 0;
    
    // Add named values to the context object. 
    VariantInit(&vExtensions);
    V_VT(&vExtensions) = VT_BOOL;
    V_BOOL(&vExtensions) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXTENSIONS"), 
        0, &vExtensions);
    VariantClear(&vExtensions);

    VariantInit(&vClient);
    V_VT(&vClient) = VT_BOOL;
    V_BOOL(&vClient) = VARIANT_TRUE;
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_CLIENT_REQUEST"), 
       0, &vClient);
    VariantClear(&vClient);
    // Create an array of properties to return.
    saBounds.cElements = 1;
    saBounds.lLbound = 0;
    psaProperties = SafeArrayCreate(VT_BSTR, 1, &saBounds);

    // Add the Caption property to the array.
    VariantInit(&vProperty);
    V_VT(&vProperty) = VT_BSTR;
    V_BSTR(&vProperty) = _bstr_t(L"Caption");
    SafeArrayPutElement(psaProperties, &lArrayIndex, 
       V_BSTR(&vProperty));
    VariantClear(&vProperty);
    
    VariantInit(&vPropertyList);
    V_VT(&vPropertyList) = VT_ARRAY | VT_BSTR;
    V_ARRAY(&vPropertyList) = psaProperties;
    // Put the array in the named value __GET_EXT_PROPERTIES.
    hr = pctxDrive->SetValue(_bstr_t(L"__GET_EXT_PROPERTIES"), 
        0, &vPropertyList);
    VariantClear(&vPropertyList);
    SafeArrayDestroy(psaProperties);

    // Pass the context object as the pCtx parameter of GetObject.
    hr = pServices->GetObject(bstrPath, 0, pctxDrive, &pDrive, 0);
    if( FAILED(hr) )
    { 
        pServices->Release();
        CoUninitialize();
        printf("failed property GetObject\n");
        return;
    }    
    // Display the object
    hr = pDrive->GetObjectText(0, &bstrDriveObj);
    printf("%S\n\n", bstrDriveObj);

    SysFreeString(bstrPath);

    VARIANT vFileSystem;
    // Attempt to get a property that was not requested.
    // The following should return a NULL property if
    // the partial-instance retrieval succeeded.

    hr = pDrive->Get(_bstr_t(L"FileSystem"), 0,
                       &vFileSystem, NULL, NULL);

    if( FAILED(hr) )
    { 
        pServices->Release();
        pDrive->Release();    
        CoUninitialize();
        printf("failed get for file system\n");
        return;
    }    
 
    if (V_VT(&vFileSystem) == VT_NULL)
        printf("file system variable is null - expected\n");
    else
        printf("FileSystem = %S\n", V_BSTR(&vFileSystem));
    
    VariantClear(&vFileSystem);

    pDrive->Release();    
    pctxDrive->Release();
    pServices->Release();
    pServices = NULL;    // MUST be set to NULL
    CoUninitialize();
    return;  // -- program successfully completed
};
```



<span data-ttu-id="dac3d-152">Quando executado, o exemplo de código anterior grava as informações a seguir.</span><span class="sxs-lookup"><span data-stu-id="dac3d-152">When executed, the previous code example writes the following information.</span></span> <span data-ttu-id="dac3d-153">A primeira descrição do objeto é da recuperação de instância completa.</span><span class="sxs-lookup"><span data-stu-id="dac3d-153">The first object description is from the full-instance retrieval.</span></span> <span data-ttu-id="dac3d-154">A segunda descrição do objeto é da recuperação de instância parcial.</span><span class="sxs-lookup"><span data-stu-id="dac3d-154">The second object description is from the partial-instance retrieval.</span></span> <span data-ttu-id="dac3d-155">A última seção mostra que você receberá um valor **nulo** se solicitar uma propriedade que não foi solicitada na chamada [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) original.</span><span class="sxs-lookup"><span data-stu-id="dac3d-155">The last section shows that you receive a **null** value if you request a property that was not requested in the original [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) call.</span></span>

``` syntax
Successfully connected to namespace

instance of Win32_LogicalDisk
{
        Caption = "C:";
        Compressed = FALSE;
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        FileSystem = "NTFS";
        FreeSpace = "3085668352";
        MaximumComponentLength = 255;
        MediaType = 12;
        Name = "C:";
        Size = "4581445632";
        SupportsFileBasedCompression = TRUE;
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "TITUS";
        VolumeName = "titus-c";
        VolumeSerialNumber = "7CB4B90E";
};

instance of Win32_LogicalDisk
{
        Caption = "C:";
        CreationClassName = "Win32_LogicalDisk";
        Description = "Local Fixed Disk";
        DeviceID = "C:";
        DriveType = 3;
        MediaType = 12;
        Name = "C:";
        SystemCreationClassName = "Win32_ComputerSystem";
        SystemName = "MySystem";
};
```

<span data-ttu-id="dac3d-156">A saída a seguir é gerada pelo exemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="dac3d-156">The following output is generated by the previous example.</span></span>

``` syntax
file system variable is null - expected
Press any key to continue
```

 

