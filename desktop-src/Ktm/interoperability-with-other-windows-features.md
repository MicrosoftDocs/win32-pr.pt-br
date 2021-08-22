---
description: O Coordenador de Transações Distribuídas (DTC) permite transações distribuídas ou transações que estão sob o controle de vários gerenciadores de recursos em um ou mais sistemas. KTM e DTC trabalham em conjunto para fazer isso.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilidade com outros Windows recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18595140676539c6e5acaa5fc62835ac279215d068834e3e56dffe50d01e0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119265066"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilidade com outros Windows recursos

O [Coordenador de Transações Distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) permite transações *distribuídas* ou transações que estão sob o controle de vários gerenciadores de recursos em um ou mais sistemas. KTM e DTC trabalham em conjunto para fazer isso.

O COM+ expõe um modelo declarativo para programação transacional. Em outras palavras, o programador declara a extensão até a qual um objeto pode aproveitar as transações e o runtime COM+ gerencia as transações em nome do objeto. Por exemplo, um objeto pode ser declarado para participar de uma transação somente se já existir, para exigir uma transação (uma é criada se ela ainda não existe), para exigir uma nova transação (uma é criada independentemente de uma já existir) ou não é transacional. Essas transações gerenciadas declarativamente são usadas automaticamente em conexões de banco de dados criadas por objetos COM+ que estão sendo executados no contexto de uma transação.

 

 
