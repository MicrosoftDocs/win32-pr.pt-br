---
description: A ação de BindImage associa cada executável ou DLL que deve ser associado às DLLs importadas por ele.
ms.assetid: bf90acc0-4e90-4180-9df7-268b63a66538
title: Ação de BindImage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d621728de551c182d6678561b2ef5daf649fb8fae840f47a460d83a4d38f3635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638772"
---
# <a name="bindimage-action"></a>Ação de BindImage

A ação de BindImage associa cada executável ou DLL que deve ser associado às DLLs importadas por ele. A ação de BindImage atua em cada arquivo na tabela [BindImage](bindimage-table.md) , mas somente os que devem ser instalados localmente. O instalador computa o endereço virtual de cada função importada de todas as DLLs e salva o endereço virtual calculado na tabela de endereços de [*importação*](i-gly.md) da imagem de importação (IAT).

a ação de BindImage chama internamente a API de Windows **BindImageEx** .

## <a name="sequence-restrictions"></a>Restrições de sequência

A ação de BindImage deve vir após a ação [InstallFiles](installfiles-action.md) .

## <a name="actiondata-messages"></a>Mensagens ActionData



| Campo | Descrição dos dados da ação     |
|-------|--------------------------------|
| \[1\] | Identificador de arquivo do executável. |



 

 

 



