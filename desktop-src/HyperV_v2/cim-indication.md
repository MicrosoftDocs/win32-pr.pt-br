---
description: '\_A indicação CIM é a classe base abstrata para todas as notificações sobre alterações em objetos de esquema e dados de objeto de esquema, eventos detectados por provedores e instrumentação. As subclasses da \_ indicação CIM representam tipos específicos de notificações.'
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: Classe CIM_Indication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Indication
- CIM_Indication.IndicationIdentifier
- CIM_Indication.CorrelatedIndications
- CIM_Indication.IndicationTime
- CIM_Indication.PerceivedSeverity
- CIM_Indication.OtherSeverity
- CIM_Indication.IndicationFilterName
- CIM_Indication.SequenceContext
- CIM_Indication.SequenceNumber
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e859e7834a051bad0a5ea402e8bd6c3685b5ad54
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883531"
---
# <a name="cim_indication-class"></a>\_Classe de indicação CIM

**CIM \_ A indicação** é a classe base abstrata para todas as notificações sobre alterações em objetos de esquema e dados de objeto de esquema, eventos detectados por provedores e instrumentação. As subclasses **da \_ indicação CIM** representam tipos específicos de notificações.

## <a name="syntax"></a>Sintaxe

``` syntax
[Indication, Version("2.24.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_Indication : __ExtrinsicEvent
{
  string   IndicationIdentifier;
  string   CorrelatedIndications[];
  datetime IndicationTime;
  uint16   PerceivedSeverity;
  string   OtherSeverity;
  string   IndicationFilterName;
  string   SequenceContext;
  sint64   SequenceNumber;
};
```

## <a name="members"></a>Membros

A classe de **\_ indicação CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ indicação CIM** tem essas propriedades.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Notificações correlacionadas "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicação CIM**.**IndicationIdentifier**")
</dt> </dl>

Uma matriz que contém valores **IndicationIdentifier** de notificações que estão relacionadas a este.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

O identificador do filtro de indicação que processa a indicação. O serviço de envio define essa propriedade. Essa propriedade correlaciona com a propriedade **Name** do objeto **CIM \_ IndicationFilter** . O valor de **IndicationFilterName** deve usar o seguinte formato:

-   *&lt; OrgID &gt;*:*&lt; LocalId &gt;*
-   *&lt; OrgID &gt;* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que possui o objeto.
-   *&lt; OrgID &gt;* não deve conter dois-pontos (:)
-   LocalId um identificador exclusivo escolhido pela entidade de negócios que possui o objeto. *&lt; &gt;*

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Identificador de notificação ")
</dt> </dl>

Um identificador da indicação. Essa propriedade pode ser usada como um valor de chave na matriz da propriedade **CorrelatedIndications** . Portanto, **IndicationIdentifier** deve ser um valor exclusivo dentro do namespace dessa instância de classe.

Para garantir que o **IndicationIdentifier** seja exclusivo, ele deve usar o seguinte formato:

-   *&lt; OrgID &gt;*:*&lt; LocalId &gt;*
-   *&lt; OrgID &gt;* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que possui o objeto.
-   *&lt; OrgID &gt;* não deve conter dois-pontos (:)
-   LocalId um identificador exclusivo escolhido pela entidade de negócios que possui o objeto. *&lt; &gt;*
-   Para instâncias definidas por DMTF, *&lt; OrgID &gt;* deve ser definido como "CIM".

</dd> <dt>

**Indicaçãotime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que a indicação foi criada. A propriedade pode ser definida como **NULL** se a entidade que criou a indicação não for capaz de determinar essas informações.

> [!Note]  
> O valor de **indicatime** pode ser o mesmo para indicações que são geradas em sucessão rápida.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

A severidade da indicação do ponto de vista do notificador quando **PerceivedSeverity** é definido como "1" (outro).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Severidade percebida ")
</dt> </dl>

A severidade da indicação do ponto de vista do notificador.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

a severidade percebida da indicação é desconhecida ou indeterminada.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd>

Indica que o valor da severidade pode ser encontrado na propriedade **OtherSeverity** .

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)


</dt> <dd>

As informações devem ser usadas ao fornecer uma resposta informativa.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/aviso** (3)


</dt> <dd>

Deve ser usado quando apropriado para permitir que o usuário decida se a ação é necessária.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundária** (4)


</dt> <dd>

A ação é necessária, mas a situação não é séria no momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

A ação é necessária agora.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)


</dt> <dd>

A ação é necessária agora e o escopo é amplo (talvez uma interrupção iminente a um recurso crítico resulte).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/não recuperável** (7)


</dt> <dd>

ocorreu um erro, mas é tarde demais para realizar uma ação corretiva.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicação CIM**.**SequenceNumber**")
</dt> </dl>

O contexto de sequência do identificador de sequência para a indicação. Se um serviço não oferecer suporte a identificadores de sequência para indicações, essa propriedade deverá ser definida como **NULL**. Se a indicação for entregue novamente, essa propriedade permanecerá a mesma.

> [!Note]  
> O identificador de sequência para a indicação permite que um ouvinte identifique indicações duplicadas quando o serviço tenta entregar indicações novamente, reordenar as indicações que chegam fora de ordem e detectar indicações perdidas.

 

Para garantir que o **SequenceContext** seja exclusivo, ele deve usar o seguinte formato:

-   *indicação-nome* \# -do-serviço *CIM-Service-Start-ID* \# *ouvinte-destino-criação-de-tempo*
-   *indica-Service-Name* é o valor da propriedade **Name** da instância **\_ IndicationService do CIM** que fornece a indicação.
-   *CIM-Service-Start-ID* é um identificador que identifica exclusivamente a operação de início de um serviço. Por exemplo, isso pode ser um carimbo de hora da hora de início ou um contador que aumenta para cada início ou reinício do serviço.
-   *Listener-destino-Creation-time* é um carimbo de data/hora do tempo de criação da instância **\_ ListenerDestination do CIM** que representa o destino do ouvinte. nSince esse formato é apenas uma recomendação, os clientes CIM devem tratar o valor como um identificador opaco para o contexto de sequência e não devem depender desse formato.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicação CIM**.**SequenceContext**")
</dt> </dl>

O número de sequência do identificador de sequência para a indicação.

> [!Note]  
> O identificador de sequência para a indicação permite que um ouvinte identifique indicações duplicadas quando o serviço tenta entregar indicações novamente, reordenar as indicações que chegam fora de ordem e detectar indicações perdidas.

 

O número de sequência tem as seguintes características:

-   O número de sequência é redefinido como "0" sempre que o valor de **SequenceContext** é alterado.
-   Sempre que o destino do ouvinte receber uma nova indicação, o número de sequência será aumentado por "1".
-   O número de sequência é quebrado em "0" quando o intervalo de valores é excedido.
-   Se a indicação for entregue novamente, **SequenceNumber** permanecerá o mesmo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

