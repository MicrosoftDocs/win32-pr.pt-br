---
description: Um serviço, driver ou aplicativo que deseja fornecer dados de contador pode gravar uma DLL de desempenho para fornecer os dados.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fornecendo dados de contador usando uma DLL de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105783249"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Fornecendo dados de contador usando uma DLL de desempenho

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou indisponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e migrar contadores de desempenho existentes para usar esse método também.

Um serviço, driver ou aplicativo que deseja fornecer dados de contador pode gravar uma DLL de desempenho para fornecer os dados. Quando um consumidor consulta dados de desempenho, o sistema carrega a DLL do provedor no processo do consumidor e chama o provedor para coletar os dados. Para obter detalhes sobre como escrever a DLL de desempenho, consulte [criando uma DLL de extensão de desempenho](creating-a-performance-extension-dll.md).

O sistema usa o registro para determinar qual provedor deve ser chamado. Para obter informações sobre como registrar seu provedor e os contadores aos quais ele dá suporte, consulte [adicionando contadores de desempenho](adding-performance-counters.md).

> [!Note]
> Não há suporte para DLLs de desempenho no Windows OneCore. Se estiver escrevendo um componente que deve ser executado no Windows OneCore, use o método descrito em [fornecendo dados de contador usando a versão 2,0](providing-counter-data-using-version-2-0.md).
