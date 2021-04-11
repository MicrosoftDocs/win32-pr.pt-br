---
description: Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco.
ms.assetid: 7dbe1133-f5cb-4925-9448-5d40f1c553ff
title: Arquivos esparsos e cotas de disco
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 326780e2b2c5119256272c0d297613d2c32e6e6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090675"
---
# <a name="sparse-files-and-disk-quotas"></a>Arquivos esparsos e cotas de disco

Um arquivo esparso afeta as cotas de usuário pelo tamanho nominal do arquivo, não pela quantidade real alocada de espaço em disco. Ou seja, a criação de um arquivo de 50 MB com todos os zero bytes consome 50 MB da cota desse usuário. Isso significa que, à medida que o usuário grava dados no arquivo esparso, ele não precisa se preocupar em exceder seu limite de cota rígido, pois já foi cobrado pelo espaço. Os administradores do sistema não devem contar com o tamanho de um arquivo esparso que permanece pequeno. Portanto, eles não devem conceder aos seus usuários limites de cota rígido que excedem o espaço físico disponível, apesar do uso de arquivos esparsos.

 

 



