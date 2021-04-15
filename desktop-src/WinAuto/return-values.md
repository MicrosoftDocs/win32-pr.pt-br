---
title: Valores de retorno (recursos de acessibilidade do Windows)
description: Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que podem ser exibidos com menos frequência.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae2ccaf8bc74b1802be7569bc9e783cde4e11f9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454498"
---
# <a name="return-values-windows-accessibility-features"></a>Valores de retorno (recursos de acessibilidade do Windows)

Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que podem ser exibidos com menos frequência.

## <a name="common-return-values"></a>Valores de retorno comuns

Os métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) retornam um dos seguintes valores, definidos em Winerror. h ou outro código de erro de Component Object Model padrão (com):



|                         |                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | O método foi bem-sucedido.                                                                                                                                                                                                                                                                                                                                                                     |
| \_falso                | O método foi bem-sucedido na parte. Isso acontece quando o método é executado com sucesso, mas as informações solicitadas não estão disponíveis. Por exemplo, Microsoft Acessibilidade Ativa retornará S \_ false se você chamar [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar um objeto filho em um determinado ponto e o ponto especificado não estiver dentro do objeto ou do filho do objeto. |
| DISP \_ E \_ MEMBERNOTFOUND | O objeto não oferece suporte à propriedade ou ação solicitada. Por exemplo, um botão de ação retorna esse valor se você solicitar sua [propriedade Value](value-property.md), porque ela não tem uma propriedade Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | O método não está implementado. Esse valor ocorre quando um cliente chama um método que ainda não tem suporte nesse sistema operacional.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Um ou mais argumentos não eram válidos. Esse erro ocorre quando o chamador tenta identificar um objeto filho usando um identificador que o servidor não reconhece. Esse erro também ocorre quando um cliente tenta identificar um objeto filho dentro de um objeto que não tem filhos.                                                                                                      |
| E \_ OUTOFMEMORY          | O método não pôde alocar memória necessária para concluir uma operação crucial para seu sucesso.                                                                                                                                                                                                                                                                                        |
| E \_ falha                 | Ocorreu um erro desconhecido ou genérico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valores de retorno adicionais

Os seguintes são valores de retorno que os métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) podem retornar. Esses valores de retorno não são tão comuns quanto os anteriores, mas você deve estar ciente deles.



|                        |                                                                                      |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSDENIED        | Isso é retornado quando você chama get \_ accValue para obter o valor de um controle de senha. |
| obter \_ E \_ exceção     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




