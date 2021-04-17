---
title: Valores de retorno de função
description: Os valores de retorno de função são semelhantes aos parâmetros somente-out-only porque seus dados não são fornecidos pelo aplicativo cliente.
ms.assetid: 98d8d228-7222-49bf-9f29-7749a7a76d5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ada3808d024f201ef01a5f4977149a0ab9c75e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105787028"
---
# <a name="function-return-values"></a>Valores de retorno de função

Os valores de retorno de função são semelhantes aos parâmetros somente de **\[ saída \]** porque seus dados não são fornecidos pelo aplicativo cliente. No entanto, eles são gerenciados de forma diferente. Ao contrário dos parâmetros somente **\[ out \]**, eles não precisam ser ponteiros. O procedimento remoto pode retornar qualquer tipo de dados válido, exceto ponteiros de referência e uniões não encapsuladas.

No entanto, é recomendável usar um parâmetro **\[ out \]** em vez de um valor de retorno para tipos de dados complexos. Ao retornar tipos de dados complexos, o compilador MIDL gerará um stub de modo/os. Como resultado, todas as informações recentes de verificação de erros fornecidas pelo/robust são perdidas.

Os valores de retorno de função que são tipos de ponteiro são alocados pelo stub do cliente com uma chamada para [ \_ \_ alocar usuário de MIDL](/windows/desktop/Midl/midl-user-allocate-1). Da mesma forma, somente o atributo de ponteiro exclusivo ou completo pode ser aplicado a um tipo de retorno de função de ponteiro.

 

 