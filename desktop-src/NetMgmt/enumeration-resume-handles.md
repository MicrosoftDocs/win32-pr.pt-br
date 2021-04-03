---
title: Identificadores de retomada de enumeração
description: Identificadores de retomada de enumeração são identificadores para a chave de retomada real contida nos dados da instância para a função. Isso é necessário para segurança, interoperabilidade e para simplificar o código do chamador para a função.
ms.assetid: 6734e99b-7f8c-43c9-96e3-44c9783960dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f20e7a7d5e1f9afb15e6adad4c0d7643bf841d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916301"
---
# <a name="enumeration-resume-handles"></a>Identificadores de retomada de enumeração

Identificadores de retomada de enumeração são identificadores para a chave de retomada real contida nos dados da instância para a função. Isso é necessário para segurança, interoperabilidade e para simplificar o código do chamador para a função.

Se um **NULL** for passado para o ponteiro para o identificador de retomada, nenhum identificador será armazenado e a pesquisa de enumeração não poderá continuar. Isso é útil em casos em que o aplicativo não deseja enumerar todos os itens.

Se um erro for retornado de uma chamada de enumeração, o identificador de retomada deverá ser tratado como inválido e não será usado para nenhuma chamada de enumeração subsequente. Quando isso ocorrer, você deve reiniciar a enumeração desde o início.

 

 




