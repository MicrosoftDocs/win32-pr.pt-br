---
description: Recuperação automática de recursos
ms.assetid: c889dd3f-82d1-4bc3-ac2c-6f468d5b2c7f
title: Recuperação automática de recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eec280c0b0ae222cf0c63e136b7643bbd05c1fffa5589ccc4b736dd247a43b1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119730666"
---
# <a name="automatic-resource-reclamation"></a>Recuperação automática de recursos

O COM+ notifica o Gerenciador do dispensador sempre que o tempo de vida de um objeto termina. Em seguida, o Gerenciador do dispensador notifica cada portador da dispensador do recurso registrado para ver se ele tem algum recurso ainda mantido por esse objeto. Nesse caso, esses recursos são liberados, impedindo a possibilidade de vazamentos de recursos por componentes que obtêm recursos por meio de um dispensador de recursos.

O recurso de recuperação automática é uma opção desativada por padrão. Um dispensador de recurso pode optar por habilitar essa opção e, ao fazer isso, garante que uma referência a qualquer recurso dispensado para um objeto nunca seja retornada pelos métodos de objeto.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conceitos do dispensador de recursos COM+](com--resource-dispenser-concepts.md)
</dt> </dl>

 

 



