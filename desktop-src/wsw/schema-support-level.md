---
title: Nível de suporte do esquema
description: Esta seção aborda os detalhes sobre o nível de suporte ao esquema.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Serviços Web de nível de suporte do esquema para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104563768"
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

-   complexContent dá suporte à extensão de conteúdo complexo. Mapeia para a herança de estrutura.
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
-   (em branco) com suporte; complexType pode ser uma estrutura vazia se não houver nenhum atributo.

## <a name="elements"></a>Elementos

<xs: Element>pode ocorrer em três contextos.

-   Pode ocorrer dentro de um <xs: Sequence>, descrevendo um campo de uma estrutura regular. Nesse caso, o atributo maxOccurs deve ser 1. O campo será opcional se minOccurs for 0.
-   Pode ocorrer dentro de um <xs: Sequence>, descrevendo um campo de uma matriz. Nesse caso, o atributo maxOccurs deve ser maior que 1 ou ' unbounded '.
-   Pode ocorrer dentro de um <xs: Schema> como uma descrição de elemento global.

<xs: Element> em um <xs: Sequence> ou <xs: Choice> como um campo em uma estrutura

-   referência com suporte; resolvido para referência ao elemento global.
-   nome com suporte, mapeado para o nome do campo.
-   tipo com suporte, é mapeado para o tipo de campo. Para obter mais informações, consulte ' mapeamento de tipo '. Se não for especificado (e o elemento não contiver um tipo anônimo), xs: anyType será assumido.
-   bloquear gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   padrão gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   correção de aviso de geração de recurso sem suporte, nenhuma alteração na criação de código.
-   formulário ignorado. Nossa camada de serialização dá suporte a formulários qualificados e não qualificados.
-   ID ignorada.
-   maxOccurs é mapeado para um único campo de dados se for igual a 1. Ele será mapeado para um campo de matriz (elemento repetitivo) se maxOccurs for maior que 1.
-   minOccurs se for 0, as opções de campo serão definidas como campo \_ opcional, se anulável não estiver definido.
-   anulável o campo é anulável. Consulte [serialização](serialization.md) para obter mais detalhes.

<xs: Element> como elemento global: Attributes

os atributos minOccurs e maxOccurs são inválidos como descrição do elemento global. O aplicativo pode usar a descrição do elemento gerado na camada de serialização ou nas camadas de canal diretamente.

-   Abstract gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   bloquear gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   padrão gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   final da geração de aviso sobre o recurso sem suporte, nenhuma alteração na criação de código.
-   correção de aviso de geração de recurso sem suporte, nenhuma alteração na criação de código.
-   ID ignorada.
-   nome com suporte – mapeie para o nome da descrição do elemento global e é a base para o tipo anônimo quando especificado.
-   anulável ignorado-o aplicativo precisa chamar com o sinalizador direito.
-   fallback do grupo de substituição para a estrutura com o buffer XML do WS, \_ \_ se definido. Wsutil não oferece suporte a Substitution.
-   tipo com suporte e mapear para o tipo do elemento.

<xs: Element> como elemento global: Contents

-   simpleType com suporte; mapeia para definição de tipo.
-   complexType com suporte; mapeia para um tipo complexo.
-   aviso de geração exclusiva sobre recurso sem suporte, nenhuma alteração na geração de código. Wsutil não dá suporte a restrições de elemento.
-   chave de geração de aviso sobre recurso sem suporte, nenhuma alteração na geração de código. Wsutil não dá suporte a restrições de elemento.
-   keyref gera um aviso sobre o recurso sem suporte; nenhuma alteração na geração de código. Wsutil não dá suporte a restrições de elemento.
-   ficará Porta o elemento sem nenhuma especificação de tipo é tratado como xs: anyType.

## <a name="simple-types"></a>Tipos simples

Atributos <xs: simpleType>

-   Final da geração de aviso sobre o recurso sem suporte, nenhuma alteração na criação de código.
-   ID ignorada
-   Nome com suporte, mapeado para o nome do tipo.

<xs: simpleType> conteúdo

-   Restrição com suporte, é mapeada para o tipo ou intervalo de enumeração. Consulte a seção "xs: simpleType Restrictions".
-   Lista gerar aviso sobre o recurso sem suporte, fallback para o \_ buffer XML.
-   União gere um aviso sobre o recurso sem suporte, fallback para o \_ buffer XML.

## <a name="simple-type-restriction"></a>Restrição de tipo simples

Determinadas facetas são permitidas em tipos integrais e tipo de cadeias de caracteres para permitir suporte a intervalo e enumeração.

suporte à enumeração

<xs: Enumeration> restrição de tipo simples para o tipo base da cadeia de caracteres é tratada como tipo enum. Nesse caso, o atributo base deve ser do tipo cadeia de caracteres. Em caso de enumeração, todas as outras facetas são ignoradas.

intervalo no suporte de tipo simples

Algumas facetas são suportadas em tipos simples dão suporte a um intervalo efetivamente permitido no tipo. A seguir estão restrições para tipos integrais e tipos float/double. Tipos simples com outras facetas são submetidos a backup para o \_ tipo de cadeia de caracteres WS

-   Suporte para minExclusive
-   minInclusive com suporte
-   maxExclusive com suporte
-   maxInclusive com suporte
-   totalDigits gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   fractionDigits gere aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   comprimento gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.
-   minLength gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.
-   maxLength gerar aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   a enumeração gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.
-   Espaço em branco gera aviso sobre recurso sem suporte, nenhuma alteração na geração de código.
-   padrão gera um aviso sobre o recurso sem suporte, nenhuma alteração na geração de código.
-   ficará Porta.

Não há suporte para minLength e maxLength na cadeia de caracteres no momento, mas é um recurso desejável para dar suporte ao.

## <a name="inheritance"></a>Herança

O Wsutil dá suporte à herança de tipos complexos, ou seja, uma estrutura pode herdar de outra estrutura, semelhante à herança de interface em C++. Isso é feito por meio do <xs: complexContentExtension>. <há suporte para o> xs: simpleContentExtension, mas é gerado como uma estrutura simples com o tipo base como primeiro campo, em vez de herança de tipo.

## <a name="typeprimitive-mapping"></a>Mapeamento de tipo/primitivo

Os identificadores precisam ser normalizados ao converter de NCNames em XML. Cadeias de caracteres são anuláveis; os tipos de ponteiro são anuláveis; tipos integrais e float/double são anuláveis e defaultValue é definido como 0.

![Tabela mostrando o mapeamento entre tipos XSD e tipos de dados Sapphire.](images/schematypemap.png)

 

 




