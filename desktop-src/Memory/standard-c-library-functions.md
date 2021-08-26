---
description: Os aplicativos podem usar com segurança os recursos de gerenciamento de memória da biblioteca de tempo de execução do C (malloc, Free e assim por diante) e do C++ (novo, excluir e assim por diante).
ms.assetid: c58ed263-577d-47c5-93cb-5a7c83604171
title: Funções da biblioteca C padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1447a64f00fbd1b4cccf70f7589f267ebba526d66528d7342da68068f81ebfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963206"
---
# <a name="standard-c-library-functions"></a>Funções da biblioteca C padrão

Os aplicativos podem usar com segurança os recursos de gerenciamento de memória da biblioteca de tempo de execução do C (**malloc**, **Free** e assim por diante) e do C++ (**novo**, **excluir** e assim por diante). As funções de biblioteca de tempo de execução do C não têm os possíveis problemas que têm em Windows de 16 bits. O gerenciamento de memória não é mais um problema porque o sistema está livre para gerenciar a memória movendo as páginas da memória física sem afetar os endereços virtuais. Da mesma forma, a distinção entre ponteiros próximos e distantes não é mais relevante. Portanto, você pode usar as funções da biblioteca C padrão para gerenciamento de memória. No entanto, as funções de gerenciamento de memória fornecem funcionalidade que não está disponível na biblioteca de tempo de execução do C.

 

 



