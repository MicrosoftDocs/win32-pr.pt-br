---
title: Sincronização de retorno de chamada
description: Sincronização de retorno de chamada
ms.assetid: e8268f18-49e7-4e09-9006-77858b734bf4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c274c35a6df176f65c505f2a3fecc9a53a20e5d9
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105798450"
---
# <a name="callback-synchronization"></a>Sincronização de retorno de chamada

A [API do Wininet](/windows/desktop/WinInet/portal) assíncrona (usada para os protocolos mais comuns) deixa a sincronização do mecanismo de retorno de chamada e o aplicativo de chamada como um exercício para o cliente. Isso é intencional porque permite o maior grau de flexibilidade. Os protocolos padrão e a implementação do moniker da URL executam essa sincronização e garantem que aplicativos de thread único e apartamento não precisem lidar com a contenção no estilo de thread livre. Ou seja, as interfaces [**IEnumFORMATETC**](/windows/desktop/api/ObjIdl/nn-objidl-ienumformatetc) e [**IBindStatusCallback**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775060(v=vs.85)) do cliente são chamadas somente em seus threads apropriados. Esse recurso é transparente para o usuário da URL mMoniker, desde que cada thread que chama [**IMoniker:: BindToStorage**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtostorage) e [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) tenha uma fila de mensagens.

A especificação de moniker assíncrona requer um controle mais preciso sobre a priorização e o gerenciamento de downloads do que o é permitido pelo WinSock ou pelo WinInet. Da mesma forma, um moniker de URL gerencia todos os downloads de qualquer thread do chamador específico, usando (como parte de sua sincronização) um esquema de prioridade baseado na especificação [**IBinding**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775071(v=vs.85)) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Identificadores de URL](url-monikers.md)
</dt> </dl>

 

 