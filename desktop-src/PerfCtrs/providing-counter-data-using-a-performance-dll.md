---
description: Um serviço, driver ou aplicativo que deseja fornecer dados de contador pode escrever uma DLL de desempenho para fornecer os dados.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fornecendo dados de contador usando uma DLL de desempenho
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 165e6a8797c50a22acff1d3cd3ded7f8b06a0ee2a7153300e98e46bea1127f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910306"
---
# <a name="providing-counter-data-using-a-performance-dll"></a>Fornecendo dados de contador usando uma DLL de desempenho

> [!IMPORTANT]
> Devido a limitações significativas de desempenho e confiabilidade, o método para fornecer dados do contador de desempenho que este tópico descreve pode ser alterado ou não disponível no futuro. Em vez disso, a Microsoft recomenda que você use o método descrito em Fornecendo dados de contador usando a versão [2.0](providing-counter-data-using-version-2-0.md) para criar novos contadores de desempenho e que você migre contadores de desempenho existentes para usar esse método também.

Um serviço, driver ou aplicativo que deseja fornecer dados de contador pode escrever uma DLL de desempenho para fornecer os dados. Quando um consumidor consulta dados de desempenho, o sistema carrega a DLL do provedor no processo do consumidor e chama o provedor para coletar os dados. Para obter detalhes sobre como escrever a DLL de desempenho, consulte [Criando uma DLL de extensão de desempenho.](creating-a-performance-extension-dll.md)

O sistema usa o Registro para determinar qual provedor chamar. Para obter informações sobre como registrar seu provedor e os contadores que ele dá suporte, consulte [Adicionando contadores de desempenho](adding-performance-counters.md).

> [!Note]
> Não há suporte para DLLs de desempenho Windows OneCore. Se estiver escrevendo um componente que deve ser executado no Windows OneCore, use o método descrito em Fornecendo dados de contador usando a [versão 2.0](providing-counter-data-using-version-2-0.md).
