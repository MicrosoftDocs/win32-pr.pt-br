---
description: Gera representações XML de objetos.
ms.assetid: 06d2b532-7ab2-489d-9021-27b5187c8f2b
ms.tgt_platform: multiple
title: Representando objetos em XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9698c54eeff61517a1389ceea14bc2415727f085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773007"
---
# <a name="representing-objects-in-xml"></a><span data-ttu-id="e09fa-103">Representando objetos em XML</span><span class="sxs-lookup"><span data-stu-id="e09fa-103">Representing Objects in XML</span></span>

<span data-ttu-id="e09fa-104">O componente codificador XML no WMI gera representações XML de objetos.</span><span class="sxs-lookup"><span data-stu-id="e09fa-104">The XML encoder component in WMI generates XML representations of objects.</span></span>

<span data-ttu-id="e09fa-105">Em C++, você pode iniciar o codificador XML com uma chamada para o método [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , especificando o objeto a ser representado em XML e o formato de texto a ser usado na representação.</span><span class="sxs-lookup"><span data-stu-id="e09fa-105">In C++, you can start the XML encoder with a call to the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method, specifying the object to be represented in XML and the text format to use in the representation.</span></span> <span data-ttu-id="e09fa-106">Para obter mais informações e um exemplo de código, consulte para codificar um objeto em XML usando C/C++.</span><span class="sxs-lookup"><span data-stu-id="e09fa-106">For more information and a code example, see To encode an object in XML using C/C++.</span></span>

<span data-ttu-id="e09fa-107">No VBScript ou Visual Basic, para codificar dados para uma instância XML, chame [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md).</span><span class="sxs-lookup"><span data-stu-id="e09fa-107">In VBScript or Visual Basic, to encode data for an XML instance, call [**SWbemObjectEx.GetText**](swbemobjectex-gettext-.md).</span></span> <span data-ttu-id="e09fa-108">Para obter mais informações e um exemplo de código, consulte para codificar um objeto em XML usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="e09fa-108">For more information and a code example, see To encode an object in XML using VBScript.</span></span>

<span data-ttu-id="e09fa-109">As seções a seguir são discutidas neste tópico:</span><span class="sxs-lookup"><span data-stu-id="e09fa-109">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="e09fa-110">Codificar um objeto usando C ou C++</span><span class="sxs-lookup"><span data-stu-id="e09fa-110">Encode an Object Using C or C++</span></span>](#encode-an-object-using-c-or-c)
-   [<span data-ttu-id="e09fa-111">Codificar um objeto usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="e09fa-111">Encode an Object Using VBScript</span></span>](#encode-an-object-using-vbscript)
-   [<span data-ttu-id="e09fa-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e09fa-112">Related topics</span></span>](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a><span data-ttu-id="e09fa-113">Codificar um objeto usando C ou C++</span><span class="sxs-lookup"><span data-stu-id="e09fa-113">Encode an Object Using C or C++</span></span>

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

<span data-ttu-id="e09fa-114">O procedimento a seguir descreve como codificar um objeto em XML usando C ou C++.</span><span class="sxs-lookup"><span data-stu-id="e09fa-114">The following procedure describes how to encode an object in XML using C or C++.</span></span>

<span data-ttu-id="e09fa-115">**Para codificar um objeto em XML usando C ou C++**</span><span class="sxs-lookup"><span data-stu-id="e09fa-115">**To encode an object in XML using C or C++**</span></span>

1.  <span data-ttu-id="e09fa-116">Configure seu programa para acessar dados do WMI.</span><span class="sxs-lookup"><span data-stu-id="e09fa-116">Set up your program to access WMI data.</span></span>

    <span data-ttu-id="e09fa-117">Como o WMI é baseado em tecnologia COM, você deve executar as chamadas necessárias para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acessar o WMI.</span><span class="sxs-lookup"><span data-stu-id="e09fa-117">Because WMI is based on COM technology, you must perform the requisite calls to the [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) and [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) functions to access WMI.</span></span> <span data-ttu-id="e09fa-118">Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).</span><span class="sxs-lookup"><span data-stu-id="e09fa-118">For more information, see [Initializing COM for a WMI Application](initializing-com-for-a-wmi-application.md).</span></span>

2.  <span data-ttu-id="e09fa-119">Opcionalmente, crie um objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inicialize-o.</span><span class="sxs-lookup"><span data-stu-id="e09fa-119">Optionally, create an [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object and initialize it.</span></span>

    <span data-ttu-id="e09fa-120">Você não precisa criar o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , a menos que precise alterar a operação padrão.</span><span class="sxs-lookup"><span data-stu-id="e09fa-120">You do not need to create the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) object unless you need to change the default operation.</span></span> <span data-ttu-id="e09fa-121">O objeto Context é usado pelo codificador XML para controlar a quantidade de informações incluídas na representação XML do objeto.</span><span class="sxs-lookup"><span data-stu-id="e09fa-121">The context object is used by the XML encoder to control the amount of information included in the object's XML representation.</span></span>

    <span data-ttu-id="e09fa-122">A tabela a seguir lista os valores opcionais que podem ser especificados para o objeto Context.</span><span class="sxs-lookup"><span data-stu-id="e09fa-122">The following table lists the optional values that can be specified for the context object.</span></span>

    

    <table>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="e09fa-123">Valor/tipo</span><span class="sxs-lookup"><span data-stu-id="e09fa-123">Value/type</span></span></th>
    <th><span data-ttu-id="e09fa-124">Significado</span><span class="sxs-lookup"><span data-stu-id="e09fa-124">Meaning</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="e09fa-125">&quot;&quot; <strong>VT_BOOL</strong> LocalOnly</span><span class="sxs-lookup"><span data-stu-id="e09fa-125">&quot;LocalOnly&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="e09fa-126">Quando <strong>true</strong>, somente as propriedades e os métodos definidos localmente na classe estão presentes no XML resultante.</span><span class="sxs-lookup"><span data-stu-id="e09fa-126">When <strong>TRUE</strong>, only properties and methods defined locally in the class are present in the resulting XML.</span></span> <span data-ttu-id="e09fa-127">O valor padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e09fa-127">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e09fa-128">&quot;&quot; <strong>VT_BOOL</strong> IncludeQualifiers</span><span class="sxs-lookup"><span data-stu-id="e09fa-128">&quot;IncludeQualifiers&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="e09fa-129">Quando <strong>verdadeiro</strong>, a classe, a instância, as propriedades e os qualificadores de método são incluídos no XML resultante.</span><span class="sxs-lookup"><span data-stu-id="e09fa-129">When <strong>TRUE</strong>, class, instance, properties, and method qualifiers are included in the resulting XML.</span></span> <span data-ttu-id="e09fa-130">O valor padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e09fa-130">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="e09fa-131">&quot;&quot; <strong>VT_BOOL</strong> ExcludeSystemProperties</span><span class="sxs-lookup"><span data-stu-id="e09fa-131">&quot;ExcludeSystemProperties&quot; <strong>VT_BOOL</strong></span></span></td>
    <td><span data-ttu-id="e09fa-132">Quando <strong>true</strong>, as propriedades do sistema WMI são filtradas fora da saída.</span><span class="sxs-lookup"><span data-stu-id="e09fa-132">When <strong>TRUE</strong>, WMI system properties are filtered out of the output.</span></span> <span data-ttu-id="e09fa-133">O valor padrão é <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e09fa-133">The default value is <strong>FALSE</strong>.</span></span></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="e09fa-134">&quot;&quot; <strong>VT_I4</strong> PathLevel</span><span class="sxs-lookup"><span data-stu-id="e09fa-134">&quot;PathLevel&quot; <strong>VT_I4</strong></span></span></td>
    <td><dl> <span data-ttu-id="e09fa-135">0 = um <CLASS> <INSTANCE> elemento ou é gerado.</span><span class="sxs-lookup"><span data-stu-id="e09fa-135">0 = A <CLASS> or <INSTANCE> element is generated.</span></span><br />
<span data-ttu-id="e09fa-136">1 = um <VALUE.NAMEDOBJECT> elemento é gerado.</span><span class="sxs-lookup"><span data-stu-id="e09fa-136">1 = A <VALUE.NAMEDOBJECT> element is generated.</span></span><br />
<span data-ttu-id="e09fa-137">2 = um <VALUE.OBJECTWITHLOCALPATH> elemento é gerado.</span><span class="sxs-lookup"><span data-stu-id="e09fa-137">2 = A <VALUE.OBJECTWITHLOCALPATH> element is generated.</span></span><br />
<span data-ttu-id="e09fa-138">3 = A <VALUE.OBJECTWITHPATH> é gerada.</span><span class="sxs-lookup"><span data-stu-id="e09fa-138">3 = A <VALUE.OBJECTWITHPATH> is generated.</span></span><br />
    </dl> <span data-ttu-id="e09fa-139">O padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="e09fa-139">The default is 0 (zero).</span></span><br/></td>
    </tr>
    </tbody>
    </table>

    

     

    <span data-ttu-id="e09fa-140">O exemplo de código a seguir mostra como o objeto Context é inicializado para incluir qualificadores e excluir propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="e09fa-140">The following code example shows how the context object is initialized to include qualifiers and exclude system properties.</span></span>

    ```C++
    VARIANT vValue;
    IWbemContext *pContext = NULL;
    HRESULT hr = CoCreateInstance (CLSID_WbemContext, 
                           NULL, 
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemContext, 
                           (void**) &pContext);
    if (FAILED(hr))
    {
      printf("Create context failed with %x\n", hr);
      return hr;
    }

    // Generate a <VALUE.OBJECTWITHLOCALPATH> element
    VariantInit(&vValue);
    vValue.vt = VT_I4;
    vValue.lVal = 2;
    pContext->SetValue(L"PathLevel", 0, &vValue);
    VariantClear(&vValue);

    // Include qualifiers
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
    VariantClear(&vValue);

    // Exclude system properties
    VariantInit(&vValue);
    vValue.vt = VT_BOOL;
    vValue.boolVal = VARIANT_TRUE;
    pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
    VariantClear(&vValue);
    ```

    

3.  <span data-ttu-id="e09fa-141">Obtenha uma referência à classe ou instância a ser codificada em XML.</span><span class="sxs-lookup"><span data-stu-id="e09fa-141">Get a reference to the class or instance to encode in XML.</span></span>

    <span data-ttu-id="e09fa-142">Depois que você inicializar COM e estiver conectado ao WMI, chame [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar uma referência à classe ou instância especificada.</span><span class="sxs-lookup"><span data-stu-id="e09fa-142">After you have initialized COM and are connected to WMI, call [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) to retrieve a reference to the specified class or instance.</span></span> <span data-ttu-id="e09fa-143">Se você usou um BSTR para especificar a classe ou instância, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada por [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="e09fa-143">If you used a BSTR to specify the class or instance, call [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free up the memory allocated by [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).</span></span>

    <span data-ttu-id="e09fa-144">O exemplo de código a seguir recupera uma referência a uma instância de [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="e09fa-144">The following code example retrieves a reference to an [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) instance.</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemClassObject *pClass = NULL;
    BSTR strObj = SysAllocString(L"Win32_LogicalDisk");

    hr = pConnection->GetObject(strObj, 
                                0, 
                                NULL, 
                                &pClass, 
                                NULL);

    SysFreeString(strObj);
    if (FAILED(hr))
    {
      printf("GetObject failed with %x\n",hr)
      return hr;
    }
    ```

    

4.  <span data-ttu-id="e09fa-145">Crie um objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .</span><span class="sxs-lookup"><span data-stu-id="e09fa-145">Create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object.</span></span>

    <span data-ttu-id="e09fa-146">Depois de ter uma referência a um objeto, você deve criar o objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e09fa-146">After you have a reference to an object you must create the [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object with a call to [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="e09fa-147">O objeto **IWbemObjectTextSrc** é usado para gerar o texto XML real.</span><span class="sxs-lookup"><span data-stu-id="e09fa-147">The **IWbemObjectTextSrc** object is used to generate the actual XML text.</span></span>

    <span data-ttu-id="e09fa-148">O exemplo de código a seguir mostra como criar um objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="e09fa-148">The following code example shows how to create an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object by calling [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

    ```C++
    HRESULT hr = NULL;
    IWbemObjectTextSrc *pSrc = NULL;

    hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                           NULL,
                           CLSCTX_INPROC_SERVER,
                           IID_IWbemObjectTextSrc, 
                           (void**) &pSrc);

    if (FAILED(hr))
    {
        printf("CoCreateInstance of IWbemObjectTextSrc failed %x\n",hr);
        return hr;
    }
    ```

    

5.  <span data-ttu-id="e09fa-149">Invoque o método [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) para obter uma representação XML de um objeto.</span><span class="sxs-lookup"><span data-stu-id="e09fa-149">Invoke the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method to get an XML representation of an object.</span></span>

    <span data-ttu-id="e09fa-150">Depois de definir o contexto para a representação do objeto, obter uma referência ao objeto e criar um objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , você estará pronto para gerar uma representação XML do objeto especificado chamando o método [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="e09fa-150">After setting the context for the object's representation, getting a reference to the object, and creating an [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) object, you are ready to generate an XML representation of the specified object by calling the [**IWbemObjectTextSrc.GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) method.</span></span>

    <span data-ttu-id="e09fa-151">O código de exemplo C++ a seguir gera uma representação XML do objeto referenciado por *pClass*.</span><span class="sxs-lookup"><span data-stu-id="e09fa-151">The following C++ example code generates an XML representation of the object referenced by *pClass*.</span></span> <span data-ttu-id="e09fa-152">A representação XML é retornada em *strText*.</span><span class="sxs-lookup"><span data-stu-id="e09fa-152">The XML representation is returned in *strText*.</span></span> <span data-ttu-id="e09fa-153">O terceiro parâmetro de [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) especifica o formato de texto a ser usado para o XML e deve ser o texto de obj do WMI de \_ \_ \_ CIM \_ DTD \_ 2 \_ 0 (0x1) ou WMI \_ obj \_ Text \_ WMI \_ DTD \_ 2 \_ 0 (0x2).</span><span class="sxs-lookup"><span data-stu-id="e09fa-153">The third parameter of [**GetText**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) specifies the text format to be used for the XML and must be either WMI\_OBJ\_TEXT\_CIM\_DTD\_2\_0 (0x1) or WMI\_OBJ\_TEXT\_WMI\_DTD\_2\_0 (0x2).</span></span> <span data-ttu-id="e09fa-154">Para obter mais informações sobre esses valores, consulte valores de parâmetro [**IWbemObjectTextSrc:: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .</span><span class="sxs-lookup"><span data-stu-id="e09fa-154">For more information about these values, see [**IWbemObjectTextSrc::GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) Parameter Values.</span></span>

    ```C++
    HRESULT hr = NULL;
    BSTR strText = NULL;
    hr = pSrc->GetText(0, 
                       pClass, 
                       WMI_OBJ_TEXT_CIM_DTD_2_0,
                       pContext, 
                       &strText);

    // Perform a task with strText
    SysFreeString(strText);

    if (FAILED(hr))
    {
      printf("GetText failed with %x\n", hr);
      return hr;
    }
    ```

    

<span data-ttu-id="e09fa-155">O seguinte código de exemplo C++ inclui todas as etapas do procedimento anterior e codifica a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em XML, incluindo classe, propriedade e qualificadores de método e exclusão de propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="e09fa-155">The following C++ example code includes all of the steps in the previous procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML including class, property, and method qualifiers and excluding system properties.</span></span>


```C++
// The following #define statement is needed so that 
// the proper values are loaded by the #include files.
#define _WIN32_WINNT 0x0500

#include <stdio.h>
#include <wbemcli.h>
#pragma comment(lib, "wbemuuid.lib")

// Initialize the context object
// ---------------------------------------------
void FillUpContext(IWbemContext *pContext)
{
  VARIANT vValue;

  // IncludeQualifiers
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_FALSE;
  pContext->SetValue(L"IncludeQualifiers", 0, &vValue);
  VariantClear(&vValue);

  VariantInit(&vValue);
  vValue.vt = VT_I4;
  vValue.lVal = 0;
  pContext->SetValue(L"PathLevel", 0, &vValue);
  VariantClear(&vValue);

  // ExcludeSystemProperties
  VariantInit(&vValue);
  vValue.vt = VT_BOOL;
  vValue.boolVal = VARIANT_TRUE;
  pContext->SetValue(L"ExcludeSystemProperties", 0, &vValue);
  VariantClear(&vValue);
}

// Main method ... drives the program
// ---------------------------------------------
int _cdecl main(int argc, char * argv[])
{
  BSTR strNs = NULL;
  BSTR strObj = NULL;
  BSTR strText = NULL;

  if(FAILED(CoInitialize(NULL)))
    return 1;
  HRESULT hr = E_FAIL;
  IWbemObjectTextSrc *pSrc = NULL;

  IWbemLocator *pL = NULL;
  if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemLocator, 
                                      NULL, 
                                      CLSCTX_INPROC_SERVER,
                                      IID_IWbemLocator, 
                                      (void**) &pL)))
  {
    // Create a context object
    IWbemContext *pContext = NULL;
    if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemContext, 
                                        NULL, 
                                        CLSCTX_INPROC_SERVER,
                                        IID_IWbemContext, 
                                        (void**) &pContext)))
    {
      FillUpContext(pContext);
      IWbemServices *pConnection = NULL;
      strNs = SysAllocString(L"root\\cimv2");
      strText = NULL;
      if(SUCCEEDED(hr = pL->ConnectServer(strNs, 
                                          NULL, 
                                          NULL, 
                                          NULL, 
                                          0, 
                                          NULL, 
                                          NULL, 
                                          &pConnection)))
      {
        IWbemClassObject *pClass = NULL;
        strObj = SysAllocString(L"Win32_LogicalDisk");

        if(SUCCEEDED(hr = CoCreateInstance (CLSID_WbemObjectTextSrc, 
                                            NULL,
                                            CLSCTX_INPROC_SERVER,
                                            IID_IWbemObjectTextSrc, 
                                            (void**) &pSrc)))
        {
          // Test for GetObject
          if(SUCCEEDED(hr = pConnection->GetObject(strObj, 
                                                   0, 
                                                   NULL, 
                                                   &pClass, 
                                                   NULL)))
          {
            if(SUCCEEDED(hr = pSrc->GetText(0, 
                                            pClass, 
                                            WMI_OBJ_TEXT_CIM_DTD_2_0,
                                            pContext, 
                                            &strText)))
            {
              printf("GETOBJECT SUCCEEDED\n");
              printf("==========================================\n");
              wprintf(strText);
              pContext->Release();
              pClass->Release();
            }
            else
            {
              printf("GetText failed with %x\n", hr);
              // Free up the object
              pContext->Release();
              pClass->Release();
            }
          }
          else
            printf("GetObject failed with %x\n", hr);
        }
        else
          printf("CoCreateInstance on WbemObjectTextSrc failed with %x\n", hr);
      }
      else
        printf("ConnectServer on root\\cimv2 failed with %x\n", hr);
    }
    else
      printf("CoCreateInstance on Context failed with %x\n", hr);
  }
  else
    printf("CoCreateInstance on Locator failed with %x\n", hr);

