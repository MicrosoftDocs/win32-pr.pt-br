---
description: Todas as implementações em conformidade com CIM devem lidar com um conjunto padrão de qualificadores.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Qualificadores padrão
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 67877cfc07a247d6b5e3309270d145bc64fbb814416fa4288c6e85ff2ad2e986
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315132"
---
# <a name="standard-qualifiers"></a>Qualificadores padrão

Todas as implementações em conformidade com CIM devem lidar com um conjunto padrão de qualificadores. Qualquer objeto específico não tem todos os qualificadores listados. Normalmente, as classes de extensão fornecem qualificadores adicionais para facilitar o provisionamento de instâncias de classe e outras operações na classe .

É responsabilidade do provedor impor os qualificadores. O WMI não impõe qualificadores, mas os usa apenas para informar o usuário sobre como a propriedade é usada.

> [!Note]  
> O WMI está em conformidade com a especificação cim 2.5.

 

Os qualificadores têm as seguintes limitações:

-   Nem todos os qualificadores padrão podem ser usados juntos.
-   Nem todos os qualificadores podem ser aplicados a todos os constructos, como associação ou referência. Essas limitações são identificadas na lista Aplica-se a.
-   Para um constructo específico, como associação ou referência, o uso dos qualificadores legais pode ser mais restrito porque alguns qualificadores são mutuamente exclusivos, o uso de um qualificador pode implicar algumas restrições no valor de outro e assim por diante. Essas regras de uso estão documentadas.
-   Qualificadores legais são herdados por entidades como propriedades, métodos, instâncias ou subclasses somente, não por associações ou referências. Por exemplo, o **qualificador MaxLen** que se aplica às propriedades não é herdado por referências.

O exemplo a seguir lista os qualificadores padrão WMI.

<dt>

<span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstrata**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: classes, associações, indicações

Indica se a classe é abstrata e serve apenas como base para novas classes. O padrão é **FALSE.** Não é possível criar instâncias de classes abstratas. A ausência desse qualificador indica que a classe não é abstrata; portanto, esse qualificador é necessário para todas as classes abstratas.

</dd> <dt>

<span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Agregado**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: referências

Indica se a referência é o componente pai de uma associação de agregação. O padrão é **FALSE.**

Uso: **os qualificadores Agregação** e Agregação são usados juntos A **agregação** qualifica a associação e **Aggregate** especifica a referência pai. 

</dd> <dt>

<span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Agregação**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: associações

Indica se a associação é uma agregação. O padrão é **FALSE.** Usado com a **agregação**. Esse qualificador é necessário para todas as associações de agregação.

</dd> <dt>

<span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: propriedades, referências, métodos

Nome alternativo para uma propriedade ou método no esquema. O padrão é **NULL.**

</dd> <dt>

<span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**Arraytype**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: propriedades, parâmetros

Tipo da matriz qualificada.

Os valores válidos são:

-   bag (padrão)
-   indexado
-   ordered

Uso: aplique esse tipo de qualificador somente a propriedades e parâmetros que são matrizes (definidos usando a sintaxe de colchete).

</dd> <dt>

<span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap**
</dt> <dd>

Tipo de dados: matriz **de cadeia de caracteres**

Aplica-se a: propriedades, métodos, parâmetros

Mapa de posições de bits significativas em que cada posição significativa pode ser "on" ou "off". Cada bit "on" mapeia para um valor correspondente na **matriz BitValues.** Ao ter vários bits "on", vários valores simultâneos na matriz **BitValues** são indicados. O padrão é **NULL.**

