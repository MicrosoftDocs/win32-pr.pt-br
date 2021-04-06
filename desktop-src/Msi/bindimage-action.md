---
description: A ação de BindImage associa cada executável ou DLL que deve ser associado às DLLs importadas por ele.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Ação de BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa2ac4c5ca16b83a3f0f0796d9a755542ec108c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828049"
---
# <a name="bindimage-action"></a>Ação de BindImage

A ação de BindImage associa cada executável ou DLL que deve ser associado às DLLs importadas por ele. A ação de BindImage atua em cada arquivo na tabela [BindImage](bindimage-table.md) , mas somente os que devem ser instalados localmente. O instalador computa o endereço virtual de cada função importada de todas as DLLs e salva o endereço virtual calculado na tabela de endereços de [*importação*](i-gly.md) da imagem de importação (IAT).

A ação de BindImage chama internamente a API do Windows **BindImageEx** .

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação de BindImage deve vir após a ação [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação     |
|-------|--------------------------------|
| \[1\] | Identificador de arquivo do executável. |



 

 

 



