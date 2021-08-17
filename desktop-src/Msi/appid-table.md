---
description: A tabela AppId ou a tabela de registro especifica que o instalador configura e registra servidores DCOM para executar uma das ações a seguir durante uma instalação.
ms.assetid: d76ed6df-944b-4996-bf07-e42ceb7a1b69
title: Tabela AppId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8452635cd7c167d6a8618629eaec2f6f6c1aa2e72e0b3628a7d4542a9e7160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066266"
---
# <a name="appid-table"></a>Tabela AppId

A tabela AppId ou a [tabela de registro](registry-table.md) especifica que o instalador configura e registra servidores DCOM para executar uma das ações a seguir durante uma instalação.

-   Execute o servidor DCOM com uma identidade diferente do usuário que está ativando o servidor. Por exemplo, para configurar um servidor DCOM para sempre executar como um usuário interativo ou como um usuário predefinido.
-   Execute o servidor DCOM como um serviço.
-   Configure o acesso de segurança padrão para o servidor DCOM.
-   Registre o servidor DCOM de modo que ele seja ativado em um computador diferente.

Essa tabela é processada na instalação do componente associado ao servidor DCOM na \_ coluna componente da [tabela classe](class-table.md). Uma AppId não é anunciada.

A tabela AppId tem as colunas a seguir.



| Coluna               | Tipo                       | Chave | Nullable |
|----------------------|----------------------------|-----|----------|
| AppId                | [GUID](guid.md)           | Y   | N        |
| RemoteServerName     | [Binário](formatted.md) | N   | Y        |
| LocalService         | [Text](text.md)           | N   | Y        |
| Serviceparameters    | [Text](text.md)           | N   | Y        |
| DllSurrogate         | [Text](text.md)           | N   | Y        |
| ActivateAtStorage    | [Inteiro](integer.md)     | N   | Y        |
| RunAsInteractiveUser | [Inteiro](integer.md)     | N   | Y        |



 

## <a name="columns"></a>Colunas

<dl> <dt>

<span id="AppId"></span><span id="appid"></span><span id="APPID"></span>AppId
</dt> <dd>

A coluna AppId da [tabela de classes](class-table.md) é uma chave estrangeira nessa coluna da tabela AppID. Esta coluna contém o valor AppId que será gravado sob o CLSID e criará a chave de GUID AppId em HKCR \\ AppID.

</dd> <dt>

<span id="RemoteServerName"></span><span id="remoteservername"></span><span id="REMOTESERVERNAME"></span>RemoteServerName
</dt> <dd>

Esta coluna contém o valor de "RemoteServerName" = <xxxx> que será gravado em HKCR \\ AppID \\ {AppID} \\ .

</dd> <dt>

<span id="LocalService"></span><span id="localservice"></span><span id="LOCALSERVICE"></span>LocalService
</dt> <dd>

Esta coluna contém o valor de LocalService que será gravado em HKCR \\ AppID \\ { <appid> } "LocalService" = <xxx> .

</dd> <dt>

<span id="ServiceParameters"></span><span id="serviceparameters"></span><span id="SERVICEPARAMETERS"></span>Serviceparameters
</dt> <dd>

Esta coluna contém o valor de Serviceparameters que será gravado em HKCR \\ AppID \\ {AppID>} "serviceparameters".

</dd> <dt>

<span id="DllSurrogate"></span><span id="dllsurrogate"></span><span id="DLLSURROGATE"></span>DllSurrogate
</dt> <dd>

Esta coluna contém o valor de DllSurrogate que será gravado em HKCR \\ AppID \\ { <appid> } "DllSurrogate" = <xxx> . Se essa coluna estiver presente, ela normalmente será uma cadeia de caracteres vazia.

</dd> <dt>

<span id="ActivateAtStorage"></span><span id="activateatstorage"></span><span id="ACTIVATEATSTORAGE"></span>ActivateAtStorage
</dt> <dd>

um valor inteiro diferente de zero nesse campo faz com que Windows Installer grave \\ o HKCR AppID \\ { <appid> } "ActivateAtStorage" = "Y" no registro. Se o campo for deixado vazio ou tiver um valor igual a zero, nenhum valor será gravado.

</dd> <dt>

<span id="RunAsInteractiveUser"></span><span id="runasinteractiveuser"></span><span id="RUNASINTERACTIVEUSER"></span>RunAsInteractiveUser
</dt> <dd>

um valor inteiro diferente de zero nesse campo faz com que Windows Installer grave o HKCR \\ AppID \\ {appid>} "RunAs" = "usuário interativo" no registro. Se o campo for deixado vazio ou tiver um valor igual a zero, nenhum valor será gravado.

</dd> </dl>

## <a name="remarks"></a>Comentários

Essa tabela é usada pela ação [RegisterClassInfo](registerclassinfo-action.md) e [ação UnregisterClassInfo](unregisterclassinfo-action.md).

Observe que a tabela AppId não tem uma coluna para registrar um nome padrão. Portanto, nos casos em que você precisa escrever um nome amigável de usuário como o valor de nome padrão, você deve registrar-se usando a [tabela de registro](registry-table.md).

## <a name="validation"></a>Validação

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE33](ice33.md)  
[ICE46](ice46.md)  
[ICE69](ice69.md)  
</dl>

 

 



