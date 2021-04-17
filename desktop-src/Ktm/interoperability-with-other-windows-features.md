---
description: O Coordenador de Transações Distribuídas (DTC) permite transações distribuídas ou transações que estão sob o controle de vários gerenciadores de recursos em um ou mais sistemas. O KTM e o DTC trabalham juntos para fazer isso.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: Interoperabilidade com outros recursos do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa3aeac3d920b408a9a18c32eab83cf747525e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780131"
---
# <a name="interoperability-with-other-windows-features"></a>Interoperabilidade com outros recursos do Windows

O [Coordenador de transações distribuídas](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) permite *transações distribuídas* ou transações que estão sob o controle de vários gerenciadores de recursos em um ou mais sistemas. O KTM e o DTC trabalham juntos para fazer isso.

O COM+ expõe um modelo declarativo para programação transacional. Em outras palavras, o programador declara a extensão até a qual um objeto pode tirar proveito das transações, e o tempo de execução do COM+ gerencia as transações em nome do objeto. Por exemplo, um objeto pode ser declarado para participar de uma transação somente se já existir uma, para exigir uma transação (uma é criada se ela ainda não existir), para exigir uma nova transação (uma é criada independentemente de se já existir) ou não é transacional. Essas transações gerenciadas declarativamente são usadas automaticamente em conexões de banco de dados criadas por objetos COM+ que estão sendo executados no contexto de uma transação.

 

 
