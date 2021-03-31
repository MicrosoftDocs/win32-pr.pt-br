---
title: Registrando o servidor DLL para ativação alternativa
description: Registrando o servidor DLL para ativação alternativa
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641891"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a>Registrando o servidor DLL para ativação alternativa

Um servidor DLL será carregado em um processo substituto sob as seguintes condições:

-   Deve haver um valor AppID especificado na chave CLSID no registro e uma chave [AppID](appid-key.md) correspondente.
-   Em uma chamada de ativação, o bit do [**\_ \_ servidor local CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) é definido e a chave CLSID não especifica [LocalServer32](localserver32.md), [LocalServer](localserver.md)ou [LocalService](localservice.md). Se outros bits **CLSCTX** estiverem definidos, o [**algoritmo de processamento**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)para os sinalizadores de execução em processo, local ou remoto será seguido.
-   A chave CLSID contém a subchave [InprocServer32](inprocserver32.md) .
-   A DLL de proxy/stub especificada na chave **InprocServer32** existe.
-   O valor de [DllSurrogate](dllsurrogate.md) existe na chave **AppID** .

Se houver um **LocalServer**, **LocalServer32** ou **LocalService**, indicando a existência de um exe, o servidor exe ou o serviço sempre será iniciado em preferência ao carregamento de um servidor dll em um processo substituto.

O valor nomeado **DllSurrogate** deve ser especificado para que a ativação substituta ocorra. A ativação refere-se a chamadas para qualquer uma das seguintes funções de ativação:

-   [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [**CoCreateInstanceEx**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [**CoGetInstanceFromFile**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [**CoGetInstanceFromIStorage**](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [**IMoniker::BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

Para iniciar uma instância do substituto fornecido pelo sistema, defina o valor de **DllSurrogate** como uma cadeia de caracteres vazia ou como **NULL**. Para especificar o início de um substituto personalizado, defina o valor para o caminho do substituto.

Se [RemoteServerName](remoteservername.md) e **DllSurrogate** forem especificados para a mesma AppID, o valor de **RemoteServerName** será ignorado e o valor **DllSurrogate** causará uma ativação no computador local. Para ativação alternativa remota, especifique **RemoteServerName** , mas não **DllSurrogate** no cliente, e especifique **DllSurrogate** no servidor.

Um servidor DLL que é projetado para ser sempre executado sozinho em seu próprio processo substituto é melhor configurado com um AppID igual a seu CLSID. Em **AppID**, basta especificar um valor nomeado **DllSurrogate** com um valor de cadeia de caracteres vazio.

É melhor configurar um servidor DLL que foi projetado para ser executado sozinho em seu próprio processo substituto e para atender a vários clientes em uma rede com um valor [runas](runas.md) especificado na chave do registro **AppID** . Se o **runas** especifica "usuário interativo" ou uma identidade de usuário específica depende da interface do usuário, da segurança e de outros requisitos do servidor. Quando um valor **runas** é especificado, apenas uma instância do servidor é carregada para atender a todos os clientes, independentemente da identidade do cliente. Por outro lado, não configure o servidor com **runas** se a intenção for ter uma instância do servidor dll em execução em substituto para atender a cada identidade de cliente remoto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Requisitos do servidor DLL](dll-server-requirements.md)
</dt> <dt>

[Compartilhamento substituto](surrogate-sharing.md)
</dt> </dl>

 

 