// Clean up memory
  if (strNs != NULL)
    SysFreeString(strNs);
  if (strObj != NULL)
    SysFreeString(strObj);
  if (strText != NULL)
    SysFreeString(strText);
  if (pSrc != NULL)
    pSrc->Release();
  if (pL != NULL)
    pL->Release();
  return 0;
}
```



## <a name="encode-an-object-using-vbscript"></a><span data-ttu-id="e09fa-156">Codificar um objeto usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="e09fa-156">Encode an Object Using VBScript</span></span>

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

<span data-ttu-id="e09fa-157">O procedimento a seguir descreve como codificar um objeto em XML usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="e09fa-157">The following procedure describes how to encode an object in XML using VBScript.</span></span>

<span data-ttu-id="e09fa-158">**Para codificar um objeto em XML usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="e09fa-158">**To encode an object in XML using VBScript**</span></span>

1.  <span data-ttu-id="e09fa-159">Opcionalmente, crie um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) e inicialize-o para definir os valores de contexto necessários para a representação XML.</span><span class="sxs-lookup"><span data-stu-id="e09fa-159">Optionally, create an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object and initialize it so as to set the context values required for the XML representation.</span></span>

    <span data-ttu-id="e09fa-160">O exemplo de código a seguir mostra como os valores instruem o codificador XML a gerar um valor <. OBJECTWITHLOCALPATH> elemento, incluindo todos os qualificadores e excluindo Propriedades do sistema quando ele constrói a representação XML do objeto.</span><span class="sxs-lookup"><span data-stu-id="e09fa-160">The following code example shows how the values instruct the XML encoder to generate a <VALUE.OBJECTWITHLOCALPATH> element, including all of the qualifiers and excluding system properties when it constructs the XML representation of the object.</span></span>

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  <span data-ttu-id="e09fa-161">Recupere uma instância do objeto ou classe para representar em XML.</span><span class="sxs-lookup"><span data-stu-id="e09fa-161">Retrieve an instance of the object or class to represent in XML.</span></span>

    <span data-ttu-id="e09fa-162">O exemplo de código a seguir recupera uma instância do objeto.</span><span class="sxs-lookup"><span data-stu-id="e09fa-162">The following code example retrieves an instance of the object.</span></span>

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  <span data-ttu-id="e09fa-163">Invoque o método [**gettext \_**](swbemobjectex-gettext-.md) da instância criada na etapa anterior, usando 1 como o parâmetro para especificar o formato de texto que corresponde ao CIM DTD versão 2,0 ou 2 para especificar o formato de texto que corresponde à versão 2,0 do DTD do WMI.</span><span class="sxs-lookup"><span data-stu-id="e09fa-163">Invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance created in the preceding step, using 1 as the parameter to specify the text format that corresponds to CIM DTD version 2.0, or 2 to specify the text format that corresponds to WMI DTD version 2.0.</span></span> <span data-ttu-id="e09fa-164">Se você criou o objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) na etapa 1, inclua-o na lista de parâmetros como o terceiro parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e09fa-164">If you created the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object in Step 1, include it in the parameter list as the third parameter.</span></span>

    <span data-ttu-id="e09fa-165">O exemplo de código a seguir mostra como invocar o método [**gettext \_**](swbemobjectex-gettext-.md) da instância.</span><span class="sxs-lookup"><span data-stu-id="e09fa-165">The following code example shows how to invoke the [**GetText\_**](swbemobjectex-gettext-.md) method of the instance.</span></span>

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  <span data-ttu-id="e09fa-166">Opcionalmente, valide que o XML gerado na etapa 3 é um XML bem formado, criando e inicializando um objeto XML Modelo de Objeto do Documento (DOM) e, em seguida, carregar o texto XML nele.</span><span class="sxs-lookup"><span data-stu-id="e09fa-166">Optionally, validate that the XML generated in Step 3 is well-formed XML, by creating and initializing an XML Document Object Model (DOM) object and then load the XML text into it.</span></span>

    <span data-ttu-id="e09fa-167">O exemplo de código a seguir mostra como criar e inicializar um objeto XML DOM e carregar o texto XML nele.</span><span class="sxs-lookup"><span data-stu-id="e09fa-167">The following code example shows how to create and initialize an XML DOM object and load the XML text into it.</span></span>

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  <span data-ttu-id="e09fa-168">Saída da representação XML do objeto.</span><span class="sxs-lookup"><span data-stu-id="e09fa-168">Output the XML representation of the object.</span></span>

    <span data-ttu-id="e09fa-169">O exemplo de código a seguir mostra como usar o WScript para gerar o XML.</span><span class="sxs-lookup"><span data-stu-id="e09fa-169">The following code example shows how to use wscript to output the XML.</span></span>

    ```VB
    wscript.echo strText
    ```

    

    <span data-ttu-id="e09fa-170">Se você optar por usar o XML DOM para verificar se o XML gerado está bem formado, substitua a linha anterior pelo seguinte.</span><span class="sxs-lookup"><span data-stu-id="e09fa-170">If you chose to use XML DOM to verify that the XML generated is well-formed, replace the previous line with the following.</span></span>

    ```VB
    wscript.echo xml.xml
    ```

    

<span data-ttu-id="e09fa-171">O exemplo de código VBScript a seguir inclui todas as etapas no procedimento anterior e codifica a classe do [**disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em XML, incluindo a classe, a propriedade e os qualificadores de método e a exclusão de propriedades do sistema.</span><span class="sxs-lookup"><span data-stu-id="e09fa-171">The following VBScript code example includes all of the steps in the preceding procedure and encodes the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class in XML, including class, property, and method qualifiers and excluding system properties.</span></span>


```VB
' Create optional SWbemNamedValueSet object
set context = CreateObject("Wbemscripting.SWbemNamedValueSet")

' Initialize the context object
context.add "PathLevel", 2
context.add "IncludeQualifiers", true
context.add "ExcludeSystemProperties", true

' Retrieve the object/class to be represented in XML
set myObj = GetObject("winmgmts:\\.\root\cimv2:Win32_LogicalDisk")

' Get the XML representation of the object
strText = myObj.GetText_(2,,context)
' If you have not used a SWbemNamedValueSet object 
'   use the following line
'   strText = myObj.GetText(2)

' Print the XML representation
wscript.echo strText

' If you choose to use the XML DOM to verify 
'   that the XML generated is well-formed, replace the last
'   line in the above code example with the following lines:

' Create an XMLDOM object
set xml = CreateObject("Microsoft.xmldom")

' Initialize the XMLDOM object so results are 
'   returned synchronously
xml.async = false

' Load the XML into the XMLDOM object
xml.loadxml strText

' Print the XML representation
wscript.echo xml.xml
```



## <a name="related-topics"></a><span data-ttu-id="e09fa-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e09fa-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e09fa-173">Usando o WMI</span><span class="sxs-lookup"><span data-stu-id="e09fa-173">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

