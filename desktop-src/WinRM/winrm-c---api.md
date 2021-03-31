---
title: API C++ do WinRM
description: As interfaces de Gerenciamento Remoto do Windows podem ser usadas para obter dados ou gerenciar recursos em um computador remoto. Essa API é destinada principalmente para uso interno. É recomendável usar a API do shell do cliente WinRM, em vez disso, sempre que possível.
ms.assetid: e50075a1-cb43-4bd6-9bbf-6b715fde6a3a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa7cff2334d9839936d15f7258a70ce03f9751e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916430"
---
# <a name="winrm-c-api"></a>API C++ do WinRM

As interfaces de Gerenciamento Remoto do Windows podem ser usadas para obter dados ou gerenciar [*recursos*](windows-remote-management-glossary.md) em um computador remoto. Essa API é destinada principalmente para uso interno. É recomendável usar a [API do shell do cliente WinRM](client-shell-api.md) , em vez disso, sempre que possível. As interfaces correspondem exatamente à [API de script do WinRM](winrm-scripting-api.md).

As interfaces do WinRM que herdam diretamente do **IDispatch** têm um objeto de script correspondente. Para obter mais informações, consulte a [API de script do WinRM](winrm-scripting-api.md).

Para aplicativos multissegmentados, o WinRM não dá suporte a threads separados que acessam o mesmo objeto [**IWSMAN**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) .

As interfaces a seguir são fornecidas pelo WinRM.

<dl> <dt>

<span id="IWSMan"></span><span id="iwsman"></span><span id="IWSMAN"></span>[**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornece métodos e propriedades usados para criar uma nova sessão e gerenciar uma sessão estabelecida. [**WSMan**](wsman.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManEx"></span><span id="iwsmanex"></span><span id="IWSMANEX"></span>[**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman)
</dt> <dd>

Fornece métodos e propriedades usados para criar um novo [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator). Esse método está disponível para o objeto de script do [**WSMan**](wsman.md) .

</dd> <dt>

<span id="IWSManConnectionOptions"></span><span id="iwsmanconnectionoptions"></span><span id="IWSMANCONNECTIONOPTIONS"></span>[**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions)
</dt> <dd>

Define o nome de usuário e a senha usados para conexões remotas. [**ConnectionOptions**](connectionoptions.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManSession"></span><span id="iwsmansession"></span><span id="IWSMANSESSION"></span>[**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession)
</dt> <dd>

Define as operações de rede e as propriedades disponíveis para a sessão. [**Session**](session.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManEnumerator"></span><span id="iwsmanenumerator"></span><span id="IWSMANENUMERATOR"></span>[**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator)
</dt> <dd>

Representa uma coleção de resultados retornados da enumeração de um recurso. O [**enumerador**](enumerator.md) é o objeto de script correspondente.

</dd> <dt>

<span id="IWSManResourceLocator"></span><span id="iwsmanresourcelocator"></span><span id="IWSMANRESOURCELOCATOR"></span>[**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator)
</dt> <dd>

Fornece o caminho para um recurso. Você pode usar um objeto [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator) em vez de um [*URI de recurso*](windows-remote-management-glossary.md) em operações de objeto de [**sessão**](session.md) . [**ResourceLocator**](resourcelocator.md) é o objeto de script correspondente.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de Gerenciamento Remoto do Windows](windows-remote-management-reference.md)
</dt> </dl>

 

 




