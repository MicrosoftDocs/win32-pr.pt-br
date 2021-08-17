---
title: API de script do WinRM
description: Windows Os objetos de script de gerenciamento remoto são implementados como uma camada acima do protocolo WS-Management.
ms.assetid: bd642669-554f-40ab-bd40-235013afa077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c7ce6311fe80884ab0c71e66360a2072381221b5b85a8626fda0e0104168b4f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742754"
---
# <a name="winrm-scripting-api"></a>API de script do WinRM

Windows Os objetos de script de gerenciamento remoto são implementados como uma camada acima da [protocolo WS-Management](ws-management-protocol.md). Os objetos de script permitem que você obtenha dados ou gerencie [*recursos*](windows-remote-management-glossary.md) em computadores locais e remotos.

## <a name="ws-management-objects"></a>Objetos WS-Management

Cada objeto de script tem uma interface C++ correspondente. para obter mais informações, consulte [API C++ do WinRM](winrm-c---api.md) e [scripts em Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md).

Os objetos a seguir são fornecidos pela API de script do WinRM.

<dl> <dt>

<span id="ConnectionOptions"></span><span id="connectionoptions"></span><span id="CONNECTIONOPTIONS"></span>[**ConnectionOptions**](connectionoptions.md)
</dt> <dd>

Define o nome de usuário e a senha usados para conexões remotas. O nome de usuário e a senha são passados ao chamar o método [**Createconnectoptions**](wsman-createconnectionoptions.md) . Para obter mais informações, consulte [obtendo dados de um computador remoto](obtaining-data-from-a-remote-computer.md). A interface C++ correspondente é [**IWSManConnectionOptions**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanconnectionoptions).

</dd> <dt>

<span id="Enumerator"></span><span id="enumerator"></span><span id="ENUMERATOR"></span>[**Enumera**](enumerator.md)
</dt> <dd>

Representa uma coleção de resultados retornados da enumeração de um recurso. Para obter mais informações, consulte [enumerando ou listando todas as instâncias de um recurso](enumerating-or-listing-all-instances-of-a-resource.md). A interface C++ correspondente é [**IWSManEnumerator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanenumerator).

</dd> <dt>

<span id="ResourceLocator"></span><span id="resourcelocator"></span><span id="RESOURCELOCATOR"></span>[**ResourceLocator**](resourcelocator.md)
</dt> <dd>

Fornece o caminho para um recurso. Você pode usar um objeto [**ResourceLocator**](resourcelocator.md) em vez de um [*URI de recurso*](windows-remote-management-glossary.md) em operações de objeto de [**sessão**](session.md) , como [**Session. Get**](session-get.md), [**Session. put**](session-put.md)ou [**Session. Enumerate**](session-enumerate.md). A interface C++ correspondente é [**IWSManResourceLocator**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanresourcelocator).

</dd> <dt>

<span id="Session"></span><span id="session"></span><span id="SESSION"></span>[**Sessão**](session.md)
</dt> <dd>

Define as operações de rede e as propriedades disponíveis para a sessão, como [**Session. Get**](session-get.md), [**Session. Enumerate**](session-enumerate.md), [**Session. Invoke**](session-invoke.md). Para obter mais informações, consulte [obtendo dados do computador local](obtaining-data-from-the-local-computer.md). A interface C++ correspondente é [**IWSManSession**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmansession).

</dd> <dt>

<span id="WSMan"></span><span id="wsman"></span><span id="WSMAN"></span>[**WSMan**](wsman.md)
</dt> <dd>

Fornece métodos e propriedades usados para criar uma nova sessão ou gerenciar uma sessão estabelecida. para obter mais informações, consulte [usando Gerenciamento Remoto do Windows](using-windows-remote-management.md). As interfaces C++ correspondentes são [**IWSMan**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsman) e [**IWSManEx**](/windows/desktop/api/WSManDisp/nn-wsmandisp-iwsmanex).

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> <dt>

[usando Gerenciamento Remoto do Windows](using-windows-remote-management.md)
</dt> <dt>

[criando scripts no Gerenciamento Remoto do Windows](scripting-in-windows-remote-management.md)
</dt> <dt>

[Windows Referência de gerenciamento remoto](windows-remote-management-reference.md)
</dt> </dl>

 

 




