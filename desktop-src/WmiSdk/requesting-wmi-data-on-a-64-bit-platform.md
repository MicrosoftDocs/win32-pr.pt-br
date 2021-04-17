---
description: Por padrão, um aplicativo ou script recebe dados do provedor correspondente quando há duas versões de provedores.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Solicitando dados WMI em uma plataforma de 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759793"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a><span data-ttu-id="a1b9a-103">Solicitando dados WMI em uma plataforma de 64 bits</span><span class="sxs-lookup"><span data-stu-id="a1b9a-103">Requesting WMI Data on a 64-bit Platform</span></span>

<span data-ttu-id="a1b9a-104">Por padrão, um aplicativo ou script recebe dados do provedor correspondente quando há duas versões de provedores.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-104">By default, an application or script receives data from the corresponding provider when two versions of providers exist.</span></span> <span data-ttu-id="a1b9a-105">O provedor de 32 bits retorna dados para um aplicativo de 32 bits, incluindo todos os scripts, e o provedor de 64 bits retorna dados para os aplicativos compilados de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-105">The 32-bit provider returns data to a 32-bit application, including all scripts, and the 64-bit provider returns data to the 64-bit compiled applications.</span></span> <span data-ttu-id="a1b9a-106">No entanto, um aplicativo ou script pode solicitar dados do provedor não padrão, se existir, notificando o WMI por meio de sinalizadores em chamadas de método.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-106">However, an application or script can request data from the nondefault provider, if it exists, by notifying WMI through flags on method calls.</span></span>

## <a name="context-flags"></a><span data-ttu-id="a1b9a-107">Sinalizadores de contexto</span><span class="sxs-lookup"><span data-stu-id="a1b9a-107">Context Flags</span></span>

<span data-ttu-id="a1b9a-108">Os sinalizadores de cadeia de caracteres **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** têm um conjunto de valores manipulados pelo WMI, mas não são definidos no cabeçalho do SDK ou em arquivos de biblioteca de tipos.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-108">The **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** string flags have a set of values handled by WMI but not defined in SDK header or type library files.</span></span> <span data-ttu-id="a1b9a-109">Os valores são colocados em um parâmetro de contexto para sinalizar o WMI que ele deve solicitar dados do provedor não padrão.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-109">The values are placed in a context parameter to signal WMI that it should request data from the nondefault provider.</span></span>

<span data-ttu-id="a1b9a-110">O a seguir lista os sinalizadores e seus valores possíveis.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-110">The following lists the flags and their possible values.</span></span>

<dl> <dt>

<span data-ttu-id="a1b9a-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-111"><span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-112">Valor inteiro, 32 ou 64, que especifica a versão de 32 bits ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-112">Integer value, either 32 or 64, that specifies the 32-bit or 64-bit version.</span></span>

</dd> <dt>

<span data-ttu-id="a1b9a-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span><span class="sxs-lookup"><span data-stu-id="a1b9a-113"><span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**</span></span>
</dt> <dd>

<span data-ttu-id="a1b9a-114">Valor booliano usado em adição ao **\_ \_ ProviderArchitecture** para forçar a carga da versão do provedor especificada.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-114">Boolean value used in addition to **\_\_ProviderArchitecture** to force load the specified provider version.</span></span> <span data-ttu-id="a1b9a-115">Se a versão não estiver disponível, o WMI retornará o erro 0x80041013, **wbemErrProviderLoadFailure** para Visual Basic e **\_ falha de \_ \_ carregamento do \_ provedor WBEM** para C++.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-115">If the version is unavailable, then WMI returns the error 0x80041013, **wbemErrProviderLoadFailure** for Visual Basic and **WBEM\_E\_PROVIDER\_LOAD\_FAILURE** for C++.</span></span> <span data-ttu-id="a1b9a-116">O valor padrão para esse sinalizador quando não é especificado é **false**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-116">The default value for this flag when it is not specified is **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="a1b9a-117">Em um sistema de 64 bits que tem versões lado a lado de um provedor, um script ou aplicativo de 32 bits recebe automaticamente dados do provedor de 32 bits, a menos que esses sinalizadores sejam fornecidos e indiquem que os dados do provedor de 64 bits devem ser retornados.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-117">On a 64-bit system that has side-by-side versions of a provider, a 32-bit application or script automatically receives data from the 32-bit provider, unless these flags are supplied and indicate that the 64-bit provider data should be returned.</span></span>

## <a name="using-the-context-flags"></a><span data-ttu-id="a1b9a-118">Usando os sinalizadores de contexto</span><span class="sxs-lookup"><span data-stu-id="a1b9a-118">Using the Context Flags</span></span>

<span data-ttu-id="a1b9a-119">Os aplicativos C++ podem usar a interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) para comunicar o uso de um provedor não padrão ao WMI.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-119">C++ applications can use the [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) interface with [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) to communicate the use of a nondefault provider to WMI.</span></span>

