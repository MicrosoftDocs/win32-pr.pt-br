---
description: Uma ACE (entrada de controle de acesso condicional) permite que uma condição de acesso seja avaliada quando uma verificação de acesso é executada. A SDDL (linguagem de definição do descritor de segurança) fornece sintaxe para definir ACEs condicionais em um formato de cadeia de caracteres.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Linguagem de definição do descritor de segurança para ACEs condicionais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0a746460c7582d95e0c95e2a2c179aac2eb29456418234cb52e842c8c56738
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117780521"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Linguagem de definição do descritor de segurança para ACEs condicionais

Uma ACE [*(entrada de controle de*](/windows/desktop/SecGloss/a-gly) acesso condicional) permite que uma condição de acesso seja avaliada quando uma verificação de acesso é executada. A SDDL (linguagem de definição do descritor de segurança) fornece sintaxe para definir ACEs condicionais em um formato de cadeia de caracteres.

O SDDL para uma ACE condicional é o mesmo que para qualquer ACE, com a sintaxe da instrução condicional anexada ao final da cadeia de caracteres ACE. Para obter informações sobre o SDDL, consulte [Linguagem de Definição do Descritor de Segurança](security-descriptor-definition-language.md).

O sinal \# " " é sinônimo de "0" em atributos de recurso. Por exemplo, D:AI(XA;OICI;FA;;; WD;(OctetStringType== 1 2 3 )) é equivalente a e interpretado como \# \# \# \# \# D:AI(XA;OICI;FA;;; WD;(OctetStringType== \# 01020300)).

