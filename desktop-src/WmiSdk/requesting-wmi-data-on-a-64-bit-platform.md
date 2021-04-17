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
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Solicitando dados WMI em uma plataforma de 64 bits

Por padrão, um aplicativo ou script recebe dados do provedor correspondente quando há duas versões de provedores. O provedor de 32 bits retorna dados para um aplicativo de 32 bits, incluindo todos os scripts, e o provedor de 64 bits retorna dados para os aplicativos compilados de 64 bits. No entanto, um aplicativo ou script pode solicitar dados do provedor não padrão, se existir, notificando o WMI por meio de sinalizadores em chamadas de método.

## <a name="context-flags"></a>Sinalizadores de contexto

Os sinalizadores de cadeia de caracteres **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** têm um conjunto de valores manipulados pelo WMI, mas não são definidos no cabeçalho do SDK ou em arquivos de biblioteca de tipos. Os valores são colocados em um parâmetro de contexto para sinalizar o WMI que ele deve solicitar dados do provedor não padrão.

O a seguir lista os sinalizadores e seus valores possíveis.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**
</dt> <dd>

Valor inteiro, 32 ou 64, que especifica a versão de 32 bits ou de 64 bits.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**
</dt> <dd>

Valor booliano usado em adição ao **\_ \_ ProviderArchitecture** para forçar a carga da versão do provedor especificada. Se a versão não estiver disponível, o WMI retornará o erro 0x80041013, **wbemErrProviderLoadFailure** para Visual Basic e **\_ falha de \_ \_ carregamento do \_ provedor WBEM** para C++. O valor padrão para esse sinalizador quando não é especificado é **false**.

</dd> </dl>

Em um sistema de 64 bits que tem versões lado a lado de um provedor, um script ou aplicativo de 32 bits recebe automaticamente dados do provedor de 32 bits, a menos que esses sinalizadores sejam fornecidos e indiquem que os dados do provedor de 64 bits devem ser retornados.

## <a name="using-the-context-flags"></a>Usando os sinalizadores de contexto

Os aplicativos C++ podem usar a interface [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) com [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) para comunicar o uso de um provedor não padrão ao WMI.

Em script e Visual Basic, você deve criar um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) contendo os sinalizadores para o parâmetro *ObjWbemNamedValueSet* de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md). Para obter mais informações sobre como configurar os objetos de parâmetros para essa chamada, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

Você pode executar scripts e aplicativos com segurança usando os sinalizadores de contexto em sistemas operacionais mais antigos, pois o WMI os ignora em sistemas nos quais eles não são implementados. Embora existam versões de 32 bits e 64 bits do provedor de registro do sistema, observe que existe apenas uma versão do repositório WMI.

## <a name="accessing-the-default-registry-hive"></a>Acessando o hive do registro padrão

A série de exemplos a seguir usa o [provedor de registro](/previous-versions/windows/desktop/regprov/system-registry-provider), que tem versões lado a lado de 32 bits e de 64 bits pré-instalados em sistemas operacionais de 64 bits. Nestes exemplos, os clientes de 32 bits obtêm dados retornados pelo provedor do nó de 32 bits **HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft**. Os clientes de 64 bits obtêm dados retornados pelo provedor do nó de 64 bits **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ log**.

Os scripts mostram como chamar os métodos da classe [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) do registro por meio de [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) para obter dados do hive do registro de 32 bits.

O script a seguir obtém dados de volta do provedor que corresponde à largura de bits do chamador, neste caso, 64 bits, porque é um script em execução no WSH (Windows Script Host) de 64 bits. O script Obtém o valor do nó do registro 64-bit **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ WBEM \\ cimom \\ Logging** em vez do nó 32-bit **HKEY \_ local \_ Machine \\ software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM**.


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



Se o valor de **log** no hive padrão for definido como 1, a saída do script deverá ser semelhante ao seguinte:

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Exemplo: solicitando especificamente o hive do registro de 32 bits em um computador de 64 bits

O exemplo modificado a seguir do script padrão usa o sinalizador de cadeia de caracteres **\_ \_ ProviderArchitecture** para solicitar acesso aos dados de registro de 32 bits em um computador de 64 bits. O chamador está conectado ao hive de 32 bits, independentemente de ser um aplicativo de 32 ou de 64 bits.


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



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Exemplo: forçando o WMI a acessar o hive do registro de 32 bits em um computador de 64 bits

A seguinte modificação do script acima, adicionando os sinalizadores **\_ \_ ProviderArchitecture** e **\_ \_ RequiredArchitecture** ao parâmetro context, força o WMI a carregar o provedor de 32 bits e obter dados de 32 bits. Se o provedor não existir, ocorrerá um erro de carregamento do provedor. O objeto de contexto deve ser fornecido na conexão com o WMI chamando [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Obter e fornecer dados em um computador de 64 bits](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
