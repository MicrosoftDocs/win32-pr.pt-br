---
description: Módulos de saída personalizados devem implementar a interface ICertExit, que é chamada pelo mecanismo do servidor.
ms.assetid: 509e7945-b656-4c4c-b5eb-45fbe80377c7
title: Gravando módulos de saída personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81798996059e878ef11dbcdf290298094d0849cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105766814"
---
# <a name="writing-custom-exit-modules"></a>Gravando módulos de saída personalizados

Módulos de saída personalizados devem implementar a interface [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) , que é chamada pelo mecanismo do servidor. O método [**ICertExit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) é chamado pelo mecanismo de servidor quando o módulo de saída é carregado. Ele permite que o módulo de saída execute a inicialização e retorne um valor que informará ao mecanismo do servidor os tipos de eventos para os quais ele deseja notificação. O método [**ICertExit:: GetDescription**](/windows/desktop/api/Certexit/nf-certexit-icertexit-getdescription) deve retornar uma cadeia de caracteres de descrição quando o mecanismo do servidor a solicitar. O método [**ICertExit:: Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify) é chamado pelo mecanismo de servidor para notificar o módulo de saída de que um evento ocorreu.

Os módulos de saída podem chamar a interface [**ICertServerExit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) , que dá suporte a muitos dos mesmos métodos da interface [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) , com exceção dos métodos [**SetCertificateExtension**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateextension) e [**setcertificaproperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty) .

Para obter informações sobre como remover o módulo de saída existente e instalar um novo, consulte o tópico sobre a personalização do módulo de saída na ajuda.

 

 



