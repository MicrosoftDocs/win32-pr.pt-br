---
title: Alças de retomada de enumeração
description: Identificadores de retomada de enumeração são identificadores para a chave de retomada real contida nos dados da instância da função. Isso é necessário para segurança, interoperabilidade e para simplificar o código do chamador para a função.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10976661723af59af945b9dec1080196e682b308fa1a597edfc4cee6047aa783
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912186"
---
# <a name="enumeration-resume-handles"></a>Alças de retomada de enumeração

Identificadores de retomada de enumeração são identificadores para a chave de retomada real contida nos dados da instância da função. Isso é necessário para segurança, interoperabilidade e para simplificar o código do chamador para a função.

Se um **NULL** for passado para o ponteiro para o alça de retomada, nenhum alça será armazenado e a pesquisa de enumeração não poderá ser continuada. Isso é útil em casos em que o aplicativo não deseja enumerar todos os itens.

Se um erro for retornado de uma chamada de enumeração, o alça de retomada deverá ser tratado como inválido e não usado para chamadas de enumeração subsequentes. Quando isso ocorre, você deve reiniciar a enumeração desde o início.

 

 




