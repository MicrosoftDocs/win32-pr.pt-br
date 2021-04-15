---
description: Os códigos de erro a seguir são específicos para a API de instalação.
ms.assetid: C4EB130F-2A83-4A14-BBA8-DB10225D0C0A
title: Códigos de erro (API de instalação)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ce77fd224abb16c519f4b77fa93f775fe203d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461263"
---
# <a name="error-codes-setup-api"></a>Códigos de erro (API de instalação)

Os códigos de erro a seguir são específicos para a API de instalação.



| Erros de análise de INF              | Descrição                                                                                                         |
|---------------------------------|---------------------------------------------------------------------------------------------------------------------|
| ERRO \_ esperado \_ nome da seção \_  | Um nome de seção era esperado e não foi encontrado.                                                                          |
| ERRO \_ de \_ \_ linha de nome de seção inadequada \_ | O nome da seção não estava no formato correto. (Por exemplo, um nome não terminado por um colchete direito ( \] ). |
| nome da seção de erro \_ \_ \_ muito \_ longo | O nome da seção excedeu o comprimento máximo de Len de nome de separador máximo \_ \_ \_ .                                               |
| ERRO \_ de \_ sintaxe geral          | A sintaxe geral está incorreta.                                                                                    |



 



| Erros de tempo de execução INF         | Descrição                                                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ERRO \_ de \_ estilo inf incorreto \_   | O arquivo INF não é do tipo especificado na chamada de função. Por exemplo, esse erro pode ser retornado pela função [**SetupOpenAppendInfFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupopenappendinffilea) se o arquivo inf foi desenvolvido para uma versão anterior do Windows. |
| seção de erro \_ \_ não \_ encontrada | A seção não foi encontrada no arquivo INF.                                                                                                                                                                                                     |
| linha de erro \_ \_ não \_ encontrada    | A linha não foi encontrada na seção INF.                                                                                                                                                                                                     |



 

 

 



