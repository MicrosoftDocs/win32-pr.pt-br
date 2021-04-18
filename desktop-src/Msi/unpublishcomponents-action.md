---
description: A ação UnpublishComponents gerencia o desanúncio de componentes listados na tabela PublishComponent.
ms.assetid: 3e50f668-6d08-405e-a5a4-f422041ef0b1
title: Ação UnpublishComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f58d9fff862295bcc06e61e1b35c05cdddb58daa
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "104370910"
---
# <a name="unpublishcomponents-action"></a>Ação UnpublishComponents

A ação UnpublishComponents gerencia o desanúncio de componentes listados na tabela PublishComponent. Esses são componentes que podem ter falhado em outros produtos. Essa ação remove informações sobre os componentes publicados da [tabela PublishComponent](publishcomponent-table.md) para a qual o recurso correspondente está selecionado no momento para ser desinstalado.

## <a name="sequence-restrictions"></a>Restrições de sequência

Não há restrições de sequência.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação                                   |
|-------|--------------------------------------------------------------|
| \[1\] | GUID que representa a ID do componente de um recurso anunciado. |
| \[2\] | Qualificador da ID do componente.                               |



 

