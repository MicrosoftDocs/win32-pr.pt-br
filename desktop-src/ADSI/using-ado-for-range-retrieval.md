---
title: Usando o ADO para recuperação de intervalo
description: Se uma linguagem de automação for usada, o ActiveX ADO (Directory Objects) deverá ser usado para recuperar um intervalo de valores de propriedade. Ao usar o ADO para recuperação de intervalo, há um problema que deve ser resolvido especificamente.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Usando a ADO para ADSI de Recuperação de Intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 523cd65e7d26a82b9b647913c919bef374b1c76ddf1a18fd9f99384b4ae6e483
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023044"
---
# <a name="using-ado-for-range-retrieval"></a>Usando o ADO para recuperação de intervalo

Se uma linguagem de automação for usada, o ActiveX ADO (Directory Objects) deverá ser usado para recuperar um intervalo de valores de propriedade.

Ao usar o ADO para recuperação de intervalo, há um problema que deve ser resolvido especificamente. Ao consultar o grupo final de valores de propriedade, o objeto ADO recuperará zero objetos, mesmo que mais permaneçam. Para recuperar os valores restantes, use o curinga de intervalo \* ' '. Por exemplo, se um grupo contiver 150 membros, os valores de membro de 0 a 100 poderão ser recuperados normalmente usando a recuperação de intervalo. Se o intervalo 101-200 for solicitado, o objeto ADO retornará zero objetos. Neste ponto, é necessário modificar a consulta para solicitar o intervalo 101- \* . Isso recuperará valores de 101 a 150. Para obter mais informações e um exemplo de código, consulte Código de exemplo para usar [variando para recuperar membros de um grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Para obter mais informações sobre como usar o ADO para recuperação de intervalo, consulte:

-   [Dialeto de LDAP de ADO](ado-ldap-ranging-dialect.md)
-   [Dialeto de SQL ADO](ado-sql-ranging-dialect.md)
-   [Código de exemplo para usar variando para recuperar membros de um grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




