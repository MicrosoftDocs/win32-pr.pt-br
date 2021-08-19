---
description: A macro do tipo de objeto contém cláusulas obrigatórias e opcionais que descrevem as características básicas de um objeto MIB. O provedor SNMP converte uma MIB nas partes correspondentes da macro do tipo de objeto.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Macro de tipo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef71bcdd915dfaa59ace008c28a5d63a323c2cd1d0f119b9d91e5a0720e192e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118818002"
---
# <a name="object-type-macro"></a>Macro de tipo de objeto

A macro do tipo de objeto contém cláusulas obrigatórias e opcionais que descrevem as características básicas de um objeto MIB. O provedor SNMP converte uma MIB nas partes correspondentes da macro do tipo de objeto.

> [!Note]  
> Para obter mais informações sobre como instalar o provedor, consulte [Configurando o ambiente SNMP WMI](setting-up-the-wmi-snmp-environment.md).

 

## <a name="components"></a>Componentes

<dl> <dt>

<span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>Objeto MIB
</dt> <dd>

Objeto que contém a maioria dos dados em questão.

</dd> <dt>

<span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Descritor de objeto
</dt> <dd>

Nome exclusivo ou descritor de objeto identificando cada objeto MIB. Cada descritor de objeto MIB é mapeado exatamente para um nome de propriedade CIM. Por exemplo, **ifIndex** é convertido em **ifIndex**.

</dd> <dt>

<span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Cláusula de sintaxe](syntax-clause.md)
</dt> <dd>

Define os dados e o tipo de um objeto MIB.

</dd> <dt>

<span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Cláusula de índice](index-clause.md)
</dt> <dd>

Define uma chave para selecionar uma linha de tabela exclusiva.

</dd> <dt>

<span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUMENTA a cláusula
</dt> <dd>

Indica que a coleção de tabelas que ele especifica pode ser considerada uma extensão de outra coleção de tabelas e pode substituir a cláusula de índice em SNMPv2. As coleções referenciadas pela cláusula reaumentás podem ser combinadas com a outra coleção de tabelas para formar uma coleção. A coleção resultante compartilha as propriedades de chave primária especificadas na última coleção de tabelas na cadeia.

Nesse caso, as regras de mapeamento anteriores especificadas para a cláusula INDEX são aplicadas à última coleção de tabelas na cadeia. Em seguida, a coleção de objetos é mapeada para uma definição de classe CIM.

</dd> <dt>

<span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Cláusula do identificador de objeto
</dt> <dd>

Contém um identificador de objeto exclusivo para um objeto MIB. Esse identificador de objeto é mapeado para o **\_ identificador de objeto** de qualificador de propriedade CIM.

</dd> <dt>

<span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Cláusulas ACCESS e MAX-ACCESS](access-and-max-access-clauses.md)
</dt> <dd>

Defina os direitos de acesso ao objeto MIB.

</dd> <dt>

<span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Cláusula de descrição
</dt> <dd>

Fornece uma descrição de texto do objeto, que é mapeada para a **Descrição** do qualificador de propriedade CIM. Essa cláusula pode estar vazia.

Cada **tabela** e objeto de **entrada** em uma definição de tabela SNMP também contém uma cláusula Description, que também pode estar vazia. As cláusulas de descrição de tabela e entrada são concatenadas e o resultado é mapeado para a **Descrição** do qualificador de classe CIM.

</dd> <dt>

<span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Cláusula de STATUS
</dt> <dd>

Indica se o objeto deve ter suporte. Quando o valor da cláusula STATUS é **obsoleto**, o provedor descarta o objeto MIB do mapeamento. Caso contrário, a cláusula de STATUS será mapeada para o **status** do qualificador de propriedade CIM.

Para SNMPv1, o valor preferencial do **status** é **obrigatório** ou **opcional**, mas o qualificador pode conter algum outro valor. Para o SNMPv2C, o valor preferencial do **status** é **atual** ou **preterido**, mas o qualificador pode conter algum outro valor.

</dd> <dt>

<span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Cláusula DEFVAL
</dt> <dd>

Atribui um valor padrão a uma variável em uma linha de tabela lógica e mapeia para o qualificador de propriedade CIM de cadeia de caracteres **defval**.

</dd> <dt>

<span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Cláusula de referência
</dt> <dd>

Refere-se a outro documento que contém mais informações sobre o objeto. Essa cláusula é mapeada para a **referência** do qualificador de propriedade CIM, que é do tipo cadeia de caracteres.

</dd> <dt>

<span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Cláusula UNITs
</dt> <dd>

Fornece uma definição precisa do que o objeto representa. Essa cláusula é mapeada para as **unidades** de qualificador de propriedade CIM, que é do tipo cadeia de caracteres.

</dd> </dl>

## <a name="remarks"></a>Comentários

A macro do tipo de objeto descreve as características básicas de um objeto MIB individual. Um conjunto de macros de tipo de objeto pode ser considerado um grupo de objetos relacionados. No SNMPv2C, use a macro do grupo de objetos para agrupar formalmente os conjuntos de objetos relacionados em uma coleção. No entanto, não há um mecanismo formal para a criação de coleções em SNMPv1. Para os fins do provedor SNMP, a macro do grupo de objetos é ignorada, mas você pode inventar o agrupamento de relações e as coleções de malha.

 

 