Para obter mais informações, consulte [BitMap e BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**
</dt> <dd>

Tipo de dados: matriz **de cadeia de caracteres**

Aplica-se a: propriedades, métodos, parâmetros

Conversão de um valor de posição de bit em uma cadeia de caracteres **associada.** O padrão é **NULL.**

Para obter mais informações, consulte [BitMap e BitValues](bitmap-and-bitvalues.md).

</dd> <dt>

<span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Construtor**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: métodos

Indica se o método cria instâncias. Esses métodos não são restritos a agir em uma única instância ou em uma única classe. Por exemplo, um construtor pode criar instâncias de associação, bem como instâncias da classe que define o construtor.

O **qualificador** construtor destina-se apenas a informações e não se espera que ele seja agido pelo gerenciador de objetos. O gerenciador de objetos não precisa chamar métodos de construtor quando um objeto é criado. Além disso, quando um construtor é chamado, o gerenciador de objetos não precisa invocar nenhum método de construtor definido para qualquer classe pai da classe original. O padrão é **FALSE.**

</dd> <dt>

<span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes

Nome do método pelo qual as instâncias dessa classe são criadas. O valor é "PutInstance" ou o nome de outro método que cria as instâncias. O padrão é **NULL.**

Uso: esse qualificador só poderá ser usado se o qualificador **SupportsCreate** estiver presente.

</dd> <dt>

<span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes

Nome do método pelo qual as instâncias dessa classe são excluídas. O valor é "DeleteInstance" ou o nome de outro método que exclui as instâncias. O padrão é **NULL.**

Uso: esse qualificador só poderá ser usado se o qualificador **SupportsDelete** estiver presente.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrição**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: qualquer

Descrição de um elemento nomeado. O padrão é **NULL.**

</dd> <dt>

<span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destruidor**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: métodos

Indica se o método exclui instâncias. Os métodos  que usam o qualificador destruidor excluem as instâncias às quais o destruidor é aplicado e não são restritos a agir em uma única instância ou classe. Por exemplo, um destruidor pode excluir instâncias de associação, bem como instâncias da classe que define o destruidor.

O **qualificador** destruidor destina-se apenas a informações e não se espera que ele seja agido pelo gerenciador de objetos. Não há nenhuma obrigação para o gerenciador de objetos chamar um método que tenha o qualificador **destruidor** quando uma instância é excluída. Além disso, quando um destruidor é chamado, o gerenciador de objetos não precisa invocar nenhum método destruidor definido para qualquer classe pai da classe original. O padrão é **FALSE.**

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: qualquer

Nome exibido na interface do usuário em vez do nome real do elemento. O padrão é **NULL.**

</dd> <dt>

<span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: qualquer

O elemento de tipo de cadeia de caracteres qualificado contém uma instância inserida. O valor do qualificador especifica o nome de uma classe CIM no mesmo namespace que a classe que possui o elemento qualificado. A instância inserida é uma instância da classe especificada, incluindo instâncias de suas subclasses. O padrão é **NULL.**

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Calibre**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: qualquer

Indica se a propriedade representa um inteiro não negativo, que pode aumentar ou diminuir, mas nunca exceder um valor máximo. O padrão é **FALSE.**

O valor máximo da propriedade não pode ser maior que 2^*n* - 1. *N* pode ser 8, 16, 32 ou 64, dependendo do tipo de dados da propriedade à qual esse qualificador é aplicado. O valor de um medidor tem seu valor máximo sempre que as informações que estão sendo modeladas são maiores ou iguais a esse valor máximo. Se as informações que estão sendo modeladas subsequentemente diminuirem abaixo do valor máximo, o medidor também diminuirá. Esse qualificador é aplicável somente a propriedades com um tipo de dados inteiro sem sinal.

</dd> <dt>

<span id="In"></span><span id="in"></span><span id="IN"></span>**Em**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: parâmetros

Indica se o parâmetro é usado para passar valores para um método . O padrão é **TRUE.**

</dd> <dt>

<span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: parâmetros

Indica se o parâmetro é um parâmetro de entrada e saída.

</dd> <dt>

<span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Chave**](key-qualifier.md)
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: propriedades, referências

Indica se a propriedade faz parte do alça de namespace. Se mais de uma propriedade tiver o [**qualificador**](key-qualifier.md) Key, todas essas propriedades formarão coletivamente a chave (uma chave composta). Quando juntas, as propriedades de chave devem fornecer uma referência exclusiva para cada instância de classe. Se esse qualificador for colocado em uma propriedade, somente o valor **TRUE** será permitido.

</dd> <dt>

<span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Preguiçoso**
</dt> <dd>

Aplica-se a: propriedades

Indica que a propriedade é de uso intensivo de recursos para retornar e requer muito tempo e memória do processador. O WMI melhora o desempenho das consultas ao não tentar retornar as propriedades marcadas com o **qualificador** Lento.

</dd> <dt>

<span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**
</dt> <dd>

