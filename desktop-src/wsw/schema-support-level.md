---
title: Nível de suporte do esquema
description: Esta seção aborda os detalhes sobre o nível de suporte ao esquema.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Serviços Web de nível de suporte de esquema para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6cae112e074d50b90425c1d8952f3b6c06463378d73767346742193b406d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026274"
---
# <a name="schema-support-level"></a>Nível de suporte do esquema

Esta seção aborda os detalhes sobre o nível de suporte ao esquema.


O esquema dá suporte diretamente ao seguinte:

-   Sequências de elementos.
-   Derivação de tipos de elemento.
-   Opções simples de elementos (aqueles que são mapeados para uma União marcada).
-   Tipos básicos definidos pelo formato binário XSD/.NET incluindo intervalos (mín./máx.).
-   Suporte simples para qualquer elemento (sem restrições no tipo de elemento).
-   Elementos opcionais e atributos com valores padrão.
-   Repetindo elementos com intervalos (mín./máx.).
-   Elementos anuláveis.

O esquema não oferece suporte ao seguinte diretamente (o que implica o comportamento de "fallback"):

-   Tipos básicos definidos pelo usuário.
-   Opções mais complicadas.
-   Rejeitando atributos desconhecidos.
-   Arredondar atributos desconhecidos.
-   Suporte mais complicado para qualquer elemento.
-   A construção all.
-   Key/keyref.

Veja a seguir uma análise detalhada do suporte a componentes de esquema diferentes. Ele é comparado com o contrato de dados no WCF porque a similaridade na funcionalidade. A diferença será descrita.

Em geral, para comportamentos de fallback:

-   os atributos são submetidos a backup à \_ cadeia de caracteres WS;
-   o conteúdo do elemento é submetido a backup no \_ buffer XML do WS \_ .
-   complexType é submetido a uma estrutura que contém um campo de \_ buffer XML do WS \_ .
-   Os tipos simples são submetidos a backup à \_ cadeia de caracteres WS.

o Wsutil gera avisos para componentes de esquema que atualmente não têm suporte total. O aplicativo pode precisar fazer uma verificação adicional para esses componentes são necessários. O Wsutil de horas extras pode ser melhorado para lidar com alguns dos recursos que atualmente têm suporte no tempo de execução, como suporte a valor padrão. o Wsutil também pode ser melhorado junto com a serialização para dar suporte a outros recursos, como o abstrato. O número de componentes de esquema sem suporte pode ser reduzido ao longo do tempo.

## <a name="the-overall-schema-document"></a>O documento de esquema geral

Definição global que pode afetar as definições inseridas no esquema. Esses são atributos globais que são aplicáveis a todas as definições no esquema.

Atributos de> de <xs: Schema

-   attributeFromDefault ignorado.
-   blockDefault ignorado.
-   elementFormDefault ignorado. Isso é diferente do DataContract, pois elementos não qualificados têm suporte em tempo de execução.
-   finalDefault ignorado. Não há nenhum suporte de linguagem C para o conceito de final.
-   ID ignorada.
-   targetNamespace com suporte e mapeado para o namespace de serviço.
-   versão ignorada.

<xs: conteúdo do> do esquema

-   incluir com suporte; Wsutil requer que toda a definição necessária esteja disponível como arquivos de entrada durante o tempo de compilação.
-   redefinição ignorada. Wsutil não dá suporte a isso.
-   importação com suporte; Wsutil requer que toda a definição necessária esteja disponível como arquivos de entrada durante o tempo de compilação.
-   simpleType com suporte – consulte a seção de tipo simples abaixo.
-   complexType com suporte-consulte a seção ' complexType '
-   Grupo ignorado.
-   attributeGroup ignorado.
-   elemento com suporte; mapeia para definições de elementos globais.
-   atributo com suporte; mapeia para definições de atributo globais.
-   notação ignorada

## <a name="complex-type"></a>Tipo complexo

