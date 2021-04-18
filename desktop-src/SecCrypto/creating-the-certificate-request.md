---
description: O processo de criação de uma solicitação de certificado envolve a coleta de determinadas informações do solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Criando a solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be29a1fbdbaf9fd956150808471086b7d8ca2815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755310"
---
# <a name="creating-the-certificate-request"></a>Criando a solicitação de certificado

O processo de criação de uma solicitação de certificado envolve a coleta de determinadas informações do solicitante. Normalmente, isso é feito por meio de algum tipo de interface do usuário (IU), embora as informações possam ser obtidas diretamente de um banco de dados sem a necessidade de uma interface de usuário. O nível de informações necessárias é definido pela política da autoridade de [*certificação*](../secgloss/c-gly.md) (CA).

Um exemplo das informações necessárias pode ser o seguinte:

-   Nome comum
-   Nome da unidade
-   Nome da empresa
-   City
-   Estado
-   País/Região

> [!Note]  
> A interface é projetada para fazer uma única solicitação para cada instância de Xenroll. Uma instância de XEnroll separada deve ser criada para criar cada [*solicitação de certificado*](../secgloss/c-gly.md).

 

Para obter informações sobre como usar o controle de registro de certificado para solicitar um certificado em linguagens de programação específicas, consulte os seguintes tópicos:

-   [Exemplo de solicitação em C++](request-sample-in-c-.md)
-   [Exemplo de solicitação no VBScript](request-sample-in-vbscript.md)

 

 