Tipo de dados: matriz **de cadeia de caracteres**

Aplica-se a: classes, propriedades, associações, indicações, referências

Conjunto de valores que indicam um caminho para um local em que você pode encontrar mais informações sobre a origem de uma propriedade, classe, associação, indicação ou referência. A cadeia de caracteres de mapeamento pode ser um caminho de diretório, uma URL, uma chave do Registro, um arquivo de inclusão, uma referência a uma classe CIM ou algum outro formato. O padrão é **NULL.**

</dd> <dt>

<span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**
</dt> <dd>

Tipo de dados: **int**

Aplica-se a: referências

Número máximo de valores que uma determinada referência pode ter para cada conjunto de outros valores de referência na associação. O padrão é **NULL.** Por exemplo, se uma associação relaciona instâncias A a instâncias B e deve haver no máximo uma instância A para cada instância B, a referência a A deve ter um máximo de um qualificador.

</dd> <dt>

<span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**Maxlen**
</dt> <dd>

Tipo de dados: **int**

Aplica-se a: propriedades, métodos, parâmetros

Comprimento máximo (em caracteres) de **um** item de dados de cadeia de caracteres e indica suporte a matrizes de comprimento fixo.

Se uma matriz de comprimento fixo for encontrada, o qualificador **MaxLen** conterá o comprimento fixo encontrado durante a análise. Se uma matriz de comprimento variável for encontrada, esse qualificador não será usado. **MaxLen** é usado para sugerir o número máximo de elementos que devem ser armazenados em uma matriz. Ao substituindo o valor padrão, qualquer valor inteiro sem sinal (**uint32**) pode ser especificado. Um valor **null** (padrão) implica um comprimento ilimitado.

</dd> <dt>

<span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**Maxvalue**
</dt> <dd>

Tipo de dados: **int**

Aplica-se a: propriedades, métodos, parâmetros

Valor máximo do objeto . O padrão é **NULL.**

</dd> <dt>

<span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**
</dt> <dd>

Tipo de dados: **int**

Aplica-se a: referências

Cardinalidade mínima da referência (o número mínimo de valores que uma determinada referência pode ter para cada conjunto de outros valores de referência na associação). O padrão é 0.

Por exemplo, se uma associação relaciona instâncias A a instâncias B e deve haver pelo menos uma instância A para cada instância B, a referência a A deve ter um mínimo de um qualificador.

</dd> <dt>

<span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**Minvalue**
</dt> <dd>

Tipo de dados: **int**

Aplica-se a: propriedades, métodos, parâmetros

Indica o valor mínimo do objeto . O padrão é **NULL.**

</dd> <dt>

<span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**
</dt> <dd>

Tipo de dados: matriz **de cadeia de caracteres**

Aplica-se a: propriedades

Conjunto de valores que indicam correspondência entre a propriedade de um objeto e outras propriedades no esquema CIM. O padrão é **NULL.**

As propriedades do objeto são identificadas usando a sintaxe a seguir.

<schema name> "\_" <class or association name> "." <property name>

</dd> <dt>

<span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Não local**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: referências

Local de uma instância, cujo valor é <*namespacetype*>://<*namespacehandle*> O padrão é **NULL.**

Uso: esse qualificador não pode ser usado com **o qualificador NonlocalType.**

</dd> <dt>

<span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: referências

Tipo de local de uma instância. Seu valor é <namespacetype> . O padrão é **NULL**.

Uso: este qualificador não pode ser usado com o qualificador não **local** .

</dd> <dt>

<span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: Propriedades

Valor que indica que a propriedade associada é **nula** (a propriedade não tem um valor válido ou significativo). O padrão é **NULL**.

As convenções e restrições usadas para definir valores **nulos** são as mesmas aplicáveis ao qualificador **ValueMap** . Observe que esse qualificador não pode ser substituído. Não é razoável permitir que uma subclasse retorne um valor **nulo** diferente daquele da classe pai.

</dd> <dt>

<span id="Out"></span><span id="out"></span><span id="OUT"></span>**Fora**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: parâmetros

Indica se o parâmetro retorna valores de um método. O padrão é **false**.

</dd> <dt>

<span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Substituição**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: Propriedades, métodos, referências

