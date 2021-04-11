---
description: Os módulos de saída recebem notificações do mecanismo do servidor quando ocorrem operações como a emissão de um certificado.
ms.assetid: 5e7ee1f4-7e07-4a08-8e72-89b449804bc2
title: Módulos de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fc0668717c4a7a690cce8a03ff8c140333347b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170639"
---
# <a name="exit-modules"></a>Módulos de saída

Os módulos de saída recebem notificações do mecanismo do servidor quando ocorrem operações como a emissão de um certificado. Um módulo de saída é implementado como uma dll ( [*biblioteca de vínculo dinâmico*](../secgloss/d-gly.md) ). Uma operação típica para um módulo de saída é publicar um certificado concluído em um local especificado (o módulo de saída da autoridade de certificação corporativa padrão, por exemplo, publica certificados de usuário e [*listas de certificados revogados*](../secgloss/c-gly.md) (CRLs) no Active Directory). Um módulo de saída pode usar a interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) para se comunicar com os serviços de certificados. Os serviços de certificados se comunicam com um módulo de saída por meio de chamadas COM diretas ou, se o módulo não oferecer suporte a chamadas COM diretas, por meio de automação.

Um módulo de saída pode exibir as propriedades e extensões de certificado existentes e também pode exibir atributos e propriedades de solicitação. No entanto, um módulo de saída não pode modificar nenhuma propriedade.

Os serviços de certificados fornecem um módulo de saída padrão, mas você também pode criar módulos de saída personalizados para atender às necessidades especiais. No entanto, antes de gravar um módulo de saída personalizado, considere usar o módulo de saída padrão. Além disso, para uma autoridade de certificação corporativa, o módulo de saída padrão sempre deve ser usado, embora você possa adicionar outros módulos de saída personalizados. Para obter mais informações, consulte [escrevendo módulos de saída personalizados](writing-custom-exit-modules.md).

 

 
