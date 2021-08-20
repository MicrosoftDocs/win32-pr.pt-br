---
description: As Windows atualizações que exigem interação do usuário não poderão ser instaladas por aplicativos WUA (Update Agent) se os aplicativos WUA estão em execução no contexto do serviço de Logon Secundário.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Usando WUA de um processo de logon secundário (Executar como)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a659b9c46429100393138751039fdc1ce529191970a35c76d36e45bb16eb0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049084"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Usando WUA de um processo de logon secundário (Executar como)

As Windows atualizações que exigem interação do usuário não poderão ser instaladas por aplicativos WUA (Update Agent) se os aplicativos WUA estão em execução no contexto do serviço de Logon Secundário.

Se o processo que está chamando WUA estiver em execução no contexto do serviço RunAs ou do serviço logon secundário, uma tentativa de instalar uma atualização que exige interação do usuário falhará e retornará o erro **WU E NO INTERACTIVE \_ \_ \_ \_ USER.**

No Microsoft Windows, você pode executar programas como um usuário diferente do usuário que está conectado no momento. Para fazer isso, o serviço logon secundário deve estar em execução.

 

 



