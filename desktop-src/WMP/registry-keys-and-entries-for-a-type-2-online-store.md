---
title: Chaves e entradas do registro para uma loja online tipo 2
description: Chaves e entradas do registro para uma loja online tipo 2
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Armazenamentos online do Windows Media Player, registro
- lojas online, registro
- tipo 2 lojas online, registro
- registro, tipo 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 685a26514730e7c370c698cbc9c64c29366c35ee
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104084390"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Chaves e entradas do registro para uma loja online tipo 2

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

Para disponibilizar um armazenamento online tipo 2 no Windows Media Player, o provedor de loja online deve criar as seguintes subchaves de registro e entradas no computador do usuário.


```C++
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\Subscriptions\keyName]
"Capabilities"=dword:flags
"SubscriptionObjectGUID"=clsid
"FriendlyName"=friendlyName

[HKEY_CLASSES_ROOT\CLSID\clsid]
@=className

[HKEY_CLASSES_ROOT\CLSID\clsid\InprocServer32]
@=moduleName
"ThreadingModel"="Apartment"
```



Na sintaxe de registro anterior, os símbolos em itálico são espaços reservados para nomes e identificadores globalmente exclusivos (GUIDs) que são específicos para a loja online. A tabela a seguir descreve esses espaços reservados.



| Espaço reservado    | Descrição                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Uma cadeia de caracteres acordada entre a Microsoft e a loja online. Essa cadeia de caracteres identifica exclusivamente o repositório online. Exemplo: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *sinalizadores*        | Um operador de plug-in ou uma operação unificada **ou** de um ou mais sinalizadores especificam se o Windows Media Player deve chamar métodos específicos de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2). Para obter informações sobre sinalizadores com suporte, consulte a tabela de sinalizadores de recurso de plug-in que segue esta tabela. Exemplo: 00000037<br/> |
| *CLSID*        | Um GUID que é o identificador de classe (CLSID) para a classe que implementa **IWMPSubscriptionService** no plug-in da loja online. Esse GUID deve estar no formato de registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *FriendlyName* | Um nome amigável para a loja online. Exemplo: "serviço de música da Proseware"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Um nome para o plug-in da loja online. Exemplo: "plug-in de serviço de Proseware"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | O nome da classe que implementa **IWMPSubscriptionService** no plug-in da loja online. Exemplo: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | O caminho totalmente qualificado para a DLL que implementa o plug-in da loja online. Exemplo: "C: \\ arquivos de programa \\ Proseware \\ProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

A tabela a seguir descreve os sinalizadores de capacidade de plug-in.



| Sinalizador                                    | Valor | Descrição                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_ALLOWPLAY do limite da assinatura \_            | 0X1   | O Windows Media Player deve chamar [IWMPSubscriptionService:: allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay).                                                                                                                      |
| \_ALLOWCDBURN do limite da assinatura \_          | 0X2   | O Windows Media Player deve chamar [IWMPSubscriptionService:: allowCDBurn](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| \_ALLOWPDATRANSFER do limite da assinatura \_     | 0X4   | O Windows Media Player deve chamar [IWMPSubscriptionService:: allowPDATransfer](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer).                                                                                                        |
| \_BACKGROUNDPROCESSING do limite da assinatura \_ | 0X8   | O Windows Media Player deve chamar [IWMPSubscriptionService:: startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| \_DEVICEAVAILABLE do limite da assinatura \_      | 0X10  | O Windows Media Player deve chamar [IWMPSubscriptionService2::D eviceavailable](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable).                                                                                                        |
| \_PREPAREFORSYNC do limite da assinatura \_       | 0X20  | O Windows Media Player deve chamar [IWMPSubscriptionService2::P repareforsync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| Limites de assinatura \_ v1 \_                  | 0XF   | Padrão. Esse valor será usado se nenhum for registrado. Isso é equivalente a combinar \_ \_ ALLOWPLAY de extremidade de assinatura \_ , \_ ALLOWCDBURN de limite de assinatura, limite de assinatura \_ \_ ALLOWPDATRANSFER e limite de assinatura \_ \_ BACKGROUNDPROCESSING. |



 

**Entradas de registro para desenvolvimento e teste**

Quando você começa a desenvolver sua loja online, a Microsoft fornece duas chaves: uma chave de teste e uma chave de produção. Durante a fase de desenvolvimento e teste, sua loja online será exibida no Windows Media Player somente se sua chave de teste ou sua chave de produção estiver no registro no computador do usuário. Para obter mais informações sobre as chaves de teste e de produção, consulte [chaves de teste e de produção para uma loja online tipo 2](test-and-production-keys-for-a-type-2-online-store.md).

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

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





