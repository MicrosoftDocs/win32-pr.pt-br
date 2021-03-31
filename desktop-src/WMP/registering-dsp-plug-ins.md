---
title: Registrando plug-ins do DSP
description: Registrando plug-ins do DSP
ms.assetid: af264ff7-702b-4a49-a14d-ab8563a40c4e
keywords:
- Plug-ins do Windows Media Player, entradas do registro
- plug-ins, entradas do registro
- plug-ins de processamento de sinal digital, entradas de registro
- Plug-ins do DSP, entradas do registro
- registro, plug-ins do DSP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64e7afd43cf242d57c0a9375c4cbda56e457ef1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103916997"
---
# <a name="registering-dsp-plug-ins"></a>Registrando plug-ins do DSP

Para disponibilizar seu plug-in do DSP no Windows Media Player, você deve criar as seguintes subchaves e entradas do registro no computador do usuário.


```C++
[HKEY_CLASSES_ROOT\CLSID\PluginClsid]
@=PluginClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PluginClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Threading"
```



Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para o plug-in do DSP. A tabela a seguir descreve esses espaços reservados.



| Espaço reservado               | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                  |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PluginClsid*             | Um GUID que é o identificador de classe para a classe principal do plug-in do DSP. Essa é a classe que implementa **IMediaObject**, **IPluginEnable** e possivelmente **ISpecifyPropertyPages**. Em um plug-in de modo duplo, essa classe também implementa **IMFTransform** e **IMFGetService**. Esse GUID deve estar no formato de registro, completo com as chaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PluginClassFriendlyName* | Um nome amigável para a classe principal do plug-in do DSP. Exemplo: "classe ProsewareDSP"<br/>                                                                                                                                                                                                                                                                                                                                 |
| *PluginModuleName*        | O caminho totalmente qualificado para a DLL que implementa o plug-in do DSP. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                                                                                                                                                                                                                     |
| *Threading*               | Uma cadeia de caracteres que especifica o modelo de threading para o plug-in. Se o plug-in for executado com o Windows Media Player 11 no Windows Vista, essa entrada de registro deverá ser igual a "both". Se o plug-in for executado no Windows XP ou em sistemas operacionais mais antigos, essa entrada de registro poderá ser igual a "Apartment" ou "both".                                                                                           |



 

Se o seu plug-in do DSP implementar uma interface personalizada e se o seu plug-in for executado no Windows Media Player 11 no Windows Vista, você deverá criar as seguintes subchaves e entradas do registro no computador do usuário.


```C++
[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid]
@=PSFactoryBuffer

[HKEY_CLASSES_ROOT\CLSID\ProxyStubClsid\InprocServer32]
@=ProxyStubModuleName
"ThreadingModel"="Apartment"

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId]
@=CustomInterfaceName

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\NumMethods]
@=NumberOfMethods

[HKEY_CLASSES_ROOT\Interfaces\CustomInterfaceId\ProxyStubClsid32]
@=ProxyStubClsid
```



Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes, valores numéricos e identificadores globalmente exclusivos (GUIDs) que são específicos para o plug-in do DSP. A tabela a seguir descreve esses espaços reservados.



| Espaço reservado           | Descrição                                                                                                                                                                                                                                                                |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *ProxyStubClsid*      | Um GUID que é o identificador de classe da classe que implementa os proxies e os stubs para as interfaces personalizadas do plug-in do DSP. Esse GUID deve estar no formato de registro, completo com as chaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *ProxyStubModuleName* | O caminho totalmente qualificado para a DLL que implementa as interfaces de proxy e stub para o plug-in do DSP. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareDspPS.dll"<br/>                                                                                               |
| *CustomInterfaceId*   | Um GUID que é o identificador de interface para uma interface personalizada que é implementada pelo plug-in do DSP. Esse GUID deve estar no formato de registro, completo com as chaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                           |
| *CustomInterfaceName* | O nome de uma interface personalizada que é implementada pelo plug-in do DSP. Exemplo: "IProsewareDsp"<br/>                                                                                                                                                                  |
| *NumberOfMethods*     | O número de métodos, incluindo os métodos herdados, definidos por uma interface personalizada. Exemplo: "5"<br/>                                                                                                                                                                  |



 

Se o plug-in do DSP fornecer uma página de propriedades, você deverá criar as seguintes subchaves e entradas do registro no computador do usuário.


```C++
[HKEY_CLASSES_ROOT\CLSID\PropPageClsid]
@=PropPageClassFriendlyName

[HKEY_CLASSES_ROOT\CLSID\PropPageClsid\InprocServer32]
@=PluginModuleName
"ThreadingModel"="Apartment"
```



Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para o plug-in do DSP. A tabela a seguir descreve esses espaços reservados.



| Espaço reservado                 | Descrição                                                                                                                                                                                                                            |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *PropPageClsid*             | Um GUID que é o identificador de classe para a classe de página de propriedades fornecida pelo plug-in DSP. Esse GUID deve estar no formato de registro, completo com as chaves.<br/> Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/> |
| *PropPageClassFriendlyName* | Um nome amigável para a classe da página de propriedades. Exemplo: "classe de página da propriedade ProsewareDSP"<br/>                                                                                                                                     |
| *PluginModuleName*          | O caminho totalmente qualificado para a DLL que implementa o plug-in do DSP. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareDsp.dll"<br/>                                                                                               |



 

**Chamando IWMPPluginRegistrar**

Além das entradas e das subchaves do Registro descritas nas listas e tabelas anteriores, você deve criar algumas chaves e entradas do registro chamando [IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpregisterplayerplugin). Esse método executa o registro necessário para habilitar o Windows Media Player a reconhecer seu plug-in e apresentá-lo como uma opção para o usuário.

Chame **IWMPMediaPluginRegistrar:: WMPRegisterPlayerPlugin** na função **DllRegisterServer** de seu plug-in e chame [IWMPMediaPluginRegistrar:: WMPUnRegisterPlayerPlugin](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpmediapluginregistrar-wmpunregisterplayerplugin) na função **DllUnregisterServer** do seu plug-in. Para obter um ponteiro para uma interface **IWMPMediaPluginRegistrar** , chame **COCREATEINSTANCE**, passando CLSID \_ WMPMediaPluginRegistrar como a ID de classe. A constante CLSID \_ WMPMediaPluginRegistrar é definida em wmpservices. h.

**Registro no assistente de plug-in do DSP**

O assistente de plug-in do DSP, que está incluído na SDK do Windows, gera um código de exemplo baseado em Active Template Library (ATL). A função **DllRegisterServer** do plug-in de exemplo chama a função **RegisterServer** da ATL, que cria subchaves e entradas do registro de acordo com dois arquivos de script do registro no projeto do Visual Studio. O arquivo *ProjectName*. RGS contém o script para registrar a classe principal do plug-in e o arquivo *ProjectName* PropPage. RGS contém o script para registrar a classe da página de propriedades do plug-in. A função **DllRegisterServer** do plug-in de exemplo também chama **IWMPPluginRegistrar:: WMPRegisterPlayerPlugin**.

O assistente de plug-in do DSP também gera código para um componente de stub de proxy que é um arquivo. dll de registro automático. O código de registro para esse arquivo está em dlldata. cpp. As **\_ rotinas de dlldata** de macros se expandem para incluir uma implementação de **DllRegisterServer**.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Visão geral do desenvolvedor de plug-in do DSP**](dsp-plug-in-developer-overview.md)
</dt> <dt>

[**IWMPMediaPluginRegistrar**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpmediapluginregistrar)
</dt> </dl>

 

 





