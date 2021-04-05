---
description: Você pode escrever módulos de política na linguagem de programação C, C++ ou Visual Basic.
ms.assetid: 37a93c67-02f2-4c4e-a000-2bb98e0ca948
title: Gravando módulos personalizados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92247cd6b975bac520032dcc3aada1328f7b6c2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921846"
---
# <a name="writing-custom-modules"></a>Gravando módulos personalizados

Você pode escrever módulos de política na linguagem de programação C, C++ ou Visual Basic. O compilador da Microsoft necessário está disponível no Visual C++ versão 5,0 ou posterior ou no Visual Basic versão 5,0 ou posterior. Uma AC ( [*autoridade de certificação*](../secgloss/c-gly.md) ) corporativa deve usar apenas o módulo de política corporativa fornecido pela Microsoft.

Você deve implementar o [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) ao gravar um módulo de política personalizada. Além disso, você deve implementar o [**ICertManageModule**](/windows/desktop/api/Certmod/nn-certmod-icertmanagemodule) ao gravar um módulo de política personalizada.

Os módulos de política podem chamar métodos de [**ICertServerPolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) para auxiliar no processamento de uma [*solicitação de certificado*](../secgloss/c-gly.md); **ICertServerPolicy** permite que as propriedades e extensões de certificado sejam definidas e recuperadas.

Para obter mais informações, consulte os tópicos a seguir.



| Tópico                                                                      | Descrição                             |
|----------------------------------------------------------------------------|-----------------------------------------|
| [Definindo propriedades de certificado](setting-certificate-properties.md)       | Definindo as propriedades de um certificado |
| [Gravando módulos de saída personalizados](writing-custom-exit-modules.md)             | Gravando módulos de saída personalizados             |
| [Gravando manipuladores de extensão personalizados](writing-custom-extension-handlers.md) | Gravando manipuladores de extensão personalizados       |



 

 

 
