---
description: As atualizações que exigem a interação do usuário não poderão ser instaladas por aplicativos do Windows Update Agent (WUA) se os aplicativos do WUA estiverem em execução no contexto do serviço de logon secundário.
ms.assetid: 090cd730-cfcd-49fc-b748-f66e696edaf3
title: Usando o WUA de um processo de logon secundário (executar como)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f08626532b588f044ca866f78ebab836671f12d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807197"
---
# <a name="using-wua-from-a-secondary-logon-run-as-process"></a>Usando o WUA de um processo de logon secundário (executar como)

As atualizações que exigem a interação do usuário não poderão ser instaladas por aplicativos do Windows Update Agent (WUA) se os aplicativos do WUA estiverem em execução no contexto do serviço de logon secundário.

Se o processo que está chamando o WUA estiver em execução no contexto do serviço RunAs ou do serviço de logon secundário, uma tentativa de instalar uma atualização que exige a interação do usuário falhará e retornará o erro de **\_ \_ \_ \_ usuário interativo e nenhum** .

No Microsoft Windows, você pode executar programas como um usuário que difere do usuário que está conectado no momento. Para fazer isso, o serviço de logon secundário deve estar em execução.

 

 



