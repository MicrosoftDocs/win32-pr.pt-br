---
title: Mensagens de erro estendidas ADSI
description: Este tópico contém uma lista de tópicos que explicam como trabalhar com mensagens de erro ADSI retornadas por IADs, IADsContainer, IDirectoryObject e IDirectorySearch.
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- Mensagens de erro estendidas ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004885"
---
# <a name="adsi-extended-error-messages"></a>Mensagens de erro estendidas ADSI

Além dos valores **HRESULT** , vários provedores de sistema ADSI (principalmente LDAP) retornam dados de erro adicionais para operações executadas pelas seguintes interfaces:

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

Uma parte desses dados de erro estendidos é a cadeia de caracteres enviada pelo servidor como parte do resultado da mensagem.

Chame [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) para recuperar essas mensagens de erro estendidas. O primeiro parâmetro dessa função, *lpError*, é um valor **DWORD** . Para um servidor Active Directory, a ADSI tenta mapear uma mensagem de erro LDAP para um código de erro Win32 apropriado e atribui o valor de código de erro do Win32 a *lpError*. Falha ao resolver o mapeamento, a ADSI atribui **dados de \_ erro \_ inválidos** ao *lpError*, como faz para qualquer outro servidor de diretório. Em todos os casos, a ADSI retransmite com fidelidade a cadeia de caracteres da descrição do erro do servidor para o cliente por meio de *lpErrorBuf*, o segundo parâmetro da função **ADsGetLastError** .

 

 




