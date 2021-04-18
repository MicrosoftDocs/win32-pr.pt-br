---
description: A ação AllocateRegistrySpace garante que a quantidade de espaço livre no Registro especificada pela propriedade AVAILABLEFREEREG exista no registro.
ms.assetid: bb6ac685-5ad8-48e6-9c03-9ca42268d727
title: Ação AllocateRegistrySpace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e6f986561595c73bf3bb1188d899af3d3d7d528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764669"
---
# <a name="allocateregistryspace-action"></a>Ação AllocateRegistrySpace

A ação AllocateRegistrySpace garante que a quantidade de espaço livre no Registro especificada pela propriedade [**AVAILABLEFREEREG**](availablefreereg.md) exista no registro.

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação AllocateRegistrySpace deve ser chamada após [InstallInitialize](installinitialize-action.md). É aconselhável agendar o AllocateRegistrySpace antes de todas as outras ações para garantir que haja espaço de registro suficiente disponível para continuar.

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação     |
|-------|--------------------------------|
| \[1\] | Espaço de registro necessário em KB. |



 

 

 



