---
description: Uma DACL nula concede acesso completo a qualquer usuário que a solicita. Uma DACL vazia é uma DACL alocada e inicializada corretamente que não contém entradas de controle de acesso. Uma DACL vazia não concede acesso ao objeto ao seu atribuído.
ms.assetid: 26e5c98d-bbdc-4f9f-96e0-18d1c429f1e6
title: DACLs nulos e DACLs vazias (autorização)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c15f9a3aeed120ff91dc19a091232721c623683d90f0c9cdccbc065516eea8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907816"
---
# <a name="null-dacls-and-empty-dacls-authorization"></a>DACLs nulos e DACLs vazias (autorização)

Se [*a*](/windows/desktop/SecGloss/d-gly) DACL (lista de controle de acesso discricionário) que pertence ao [*descritor de*](/windows/desktop/SecGloss/s-gly) segurança de um objeto estiver definida como **NULL,** uma DACL nula será criada. Uma DACL nula concede acesso completo a qualquer usuário que a solicita; A verificação de segurança normal não é executada em relação ao objeto . Uma DACL nula não deve ser confundida com uma DACL vazia. Uma DACL vazia é uma DACL alocada e inicializada corretamente que não contém ACEs [*(entradas de*](/windows/desktop/SecGloss/a-gly) controle de acesso). Uma DACL vazia não concede acesso ao objeto ao seu atribuído.

Para ver um exemplo de como criar uma DACL, consulte [Criando uma DACL.](/windows/desktop/SecBP/creating-a-dacl)

 

 
