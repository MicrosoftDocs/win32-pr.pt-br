---
title: Usando ADO para recuperação de intervalo
description: Se for usado um idioma de automação, os ADO (objetos de diretório do ActiveX) deverão ser usados para recuperar um intervalo de valores de propriedade. Ao usar o ADO para recuperação de intervalo, há um problema que deve ser resolvido especificamente.
ms.assetid: ca06169d-7de7-4552-aa7d-e9427353e49e
ms.tgt_platform: multiple
keywords:
- Usando ADO para o ADSI de recuperação de intervalo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cb8950a71708bd9c824c90842f043808c897554
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634857"
---
# <a name="using-ado-for-range-retrieval"></a>Usando ADO para recuperação de intervalo

Se for usado um idioma de automação, os ADO (objetos de diretório do ActiveX) deverão ser usados para recuperar um intervalo de valores de propriedade.

Ao usar o ADO para recuperação de intervalo, há um problema que deve ser resolvido especificamente. Ao consultar o grupo final de valores de propriedade, o objeto ADO recuperará zero objetos, embora mais permaneça. Para recuperar os valores restantes, use o curinga de intervalo ' \* '. Por exemplo, se um grupo contiver 150 Membros, os valores de membro 0-100 poderão ser recuperados normalmente usando a recuperação em intervalos. Se o intervalo 101-200 for solicitado, o objeto ADO retornará zero objetos. Neste ponto, é necessário modificar a consulta para o intervalo de solicitação 101- \* . Isso recuperará os valores de 101 para 150. Para obter mais informações e um exemplo de código, consulte [código de exemplo para usar a variação para recuperar membros de um grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md).

Para obter mais informações sobre como usar o ADO para recuperação de intervalo, consulte:

-   [Dialeto de intervalo de LDAP do ADO](ado-ldap-ranging-dialect.md)
-   [Dialeto de intervalo de SQL do ADO](ado-sql-ranging-dialect.md)
-   [Exemplo de código para usar o intervalo para recuperar membros de um grupo](example-code-for-using-ranging-to-retrieve-members-of-a-group.md)

 

 




