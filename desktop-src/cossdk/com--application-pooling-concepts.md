---
description: O pool de aplicativos COM+ permite que processos de thread único sejam dimensionados, de forma semelhante ao modo como o pool de threads permite que os objetos single-thread sejam dimensionados.
ms.assetid: 28bd13d9-ff5c-456e-ab98-d2ff3a499f1c
title: Conceitos do pool de aplicativos COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aab46350e3c6084c0d5e8ca61d2f3c90d27e06795f7d08568ee4a7c1e0fc26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096906"
---
# <a name="com-application-pooling-concepts"></a>Conceitos do pool de aplicativos COM+

O pool de aplicativos COM+ permite que processos de thread único sejam dimensionados, de forma semelhante ao modo como o pool de threads permite que os objetos single-thread sejam dimensionados. O pool de aplicativos também pode ajudar a recuperar-se de falhas em processos únicos, fornecendo outros processos em execução capazes de lidar com as ativações.

> [!Note]  
> Os aplicativos de biblioteca têm as propriedades de reciclagem e pooling de seu processo de host.

 

Todos os métodos da interface [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) dão suporte ao pooling de aplicativos.

O pool de aplicativos COM+ é configurável por aplicativo usando a propriedade ConcurrentApps do objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) na coleção de [**aplicativos**](applications.md) . ConcurrentApps é um valor inteiro que especifica o número máximo de processos Dllhost simultâneos que devem ser iniciados para o serviço de ativações de um aplicativo. Essa propriedade pode ser definida usando a ferramenta de administração de serviços de componentes ou programaticamente.

Se a propriedade ConcurrentApps for definida como 1, que é o valor padrão, o serviço de pooling de aplicativos COM+ será desabilitado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tarefas do pool de aplicativos COM+](com--application-pooling-tasks.md)
</dt> <dt>

[Conceitos de reciclagem de aplicativo COM+](com--application-recycling-concepts.md)
</dt> </dl>

 

 