Classe pai ou construção subordinada (Propriedade, método ou referência) que é substituída pela propriedade, método ou referência do mesmo nome na classe derivada. O padrão é **NULL**.

O formato é:

\[<> de *classe* . \] < *construção subordinada*>

Se o nome da classe for omitido, a substituição se aplicará à construção subordinada na classe pai na hierarquia de classe.

Uso: o qualificador de **substituição** pode se referir a construções com base no mesmo modelo meta apenas. Não é permitido alterar um nome ou assinatura de construção durante uma operação de substituição.

</dd> <dt>

<span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**Sobreridevalue**
</dt> <dd>

Aplica-se a: classes

Indica se o valor da propriedade em uma subclasse substitui o valor em uma classe pai. A implicação funcional é que, se você executar uma consulta em relação à classe pai e se a cláusula **Where** incluir essa propriedade, o pai deverá retornar uma instância com o valor substituído. como resultado, o gerenciamento de Windows ajusta a cláusula **where** da consulta enviada para a classe pai para excluir referências a essa propriedade.

</dd> <dt>

<span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagadas**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: Propriedades

Nome da chave que está sendo propagada. O padrão é **NULL**.

O uso desse qualificador pressupõe a existência de apenas um qualificador fraco em uma referência que tem a classe que a contém como seu destino. A propriedade associada deve ter o mesmo valor que a propriedade nomeada pelo qualificador na classe no outro lado da Associação fraca. O formato é:

\[<> de *classe* . \] < *construção subordinada*>

Uso: quando o qualificador **propagado** é usado, o qualificador de [**chave**](key-qualifier.md) deve ser especificado com um valor de **true**.

</dd> <dt>

<span id="Read"></span><span id="read"></span><span id="READ"></span>**Leitura**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: Propriedades

Indica se a propriedade é legível. O padrão é **true**.

</dd> <dt>

<span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Necessário**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: Propriedades

Indica se um valor não nulo é necessário para a propriedade. O padrão é **false**.

</dd> <dt>

<span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revisão**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes, associações, indicações, esquemas

Número de revisão secundária do objeto de esquema. O padrão é **NULL**.

Uso: o qualificador de **versão** deve estar presente para fornecer o número de versão principal quando o qualificador de **revisão** é usado.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Esquema**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: Propriedades, métodos

Nome do esquema no qual o recurso está definido. O padrão é **NULL**.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Original**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes, associações, indicações, referências

Local de uma instância. O padrão é **NULL**.

O valor do qualificador é <*namespacetype*>://<*namespacehandle*>.

Uso: o qualificador de **origem** não pode ser usado com o qualificador **SourceType** .

</dd> <dt>

<span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes, associações, indicações, referências

Tipo de local de uma instância. O valor desse qualificador é <*namespacetype*>. O padrão é **NULL**.

Uso: o qualificador **SourceType** não pode ser usado com o qualificador de **origem** .

</dd> <dt>

<span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica se a classe oferece suporte à criação de instâncias. O padrão é **false**.

</dd> <dt>

<span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica se a classe oferece suporte à exclusão de instâncias. O padrão é **false**.

</dd> <dt>

<span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica se a classe oferece suporte à modificação (atualização) de instâncias. O padrão é **false**.

</dd> <dt>

<span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Componentes**
</dt> <dd>

Tipo de dados: **booliano**

Aplica-se a: classes

Indica se a classe pode ter subclasses. O padrão é **false**.

Se uma subclasse for declarada, o compilador gerará um erro.

Uso: esse qualificador não pode coexistir com o qualificador **abstrato** . Se os qualificadores **terminal** e **abstract** forem especificados, o compilador gerará um erro.

</dd> <dt>

<span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Unit**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: propriedades, métodos, parâmetros

Tipo de unidade na qual o item de dados associado é expresso. O padrão é **NULL.**

Por exemplo, um item de dados de tamanho pode ter um valor de "bytes" para **Unidades**.

</dd> <dt>

<span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**Valuemap**
</dt> <dd>

Tipo de dados: matriz **de cadeia de caracteres**

Aplica-se a: propriedades, métodos, parâmetros

Conjunto de valores permitidos para uma propriedade, tipo de retorno de método ou parâmetro de método. O padrão é **NULL.**