-   [Formato de cadeia de caracteres ACE condicional](#conditional-ace-string-format)
-   [Expressões condicionais](#conditional-expressions)
-   [Atributos](#attributes)
-   [Operadores](#operators)
-   [Precedência de operador](#operator-precedence)
-   [Valores desconhecidos](#unknown-values)
-   [Avaliação ace condicional](#conditional-ace-evaluation)
-   [Exemplos](#examples)
-   [Tópicos relacionados](#related-topics)

## <a name="conditional-ace-string-format"></a>Formato de cadeia de caracteres ACE condicional

Cada ACE em uma cadeia [*de caracteres de descritor de*](/windows/desktop/SecGloss/s-gly) segurança é entre parênteses. Os campos da ACE estão na ordem a seguir e são separados por ponto e vírgula (;).

*AceType***;** _AceFlags_* _;_ *_Direitos_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

Os campos são conforme descrito em [Cadeias de Caracteres ACE,](ace-strings.md)com as seguintes exceções.

-   O *campo AceType* pode ser uma das cadeias de caracteres a seguir.

    | Cadeia de caracteres de tipo ACE | Constante em Sddl.h                         | Valor aceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | "XA"<br/> | ACESSO DE RETORNO DE CHAMADA SDDL \_ \_ \_ PERMITIDO<br/> | ACESSAR \_ O TIPO ACE DE RETORNO DE CHAMADA \_ \_ \_ PERMITIDO<br/> |
    | "XD"<br/> | ACESSO DE RETORNO DE CHAMADA SDDL \_ \_ \_ NEGADO<br/>  | ACESSO \_ NEGADO TIPO ACE DE RETORNO DE \_ \_ \_ CHAMADA<br/>  |

    

     

-   A cadeia de caracteres ACE inclui uma ou mais expressões condicionais, entre parênteses no final da cadeia de caracteres.

## <a name="conditional-expressions"></a>Expressões condicionais

Uma expressão condicional pode incluir qualquer um dos elementos a seguir.



| Elemento Expression                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Testa se o atributo especificado tem um valor não zero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **exists** *AttributeName*<br/>                             | Testa se o atributo especificado existe no contexto do cliente.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valor do* *operador* *AttributeName*<br/>                     | Retorna o resultado da operação especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *ConditionalExpression* **\|\|** _ConditionalExpression_<br/> | Testa se uma das expressões condicionais especificadas é verdadeira.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Testa se ambas as expressões condicionais especificadas são verdadeiras.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | O inverso de uma expressão condicional.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Membro \_ de{**_SidArray_*_}_*<br/>                         | Testa se a [**matriz SID \_ AND \_ ATTRIBUTES**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) do contexto do cliente contém todos os SIDs (Identificadores de Segurança) na lista separada por vírgulas especificada por *SidArray.* [](security-identifiers.md)<br/> Para Permitir ACEs, um SID de contexto do cliente deve ter o **atributo \_ ES GROUP \_ ENABLED** definido para ser considerado uma combinação.<br/> Para NEGAR ACEs, um SID de contexto do cliente deve ter o ES **\_ GROUP \_ ENABLED** ou o atributo **ES GROUP USE FOR DENY \_ \_ \_ \_ \_ ONLY** definido para ser considerado uma combinação.<br/> A *matriz SidArray* pode conter cadeias de caracteres SID (por exemplo, "S-1-5-6") ou aliases de SID (por exemplo, "BA"<br/> |



 

## <a name="attributes"></a>Atributos

Um atributo representa um elemento na matriz DE INFORMAÇÕES DE ATRIBUTOS DE SEGURANÇA [**AUTHZ \_ \_ \_**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) no contexto do cliente. Um nome de atributo pode conter caracteres alfanuméricos e qualquer um dos caracteres ":", "/", "." e \_ ".

Um valor de atributo pode ser qualquer um dos tipos a seguir.



| Tipo de valor         | Descrição                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer<br/> | Um inteiro de 64 bits em notação decimal ou hexadecimal.<br/>                                                                                                                              |
| String<br/>  | Um valor de cadeia de caracteres delimitado por aspas.<br/>                                                                                                                                                      |
| SID<br/>     | SID(S-1-1-0) ou SID(BA). Deve estar no RHS de Membro \_ do ou membro do dispositivo \_ \_ de.<br/>                                                                                                           |
| BLOB<br/>    | \# seguido por números hexadecimais. Se o comprimento dos números for ímpar, o \# será convertido em 0 para torná-lo ainda mais claro. Além \# disso, um que aparece em outro lugar no valor é convertido em 0.<br/> |



 

## <a name="operators"></a>Operadores

Os operadores a seguir são definidos para uso em expressões condicionais para testar os valores de atributos. Todos eles são operadores binários e usados no formato Valor do *Operador AttributeName*  *.*



| Operador            | Descrição                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Definição convencional.<br/>                                                                                      |
| !=<br/>       | Definição convencional.<br/>                                                                                      |
| <<br/>     | Definição convencional.<br/>                                                                                      |
| <=<br/>    | Definição convencional.<br/>                                                                                      |
| ><br/>     | Definição convencional.<br/>                                                                                      |
| >=<br/>    | Definição convencional.<br/>                                                                                      |
| Contém<br/> | **TRUE** se o valor do atributo especificado for um superconjunto do valor especificado; caso contrário, **FALSE.**<br/>  |
| Qualquer \_ um dos<br/>  | **TRUE** se o valor especificado for um superconjunto do valor do atributo especificado; caso contrário, **FALSE.** <br/> |



 

Além disso, os operadores unários Exists, Member of e negation (!) são definidos conforme descrito na tabela \_ Expressões Condicionais.

O operador "Contains" deve ser precedido e seguido por espaço em branco, e o operador "Any of" deve \_ ser precedido pelo espaço em branco.

## <a name="operator-precedence"></a>Precedência de operador

Os operadores são avaliados na ordem de precedência a seguir, com operações de precedência igual sendo avaliadas da esquerda para a direita.

1.  Existe, membro \_ de
2.  Contains, any \_ of
3.  ==, !=, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

Além disso, qualquer parte de uma expressão condicional pode ser entre parênteses. As expressões entre parênteses são avaliadas primeiro.

## <a name="unknown-values"></a>Valores desconhecidos

Os resultados de expressões condicionais às vezes retornam um valor **de Desconhecido.** Por exemplo, qualquer uma das operações relacionais retorna **Desconhecido** quando o atributo especificado não existe.

A tabela a seguir descreve os resultados de uma operação **AND** lógica entre duas expressões condicionais, *ConditionalExpression1* e *ConditionalExpression2.*



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



 

A tabela a seguir descreve os resultados de uma operação **OR** lógica entre duas expressões condicionais, *ConditionalExpression1* e *ConditionalExpression2.*



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



 

A negação de uma expressão condicional com um valor **UNKNOWN** também é **UNKNOWN.**

## <a name="conditional-ace-evaluation"></a>Avaliação ace condicional

A tabela a seguir descreve o resultado da verificação de acesso de uma ACE condicional, dependendo da avaliação final da expressão condicional.

| Tipo ACE         | TRUE             | FALSE                 | DESCONHECIDO               |
|------------------|------------------|-----------------------|-----------------------|
| Allow<br/> | Allow<br/> | Ignorar ACE<br/> | Ignorar ACE<br/> |
| Negar<br/>  | Negar<br/>  | Ignorar ACE<br/> | Negar<br/>       |



 

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram como as políticas de acesso especificadas são representadas por uma ACE condicional definida usando SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Política
</dt> <dd>

Permita Executar para Todos se ambas as seguintes condições são atendidas:

-   Título = PM
-   Divisão = Finanças ou Divisão = Vendas

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Title =="PM" && ( @User.Division =="Finance" \| \| @User.Division ==" Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Política
</dt> <dd>

Permitir a execução se qualquer um dos projetos do usuário se intersecção com os projetos do arquivo.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ; FX;;; S-1-1-0; ( @User.Project Qualquer um de \_ @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Política
</dt> <dd>

Permitir acesso de leitura se o usuário tiver conectado com um cartão inteligente, for um operador de backup e estiver se conectando de um computador com o Bitlocker habilitado.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>Sddl
</dt> <dd>

D:(XA; ;FR;;; S-1-1-0; (Membro \_ de {SID(SMARTcard \_ SID), SID(BO)} && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[\[MS-DTYP: \] linguagem de descrição do descritor de segurança](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