<span data-ttu-id="a1b9a-120">Em script e Visual Basic, você deve criar um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) contendo os sinalizadores para o parâmetro *ObjWbemNamedValueSet* de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="a1b9a-120">In scripting and Visual Basic, you must create a [**SWbemNamedValueSet**](swbemnamedvalueset.md) object containing the flags for the *objWbemNamedValueSet* parameter of [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="a1b9a-121">Para obter mais informações sobre como configurar os objetos de parâmetros para essa chamada, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="a1b9a-121">For more information about setting up the parameters objects for this call, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="a1b9a-122">Você pode executar scripts e aplicativos com segurança usando os sinalizadores de contexto em sistemas operacionais mais antigos, pois o WMI os ignora em sistemas nos quais eles não são implementados.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-122">You can safely run scripts and applications using the context flags in older operating systems, because WMI ignores them in systems in which they are not implemented.</span></span> <span data-ttu-id="a1b9a-123">Embora existam versões de 32 bits e 64 bits do provedor de registro do sistema, observe que existe apenas uma versão do repositório WMI.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-123">While 32-bit and 64-bit versions of the System Registry provider exist, note that only one version of the WMI repository exists.</span></span>

## <a name="accessing-the-default-registry-hive"></a><span data-ttu-id="a1b9a-124">Acessando o hive do registro padrão</span><span class="sxs-lookup"><span data-stu-id="a1b9a-124">Accessing the Default Registry Hive</span></span>

<span data-ttu-id="a1b9a-125">A série de exemplos a seguir usa o [provedor de registro](/previous-versions/windows/desktop/regprov/system-registry-provider), que tem versões lado a lado de 32 bits e de 64 bits pré-instalados em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-125">The following series of examples use the [Registry Provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which has side-by-side 32-bit and 64-bit versions preinstalled on 64-bit operating systems.</span></span> <span data-ttu-id="a1b9a-126">Nestes exemplos, os clientes de 32 bits obtêm dados retornados pelo provedor do nó de 32 bits **HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-126">In these examples, 32-bit clients get data returned by the provider from the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft**.</span></span> <span data-ttu-id="a1b9a-127">Os clientes de 64 bits obtêm dados retornados pelo provedor do nó de 64 bits **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ log**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-127">64-bit clients get data returned by the provider from the 64-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Logging**.</span></span>

<span data-ttu-id="a1b9a-128">Os scripts mostram como chamar os métodos da classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) do registro por meio de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para obter dados do hive do registro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-128">The scripts show how to call the methods of the Registry [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) class through [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) to obtain data from the 32-bit registry hive.</span></span>

<span data-ttu-id="a1b9a-129">O script a seguir obtém dados de volta do provedor que corresponde à largura de bits do chamador, neste caso, 64 bits, porque é um script em execução no WSH (Windows Script Host) de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-129">The following script gets back data from the provider that matches the bit width of the caller, in this case 64 bits, because it is a script running under the 64-bit Windows Script Host (WSH).</span></span> <span data-ttu-id="a1b9a-130">O script Obtém o valor do nó do registro 64-bit **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ cimom \\ Logging** em vez do nó 32-bit **HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-130">The script gets the value from the 64-bit registry node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WBEM\\CIMOM\\Logging** rather than the 32-bit node **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Wow6432Node\\Microsoft\\WBEM\\CIMOM**.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



<span data-ttu-id="a1b9a-131">Se o valor de **log** no hive padrão for definido como 1, a saída do script deverá ser semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="a1b9a-131">If the **Logging** value in the default hive is set to 1, then the output from the script should look something like the following:</span></span>

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="a1b9a-132">Exemplo: solicitando especificamente o hive do registro de 32 bits em um computador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="a1b9a-132">Example: Specifically Requesting the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="a1b9a-133">O exemplo modificado a seguir do script padrão usa o sinalizador de cadeia de caracteres **\_ \_ ProviderArchitecture** para solicitar acesso aos dados de registro de 32 bits em um computador de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-133">The following modified example of the default script uses the **\_\_ProviderArchitecture** string flag to request access to the 32-bit registry data on a 64-bit computer.</span></span> <span data-ttu-id="a1b9a-134">O chamador está conectado ao hive de 32 bits, independentemente de ser um aplicativo de 32 ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-134">The caller is connected to the 32-bit hive irrespective of whether it is a 32- or 64-bit application.</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a><span data-ttu-id="a1b9a-135">Exemplo: forçando o WMI a acessar o hive do registro de 32 bits em um computador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="a1b9a-135">Example: Forcing WMI to Access the 32-bit Registry Hive on a 64-bit Computer</span></span>

<span data-ttu-id="a1b9a-136">A seguinte modificação do script acima, adicionando os sinalizadores **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** ao parâmetro context, força o WMI a carregar o provedor de 32 bits e obter dados de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-136">The following modification of the script above by adding the **\_\_ProviderArchitecture** and **\_\_RequiredArchitecture** flags to the context parameter forces WMI to load the 32-bit provider and get 32-bit data.</span></span> <span data-ttu-id="a1b9a-137">Se o provedor não existir, ocorrerá um erro de carregamento do provedor.</span><span class="sxs-lookup"><span data-stu-id="a1b9a-137">If the provider does not exist, then a provider load error occurs.</span></span> <span data-ttu-id="a1b9a-138">O objeto de contexto deve ser fornecido na conexão com o WMI chamando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).</span><span class="sxs-lookup"><span data-stu-id="a1b9a-138">The context object must be supplied in the connection to WMI by calling [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md).</span></span>


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a><span data-ttu-id="a1b9a-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1b9a-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1b9a-140">Obter e fornecer dados em um computador de 64 bits</span><span class="sxs-lookup"><span data-stu-id="a1b9a-140">Getting and Providing Data on a 64-bit Computer</span></span>](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
