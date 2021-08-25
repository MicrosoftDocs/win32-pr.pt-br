---
title: Chaves e entradas do Registro para um Tipo 1 Online Store
description: Chaves e entradas do Registro para um Tipo 1 Online Store
ms.assetid: cf25a004-e0c3-407c-8704-54be3601528b
keywords:
- Windows Media Player online, registro
- lojas online, registro
- tipo 1 lojas online, registro
- registry,type 1 online stores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e42b1b75b64a8736c1491ccc058fe5548d78808ba51e142b3272d17d3c0eba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861526"
---
# <a name="registry-keys-and-entries-for-a-type-1-online-store"></a>Chaves e entradas do Registro para um Tipo 1 Online Store

Para disponibilizar um armazenamento online do tipo 1 no Windows Media Player, o provedor de lojas online deve criar as seguintes sub-chaves e entradas do Registro no computador do usuário.


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
> Definir o valor de DllSurrogate como a cadeia de caracteres vazia indica que o runtime COM carregará o plug-in do armazenamento online no substituto de DLL padrão, dllhost.exe.

 

Na sintaxe do Registro anterior, os símbolos em itálico são espaço reservados para nomes e GUIDs (identificadores globalmente exclusivos) específicos do armazenamento online. A tabela a seguir descreve esses espaço reservados.



| Espaço reservado    | Descrição                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Uma cadeia de caracteres aceita entre a Microsoft e a loja online. Essa cadeia de caracteres identifica exclusivamente o armazenamento online. Exemplo: "Proseware"<br/>                                                                                                                                                                                   |
| *sinalizadores*        | UM OR bit a **bit** de um ou mais sinalizadores de funcionalidade de plug-in Esses sinalizadores especificam se Windows Media Player devem chamar métodos específicos de [IWMPContentPartner.](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) Para obter informações sobre sinalizadores com suporte, consulte a tabela de sinalizadores de funcionalidade de plug-in que segue esta tabela. Exemplo: 00000058<br/> |
| *Clsid*        | Um GUID que é o CLSID (identificador de classe) da classe que implementa **IWMPContentPartner** no plug-in da loja online. Esse GUID deve estar no formato do Registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                  |
| *Friendlyname* | Um nome amigável para a loja online. Exemplo: "Proseware Music Service"<br/>                                                                                                                                                                                                                                              |
| *appid*        | Um GUID que é o AppID (identificador de aplicativo) para o plug-in da loja online. Esse GUID deve estar no formato do Registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                |
| *pluginName*   | Um nome para o plug-in da loja online. Exemplo: "Plug-in do Parceiro de Conteúdo proseware"<br/>                                                                                                                                                                                                                                   |
| *className*    | O nome da classe que implementa **IWMPContentpartner** no plug-in da loja online. Exemplo: "CProsewarePartner"<br/>                                                                                                                                                                                              |
| *moduleName*   | O caminho totalmente qualificado para a DLL que implementa o plug-in da loja online. Exemplo: "C: \\ Proseware de Arquivos \\ \\ de ProgramasProsewarePartner.dll"<br/>                                                                                                                                                                         |
| *Threading*    | O tipo de apartment no qual o plug-in é executado. "ThreadingModel"="Apartment" indica que o plug-in é executado em um STA (single-threaded apartment). "ThreadingModel"="Free" indica que o plug-in é executado no MTA (multithreaded apartment).                                                                                     |



 

A tabela a seguir descreve os sinalizadores de funcionalidade de plug-in.



| Sinalizador                                    | Valor | Descrição                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PLANO \_ DE FUNDO DO LIMITE DA \_ ASSINATURAPROCESSAMENTO | 0x8   | Windows Media Player deve chamar [IWMPContentPartner::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-notify) para informar o plug-in quando ele deve iniciar e parar o processamento em segundo plano.                                                                                                     |
| DISPOSITIVO \_ DE LIMITE DE \_ ASSINATURAAVAILABLE      | 0x10  | Windows Media Player deve chamar [IWMPContentPartner::UpdateDevice](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-updatedevice).                                                                                                                                                                   |
| O \_ LIMITE DA ASSINATURA É \_ \_ CONTENTPARTNER   | 0x40  | Informa Windows Media Player que o plug-in implementa a interface **IWMPContentPartner.** Todos os plug-ins de loja online do tipo 1 devem definir esse sinalizador.                                                                                                                         |
| \_ALTLOGIN DE LIMITE DE \_ ASSINATURA             | 0x80  | Informa Windows Media Player que o plug-in dá suporte a um logon alternativo. Se o plug-in for compatível com um logon alternativo, Windows Media Player recuperará a URL de logon e a legenda alternativas chamando [IWMPContentPartner::GetItemInfo.](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) |



 

**Entradas do Registro para desenvolvimento e teste**

Quando você começa a desenvolver sua loja online, a Microsoft fornece duas chaves: uma chave de teste e uma chave de produção. Durante a fase de desenvolvimento e teste, sua loja online será exibida Windows Media Player somente se a chave de teste ou a chave de produção estiver no Registro no computador do usuário. Para obter mais informações sobre as chaves de teste e produção, consulte [Test and Production Keys for a Type 1 Online Store](test-and-production-keys-for-a-type-1-online-store.md).

Coloque sua chave de teste ou de produção no local a seguir no Registro.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "key1;key2;...;keyN"
```



Observe que o valor da entrada do Registro TestParameter pode especificar várias chaves de teste ou de produção. Por exemplo, suponha que Proseware tenha uma chave de teste "1234" e a Contoso tenha uma chave de teste "2345". A entrada do Registro a seguir especifica que os armazenamentos de teste para Proseware e Contoso serão exibidos Windows Media Player.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Services]
"TestParameter" = "1234;2345"
```



**Entrada do Registro do ActiveService**

Quando o usuário ativa um armazenamento online, Windows Media Player grava informações no registro que identifica o armazenamento online ativo. Windows Media Player coloca as informações no local a seguir no Registro no computador do usuário.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



Na sintaxe do Registro anterior, *serviceInfo* é um espaço reservado para uma cadeia de caracteres que contém informações descritivas sobre o armazenamento online ativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 1**](reference-for-type-1-online-stores.md)
</dt> </dl>

 

 





