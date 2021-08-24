---
description: A ação ProcessComponents registra e cancela o registro de componentes, seus caminhos de chave e os clientes de componente.
ms.assetid: 8ad418c0-9bba-41d0-a96c-2c7b1c2467d9
title: Ação ProcessComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1e866c6003052922dfc0e1fca5bd4ff8ea63d207eeb03c5ada22cf5f2d3e7b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259276"
---
# <a name="processcomponents-action"></a>Ação ProcessComponents

A ação ProcessComponents registra e cancela o registro de componentes, seus caminhos de chave e os clientes de componente. A ação ProcessComponents consulta a coluna KeyPath da [tabela de componentes](component-table.md) para determinar os caminhos. Esse registro é usado pelo [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) para retornar o caminho de um componente para um cliente de produto.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação ProcessComponents deve vir após a ação [InstallInitialize](installinitialize-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData

Para cada componente que está sendo registrado.



| Campo | Descrição dos dados da ação      |
|-------|---------------------------------|
| \[1\] | ProductId                       |
| \[2\] | ComponentId                     |
| \[3\] | O caminho da chave para o componente. |



 

Para cada componente que está sendo cancelado.



| Campo | Descrição dos dados da ação |
|-------|----------------------------|
| \[1\] | ProductId                  |
| \[2\] | ComponentId                |



 

 

 



