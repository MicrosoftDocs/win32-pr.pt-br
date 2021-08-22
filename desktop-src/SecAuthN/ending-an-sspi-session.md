---
description: Quando o cliente tiver terminado de se comunicar com qualquer servidor ou tiver terminado de usar as credenciais adicionais passadas para a função falha AcquireCredentialsHandle, o cliente deverá chamar a função FreeCredentialsHandle.
ms.assetid: fa943e9b-d379-441f-8c6e-f0a0f5f7f1a3
title: Encerrando uma sessão SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4669d3143b480df20f1a5f1d76e73cc75802766d1db83da9b75d304e256ae4dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008264"
---
# <a name="ending-an-sspi-session"></a>Encerrando uma sessão SSPI

Depois que o cliente e o servidor tiverem terminado a comunicação, ambos os lados chamarão a função [**DeleteSecurityContext**](/windows/desktop/api/Sspi/nf-sspi-deletesecuritycontext) com seus respectivos identificadores de contexto. Quando o cliente tiver terminado de se comunicar com qualquer servidor ou tiver terminado de usar as credenciais adicionais passadas para a função [**falha AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea) , o cliente deverá chamar a função [**FreeCredentialsHandle**](/windows/desktop/api/Sspi/nf-sspi-freecredentialshandle) . Quando o servidor estiver pronto para desligar e antes de descarregar a DLL, o servidor deverá chamar **DeleteSecurityContext**.

 

 
