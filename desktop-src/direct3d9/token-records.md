---
description: Esta seção descreve o formato dos registros para cada um dos tokens de registro. As informações são divididas nas seções a seguir.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Registros de token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105772705"
---
# <a name="token-records"></a>Registros de token

Esta seção descreve o formato dos registros para cada um dos tokens de registro. As informações são divididas nas seções a seguir.

-   [nome do TOKEN \_](/windows)
-   [Cadeia de caracteres de TOKEN \_](/windows)
-   [inteiro de TOKEN \_](/windows)
-   [GUID do TOKEN \_](/windows)
-   [\_lista de inteiros de token \_](/windows)
-   [\_lista de floats de token \_](/windows)

## <a name="token_name"></a>nome do TOKEN \_

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de bytes que se seguem no campo nome. Um nome ASCII de contagem de comprimento conclui o registro.



| Campo | Tipo       | Tamanho (bytes) | Sumário                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nome do token \_                    |
| count | DWORD      | 4            | Comprimento do campo de nome, em bytes |
| name  | Matriz de bytes | count        | Nome ASCII                     |



 

## <a name="token_string"></a>Cadeia de caracteres de TOKEN \_

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de bytes que acompanham o campo de cadeia de caracteres. Uma cadeia de caracteres ASCII de contagem de comprimento continua o registro, que é concluído por um token de terminação. A escolha do terminador é determinada pelos problemas de sintaxe discutidos em outro lugar.



| Campo      | Tipo       | Tamanho (bytes) | Sumário                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | Cadeia de caracteres de token \_                    |
| count      | DWORD      | 4            | Comprimento do campo de cadeia de caracteres em bytes  |
| Strings     | Matriz de bytes | count        | Cadeia de caracteres ASCII                     |
| encerra | DWORD      | 4            | \_ponto e vírgula do \_ token |



 

## <a name="token_integer"></a>inteiro de TOKEN \_

Um registro de comprimento fixo. O token é seguido pelo valor inteiro necessário.



| Campo | Tipo  | Tamanho (bytes) | Sumário       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | inteiro de tOKEN \_ |
| Valor | DWORD | 4            | Inteiro único |



 

## <a name="token_guid"></a>GUID do TOKEN \_

Um registro de comprimento fixo. O token é seguido pelos quatro campos de dados, conforme definido pelo padrão uso do DCE.



| Campo | Tipo       | Tamanho (bytes) | Sumário          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | GUID do tOKEN \_       |
| Data1 | DWORD      | 4            | Campo de dados UUID 1 |
| Data2 | WORD       | 2            | Campo de dados UUID 2 |
| Data3 | WORD       | 2            | Campo de dados UUID 3 |
| Data4 | Matriz de bytes | 8            | Campo de dados UUID 4 |



 

## <a name="token_integer_list"></a>\_lista de inteiros de token \_

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de inteiros que se seguem no campo de lista. Para eficiência, listas de inteiros consecutivas devem ser compostas em uma única lista.



| Campo | Tipo  | Tamanho (bytes) | Sumário                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | \_lista de inteiros de tOKEN \_             |
| count | DWORD | 4            | Número de inteiros no campo de lista |
| list  | DWORD | contagem de 4 x    | Lista de inteiros                     |



 

## <a name="token_float_list"></a>\_lista de floats de token \_

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de floats ou duplos que se seguem no campo de lista. O tamanho do valor de ponto flutuante (float ou Double) é determinado pelo valor de float SizeSpecified no cabeçalho do arquivo. Para eficiência, listas flutuantes de TOKENs consecutivos devem ser compostas \_ \_ em uma única lista.



| Campo | Tipo               | Tamanho (bytes)   | Sumário                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | \_lista de floats de tOKEN \_                        |
| count | DWORD              | 4              | Número de floats ou duplos no campo de lista |
| list  | matriz float/double | contagem de 4 ou 8 x | Flutuar ou lista dupla                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação binária](binary-encoding.md)
</dt> </dl>

 

 
