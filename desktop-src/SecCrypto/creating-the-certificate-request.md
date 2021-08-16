---
description: O processo de criação de uma solicitação de certificado envolve a coleta de determinadas informações do solicitante.
ms.assetid: b03efa83-e255-4427-a796-63d5841664a9
title: Criando a solicitação de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 607ebbfd5d230c216c2b7ebc4d3b217e1f8c0d2a375d39cdd6b311ec145be361
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768864"
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

 

 
