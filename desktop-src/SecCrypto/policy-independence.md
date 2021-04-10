---
description: Os certificados são concedidos de acordo com as políticas que definem os critérios que os solicitantes devem atender para receber um certificado.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Independência de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0d99b5babeced0fb87d9e603038e23a40859b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296956"
---
# <a name="policy-independence"></a>Independência de política

Os certificados são concedidos de acordo com as políticas que definem os critérios que os solicitantes devem atender para receber um certificado. Por exemplo, uma política pode ser conceder certificados comerciais somente se os candidatos apresentarem sua identificação pessoalmente. Outra política pode conceder [*credenciais*](../secgloss/c-gly.md) com base em solicitações de email. Uma agência que emite cartões de crédito pode optar por consultar um banco de dados e fazer consultas telefônicas antes de emitir um cartão.

As políticas são implementadas em módulos de política escritos em C++, C ou Visual Basic. As funções de serviços de certificados são isoladas de quaisquer alterações na política que uma agência possa implementar. As alterações na política podem ser totalmente implementadas no código do módulo de política de servidor. Uma AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ) corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.

 

 
