---
description: Os objetos protegíveis usam um formato de máscara de acesso no qual os quatro bits de ordem superior especificam direitos de acesso genéricos.
ms.assetid: e18cede9-9bf7-4866-850b-5d7fa43a5b0f
title: Direitos de acesso genéricos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff14aa259222bc37096b8a94f30cffb5ab0876
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662738"
---
# <a name="generic-access-rights"></a>Direitos de acesso genéricos

Os objetos protegíveis usam um [formato de máscara de acesso](access-mask-format.md) no qual os quatro bits de ordem superior especificam direitos de acesso genéricos. Cada tipo de objeto protegível mapeia esses bits para um conjunto de seus direitos de acesso padrão e específicos de objeto. Por exemplo, um objeto de arquivo do Windows mapeia o \_ bit de leitura genérico para o controle de leitura \_ e sincroniza os direitos de acesso padrão e os \_ direitos de \_ acesso específicos ao objeto ler dados, ler arquivo e \_ \_ \_ atributos de leitura de arquivo \_ . Outros tipos de objetos mapeiam o \_ bit de leitura genérico para qualquer conjunto de direitos de acesso apropriado para esse tipo de objeto.

Você pode usar direitos de acesso genéricos para especificar o tipo de acesso que precisa ao abrir um identificador para um objeto. Normalmente, isso é mais simples do que especificar todos os direitos padrão e específicos correspondentes.

A tabela a seguir mostra as constantes definidas para os direitos de acesso genéricos.



| Constante         | Significado genérico            |
|------------------|----------------------------|
| \_tudo genérico     | Todos os direitos de acesso possíveis |
| \_execução genérica | Acesso de execução             |
| \_leitura genérica    | Acesso de leitura                |
| \_gravação genérica   | Acesso de gravação               |



 

Os aplicativos que definem objetos protegíveis privados também podem usar os direitos de acesso genéricos.

 

 



