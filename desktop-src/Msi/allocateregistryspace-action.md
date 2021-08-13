---
description: A ação AllocateRegistrySpace garante que a quantidade de espaço livre no Registro especificada pela propriedade AVAILABLEFREEREG exista no registro.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Ação AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e47a0a0ebc3edec4605cbfac45443e4d30ee25df82ad3eaeb9da9ec9d3a94b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639573"
---
# <a name="allocateregistryspace-action"></a>Ação AllocateRegistrySpace

A ação AllocateRegistrySpace garante que a quantidade de espaço livre no Registro especificada pela propriedade [**AVAILABLEFREEREG**](availablefreereg.md) exista no registro.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação AllocateRegistrySpace deve ser chamada após [InstallInitialize](installinitialize-action.md). É aconselhável agendar o AllocateRegistrySpace antes de todas as outras ações para garantir que haja espaço de registro suficiente disponível para continuar.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação     |
|-------|--------------------------------|
| \[1\] | Espaço de registro necessário em KB. |



 

 

 