O tipo complexo, representado por <xs: complexType>, poderia ser a restrição do tipo simples ou tipo complexo, extensão de tipo simples, matrizes ou estrutura. Observado que, na extensão de tipos simples, não há nenhuma herança e nenhum suporte xsi: Type.

Atributos <xs: complexType>

-   Abstract gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   bloquear gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   final da geração de aviso sobre o recurso sem suporte, nenhuma alteração na criação de código.
-   ID ignorada.
-   aviso de geração mista sobre recurso sem suporte, fallback para a estrutura com o buffer XML do WS, \_ \_ se for verdadeiro.
-   nome com suporte e mapeado para o nome do tipo de estrutura.

<xs: complexType> conteúdo

Essa é a definição de tipo para estrutura. Não há suporte para a restrição complexContent.

-   complexContent dá suporte à extensão de conteúdo complexo. Mapas estruturar a herança.
-   grupo de fallback no momento para a estrutura com o \_ campo de buffer XML do WS \_ . Pode ter suporte de acordo com a partícula abaixo.
-   opção com suporte como Union. Não há suporte para isso no contrato de dados.
-   sequência com suporte – mapeia para campos de uma estrutura
-   atributo com suporte com uma exceção de ' proibido '. fallback para a estrutura com o \_ buffer XML do WS \_ se ' proibido '.
-   attributeGroup com suporte – mapeia para sequência de atributos
-   anyAttribute ignorado
-   AttributeGroupRef com suporte – mapeia para sequência de atributos.
-   GroupRef atualmente, fallback para a estrutura com o \_ campo de buffer XML do WS \_ . Pode ter suporte de acordo com o grupo abaixo.
-   Qualquer suporte, mapeia para o \_ buffer XML
-   (em branco) mapa com suporte para uma descrição de struct vazia sem struct gerado.

<xs: Sequence> em um tipo complexo: Contents

Wsutil só dá suporte total à sequência de minOccurs = 1 e maxOccurs = 1; caso contrário, o tipo complexo é submetido a backup no \_ buffer XML do WS \_ . Ele pode ter suporte como uma matriz de estruturas.

-   elemento com suporte; cada instância é mapeada para um campo na estrutura.
-   Fallback de grupo; o complexType é fallback para o \_ buffer XML do WS \_ .
-   Todos os fallbacks; o complexType é fallback para o \_ buffer XML do WS \_ .
-   opção com suporte; mapear para o campo Union.
-   fallback de sequência; o complexType é fallback para o \_ buffer XML do WS \_ .
-   qualquer suporte; mapeado para o \_ buffer XML.
-   (em branco) com suporte; complexType poderá ser uma estrutura vazia se não houver atributos.

## <a name="elements"></a>Elementos

<xs:element>pode ocorrer em três contextos.

-   Isso pode ocorrer em um <xs:sequence>, descrevendo um campo de um struct regular. Nesse caso, o atributo maxOccurs deve ser 1. O campo será opcional se minOccurs for 0.
-   Isso pode ocorrer dentro de um <xs:sequence>, descrevendo um campo de uma matriz. Nesse caso, o atributo maxOccurs deve ser maior que 1 ou 'unbounded'.
-   Isso pode ocorrer dentro de um <xs:schema> como uma descrição de elemento global.

<xs:element> em um <xs:sequence> ou <xs:choice> como um campo em uma estrutura

-   ref Com suporte; resolvido para fazer referência ao elemento global.
-   name Supported, mapeia para o nome do campo.
-   type Supported, mapeia para o tipo de campo. Para obter mais informações, consulte 'Mapeamento de tipo'. Se não for especificado (e o elemento não contém um tipo anônimo), xs:anyType será presumido.
-   bloquear Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   padrão Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   fixo Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   formulário Ignorado. Nossa camada de serialização dá suporte a formulários qualificados e não qualificados.
-   id Ignorado.
-   maxOccurs é mapeado para um único campo de dados se for igual a 1. ele será mapeado para um campo de matriz (elemento de repetição) se maxOccurs for maior que 1.
-   minOccurs se 0, as opções de campo são definidas como FIELD \_ OPTIONAL, se nillable não estiver definido.
-   nillable O campo é nillable. Confira [Serialização](serialization.md) para obter mais detalhes.

