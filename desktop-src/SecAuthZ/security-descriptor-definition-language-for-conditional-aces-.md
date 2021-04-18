---
description: Uma ACE (entrada de controle de acesso condicional) permite que uma condição de acesso seja avaliada quando uma verificação de acesso é executada. A linguagem de definição do descritor de segurança (SDDL) fornece a sintaxe para definir ACEs condicionais em um formato de cadeia de caracteres.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Linguagem de definição do descritor de segurança para ACEs condicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501976"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Linguagem de definição do descritor de segurança para ACEs condicionais

Uma ACE ( [*entrada de controle de acesso*](/windows/desktop/SecGloss/a-gly) condicional) permite que uma condição de acesso seja avaliada quando uma verificação de acesso é executada. A linguagem de definição do descritor de segurança (SDDL) fornece a sintaxe para definir ACEs condicionais em um formato de cadeia de caracteres.

O SDDL para uma ACE condicional é o mesmo de qualquer ACE, com a sintaxe da instrução condicional acrescentada ao final da cadeia de caracteres ACE. Para obter informações sobre SDDL, consulte [Security Descriptor Definition Language](security-descriptor-definition-language.md).

O \# sinal "" é sinônimo de "0" em atributos de recurso. Por exemplo, D:AI (XA; OICI; FA;;; WD; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) é equivalente a e interpretado como D:ai (XA; OICI; FA;;; WD; (OctetStringType = = \# 01020300)).

