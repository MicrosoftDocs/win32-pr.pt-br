---
description: Uma versão concreta da classe de \_ trabalho CIM. Essa classe representa uma unidade de trabalho instalível genérica a ser executado, como um lote ou um trabalho de impressão.
ms.assetid: fad4d894-d1f5-428d-819f-74966dd9f410
title: CIM_ConcreteJob classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob
- CIM_ConcreteJob.InstanceID
- CIM_ConcreteJob.Name
- CIM_ConcreteJob.JobState
- CIM_ConcreteJob.TimeOfLastStateChange
- CIM_ConcreteJob.TimeBeforeRemoval
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a62ab2392ce2c069aa88ebb465f7028368f30bd5432cf96559c7eebe6edb8bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813157"
---
# <a name="cim_concretejob-class"></a>Classe CIM \_ ConcreteJob

Uma versão concreta da classe [**de \_ trabalho CIM.**](cim-job.md) Essa classe representa uma unidade de trabalho instalível genérica a ser executado, como um lote ou um trabalho de impressão.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteJob : CIM_Job
{
  string   InstanceID;
  string   Name;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = "00000000000500.000000:000";
};
```

## <a name="members"></a>Membros

A **classe CIM \_ ConcreteJob** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe CIM \_ ConcreteJob** tem esses métodos.



| Método                                                           | Descrição                                                                          |
|:-----------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**Geterror**](cim-concretejob-geterror.md)                     | Recupera informações de erro para o status operacional de um trabalho concreto.<br/> |
| [**RequestStateChange**](cim-concretejob-requeststatechange.md) | Solicita a alteração de estado especificada para um trabalho concreto.<br/>                    |



 

### <a name="properties"></a>Propriedades

A **classe CIM \_ ConcreteJob** tem essas propriedades.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Chave**](/windows/desktop/WmiSdk/key-qualifier), [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")
</dt> </dl>

Identifica de forma exclusiva e opaca uma instância dessa classe dentro do escopo do namespace que o contém.

> [!IMPORTANT]
>
> Para garantir a exclusividade no namespace, o valor da **propriedade InstanceID** deve ser construído no seguinte padrão: *OrgID*:*LocalID*
>
> *OrgID* deve incluir um nome protegido por direitos autorais, marcas comerciais ou exclusivos pertencentes à entidade de negócios que define a **InstanceID** ou ser uma ID registrada atribuída por uma autoridade global reconhecida. Esse padrão é semelhante à estrutura de nomes de classe de esquema. Além disso, para garantir a exclusividade, os primeiros dois-pontos **em InstanceID** devem estar entre *o OrgID* e *o LocalID.* Portanto, *a OrgID* não deve conter dois-pontos (':').
>
> *LocalID* é escolhido pela entidade de negócios e não deve ser usado de novo para identificar diferentes elementos subjacentes do mundo real.
>
> Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor **de InstanceID** resultante não seja rea usado em nenhuma propriedade **InstanceID** produzida por esse provedor ou outros provedores para esse namespace.
>
> Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com *o OrgID* definido como CIM.

 

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado operacional do trabalho e a transição entre esses estados.

<dt>

<span id="New"></span><span id="new"></span><span id="NEW"></span>

<span id="New"></span><span id="new"></span><span id="NEW"></span>**Novo** (2)


</dt> <dd>

o trabalho nunca foi iniciado.

</dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Iniciando** (3)


</dt> <dd>

O trabalho está mudando dos estados 'Novo', 'Suspenso' ou 'Serviço' para o estado 'Em execução'.

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em** execução (4)


</dt> <dd>

O trabalho está em execução.

</dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (5)


</dt> <dd>

O trabalho é interrompido, mas pode ser reiniciado de maneira perfeita.

</dd> <dt>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>

<span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Desligando** (6)


</dt> <dd>

O trabalho está mudando para um estado 'Concluído', 'Encerrado' ou 'Encerrado'.

</dd> <dt>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>

<span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Concluído** (7)


</dt> <dd>

O trabalho foi concluído normalmente.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (8)


</dt> <dd>

O trabalho foi interrompido por uma solicitação de alteração de estado 'Terminate'. O trabalho e todos os seus processos subjacentes são encerrados e podem ser reiniciados (isso é específico do trabalho) apenas como um novo trabalho.

</dd> <dt>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>

<span id="Killed"></span><span id="killed"></span><span id="KILLED"></span>**Morto** (9)


</dt> <dd>

O trabalho foi interrompido por uma solicitação de alteração de estado 'Kill'. Os processos subjacentes podem ter sido deixados em execução e a limpeza pode ser necessária para liberar recursos.

</dd> <dt>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>

<span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span>**Exceção** (10)


</dt> <dd>

O trabalho está em um estado anormal que pode ser um indicativo de uma condição de erro. O status real pode ser exibido por meio de objetos específicos do trabalho.

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Serviço** (11)


</dt> <dd>

O Trabalho está em um estado específico do fornecedor que dá suporte à descoberta de problemas, à resolução ou a ambos

</dd> <dt>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>

<span id="Query_Pending"></span><span id="query_pending"></span><span id="QUERY_PENDING"></span>**Consulta pendente** (12)


</dt> <dd>

Aguardando um cliente resolver uma consulta.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (13..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor Reservado** (32768..65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Obrigatório,**](/windows/desktop/WmiSdk/standard-qualifiers) [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome")
</dt> </dl>

O nome amigável da instância. Além disso, o nome amigável pode ser usado como uma propriedade para uma pesquisa ou consulta.

> [!Note]  
> O nome não precisa ser exclusivo dentro do namespace.

 

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Indica por quanto tempo um trabalho concluído é retido. O valor padrão é "0000000000500.0000000:000" (cinco minutos).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data ou a hora em que o estado do trabalho foi alterado pela última vez.

> [!Note]  
> Se o estado do Trabalho não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo zero.

 

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

[**Trabalho \_ CIM**](cim-job.md)
</dt> </dl>

 