<xs:element> como elemento global: atributos

Os atributos minOccurs e maxOccurs são inválidos como descrição do elemento global. O aplicativo pode usar a descrição do elemento gerado em camadas de serialização ou de canal diretamente.

-   abstract Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   bloquear Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   padrão Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   final Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   fixo Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   id Ignorado.
-   name Supported- map para o nome da descrição do elemento global e é a base para o tipo anônimo quando especificado.
-   Nillable Ignored-application precisa chamar com o sinalizador à direita.
-   substitutionGroup fallback to structure with WS \_ XML \_ BUFFER if set. wsutil não dá suporte a substitutionGroup.
-   type Supported e mapeie para o tipo do elemento.

<xs:element> como elemento global: conteúdo

-   simpleType com suporte; mapeia para definição de tipo.
-   complexType com suporte; mapeia para um tipo complexo.
-   unique Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código. wsutil não dá suporte a restrições de elemento.
-   key Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código. wsutil não dá suporte a restrições de elemento.
-   keyref Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código. wsutil não dá suporte a restrições de elemento.
-   (em branco) Com suporte; O elemento sem especificação de tipo é tratado como xs:anyType.

## <a name="simple-types"></a>Tipos simples

<atributos xs:simpleType>

-   Gerar aviso final sobre o recurso sem suporte, sem alteração na geração de código.
-   ID Ignorada
-   Nome Com Suporte, mapeia para o nome do tipo.

<xs:simpleType> conteúdo

-   Restrição Com suporte, mapeia para o tipo de enum ou intervalo. Consulte a seção "restrições xs:simpleType".
-   Lista Gerar aviso sobre o recurso sem suporte, fallback para BUFFER \_ XML.
-   Union Gere um aviso sobre o recurso sem suporte, fallback para BUFFER \_ XML.

## <a name="simple-type-restriction"></a>Restrição de tipo simples

Determinadas facetas são permitidas em tipos integrais e tipos de cadeias de caracteres para permitir suporte a intervalo e enum.

Suporte à enumeração

<xs:enumeration> restrição de tipo simples para o tipo base de cadeia de caracteres é tratada como tipo de enumeração. Nesse caso, o atributo Base DEVE ser o tipo de cadeia de caracteres. No caso de enumeração, todas as outras facetas são ignoradas.

intervalo no suporte de tipo simples

Algumas facetas são suportadas em tipos simples que suportam efetivamente o intervalo permitido no tipo. A seguir estão a restrição para tipos integrais e tipos float/double. Tipos simples com outras facetas são respaldados para o tipo STRING do WS \_

-   MinExclusive com suporte
-   MinInclusive com suporte
-   maxExclusive com suporte
-   maxInclusive com suporte
-   totalDigits Gere aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   fractionDigits Gere aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   length Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   minLength Gere aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   maxLength Gere aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   enumeração Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   whiteSpace Gerar aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   padrão Gere um aviso sobre o recurso sem suporte, sem alteração na geração de código.
-   (em branco) Suportado.

Atualmente, não há suporte para minLength e maxLength na cadeia de caracteres, mas é um recurso desejável para dar suporte.

## <a name="inheritance"></a>Herança

O Wsutil dá suporte à herança de tipos complexos, ou seja, uma estrutura pode herdar de outra estrutura, semelhante à herança de interface no C++. Isso é feito por meio <xs:complexContentExtension>. <xs:simpleContentExtension> é suportado, mas é gerado como estrutura simples com o tipo base como o primeiro campo em vez da herança do tipo.

## <a name="typeprimitive-mapping"></a>Mapeamento de tipo/primitivo

Os identificadores precisam ser normalizados ao traduzir de NCNames em XML. As cadeias de caracteres são nillizáveis; os tipos de ponteiro são nillable; os tipos integrais e float/double são nillable e defaultValue é definido como 0.

![Tabela mostrando o mapeamento entre tipos XSD e tipos de dados Sapfitre.](images/schematypemap.png)

 

 




