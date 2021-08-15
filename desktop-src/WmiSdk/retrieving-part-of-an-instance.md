---
description: Uma recuperação de instância parcial é quando o WMI recupera apenas um subconjunto das propriedades de uma instância.
ms.assetid: 6cc26b26-adc9-4a8a-b51e-9db94eb4295f
ms.tgt_platform: multiple
title: Recuperando parte de uma instância WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8cce9d809e5203b7c00f2b2297403f835d98f37ff86641e297673ee50e579f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316210"
---
# <a name="retrieving-part-of-a-wmi-instance"></a>Recuperando parte de uma instância WMI

Uma recuperação de instância parcial é quando o WMI recupera apenas um subconjunto das propriedades de uma instância. Por exemplo, o WMI pode recuperar apenas as **propriedades Name** **e Key.** O uso mais comum da recuperação de instância parcial está em enumerações grandes que têm várias propriedades.

## <a name="retrieving-part-of-a-wmi-instance-using-powershell"></a>Recuperando parte de uma instância WMI usando o PowerShell

Você pode recuperar uma propriedade individual de uma instância usando [Get-WmiObject](https://technet.microsoft.com/library/dd315379.aspx); a propriedade em si pode ser recuperada e exibida de várias maneiras. Assim como com a recuperação de uma instância, o PowerShell retornará por padrão todas as instâncias de uma determinada classe; você deverá especificar um valor específico se desejar recuperar apenas uma única instância.

O exemplo de código a seguir exibe o número de série do volume para uma instância da [**classe \_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```PowerShell
(Get-WmiObject -class Win32_logicalDisk).DeviceID

#or

Get-WmiObject -class Win32_LogicalDisk | format-list DeviceID

#or

$myDisk = Get-WmiObject -class Win32_LogicalDisk
$myDisk.DeviceID
```



## <a name="retrieving-part-of-a-wmi-instance-using-c-systemmanagement"></a>Recuperando parte de uma instância WMI usando C# (System.Management)

Você pode recuperar uma propriedade individual de uma instância criando um [novo ManagementObject](/dotnet/api/system.management.managementobject) usando os detalhes de uma instância específica. Em seguida, você pode recuperar implicitamente uma ou mais propriedades da instância com o [método GetPropertyValue.](/dotnet/api/system.management.managementbaseobject.getpropertyvalue#System_Management_ManagementBaseObject_GetPropertyValue_System_String_)

> [!Note]  
> **System.Management era** o namespace original do .NET usado para acessar o WMI; no entanto, as APIs nesse namespace geralmente são mais lentas e não são tão dimensionamento em relação às contrapartes mais modernas **do Microsoft.Management.Infrastructure.**

 

O exemplo de código a seguir exibe o número de série do volume para uma instância da [**classe \_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```CSharp
using System.Management;
...
ManagementObject myDisk = new ManagementObject("Win32_LogicalDisk.DeviceID='C:'");
string myProperty = myDisk.GetPropertyValue("VolumeSerialNumber").ToString();
Console.WriteLine(myProperty);
```



## <a name="retrieving-part-of-a-wmi-instance-using-vbscript"></a>Recuperando parte de uma instância WMI usando VBScript

Você pode recuperar uma propriedade individual de uma instância usando [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject).

O exemplo de código a seguir exibe o número de série do volume para uma instância da [**classe \_ LogicalDisk do Win32.**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)


```VB
MsgBox (GetObject("WinMgmts:Win32_LogicalDisk='C:'").VolumeSerialNumber)
```



## <a name="retrieving-part-of-a-wmi-instance-using-c"></a>Recuperando parte de uma instância WMI usando C++

O procedimento a seguir é usado para solicitar uma recuperação de instância parcial usando C++.

**Para solicitar uma recuperação de instância parcial usando C++**

1.  Crie um [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    Um objeto de contexto é um objeto que o WMI usa para passar mais informações para um provedor WMI. Nesse caso, você está usando o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) para instruir o provedor a processar uma recuperação de instância parcial.

2.  Adicione GET EXTENSIONS, GET EXT CLIENT REQUEST e quaisquer outros valores nomeados que descrevam as propriedades que você deseja recuperar para o \_ \_ \_ \_ \_ objeto \_ \_ \_ [**IWbemContext.**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext)

    A tabela a seguir lista os diferentes valores nomeados que usam na chamada de recuperação.

    

    | Valor nomeado                              | Descrição                                                                                                                                                                                                                                                                 |
    |------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | \_\_OBTER \_ EXTENSÕES<br/>           | **VT \_ BOOL** definido como **VARIANT \_ TRUE.** Usado para sinalizar que as operações de recuperação de instância parcial estão sendo usadas. Isso permite uma verificação rápida e única sem precisar enumerar todo o objeto de contexto. Se qualquer um dos outros valores for usado, esse deverá ser.<br/> |
    | \_\_OBTER \_ PROPRIEDADES EXT \_<br/>      | [**SAFEARRAY**](/windows/win32/api/oaidl/ns-oaidl-safearray) de cadeias de caracteres listando as propriedades a serem recuperadas. Não pode ser especificado simultaneamente apenas \_ \_ com GET EXT \_ \_ \_ KEYS.<br/> Um asterisco " \* " é um nome de propriedade inválido para GET EXT \_ \_ \_ \_ PROPERTIES.<br/>                    |
    | \_\_OBTER \_ SOMENTE CHAVES EXT \_ \_<br/>      | **VT \_ BOOL** definido como **VARIANT \_ TRUE.** Indica que apenas as chaves devem ser fornecidas no objeto retornado. Não pode ser especificado simultaneamente com \_ \_ GET EXT \_ \_ PROPERTIES. Em vez disso, tem precedência sobre \_ \_ GET EXT \_ \_ PROPERTIES.<br/>                            |
    | \_\_OBTER \_ SOLICITAÇÃO \_ DO CLIENTE \_ EXT<br/> | **VT \_ BOOL** definido como **VARIANT \_ TRUE.** Indica que o chamador foi aquele que escreveu o valor no objeto de contexto e que ele não foi propagado de outra operação dependente.<br/>                                                                        |

    

     

3.  Passe o objeto de contexto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) em qualquer chamada para [**IWbemServices::GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject), [**IWbemServices::GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync), [**IWbemServices::CreateInstanceEnum ou**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenum) [**IWbemServices::CreateInstanceEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createinstanceenumasync) por meio do *parâmetro pCtx.*

    Passar o [**objeto IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) instrui o provedor a permitir recuperações de instância parcial. Em uma recuperação de instância completa, você definiria *pCtx* como um **valor nulo.** Se o provedor não dá suporte à recuperação de instância parcial, você receberá uma mensagem de erro.

Se o provedor não puder estar em conformidade com a operação de instância parcial, o provedor prosseguirá como se você não tivesse inserir o objeto de contexto ou retornará **WBEM \_ E \_ UNSUPPORTED \_ PARAMETER**.

O exemplo a seguir descreve como executar uma recuperação de instância completa do [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)e, em seguida, executa uma recuperação de instância parcial da propriedade **\_ LogicalDisk.Caption do Win32.**


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



Quando executado, o exemplo de código anterior grava as informações a seguir. A primeira descrição do objeto é da recuperação de instância completa. A segunda descrição do objeto é da recuperação de instância parcial. A última seção mostra  que você receberá um valor nulo se solicitar uma propriedade que não foi solicitada na chamada [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) original.

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

A saída a seguir é gerada pelo exemplo anterior.

``` syntax
file system variable is null - expected
Press any key to continue
```

 