Uso: esse qualificador pode ser usado sozinho ou em combinação com o qualificador **Valores.** Quando usado em combinação com o qualificador **Valores,** o local do valor na matriz **ValueMap** fornece o local da entrada correspondente na matriz **Valores.** Use o **qualificador ValueMap** somente com valores de cadeia de caracteres e inteiros. A sintaxe para representar um valor inteiro na matriz de mapa de valor é \[ + \| = \] dígito \[ \* \] . O conteúdo, o número máximo de dígitos e o valor representado são restritos pelo tipo da propriedade associada. Por exemplo, uint8 pode não ser assinado, deve ser menor que quatro dígitos e deve representar um valor menor que 256.

</dd> <dt>

<span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Valores**
</dt> <dd>

Tipo de dados: matriz **de cadeia de caracteres**

Aplica-se a: propriedades, métodos, parâmetros

Conjunto de valores que traduziam um valor inteiro em uma cadeia de caracteres associada. O padrão é **NULL.**

Essa propriedade também especifica uma matriz de valores de cadeia de caracteres a serem mapeados para uma propriedade de enumeração. Esse qualificador pode ser aplicado a uma propriedade de inteiro ou a uma propriedade de cadeia de caracteres, e o mapeamento pode ser implícito ou explícito. Se o mapeamento for implícito, os valores de propriedade de inteiro ou de cadeia de caracteres representarão posições ordinais na matriz **Valores.** Se o mapeamento for explícito, a propriedade deverá ser um inteiro e os valores de propriedade válidos serão listados na matriz definida pelo qualificador **ValueMap.** Para obter mais informações, consulte [Mapa de valor](value-map.md).

Se um **qualificador ValueMap** não estiver presente, a matriz **Values** será indexada (zero relativo) usando o valor na propriedade associada, no tipo de retorno do método ou no parâmetro de método. Se um **qualificador ValueMap** estiver presente, o índice de valores será definido pelo local do valor da propriedade no mapa de valor.

</dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versão**
</dt> <dd>

Tipo de dados: **cadeia de caracteres**

Aplica-se a: classes, esquemas, associações, indicações

Número de versão principal do objeto de esquema. O padrão é **NULL.** O número de versão é incrementado quando são feitas alterações no esquema que altera a interface.

</dd> <dt>

<span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Fraco**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: referências

Indica se as chaves da classe referenciada incluem as chaves dos outros participantes na associação. O padrão é **FALSE.**

Esse qualificador é usado quando a identidade da classe referenciada depende da identidade dos outros participantes na associação. Não mais de uma referência a qualquer classe pode ser fraca. As outras classes na associação devem definir uma chave. As chaves das outras classes na associação são repetidas na classe referenciada e marcadas com um **qualificador Propagado.**

</dd> <dt>

<span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Escrever**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: propriedades

Indica que aplicativos ou scripts podem alterar o valor da propriedade. A conta que executa o aplicativo deve ter acesso ao namespace que contém instâncias da classe . A implementação do provedor também pode limitar o acesso aos dados do provedor. Um valor **true** indica que a propriedade é acessível e escrevêvel por consumidores que têm permissão de acesso pelo WMI e pelo provedor. O padrão é **FALSE.**

Uma propriedade que não tem o **qualificador Write** ainda pode ser writeable. A implementação do provedor pode permitir que todas as propriedades nas classes de provedor sejam alteradas, independentemente **de** o qualificador Write estar presente.

</dd> <dt>

<span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: propriedades

Indica se a propriedade pode ser escrita na criação da instância. Esse qualificador pode ser usado em conjunto com o **qualificador WriteAtCreate.** O padrão é **FALSE.**

</dd> <dt>

<span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**
</dt> <dd>

Tipo de dados: **booliana**

Aplica-se a: propriedades

Indica se a propriedade pode ser escrita na atualização da instância. Esse qualificador pode ser usado em conjunto com o **qualificador WriteAtCreate.** O padrão é **FALSE.**

</dd> </dl>

## <a name="examples"></a>Exemplos

Para obter mais informações sobre como recuperar qualificadores, consulte o exemplo de código Do PowerShell [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) na Galeria do TechNet.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>       |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Qualificadores WMI](wmi-qualifiers.md)
</dt> <dt>

[Adicionando um qualificador](adding-a-qualifier.md)
</dt> </dl>

 

 




