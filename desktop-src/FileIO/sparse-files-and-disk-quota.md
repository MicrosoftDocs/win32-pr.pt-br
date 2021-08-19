---
description: Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Arquivos esparsos e cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e78e9d35e557585f17df6c4672a04b2997792f95b0fca63d2e6a2345a7a8b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015074"
---
# <a name="sparse-files-and-disk-quotas"></a>Arquivos esparsos e cotas de disco

Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco. Ou seja, a criação de um arquivo de 50 MB com todos os zero bytes consome 50 MB da cota desse usuário. Isso significa que, à medida que o usuário grava dados no arquivo esparso, ele não precisa se preocupar em exceder seu limite de cota rígido, pois já foi cobrado pelo espaço. Os administradores do sistema não devem contar com o tamanho de um arquivo esparso que permanece pequeno. Portanto, eles não devem conceder aos seus usuários limites de cota rígido que excedem o espaço físico disponível, apesar do uso de arquivos esparsos.

 

 



