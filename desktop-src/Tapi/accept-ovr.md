---
description: Em alguns ambientes, um usuário não é automaticamente alertado para uma chamada de oferta, como por toque ou por uma mensagem na tela do computador.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Aceitar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164385"
---
# <a name="accept"></a>Aceitar

Em alguns ambientes, um usuário não é automaticamente alertado para uma chamada de oferta, como por toque ou por uma mensagem na tela do computador. A operação de aceitação inicia o processo de alerta (geralmente tocando) e a operação de [resposta](answer-ovr.md) ocorre posteriormente. O aplicativo pode [descartar](drop-ovr.md) a sessão, [redirecioná](redirect-ovr.md) -la ou aceitá-la.

Se o provedor de serviços atual oferecer suporte a ele, o aplicativo terá a opção de enviar informações de usuário do usuário no momento da aceitação. Não há nenhuma garantia de que a rede fornecerá essas informações à parte de chamada.

Nem todos os provedores de serviço dão suporte ao uso desta operação.

**TAPI 2. x:** Consulte [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).

 

 
