---
description: Os certificados são concedidos de acordo com políticas que definem critérios que os solicitantes devem atender para receber um certificado.
ms.assetid: ad79dc0d-6457-4459-80e6-ab340436ecac
title: Independência de política
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a63afc249905dc03602e38458ba326674e033648669e3187d44e58a188b122d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117978962"
---
# <a name="policy-independence"></a>Independência de política

Os certificados são concedidos de acordo com políticas que definem critérios que os solicitantes devem atender para receber um certificado. Por exemplo, uma política pode ser conceder certificados comerciais somente se os candidatos apresentarem sua identificação pessoalmente. Outra política pode conceder credenciais [*com base em*](../secgloss/c-gly.md) solicitações de email. Uma agência que emite cartões de crédito pode optar por consultar um banco de dados e fazer consultas telefônicas antes de emite um cartão.

As políticas são implementadas em módulos de política escritos em C++, C ou Visual Basic. As funções dos Serviços de Certificados são isoladas das alterações na política que uma agência pode implementar. As alterações na política podem ser totalmente implementadas no código do módulo de política do servidor. Uma AC [*(autoridade de certificação)*](../secgloss/c-gly.md) corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.

 

 
