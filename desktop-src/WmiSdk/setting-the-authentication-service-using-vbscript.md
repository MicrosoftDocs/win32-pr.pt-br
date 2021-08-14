---
description: ao acessar um servidor de Instrumentação de Gerenciamento do Windows (WMI) com um script, você pode escolher entre os protocolos de autenticação do NT LAN Manager (NTLM) ou Kerberos.
ms.assetid: db2dc750-bfdd-4f6c-859b-e104814f0800
ms.tgt_platform: multiple
title: Configurando o serviço de autenticação usando o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 837a69df251b5bbb6cc8bef5ac0b882349fde74646ac6ed33149978b8f69ad7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315383"
---
# <a name="setting-the-authentication-service-using-vbscript"></a>Configurando o serviço de autenticação usando o VBScript

ao acessar um servidor de Instrumentação de Gerenciamento do Windows (WMI) com um script, você pode escolher entre os protocolos de autenticação do NT LAN Manager (NTLM) ou Kerberos. Não é necessário especificar o Kerberos, exceto ao usar a delegação. Para obter mais informações, consulte [conectando-se a um terceiro computador-delegação](connecting-to-a-3rd-computer-delegation.md).

Como as versões do sistema operacional diferem em qual serviço de autenticação eles usam, é recomendável que você não especifique um valor para o campo autoridade ao se conectar a um sistema remoto. Em vez disso, permita que o sistema operacional e a versão distribuída do Component Object Model (DCOM) selecionem NTLM ou Kerberos. Se um serviço de autenticação for especificado, a sintaxe exigirá o nome principal do servidor, que é o nome do computador de destino em vez do controlador de domínio.

Você pode usar o parâmetro Authority somente com conexões com servidores WMI remotos. A tentativa de conexão falhará se você tentar definir níveis de autorização como parte de um moniker ou com uma chamada para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) para uma conexão local.

Execute o procedimento a seguir para especificar o serviço de autenticação que você deseja usar no parâmetro *strAuthority* do método [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md) ou a conexão de cadeia de caracteres do [moniker](constructing-a-moniker-string.md) .

**Para especificar a autenticação NTLM ou Kerberos com a API de script para WMI**

1.  Se o parâmetro *strAuthority* começar com a cadeia de caracteres "Kerberos:", o WMI assumirá que a cadeia de caracteres se refere a um nome de entidade Kerberos e a autenticação Kerberos será usada. Se o parâmetro *strAuthority* começar com a cadeia de caracteres "NTLMDOMAIN:", o WMI usará a autenticação NTLM em vez disso.
2.  Como alternativa, você pode usar a parte da autoridade de um moniker para especificar o tipo de autenticação usado para se conectar ao WMI. Para usar a autenticação Kerberos ao usar um moniker, inclua a cadeia de caracteres "Authority = Kerberos:" seguida pelo nome principal. Para usar a autenticação NTLM, inclua a cadeia de caracteres "Authority = NTLMDOMAIN:" seguida pelo nome de domínio NTLM.

    O exemplo a seguir mostra um moniker que solicita a autenticação Kerberos usando o "servidor mydomain \\ " principal.

    ```VB
    winmgmts:{impersonationLevel=delegate, _
            authority=kerberos:mydomain\server} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

    Por outro lado, o exemplo a seguir mostra um moniker que solicita a autenticação NTLM usando o domínio "mydomain".

    ```VB
    winmgmts:{impersonationLevel=impersonate, _
            authority=ntlmdomain:mydomain} _
            !//myserver/root/default:__cimomidentification=@
    ```

    

 

 



