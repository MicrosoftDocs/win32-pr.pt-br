---
title: Chaves e entradas do Registro para um tipo 2 Online Store
description: Chaves e entradas do Registro para um tipo 2 Online Store
ms.assetid: 17dff940-3884-488a-9016-29bb47c51caf
keywords:
- Windows Media Player online, registro
- lojas online, registro
- tipo 2 lojas online, registro
- registry, digite 2 lojas online
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01a5494f56a4c3fa7ea91d9537f6177453a1df54f684aa73c347029574f8dde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746447"
---
# <a name="registry-keys-and-entries-for-a-type-2-online-store"></a>Chaves e entradas do Registro para um tipo 2 Online Store

> [!Note]  
> Esta seção descreve a funcionalidade projetada para uso por lojas online. Não há suporte para o uso dessa funcionalidade fora do contexto de uma loja online.

 

Para disponibilizar uma loja online do tipo 2 no Windows Media Player, o provedor de lojas online deve criar as seguintes sub-chaves e entradas do Registro no computador do usuário.


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



Na sintaxe do Registro anterior, os símbolos em itálico são espaço reservados para nomes e GUIDs (identificadores globalmente exclusivos) específicos do armazenamento online. A tabela a seguir descreve esses espaço reservados.



| Espaço reservado    | Descrição                                                                                                                                                                                                                                                                                                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *keyName*      | Uma cadeia de caracteres aceita entre a Microsoft e a loja online. Essa cadeia de caracteres identifica exclusivamente o armazenamento online. Exemplo: "Proseware"<br/>                                                                                                                                                                                                                                                          |
| *sinalizadores*        | UM OR  bit a bit de um ou mais sinalizadores de funcionalidade de plug-in Esses sinalizadores especificam se Windows Media Player deve chamar métodos específicos de [IWMPSubscriptionService](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice) e [IWMPSubscriptionService2](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2). Para obter informações sobre sinalizadores com suporte, consulte a tabela de sinalizadores de funcionalidade de plug-in que segue esta tabela. Exemplo: 00000037<br/> |
| *Clsid*        | Um GUID que é o CLSID (identificador de classe) da classe que implementa **IWMPSubscriptionService** no plug-in da loja online. Esse GUID deve estar no formato do Registro, completo com as chaves. Formato: {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx}<br/>                                                                                                                                    |
| *Friendlyname* | Um nome amigável para a loja online. Exemplo: "Proseware Music Service"<br/>                                                                                                                                                                                                                                                                                                                     |
| *pluginName*   | Um nome para o plug-in da loja online. Exemplo: "Proseware Service Plug-in"<br/>                                                                                                                                                                                                                                                                                                                  |
| *className*    | O nome da classe que implementa **IWMPSubscriptionService** no plug-in da loja online. Exemplo: "CProsewareService"<br/>                                                                                                                                                                                                                                                                |
| *moduleName*   | O caminho totalmente qualificado para a DLL que implementa o plug-in da loja online. Exemplo: "C: \\ Proseware de Arquivos \\ \\ de ProgramasProsewareService.dll"<br/>                                                                                                                                                                                                                                                |



 

A tabela a seguir descreve os sinalizadores de funcionalidade de plug-in.



| Sinalizador                                    | Valor | Descrição                                                                                                                                                                                                                        |
|-----------------------------------------|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| SUBSCRIPTION \_ CAP \_ ALLOWPLAY            | 0X1   | Windows Media Player deve chamar [IWMPSubscriptionService::allowPlay.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay)                                                                                                                      |
| SUBSCRIPTION \_ CAP \_ ALLOWCD LTD          | 0X2   | Windows Media Player deve chamar [IWMPSubscriptionService::allowCDScript](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowcdburn).                                                                                                                  |
| LIMITE \_ DE \_ ASSINATURA ALLOWPDATRANSFER     | 0X4   | Windows Media Player deve chamar [IWMPSubscriptionService::allowPDATransfer.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowpdatransfer)                                                                                                        |
| PLANO \_ DE FUNDO DO LIMITE DA \_ ASSINATURAPROCESSAMENTO | 0X8   | Windows Media Player deve chamar [IWMPSubscriptionService::startBackgroundProcessing](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-startbackgroundprocessing).                                                                                      |
| DISPOSITIVO \_ DE LIMITE DE \_ ASSINATURAAVAILABLE      | 0X10  | Windows Media Player deve chamar [IWMPSubscriptionService2::d eviceAvailable.](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-deviceavailable)                                                                                                        |
| \_ \_ PREPAREFORSYNC DE LIMITE DE ASSINATURA       | 0X20  | Windows Media Player deve chamar [IWMPSubscriptionService2::p repareForSync](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync).                                                                                                          |
| ASSINATURA \_ V1 \_ CAPS                  | 0xf   | Padrão. Esse valor será usado se nenhum estiver registrado. Isso é equivalente a combinar SUBSCRIPTION \_ CAP \_ ALLOWPLAY, \_ SUBSCRIPTION CAP \_ ALLOWCD LTD, \_ SUBSCRIPTION CAP \_ ALLOWPDATRANSFER e SUBSCRIPTION \_ CAP \_ BACKGROUNDPROCESSING. |



 

**Entradas do Registro para desenvolvimento e teste**

Quando você começa a desenvolver sua loja online, a Microsoft fornece duas chaves: uma chave de teste e uma chave de produção. Durante a fase de desenvolvimento e teste, sua loja online será exibida Windows Media Player somente se a chave de teste ou a chave de produção estiver no Registro no computador do usuário. Para obter mais informações sobre as chaves de teste e produção, consulte [Test and Production Keys for a Type 2 Online Store](test-and-production-keys-for-a-type-2-online-store.md).

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

Quando o usuário ativa um armazenamento online, Windows Media Player grava informações no Registro que identificam o armazenamento online ativo. Windows Media Player coloca as informações no local a seguir no Registro no computador do usuário.


```C++
[HKEY_CURRENT_USER\Software\Microsoft\MediaPlayer\Subscriptions]
"ActiveService"=serviceInfo
```



Na sintaxe do Registro anterior, *serviceInfo* é um espaço reservado para uma cadeia de caracteres que contém informações descritivas sobre o armazenamento online ativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência para lojas online do tipo 2**](reference-for-type-2-online-stores.md)
</dt> </dl>

 

 





