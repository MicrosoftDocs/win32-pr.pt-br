---
title: Valores de retorno de função
description: Os valores de retorno de função são semelhantes aos parâmetros \out\ -only porque seus dados não são fornecidos pelo aplicativo cliente.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525c63422b058da5267003711efa612814907eb91ced353bd78ee78a820a7377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020996"
---
# <a name="function-return-values"></a>Valores de retorno de função

Os valores de retorno de função **\[ são semelhantes aos \]** parâmetros out-only porque seus dados não são fornecidos pelo aplicativo cliente. No entanto, eles são gerenciados de maneira diferente. Ao **\[ contrário dos \]** parâmetros out-only, eles não precisam ser ponteiros. O procedimento remoto pode retornar qualquer tipo de dados válido, exceto ponteiros de referência e uniões não truncadas.

No entanto, é **\[ recomendável usar um \] parâmetro out** em vez de um valor de retorno para tipos de dados complexos. Ao retornar tipos de dados complexos, o compilador MIDL gerará um stub de modo /Os. Como resultado, todas as informações recentes de verificação de erros fornecidas por /robust são perdidas.

Os valores de retorno de função que são tipos de ponteiro são alocados pelo stub do cliente com uma chamada para [o \_ usuário médio \_ alocar](/windows/desktop/Midl/midl-user-allocate-1). Da mesma forma, somente o atributo de ponteiro exclusivo ou completo pode ser aplicado a um tipo de retorno de função de ponteiro.

 

 