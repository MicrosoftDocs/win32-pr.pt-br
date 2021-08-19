---
description: Uma ACL de objetos pode conter ACEs herdadas de seu contêiner pai.
ms.assetid: a9e5ad4d-61c6-43ed-a162-460683bcdb16
title: Herança de ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bd239801ea15dddb142c42d86e1aa44d0d644e5d217c50fc7c9cf9388747e45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785377"
---
# <a name="ace-inheritance"></a>Herança de ACE

A ACL de um objeto pode conter ACEs herdadas de seu contêiner pai. Por exemplo, uma subchave do registro pode herdar ACEs da chave acima dela na hierarquia do registro. Da mesma forma, um arquivo em um sistema de arquivos NTFS pode herdar ACEs do diretório que a contém.

A estrutura de [**\_ cabeçalho Ace**](/windows/desktop/api/Winnt/ns-winnt-ace_header) de uma ACE contém um conjunto de sinalizadores de herança que controlam a herança de Ace e o efeito de uma ACE no objeto ao qual ele está anexado. O sistema interpreta os sinalizadores de herança e outras informações de herança de acordo com as [regras de herança de Ace](ace-inheritance-rules.md).

Essas regras foram aprimoradas com os seguintes recursos:

-   Suporte para [propagação automática de ACEs herdáveis](automatic-propagation-of-inheritable-aces.md).
-   Um sinalizador que diferencia as ACEs herdadas e as ACEs que foram aplicadas diretamente a um objeto.
-   ACEs específicas de objeto que permitem especificar o tipo de objeto filho que pode herdar a ACE.
-   a capacidade de impedir que uma dacl ou SACL herde ACEs definindo o ES \_ dacl \_ protegido ou ES \_ bits protegidos por SACL \_ nos bits de controle [*do descritor de segurança*](/windows/desktop/SecGloss/s-gly) , exceto para ace de atributo de recurso do sistema \_ \_ \_ e \_ \_ ace ID de política no escopo do sistema \_ \_ .

 

 
