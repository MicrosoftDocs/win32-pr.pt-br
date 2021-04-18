---
description: Você pode usar a biblioteca de tipos de script do WMI para chamar métodos de API de script do WMI de Microsoft Visual Studio e em arquivos WSF do host de script do Windows.
ms.assetid: 6ef4e210-0733-4f2a-89c1-1a7aca5a19d9
ms.tgt_platform: multiple
title: Usando a biblioteca de tipos de script WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8ba419d9a9b676d798b97e3b1a57f4e038d97814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105807803"
---
# <a name="using-the-wmi-scripting-type-library"></a><span data-ttu-id="de238-103">Usando a biblioteca de tipos de script WMI</span><span class="sxs-lookup"><span data-stu-id="de238-103">Using the WMI Scripting Type Library</span></span>

<span data-ttu-id="de238-104">Você pode usar a biblioteca de tipos de script do WMI para chamar métodos de API de script do WMI de Microsoft Visual Studio e em arquivos WSF do host de script do Windows.</span><span class="sxs-lookup"><span data-stu-id="de238-104">You can use the WMI scripting type library to call WMI Scripting API methods from Microsoft Visual Studio and in Windows Script Host WSF files.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-microsoft-visual-studio"></a><span data-ttu-id="de238-105">Usando a biblioteca de tipos de script WMI com Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="de238-105">Using the WMI Scripting Type Library with Microsoft Visual Studio</span></span>

