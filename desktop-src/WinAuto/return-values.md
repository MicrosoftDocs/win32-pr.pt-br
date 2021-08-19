---
title: Valores de retorno (Windows recursos de acessibilidade)
description: Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que você pode ver com menos frequência.
ms.assetid: e6deca92-42da-41ab-bfdb-75cbce3022bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71595f7a21d932ee961f9fa5f2a9443cf4d63e38de42f3d5b8c89fa8e9f84e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122056"
---
# <a name="return-values-windows-accessibility-features"></a>Valores de retorno (Windows recursos de acessibilidade)

Este tópico descreve os valores de retorno mais comuns e outros valores de retorno que você pode ver com menos frequência.

## <a name="common-return-values"></a>Valores de retorno comuns

Os [**métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) retornam um dos seguintes valores, definidos em winerror.h ou outro código de erro COM (Component Object Model padrão:



|   Valor                      |   Descrição                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| S \_ OK                   | O método foi bem-sucedido.                                                                                                                                                                                                                                                                                                                                                                     |
| S \_ FALSE                | O método foi bem-sucedido em parte. Isso acontece quando o método é bem-sucedido, mas as informações solicitadas não estão disponíveis. Por exemplo, Microsoft Active Accessibility retornará S FALSE se você chamar \_ [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest) para recuperar um objeto filho em um determinado ponto e o ponto especificado não estiver dentro do objeto ou do filho do objeto. |
| DISP \_ E \_ MEMBERNOTFOUND | O objeto não dá suporte à propriedade ou ação solicitada. Por exemplo, um botão de push retornará esse valor se você solicitar sua [propriedade Value](value-property.md), porque ele não tem uma propriedade Value.                                                                                                                                                                           |
| E \_ NOTIMPL              | O método não é implementado. Esse valor ocorre quando um cliente chama um método que ainda não tem suporte nesse sistema operacional.                                                                                                                                                                                                                                                         |
| E \_ INVALIDARG           | Um ou mais argumentos não eram válidos. Esse erro ocorre quando o chamador tenta identificar um objeto filho usando um identificador que o servidor não reconhece. Esse erro também resulta quando um cliente tenta identificar um objeto filho dentro de um objeto que não tem filhos.                                                                                                      |
| E \_ OUTOFMEMORY          | O método não pôde alocar memória necessária para concluir uma operação crucial para seu sucesso.                                                                                                                                                                                                                                                                                        |
| E \_ FAIL                 | Ocorreu um erro desconhecido ou genérico.                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="additional-return-values"></a>Valores de retorno adicionais

A seguir estão os valores de retorno [**que os métodos IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) podem retornar. Esses valores de retorno não são tão comuns quanto os anteriores, mas você deve estar ciente deles.



|    Valor                    |    Descrição                                                                                  |
|------------------------|--------------------------------------------------------------------------------------|
| E \_ ACCESSDENIED        | Isso é retornado quando você chama get \_ accValue para obter o valor de um controle de senha. |
| EXCEÇÃO \_ DISP E \_     |                                                                                      |
| CO \_ E \_ OBJNOTCONNECTED |                                                                                      |



 

 

 




