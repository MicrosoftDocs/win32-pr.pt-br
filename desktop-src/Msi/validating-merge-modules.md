---
description: Os autores devem executar a validação em todos os módulos de mesclagem novos ou modificados recentemente antes de tentar mesclar o módulo em um banco de dados de instalação pela primeira vez.
ms.assetid: 8d6794af-403a-416e-8ace-1af3f193414b
title: Validando módulos de mesclagem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5a226f72e35ce4ee76599444e86ef80bd71a8866ca80eef2a5da04a87fb79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995795"
---
# <a name="validating-merge-modules"></a>Validando módulos de mesclagem

Os autores devem executar a validação em todos os módulos de mesclagem novos ou modificados recentemente antes de tentar mesclar o módulo em um banco de dados de instalação pela primeira vez. A validação do módulo de mesclagem funciona da mesma maneira que a [validação do pacote](package-validation.md) , mas usa um conjunto diferente de [avaliadores de consistência internos](internal-consistency-evaluators-ices.md) (ICES) específicos para módulos de mesclagem. Para obter mais informações sobre este módulo de mesclagem ICEs, consulte [referência de Ice do módulo de mesclagem](merge-module-ice-reference.md).

O módulo de mesclagem ICEs é armazenado no arquivo. Cub do módulo de mesclagem, Mergemod. cub. A instalação da ferramenta Orca ou msival2 também fornece os arquivos logo. Cub, Darice. Cub e Mergemod. cub.

Para obter mais informações, consulte [referência de Ice do módulo de mesclagem](merge-module-ice-reference.md).

 

 