> [!Note]  
> <span data-ttu-id="de238-106">Os recursos do Visual InterDev 6,0 foram integrados ao [Microsoft Visual Studio .net](https://msdn.microsoft.com/vstudio/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="de238-106">Visual InterDev 6.0 features have been integrated into [Microsoft Visual Studio .NET](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

 

<span data-ttu-id="de238-107">O procedimento a seguir descreve como habilitar o IDE (ambiente de desenvolvimento integrado) para estar ciente da biblioteca de tipos WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="de238-107">The following procedure describes how to enable the integrated development environment (IDE) to be aware of the WbemScripting type library.</span></span>

<span data-ttu-id="de238-108">**Para adicionar a biblioteca de tipos de script WMI às referências do projeto**</span><span class="sxs-lookup"><span data-stu-id="de238-108">**To add the WMI Scripting type library to the project references**</span></span>

1.  <span data-ttu-id="de238-109">Selecione **Adicionar referências** no menu **projeto** .</span><span class="sxs-lookup"><span data-stu-id="de238-109">Select **Add References** from the **Project** menu.</span></span>
2.  <span data-ttu-id="de238-110">Na guia COM da caixa **Adicionar referência** , selecione biblioteca de script do Microsoft WMI v 1.2.</span><span class="sxs-lookup"><span data-stu-id="de238-110">In the COM tab of the **Add Reference** box, select Microsoft WMI Scripting V1.2 Library.</span></span>
3.  <span data-ttu-id="de238-111">Se nenhuma opção adequada aparecer na lista de referências, adicione-a usando **procurar** na caixa **referências** .</span><span class="sxs-lookup"><span data-stu-id="de238-111">If no suitable option appears in the References list, add it by using **Browse** in the **References** box.</span></span> <span data-ttu-id="de238-112">A **procura** abre uma caixa **Adicionar referência** que permite que você localize a biblioteca de tipos WbemScripting.</span><span class="sxs-lookup"><span data-stu-id="de238-112">The **Browse** opens an **Add Reference** box that enables you to locate the WbemScripting type library.</span></span>

    <span data-ttu-id="de238-113">A biblioteca de tipos WbemScripting reside no arquivo Wbemdisp. tlb no diretório% windir% \\ System32 \\ WBEM.</span><span class="sxs-lookup"><span data-stu-id="de238-113">The WbemScripting type library resides in the file Wbemdisp.tlb in the %windir%\\System32\\Wbem directory.</span></span>

4.  <span data-ttu-id="de238-114">Selecione o arquivo e clique em **Abrir**.</span><span class="sxs-lookup"><span data-stu-id="de238-114">Select the file and click **Open**.</span></span> <span data-ttu-id="de238-115">A biblioteca de scripts do Microsoft WMI V 1.2 aparece na lista de referências.</span><span class="sxs-lookup"><span data-stu-id="de238-115">Microsoft WMI Scripting V1.2 Library appears on the references list.</span></span> <span data-ttu-id="de238-116">Certifique-se de selecionar a caixa ao lado desse item na lista.</span><span class="sxs-lookup"><span data-stu-id="de238-116">Ensure that you select the box next to this item in the list.</span></span>

## <a name="using-the-wmi-scripting-type-library-with-windows-script-host-20"></a><span data-ttu-id="de238-117">Usando a biblioteca de tipos de script do WMI com o Windows Script Host 2,0</span><span class="sxs-lookup"><span data-stu-id="de238-117">Using the WMI Scripting Type Library with Windows Script Host 2.0</span></span>

<span data-ttu-id="de238-118">Você pode incluir a referência ao **WbemScripting. SWbemLocator** em um arquivo wsf do host de script do Windows, ao contrário de um script escrito em Visual Basic, Scripting Edition ou outras linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="de238-118">You can include the reference to the **WbemScripting.SWbemLocator** in a Windows Script Host WSF file, unlike a script written in Visual Basic, Scripting Edition or other scripting languages.</span></span> <span data-ttu-id="de238-119">Isso permite que você use nomes constantes em vez de valores.</span><span class="sxs-lookup"><span data-stu-id="de238-119">This enables you to use constant names instead of values.</span></span> <span data-ttu-id="de238-120">Por exemplo, use **WbemAuthenticationLevelPktPrivacy** em vez do valor 6 ao definir a autenticação.</span><span class="sxs-lookup"><span data-stu-id="de238-120">For example, use **WbemAuthenticationLevelPktPrivacy** rather than the value 6 when setting authentication.</span></span>

<span data-ttu-id="de238-121">Os scripts podem se conectar à API de script para a biblioteca de tipos do WMI usando os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="de238-121">Scripts can connect with the Scripting API for WMI type library using the following methods:</span></span>

-   <span data-ttu-id="de238-122">Especificar o GUID WbemScripting nos métodos do VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) e [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="de238-122">Specifying the WbemScripting GUID in the VBScript methods [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) and [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span></span>

    <span data-ttu-id="de238-123">Isso alerta o host de scripts do Windows para se conectar ao conjunto de objetos WMI.</span><span class="sxs-lookup"><span data-stu-id="de238-123">This alerts Windows Script Host to connect to the WMI object set.</span></span>

    <span data-ttu-id="de238-124">O exemplo de código VBScript a seguir cria um novo objeto [**SWbemDateTime**](swbemdatetime.md) .</span><span class="sxs-lookup"><span data-stu-id="de238-124">The following VBScript code example creates a new [**SWbemDateTime**](swbemdatetime.md) object.</span></span>

    ```VB
    Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
    ```

    

-   <span data-ttu-id="de238-125">Usando a [cadeia de caracteres do moniker](constructing-a-moniker-string.md) "winmgmts:" ao obter um objeto novo ou existente.</span><span class="sxs-lookup"><span data-stu-id="de238-125">Using the [Moniker string](constructing-a-moniker-string.md) "winmgmts:" when obtaining a new or existing object.</span></span>

    <span data-ttu-id="de238-126">O exemplo de código VBScript a seguir usa o moniker "winmgmts:" para obter a instância do [**\_ processo Win32**](/windows/desktop/CIMWin32Prov/win32-process) com uma propriedade **Handle** de 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="de238-126">The following VBScript code example uses the "winmgmts:" moniker to get the instance of [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) with a **Handle** property of 0 (zero).</span></span> <span data-ttu-id="de238-127">**Handle** é a propriedade de chave para essa classe.</span><span class="sxs-lookup"><span data-stu-id="de238-127">**Handle** is the key property for this class.</span></span>

    ```VB
    Set Process = GetObject("winmgmts:Win32_Process.Handle=0")
    ```

    

-   <span data-ttu-id="de238-128">Referenciando a biblioteca de tipos WMI usando a <reference> marca do formato de arquivo XML do WSH 2,0.</span><span class="sxs-lookup"><span data-stu-id="de238-128">Referencing the WMI type library using the <reference> tag of the WSH 2.0 XML file format.</span></span> <span data-ttu-id="de238-129">Se você usar a <reference> marca, a marca deverá ter um atributo **UUID** cujo valor é o **GUID** da biblioteca de tipos WMI ou (recomendado) um atributo Object cujo valor é o **ProgID** de qualquer um dos objetos de script WMI que você pode criar.</span><span class="sxs-lookup"><span data-stu-id="de238-129">If you use the <reference> tag, the tag must have either a **uuid** attribute whose value is the **GUID** of the WMI type library, or (recommended) an object attribute whose value is the **PROGID** of any of the WMI scripting objects you can create.</span></span>

    <span data-ttu-id="de238-130">O exemplo de código VBScript a seguir usa o PROGID de "WbemScripting".</span><span class="sxs-lookup"><span data-stu-id="de238-130">The following VBScript code example uses the PROGID of "WbemScripting" .</span></span> <span data-ttu-id="de238-131">Para executar o script, salve o texto em um arquivo com uma extensão. wsf.</span><span class="sxs-lookup"><span data-stu-id="de238-131">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```VB
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
    <reference object="WbemScripting.SWbemLocator"/>
    <script language="VBScript">
        set service = GetObject("winmgmts:")
        ' Following line uses a symbolic 
        ' constant from the WMI type library
        service.Security_.impersonationLevel = _
            wbemImpersonationLevelDelegate
    </script>
    </job>
    ```

    

-   <span data-ttu-id="de238-132">Usando um **objeto** <> marca para criar um objeto de script WMI.</span><span class="sxs-lookup"><span data-stu-id="de238-132">Using an <**object**> tag to create a WMI scripting object.</span></span> <span data-ttu-id="de238-133">Você pode especificar o atributo **ID** com o valor de um nome que faz referência ao objeto de script WMI que você deseja criar e o atributo **ProgID** igual ao PROID do objeto de script WMI.</span><span class="sxs-lookup"><span data-stu-id="de238-133">You can specify the **id** attribute with the value of a name that references the WMI scripting object you want to create, and the **progid** attribute equal to the PROID of the WMI scripting object.</span></span>

    <span data-ttu-id="de238-134">O script do WSH a seguir exibe o nome do host e o número de processadores no computador local.</span><span class="sxs-lookup"><span data-stu-id="de238-134">The following WSH script displays the hostname and the number of processors on the local computer.</span></span> <span data-ttu-id="de238-135">Para executar o script, salve o texto em um arquivo com uma extensão. wsf.</span><span class="sxs-lookup"><span data-stu-id="de238-135">To run the script, save the text in a file with a .wsf extension.</span></span>

    ```XML
    <?xml version="1.0" encoding="US-ASCII"?>
    <job>
     <object id="objSWbemLocator" progid="WbemScripting.SWbemLocator"/>
     <script language="VBScript">

      strComputer = "."
      Set objSWbemServices = objSWbemLocator.ConnectServer(strComputer, "root\cimv2")
      Set colSettings = objSWbemServices.ExecQuery("Select * From Win32_ComputerSystem")
      For Each objComputer in colSettings
       Wscript.Echo "System Name: " & objComputer.Name
       Wscript.Echo "Number of Processors: " & objComputer.NumberOfProcessors
      Next

     </script>
    </job>
    ```

    

## <a name="related-topics"></a><span data-ttu-id="de238-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="de238-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de238-137">Scripts no WMI</span><span class="sxs-lookup"><span data-stu-id="de238-137">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> <dt>

[<span data-ttu-id="de238-138">API de script para WMI</span><span class="sxs-lookup"><span data-stu-id="de238-138">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
