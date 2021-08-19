---
title: Verificações de kernel de drivers não-WHQL assinados
description: para dispositivos que limpam a instalação Windows 10 e onde a inicialização segura está ativada (observe que isso é o padrão para todos os novos dispositivos desde o lançamento do Windows 8 0), todos os novos drivers devem ser assinados pelo WHQL/Sysdev em vez de apenas usar certificados cruzados.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2810d0549086d36f146ca80c0b9c83a7258bb3b120202432cdab6203a081cdd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852412"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Verificações de kernel de drivers não-WHQL assinados

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

para dispositivos que limpam a instalação Windows 10 e onde a inicialização segura está ativada (observe que isso é o padrão para todos os novos dispositivos desde o lançamento do Windows 8 0), todos os novos drivers devem ser assinados pelo WHQL/Sysdev em vez de apenas usar certificados cruzados. Dispositivos que são atualizados e casos em que os drivers foram assinados com um certificado cruzado antes que essa política entrasse em vigor são excluídos desta política para garantir a compatibilidade com versões anteriores. essa política foi anunciada em abril de 2015, no entanto, ela será imposta com a edição de aniversário Windows, lançada em 2016 de agosto.

Nos casos em que um driver não está assinado corretamente, ele será manifestado como uma notificação do PCA de que os drivers são bloqueados quando não forem aprovados nos requisitos de assinatura. Isso impede que uma experiência de usuário desconectada posteriormente do driver seja bloqueada no kernel de forma transparente.

Para obter mais informações, consulte [esta postagem de blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia a alteração de assinatura de driver.

 

 




