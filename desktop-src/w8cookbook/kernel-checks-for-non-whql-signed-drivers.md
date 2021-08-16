---
title: Verificações de kernel para drivers assinados não WHQL
description: Para dispositivos que limpam a instalação do Windows 10 e em que a Inicialização Segura está em (observe que isso é padrão para todos os novos dispositivos desde o lançamento do Windows 8.0), todos os novos drivers devem ser assinados por WHQL/Sysdev em vez de apenas usar certificados assinados cruzados.
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
# <a name="kernel-checks-for-non-whql-signed-drivers"></a>Verificações de kernel para drivers assinados não WHQL

\[Algumas informações estão relacionadas ao produto pré-lançado, que pode ser substancialmente modificado antes de ser lançado comercialmente. A Microsoft não oferece garantias, expressas ou implícitas, das informações aqui fornecidas.\]

Para dispositivos que limpam a instalação do Windows 10 e em que a Inicialização Segura está em (observe que isso é padrão para todos os novos dispositivos desde o lançamento do Windows 8.0), todos os novos drivers devem ser assinados por WHQL/Sysdev em vez de apenas usar certificados assinados cruzados. Os dispositivos que são atualizados e os casos em que os drivers foram assinados com um certificado cruzado antes de essa política entrar em vigor são excluídos dessa política para garantir a compatibilidade com vertida. Essa política foi anunciada em abril de 2015, no entanto, ela será imposta com a Windows Anniversary Edition, lançada em agosto de 2016.

Nos casos em que um driver não estiver assinado corretamente, ele se manifesta como uma notificação do PCA de que os driver(s) são bloqueados quando ele não passa os requisitos de assinatura. Isso impede que uma experiência do usuário desconectada posteriormente do driver seja bloqueada no kernel de forma transparente.

Para obter mais informações, consulte [esta postagem no blog](https://techcommunity.microsoft.com/t5/Windows-Hardware-Certification/bg-p/WindowsHardwareCertification/), que anuncia a alteração na assinatura do driver.

 

 




