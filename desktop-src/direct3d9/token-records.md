---
description: Esta seção descreve o formato dos registros para cada um dos tokens de influência de registro. As informações são divididas nas seções a seguir.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Registros de token
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456ee591f15cac6e6a3d2fecaad3dfca9f0709b39a63d20fe198e591a199f4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118797418"
---
# <a name="token-records"></a>Registros de token

Esta seção descreve o formato dos registros para cada um dos tokens de influência de registro. As informações são divididas nas seções a seguir.

-   [NOME DO \_ TOKEN](/windows)
-   [CADEIA DE \_ CARACTERES DE TOKEN](/windows)
-   [NÚMERO \_ INTEIRO DO TOKEN](/windows)
-   [\_GUID DO TOKEN](/windows)
-   [LISTA \_ DE INTEIROS \_ DO TOKEN](/windows)
-   [LISTA \_ FLOAT \_ DO TOKEN](/windows)

## <a name="token_name"></a>NOME DO \_ TOKEN

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de bytes a seguir no campo nome. Um nome ASCII da contagem de comprimentos conclui o registro.



| Campo | Tipo       | Tamanho (bytes) | Sumário                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nome do token \_                    |
| count | DWORD      | 4            | Comprimento do campo de nome, em bytes |
| name  | Matriz BYTE | count        | Nome ASCII                     |



 

## <a name="token_string"></a>CADEIA DE \_ CARACTERES DE TOKEN

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de bytes a seguir no campo de cadeia de caracteres. Uma cadeia de caracteres ASCII de contagem de comprimento continua o registro, que é concluído por um token de encerramento. A escolha do terminador é determinada por problemas de sintaxe discutidos em outro lugar.



| Campo      | Tipo       | Tamanho (bytes) | Sumário                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | cadeia de \_ caracteres de token                    |
| count      | DWORD      | 4            | Comprimento do campo de cadeia de caracteres em bytes  |
| String     | Matriz BYTE | count        | Cadeia de caracteres ASCII                     |
| Terminator | DWORD      | 4            | VÍRGULA TOKEN \_ SEMICOLON \_ ou TOKEN |



 

## <a name="token_integer"></a>NÚMERO \_ INTEIRO DO TOKEN

Um registro de comprimento fixo. O token é seguido pelo valor inteiro necessário.



| Campo | Tipo  | Tamanho (bytes) | Sumário       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | tOKEN \_ INTEGER |
| Valor | DWORD | 4            | Inteiro único |



 

## <a name="token_guid"></a>\_GUID DO TOKEN

Um registro de comprimento fixo. O token é seguido pelos quatro campos de dados, conforme definido pelo padrão DCE do OSF.



| Campo | Tipo       | Tamanho (bytes) | Sumário          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | GUID tOKEN \_       |
| Data1 | DWORD      | 4            | Campo de dados UUID 1 |
| Data2 | WORD       | 2            | Campo de dados UUID 2 |
| Data3 | WORD       | 2            | Campo de dados UUID 3 |
| Data4 | Matriz BYTE | 8            | Campo de dados UUID 4 |



 

## <a name="token_integer_list"></a>LISTA \_ DE INTEIROS \_ DO TOKEN

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de inteiros que seguem no campo de lista. Para eficiência, listas de inteiros consecutivas devem ser compostas em uma única lista.



| Campo | Tipo  | Tamanho (bytes) | Sumário                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | tOKEN \_ INTEGER \_ LISt             |
| count | DWORD | 4            | Número de inteiros no campo de lista |
| list  | DWORD | Contagem de 4 x    | Lista de inteiros                     |



 

## <a name="token_float_list"></a>LISTA \_ FLOAT \_ DO TOKEN

Um registro de comprimento variável. O token é seguido por um valor de contagem que especifica o número de floats ou doubles que seguem no campo de lista. O tamanho do valor do ponto flutuante (float ou double) é determinado pelo valor de tamanho float especificado no header do arquivo. Para eficiência, OS TOKEN \_ FLOAT \_ LISTs consecutivos devem ser compostos em uma única lista.



| Campo | Tipo               | Tamanho (bytes)   | Sumário                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | tOKEN \_ FLOAT \_ LISt                        |
| count | DWORD              | 4              | Número de floats ou doubles no campo de lista |
| list  | matriz float/double | Contagem de 4 ou 8 x | Float ou lista dupla                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Codificação binária](binary-encoding.md)
</dt> </dl>

 

 
