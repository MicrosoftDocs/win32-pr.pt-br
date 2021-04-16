---
title: Chaves e entradas do registro para uma loja online tipo 1
description: Chaves e entradas do registro para uma loja online tipo 1
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Armazenamentos online do Windows Media Player, registro
- lojas online, registro
- tipo 1 lojas online, registro
- registro, tipo 1 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1329ad69e91ebce41b258d1e148403f62caceb96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105761434"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Chaves e entradas do registro para uma loja online tipo 1

Para tornar um repositório online tipo 1 disponível no Windows Media Player, o provedor de loja online deve criar as seguintes subchaves e entradas do registro no computador do usuário.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\AppID\appid]
@=pluginName
"DllSurrogate"=""

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className
"AppID"="appid"

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="threading"
```



> [!Note]  
> Definir o valor de DllSurrogate como a cadeia de caracteres vazia indica que o tempo de execução COM carregará o plug-in da loja online na DLL padrão como alternativa, dllhost.exe.

 

Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para a loja online. A tabela a seguir descreve esses espaços reservados.



| Espaço reservado    | Descrição                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Uma cadeia de caracteres acordada entre a Microsoft e a loja online. Essa cadeia de caracteres identifica exclusivamente o repositório online. Exemplo: "Proseware"<br/>                                                                                                                                                                                   |
| *sinalizadores*        | Um ou **mais bits de** capacidade de plug-in de um ou mais sinalizadores especificam se o Windows Media Player deve chamar métodos específicos de [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner). Para obter informações sobre sinalizadores com suporte, consulte a tabela de sinalizadores de recurso de plug-in que segue esta tabela. Exemplo: 00000058<br/> |
| *CLSID*        | Um GUID que é o identificador de classe (CLSID) para a classe que implementa **IWMPContentPartner** no plug-in da loja online. Esse GUID deve estar no formato de registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *FriendlyName* | Um nome amigável para a loja online. Exemplo: "serviço de música da Proseware"<br/>                                                                                                                                                                                                                                              |
| *appid*        | Um GUID que é o identificador de aplicativo (AppID) para o plug-in da loja online. Esse GUID deve estar no formato de registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Um nome para o plug-in da loja online. Exemplo: "plug-in de parceiro de conteúdo da Proseware"<br/>                                                                                                                                                                                                                                   |
| *className*    | O nome da classe que implementa **IWMPContentpartner** no plug-in da loja online. Exemplo: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | O caminho totalmente qualificado para a DLL que implementa o plug-in da loja online. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | O tipo de compartimento em que o plug-in é executado. "ThreadingModel" = "Apartment" indica que o plug-in é executado em um STA (single-threaded apartment). "ThreadingModel" = "Free" indica que o plug-in é executado no MTA (multithreaded apartment).                                                                                     |



 

A tabela a seguir descreve os sinalizadores de capacidade de plug-in.



| Sinalizador                                    | Valor | Descrição                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_BACKGROUNDPROCESSING do limite da assinatura \_ | 0x8   | O Windows Media Player deve chamar [IWMPContentPartner:: Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) para informar o plug-in quando ele deve iniciar e parar o processamento em segundo plano.                                                                                                     |
| \_DEVICEAVAILABLE do limite da assinatura \_      | 0x10  | O Windows Media Player deve chamar [IWMPContentPartner:: UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| o \_ limite da assinatura \_ é \_ CONTENTPARTNER   | 0x40  | Informa ao Windows Media Player que o plug-in implementa a interface **IWMPContentPartner** . Todos os plug-ins da loja online tipo 1 devem definir esse sinalizador.                                                                                                                         |
| \_ALTLOGIN do limite da assinatura \_             | 0x80  | Informa ao Windows Media Player que o plug-in dá suporte a um logon alternativo. Se o plug-in der suporte a um logon alternativo, o Windows Media Player recuperará a URL de logon alternativa e a legenda chamando [IWMPContentPartner:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo). |



 

**Entradas de registro para desenvolvimento e teste**

Quando você começa a desenvolver sua loja online, a Microsoft fornece duas chaves: uma chave de teste e uma chave de produção. Durante a fase de desenvolvimento e teste, sua loja online será exibida no Windows Media Player somente se sua chave de teste ou sua chave de produção estiver no registro no computador do usuário. Para obter mais informações sobre as chaves de teste e de produção, consulte [chaves de teste e de produção para uma loja online tipo 1](test-and-production-keys-for-a-type-1-online-store.md).

Coloque sua chave de teste ou de produção no seguinte local do registro.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Observe que o valor da entrada do registro TestParameter pode especificar várias chaves de teste ou de produção. Por exemplo, suponha que o Proseware tenha uma chave de teste de "1234" e que a contoso tenha uma chave de teste de "2345". A seguinte entrada do Registro especifica que os repositórios de teste para a Proseware e a contoso serão exibidos no Windows Media Player.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Entrada do registro ActiveService**

Quando o usuário ativa uma loja online, o Windows Media Player grava as informações no registro que identificam o repositório online ativo. O Windows Media Player coloca as informações no seguinte local no registro no computador do usuário.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



Na sintaxe de registro anterior, o *serviceInfo* é um espaço reservado para uma cadeia de caracteres que contém informações descritivas sobre a loja online ativa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