-   [Formato de cadeia de caracteres da ACE condicional](#conditional-ace-string-format)
-   [Expressões condicionais](#conditional-expressions)
-   [Atributos](#attributes)
-   [Operadores](#operators)
-   [Precedência de operador](#operator-precedence)
-   [Valores desconhecidos](#unknown-values)
-   [Avaliação da ACE condicional](#conditional-ace-evaluation)
-   [Exemplos](#examples)
-   [Tópicos relacionados](#related-topics)

## <a name="conditional-ace-string-format"></a>Formato de cadeia de caracteres da ACE condicional

Cada ACE em uma cadeia de caracteres de [*descritor de segurança*](/windows/desktop/SecGloss/s-gly) é colocado entre parênteses. Os campos da ACE estão na seguinte ordem e são separados por ponto e vírgula (;).

*AceType ***;** _AceFlags_* _;_ *_Direitos_*_;_ *_ObjectGUID_*_;_ *_InheritObjectGuid_*_;_ *_AccountId_*_;(_*_condicionalização_*_)_*

Os campos são descritos em [cadeias de caracteres Ace](ace-strings.md), com as seguintes exceções.

-   O campo *AceType* pode ser uma das cadeias de caracteres a seguir.

    | ACE tipo String | Constante em SDDL. h                         | Valor de AceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | XA<br/> | \_acesso de retorno de chamada SDDL \_ \_ permitido<br/> | \_tipo de \_ ACE de retorno de chamada permitido de \_ acesso \_<br/> |
    | XD<br/> | \_acesso de retorno de chamada SDDL \_ \_ negado<br/>  | tipo de ACE de retorno de \_ chamada negado de acesso \_ \_ \_<br/>  |

    

     

-   A cadeia de caracteres ACE inclui uma ou mais expressões condicionais, delimitadas por parênteses no final da cadeia de caracteres.

## <a name="conditional-expressions"></a>Expressões condicionais

Uma expressão condicional pode incluir qualquer um dos elementos a seguir.



| Elemento Expression                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Testa se o atributo especificado tem um valor diferente de zero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **existe** *AttributeName*<br/>                             | Testa se o atributo especificado existe no contexto do cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valor* do *operador* *AttributeName*<br/>                     | Retorna o resultado da operação especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| * **\|\|** _Condicionalização_ * condicional<br/> | Testa se uma das expressões condicionais especificadas é true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Condicionalização* **&&** *Condicionalização*<br/> | Testa se ambas as expressões condicionais especificadas são true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_Conditionalparameters_*_)_*<br/>                     | O inverso de uma expressão condicional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Membro \_ de {**_SidArray_*_}_*<br/>                         | Testa se a matriz de [**\_ \_ atributos e Sid**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) do contexto do cliente contém todos os SIDs ( [identificadores de segurança](security-identifiers.md) ) na lista separada por vírgulas especificada por *SidArray*.<br/> Para permitir ACEs, um SID de contexto de cliente deve ter o conjunto de atributos **\_ \_ habilitado para grupo se** definido para ser considerado uma correspondência.<br/> Para Deny ACEs, um SID de contexto de cliente deve ter **o \_ grupo se \_ habilitado** ou **o \_ grupo se \_ usar \_ para \_ negação \_** de atributo definido para ser considerado uma correspondência.<br/> A matriz *SidArray* pode conter cadeias de caracteres Sid (por exemplo, "S-1-5-6") ou aliases de Sid (por exemplo, "BA"<br/> |



 

## <a name="attributes"></a>Atributos

Um atributo representa um elemento na matriz [**de \_ \_ \_ informações de atributos de segurança de AUTHZ**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) no contexto do cliente. Um nome de atributo pode conter qualquer caractere alfanumérico e qualquer um dos caracteres ":", "/", "." e " \_ ".

Um valor de atributo pode ser qualquer um dos tipos a seguir.



| Tipo de valor         | Descrição                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer<br/> | Um inteiro de 64 bits em notação decimal ou hexadecimal.<br/>                                                                                                                              |
| String<br/>  | Um valor de cadeia de caracteres delimitado por aspas.<br/>                                                                                                                                                      |
| SID<br/>     | SID (S-1-1-0) ou SID (BA). Deve estar no RHS do membro \_ ou \_ do membro do dispositivo \_ de.<br/>                                                                                                           |
| BLOB<br/>    | \# seguido por números hexadecimais. Se o comprimento dos números for ímpar, o \# será convertido em um 0 para torná-lo par. Além disso, uma \# exibição em outro lugar no valor é convertida em 0.<br/> |



 

## <a name="operators"></a>Operadores

Os operadores a seguir são definidos para uso em expressões condicionais para testar os valores de atributos. Todos esses são operadores binários e usados no formulário de *valor* do *operador* *AttributeName* .



| Operador            | Descrição                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Definição convencional.<br/>                                                                                      |
| !=<br/>       | Definição convencional.<br/>                                                                                      |
| <<br/>     | Definição convencional.<br/>                                                                                      |
| <=<br/>    | Definição convencional.<br/>                                                                                      |
| ><br/>     | Definição convencional.<br/>                                                                                      |
| >=<br/>    | Definição convencional.<br/>                                                                                      |
| Contém<br/> | **True** se o valor do atributo especificado for um superconjunto do valor especificado; caso contrário, **false**.<br/>  |
| Qualquer \_ de<br/>  | **True** se o valor especificado for um superconjunto do valor do atributo especificado; caso contrário, **false**. <br/> |



 

Além disso, os operadores unários existem, member \_ of e Negation (!) são definidos conforme descrito na tabela de expressões condicionais.

O operador "Contains" deve ser precedido e seguido por um espaço em branco e o operador "Any \_ of" deve ser precedido por um espaço em branco.

## <a name="operator-precedence"></a>Precedência de operador

Os operadores são avaliados na seguinte ordem de precedência, com operações de precedência igual sendo avaliadas da esquerda para a direita.

1.  Existe, membro \_ de
2.  Contém, qualquer um \_ dos
3.  = =,! =, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Além disso, qualquer parte de uma expressão condicional pode ser colocada entre parênteses. As expressões dentro dos parênteses são avaliadas primeiro.

## <a name="unknown-values"></a>Valores desconhecidos

Os resultados de expressões condicionais às vezes retornam um valor **desconhecido**. Por exemplo, qualquer uma das operações relacionais retorna **desconhecido** quando o atributo especificado não existe.

A tabela a seguir descreve os resultados de uma operação **and** lógica entre duas expressões condicionais, *ConditionalExpression1* e *ConditionalExpression2*.



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **&&** *ConditionalExpression2* |
|--------------------------|--------------------------|----------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                      |
| **TRUE**<br/>      | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |
| **FALSE**<br/>     | **TRUE**<br/>      | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **UNKNOWN**<br/>                                   |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |



 

A tabela a seguir descreve os resultados de uma operação **or** lógica entre duas expressões condicionais, *ConditionalExpression1* e *ConditionalExpression2*.



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **\|\|** *ConditionalExpression2* |
|--------------------------|--------------------------|------------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **FALSE**<br/>     | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                       |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |



 

A negação de uma expressão condicional com um valor de **desconhecido** também é **desconhecida**.

## <a name="conditional-ace-evaluation"></a>Avaliação da ACE condicional

A tabela a seguir descreve o resultado da verificação de acesso de uma ACE condicional, dependendo da avaliação final da expressão condicional.

| Tipo de ACE         | TRUE             | FALSE                 | DESCONHECIDO               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | Ignorar ACE<br/> | Ignorar ACE<br/> |
| Negar<br/>  | Negar<br/>  | Ignorar ACE<br/> | Negar<br/>       |



 

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram como as políticas de acesso especificadas são representadas por uma ACE condicional definida usando SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Regras
</dt> <dd>

Permitir executar para todos se as duas condições a seguir forem atendidas:

-   Título = PM
-   Divisão = finanças ou divisão = vendas

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Title = = "PM"  &&  ( @User.Division = = "Finance" \| \| @User.Division = = "Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Regras
</dt> <dd>

Permitir executar se qualquer um dos projetos do usuário se Interseccionar com os projetos do arquivo s.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FX;;; S-1-1-0; ( @User.Project Qualquer \_ de @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Regras
</dt> <dd>

Permitir acesso de leitura se o usuário tiver feito logon com um cartão inteligente, for um operador de backup e estiver se conectando de um computador com o BitLocker habilitado.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D: (XA;; FR;;; S-1-1-0; (Membro \_ de {Sid (SID de cartão inteligente \_ ), Sid (Bo)}  && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\[MS-DTYP \] : linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

