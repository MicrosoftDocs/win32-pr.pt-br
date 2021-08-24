---
description: A ação UnpublishComponents gerencia o não reverso dos componentes listados na tabela PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Ação UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1feaca4449ffa344eeda828334f879ebc12905406446dd14623e3b9c4474c6b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810256"
---
# <a name="unpublishcomponents-action"></a>Ação UnpublishComponents

A ação UnpublishComponents gerencia o não reverso dos componentes listados na tabela PublishComponent. Esses são componentes que podem ter falhas em outros produtos. Essa ação remove informações sobre componentes publicados da tabela [PublishComponent](publishcomponent-table.md) para a qual o recurso correspondente está selecionado para ser desinstalado no momento.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados de ação                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID que representa a ID do componente de um recurso anunciado. |
| \[2\] | Qualificador da ID do componente.                               |



 

