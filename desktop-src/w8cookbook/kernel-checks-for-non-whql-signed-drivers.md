---
title: Verificações de kernel de drivers não-WHQL assinados
description: Para dispositivos que limpam a instalação do Windows 10 e onde a inicialização segura está ativada (Observe que esse é o padrão para todos os novos dispositivos desde o lançamento do Windows 8,0), todos os novos drivers devem ser assinados pelo WHQL/Sysdev, em vez de usar certificados cruzados com assinatura cruzada.
ms.assetid: D2A13F91-BA44-4044-B1F4-54393A9F1063
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582db864627a2945debca33c8e75ac74fb20acc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364283"
---
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Verificações de kernel de drivers não-WHQL assinados

\[Algumas informações estão relacionadas ao produto de pré-lançamento que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não faz nenhuma garantia, expressa ou implícita, com relação às informações fornecidas aqui.\]

Para dispositivos que limpam a instalação do Windows 10 e onde a inicialização segura está ativada (Observe que esse é o padrão para todos os novos dispositivos desde o lançamento do Windows 8,0), todos os novos drivers devem ser assinados pelo WHQL/Sysdev, em vez de usar certificados cruzados com assinatura cruzada. Dispositivos que são atualizados e casos em que os drivers foram assinados com um certificado cruzado antes que essa política entrasse em vigor são excluídos desta política para garantir a compatibilidade com versões anteriores. Essa política foi anunciada em abril de 2015, no entanto, ela será imposta com a edição de aniversário do Windows, lançada em agosto de 2016.

Nos casos em que um driver não está assinado corretamente, ele será manifestado como uma notificação do PCA de que os drivers são bloqueados quando não forem aprovados nos requisitos de assinatura. Isso impede que uma experiência de usuário desconectada posteriormente do driver seja bloqueada no kernel de forma transparente.

Para obter mais informações, consulte [esta postagem de blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia a alteração de assinatura de driver.

 

 




