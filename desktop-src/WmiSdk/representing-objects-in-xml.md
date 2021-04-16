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
# <a name="representing-objects-in-xml"></a>Representando objetos em XML

O componente codificador XML no WMI gera representações XML de objetos.

Em C++, você pode iniciar o codificador XML com uma chamada para o método [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) , especificando o objeto a ser representado em XML e o formato de texto a ser usado na representação. Para obter mais informações e um exemplo de código, consulte para codificar um objeto em XML usando C/C++.

No VBScript ou Visual Basic, para codificar dados para uma instância XML, chame [**SWbemObjectEx. GetText**](swbemobjectex-gettext-.md). Para obter mais informações e um exemplo de código, consulte para codificar um objeto em XML usando o VBScript.

As seções a seguir são discutidas neste tópico:

-   [Codificar um objeto usando C ou C++](#encode-an-object-using-c-or-c)
-   [Codificar um objeto usando o VBScript](#encode-an-object-using-vbscript)
-   [Tópicos relacionados](#related-topics)

## <a name="encode-an-object-using-c-or-c"></a>Codificar um objeto usando C ou C++

<span id="to_encode_an_object_in_xml_using_c_c_"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_C_C_"></span>

O procedimento a seguir descreve como codificar um objeto em XML usando C ou C++.

**Para codificar um objeto em XML usando C ou C++**

1.  Configure seu programa para acessar dados do WMI.

    Como o WMI é baseado em tecnologia COM, você deve executar as chamadas necessárias para as funções [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) e [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) para acessar o WMI. Para obter mais informações, consulte [Inicializando com para um aplicativo WMI](initializing-com-for-a-wmi-application.md).

2.  Opcionalmente, crie um objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) e inicialize-o.

    Você não precisa criar o objeto [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) , a menos que precise alterar a operação padrão. O objeto Context é usado pelo codificador XML para controlar a quantidade de informações incluídas na representação XML do objeto.

    A tabela a seguir lista os valores opcionais que podem ser especificados para o objeto Context.

    

    <table>
    <thead>
    <tr class="header">
    <th>Valor/tipo</th>
    <th>Significado</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>&quot;&quot; <strong>VT_BOOL</strong> LocalOnly</td>
    <td>Quando <strong>true</strong>, somente as propriedades e os métodos definidos localmente na classe estão presentes no XML resultante. O valor padrão é <strong>false</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;&quot; <strong>VT_BOOL</strong> IncludeQualifiers</td>
    <td>Quando <strong>verdadeiro</strong>, a classe, a instância, as propriedades e os qualificadores de método são incluídos no XML resultante. O valor padrão é <strong>false</strong>.</td>
    </tr>
    <tr class="odd">
    <td>&quot;&quot; <strong>VT_BOOL</strong> ExcludeSystemProperties</td>
    <td>Quando <strong>true</strong>, as propriedades do sistema WMI são filtradas fora da saída. O valor padrão é <strong>false</strong>.</td>
    </tr>
    <tr class="even">
    <td>&quot;&quot; <strong>VT_I4</strong> PathLevel</td>
    <td><dl> 0 = um <CLASS> <INSTANCE> elemento ou é gerado.<br />
1 = um <VALUE.NAMEDOBJECT> elemento é gerado.<br />
2 = um <VALUE.OBJECTWITHLOCALPATH> elemento é gerado.<br />
3 = A <VALUE.OBJECTWITHPATH> é gerada.<br />
    </dl> O padrão é 0 (zero).<br/></td>
    </tr>
    </tbody>
    </table>

    

     

    O exemplo de código a seguir mostra como o objeto Context é inicializado para incluir qualificadores e excluir propriedades do sistema.

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

    

3.  Obtenha uma referência à classe ou instância a ser codificada em XML.

    Depois que você inicializar COM e estiver conectado ao WMI, chame [**GetObject**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject) para recuperar uma referência à classe ou instância especificada. Se você usou um BSTR para especificar a classe ou instância, chame [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar a memória alocada por [**SysAllocString**](/windows/win32/api/oleauto/nf-oleauto-sysallocstring).

    O exemplo de código a seguir recupera uma referência a uma instância de [**\_ LogicalDisk do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .

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

    

4.  Crie um objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) .

    Depois de ter uma referência a um objeto, você deve criar o objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) com uma chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance). O objeto **IWbemObjectTextSrc** é usado para gerar o texto XML real.

    O exemplo de código a seguir mostra como criar um objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

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

    

5.  Invoque o método [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) para obter uma representação XML de um objeto.

    Depois de definir o contexto para a representação do objeto, obter uma referência ao objeto e criar um objeto [**IWbemObjectTextSrc**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) , você estará pronto para gerar uma representação XML do objeto especificado chamando o método [**IWbemObjectTextSrc. GetText**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

    O código de exemplo C++ a seguir gera uma representação XML do objeto referenciado por *pClass*. A representação XML é retornada em *strText*. O terceiro parâmetro de [**gettext**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemobjecttextsrc) especifica o formato de texto a ser usado para o XML e deve ser o texto de obj do WMI de \_ \_ \_ CIM \_ DTD \_ 2 \_ 0 (0x1) ou WMI \_ obj \_ Text \_ WMI \_ DTD \_ 2 \_ 0 (0x2). Para obter mais informações sobre esses valores, consulte valores de parâmetro [**IWbemObjectTextSrc:: gettext**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjecttextsrc-gettext) .

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

    

O seguinte código de exemplo C++ inclui todas as etapas do procedimento anterior e codifica a classe do disco [**\_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em XML, incluindo classe, propriedade e qualificadores de método e exclusão de propriedades do sistema.


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



## <a name="encode-an-object-using-vbscript"></a>Codificar um objeto usando o VBScript

<span id="to_encode_an_object_in_xml_using_vbscript"></span><span id="TO_ENCODE_AN_OBJECT_IN_XML_USING_VBSCRIPT"></span>

O procedimento a seguir descreve como codificar um objeto em XML usando o VBScript.

**Para codificar um objeto em XML usando o VBScript**

1.  Opcionalmente, crie um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) e inicialize-o para definir os valores de contexto necessários para a representação XML.

    O exemplo de código a seguir mostra como os valores instruem o codificador XML a gerar um valor <. OBJECTWITHLOCALPATH> elemento, incluindo todos os qualificadores e excluindo Propriedades do sistema quando ele constrói a representação XML do objeto.

    ```VB
    ' Create an optional SWbemNamedValueSet object
    set context = CreateObject("wbemscripting.SWbemNamedValueSet")

    ' Initialize the value set object to set the context
    ' Generate a <VALUE.OBJECTWITHLOCALPATH> element
    context.add "PathLevel", 2 
    context.add "IncludeQualifiers", true 
    context.add "ExcludeSystemProperties", true '
    ```

    

2.  Recupere uma instância do objeto ou classe para representar em XML.

    O exemplo de código a seguir recupera uma instância do objeto.

    ```VB
    ' Retrieve the object/class to be represented in XML
    set myObj = GetObject("winmgmts:\\.\root\cimv2:win32_LogicalDisk")
    ```

    

3.  Invoque o método [**gettext \_**](swbemobjectex-gettext-.md) da instância criada na etapa anterior, usando 1 como o parâmetro para especificar o formato de texto que corresponde ao CIM DTD versão 2,0 ou 2 para especificar o formato de texto que corresponde à versão 2,0 do DTD do WMI. Se você criou o objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) na etapa 1, inclua-o na lista de parâmetros como o terceiro parâmetro.

    O exemplo de código a seguir mostra como invocar o método [**gettext \_**](swbemobjectex-gettext-.md) da instância.

    ```VB
    ' Get the XML representation of the object
    strText = myObj.GetText_(2,,context)

    ' If you have not used a SWbemNamedValueSet object
    ' enter the following line.
    strText = myObj.GetText_(2)
    ```

    

4.  Opcionalmente, valide que o XML gerado na etapa 3 é um XML bem formado, criando e inicializando um objeto XML Modelo de Objeto do Documento (DOM) e, em seguida, carregar o texto XML nele.

    O exemplo de código a seguir mostra como criar e inicializar um objeto XML DOM e carregar o texto XML nele.

    ```VB
    ' Create an XMLDOM object
    set xml = CreateObject("Microsoft.xmldom")

    ' Initialize the XMLDOM object so results are returned synchronously
    xml.async = false

    ' Load the XML into the XMLDOM object
    xml.loadxml strText
    ```

    

5.  Saída da representação XML do objeto.

    O exemplo de código a seguir mostra como usar o WScript para gerar o XML.

    ```VB
    wscript.echo strText
    ```

    

    Se você optar por usar o XML DOM para verificar se o XML gerado está bem formado, substitua a linha anterior pelo seguinte.

    ```VB
    wscript.echo xml.xml
    ```

    

O exemplo de código VBScript a seguir inclui todas as etapas no procedimento anterior e codifica a classe do [**disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) em XML, incluindo a classe, a propriedade e os qualificadores de método e a exclusão de propriedades do sistema.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o WMI](using-wmi.md)
</dt> </dl>

 

