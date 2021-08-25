---
description: Representa uma definição de métrica que contém os metadados para um \_ objeto CIM MetricInstance.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Classe CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0614b14f3033da5cf97dfb293f0e9cc130025dbb534331f8ec3386513d8796c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829706"
---
# <a name="cim_basemetricdefinition-class"></a>\_Classe CIM BaseMetricDefinition

Representa uma definição de métrica que contém os metadados para um objeto **CIM \_ MetricInstance** .

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ BaseMetricDefinition** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ BaseMetricDefinition** tem essas propriedades.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém cadeias de caracteres de formato livre que podem ser usadas para dividir consultas de objetos [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) ao longo de uma determinada dimensão. As cadeias de caracteres devem ser significativas para os usuários finais dos dados da métrica. Além disso, as cadeias de caracteres devem indicar quais dimensões de interrupção têm suporte para a definição de métrica, pela Instrumentação subjacente.

Um exemplo é um nome de transação que permite a divisão do valor total de todas as transações em um conjunto de valores, um para cada nome de transação. Outros exemplos são um sistema de aplicativos ou um nome de grupo de usuários.

</dd> <dt>

**Calculável**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As características da métrica usada para executar cálculos.

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Não calculável** (1)


</dt> <dd>

Uma cadeia de caracteres. A aritmética não faz sentido.

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Res** . (2)


</dt> <dd>

É razoável somar esse valor em várias instâncias de, por exemplo, UnitOfWork, como o número de arquivos processados em um trabalho de backup. Por exemplo, se cada trabalho de backup for um UnitOfWork e cada trabalho fizer backup de 27.000 arquivos em média, faz sentido dizer que 100 os trabalhos de backup processaram 2,7 milhões arquivos.

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Não somable** (3)


</dt> <dd>

Não faz sentido somar esse valor em várias instâncias de UnitOfWork. Um exemplo seria uma métrica que mede o comprimento da fila quando um trabalho chega a um servidor. Se cada trabalho for um UnitOfWork e o comprimento médio da fila quando cada trabalho chega for 33, não faz sentido dizer que o comprimento da fila para 100 trabalhos é 3300. Faz sentido dizer que a média é de 33.

</dd> </dl>

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**Iscontinuous**")
</dt> </dl>

Indica como o valor da métrica muda usando atributos comuns, como alteração de direção, valores mínimos e máximos e semântica de encapsulamento.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

O designer de métrica não qualificou o ChangeType.

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span id="N_A"></span><span id="n_a"></span>**N/A** (2)


</dt> <dd>

Se a propriedade "iscontinuous" for "false", Altertype não faz sentido e deve ser definida como "N/A".

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contador** (3)


</dt> <dd>

A métrica é uma métrica de contador. Eles têm valores inteiros não negativos que aumentam de forma monotônico até atingir o número máximo reapresentável e, em seguida, encapsular e começar a aumentar de 0. Esses contadores, também conhecidos como contadores de sobreposição, podem ser usados por instância para contar o número de erros de rede ou o número de transações processadas. A única maneira de um aplicativo cliente controlar o encapsule é recuperar o valor do contador em intervalos adequadamente curtos.

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Medidor** (4)


</dt> <dd>

A métrica é uma métrica de medidor. Eles têm valores inteiros ou flutuantes que podem aumentar e diminuir arbitrariamente. Um medidor não deve encapsular ao atingir o número mínimo ou máximo representeble, em vez disso, o valor "pente" nesse número. Os valores mínimo ou máximo dentro do intervalo de valores representáveis no qual o valor de métrica "pente", pode ou não ser definido.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de dados da métrica.

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

**booliano** (1)


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

**char16** (2)


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

**data e hora** (3)


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

**real32** (4)


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

**real64** (5)


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

**sint16** (6)


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

**sint32** (7)


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

**sint64** (8)


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

**sint8** (9)


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

**cadeia de caracteres** (10)


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

**UInt16** (11)


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

**UInt32** (12)


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

**UInt64** (13)


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

**uint8** (14)


</dt> <dd></dd> </dl>

</dd> <dt>

**Gathertype**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como os valores de métrica são coletados pela Instrumentação subjacente.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

Indica que o Gathertype não é conhecido.

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)


</dt> <dd>

Indica que os valores de métrica CIM são atualizados imediatamente quando os valores dentro do recurso medido são alterados. Os valores das métricas de OnChange realmente refletem a situação atual no recurso a qualquer momento. Um exemplo é o número de usuários conectados que são atualizados imediatamente à medida que os usuários fazem logon e logoff.

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periódico** (3)


</dt> <dd>

": Indica que os valores de métrica CIM são atualizados periodicamente. Por exemplo, para um aplicativo cliente, um valor de métrica aplicável à hora atual aparecerá constante durante cada intervalo de coleta e, em seguida, salta para o novo valor no final de cada intervalo de coleta.

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)


</dt> <dd>

Indica que o valor da métrica CIM é determinado sempre que um aplicativo cliente lê-lo. Os valores de métrica OnRequest retornam realmente a situação atual dentro do recurso se alguém solicitar. No entanto, eles não mudam de "não observado" e, portanto, a assinatura para alterações de valor de métricas de OnRequest não é recomendada.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

A ID exclusiva da definição da métrica. Os GUIDs/UUID do Open Software Foundation (uso) são recomendados.

</dd> <dt>

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

True se o valor da métrica for contínuo; caso contrário, false.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da métrica. Esse nome não precisa ser exclusivo, mas deve ser descritivo e pode conter espaços em branco.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As unidades específicas de um valor. O valor dessa propriedade deve ser um valor legal do qualificador unidades programáticas, conforme definido no Apêndice C.1 de DSP0004 V2.4 ou posterior.

</dd> <dt>

**TimeScope**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM \_ BaseMetricValue**.**Duração**")
</dt> </dl>

O escopo de tempo que se aplica ao designer de métrica.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

Indica que o escopo de tempo não foi qualificado pelo designer de métrica ou é desconhecido para o provedor.

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>**Ponto** (2)


</dt> <dd>

Indica que a métrica se aplica a um ponto no tempo. Nas instâncias BaseMetricValue correspondentes, TimeStamp especifica o ponto no tempo e Duração é sempre 0.

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervalo** (3)


</dt> <dd>

Indica que a métrica se aplica a um intervalo de tempo. Nas instâncias BaseMetricValue correspondentes, TimeStamp especifica o fim do intervalo de tempo e Duração especifica sua duração

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)


</dt> <dd>

Indica que a métrica se aplica a um intervalo de tempo que começou na inicialização do recurso medido (ou seja, o ManagedElement associado por MetricDefForMe). Nas instâncias BaseMetricValue correspondentes, TimeStamp especifica o final do intervalo de tempo. Se Duration for 0, isso indicará que o tempo de inicialização do recurso medido é desconhecido. Caso afirma, Duration especifica a duração entre a inicialização do recurso e o TimeStamp.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (5..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor Reservado** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Unidades**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As unidades da métrica. Exemplos são bytes, pacotes, trabalhos, arquivos, milissegundos e amps.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ManagedElement do CIM \_**](cim-managedelement.md)
</dt> </dl>

 

