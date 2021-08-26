---
description: A Indicação CIM é a classe base abstrata para todas as notificações sobre alterações em objetos de esquema e dados de objeto de esquema, eventos detectados por \_ provedores e instrumentação. Subclasses da Indicação CIM \_ representam tipos específicos de notificações.
ms.assetid: 85a70425-7b32-449c-9fc0-1cfbf34d9187
title: CIM_Indication classe
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
ms.openlocfilehash: 84f6999add608a1b43da2d9272703dd63f52ed2d799f47a0121bd4a50b88e9ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046816"
---
# <a name="cim_indication-class"></a>Classe cim \_ indicação

**CIM \_ Indicação** é a classe base abstrata para todas as notificações sobre alterações em objetos de esquema e dados de objeto de esquema, eventos detectados por provedores e instrumentação. Subclasses da **Indicação CIM \_** representam tipos específicos de notificações.

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

A **classe \_ Cim Indication** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ Cim Indication** tem essas propriedades.

<dl> <dt>

**CorrelatedIndications**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Notificações correlacionadas"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Indicação CIM \_**.**IndicationIdentifier**")
</dt> </dl>

Uma matriz que contém **valores de IndicationIdentifier** de notificações relacionadas a esta.

</dd> <dt>

**IndicationFilterName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")
</dt> </dl>

O identificador do filtro de indicação que processa a indicação. O serviço de envio define essa propriedade. Essa propriedade está correlacionada com a **propriedade Name** do objeto **CIM \_ IndicationFilter.** O valor de **IndicationFilterName** deve usar o seguinte formato:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* deve incluir um nome com direitos autorais, marcas comerciais ou exclusivos pertencentes à entidade de negócios que possui o objeto.
-   *<OrgID>* não deve conter dois-pontos (:)
-   *<LocalID>* um identificador exclusivo escolhido pela entidade de negócios que possui o objeto .

</dd> <dt>

**IndicationIdentifier**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Identificador de notificação")
</dt> </dl>

Um identificador da indicação. Essa propriedade pode ser usada como um valor de chave na matriz de **propriedades CorrelatedIndications.** Portanto, **IndicationIdentifier** deve ser um valor exclusivo dentro do namespace dessa instância de classe.

Para garantir que **IndicationIdentifier** seja exclusivo, ele deve usar o seguinte formato:

-   *<OrgID>*:*<LocalID>*
-   *<OrgID>* deve incluir um nome com direitos autorais, marcas comerciais ou exclusivos pertencentes à entidade de negócios que possui o objeto.
-   *<OrgID>* não deve conter dois-pontos (:)
-   *<LocalID>* um identificador exclusivo escolhido pela entidade de negócios que possui o objeto .
-   Para instâncias definidas por DMTF, *<OrgID>* deve ser definido como "CIM".

</dd> <dt>

**IndicationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora e a data em que a indicação foi criada. A propriedade poderá ser definida como **NULL** se a entidade que criou a indicação não for capaz de determinar essas informações.

> [!Note]  
> O **valor IndicationTime** pode ser o mesmo para indicações geradas em sucessão rápida.

 

</dd> <dt>

**OtherSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")
</dt> </dl>

A severidade da indicação do ponto de vista do notificador quando **PerceivedSeverity** é definido como "1" (Outro).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Severidade percebida")
</dt> </dl>

A severidade da indicação do ponto de vista do notificador.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

A Gravidade Percebida da indicação é desconhecida ou indeterminada.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd>

Indica que o valor da Gravidade pode ser encontrado na **propriedade OtherSeverity.**

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)


</dt> <dd>

As informações devem ser usadas ao fornecer uma resposta informativa.

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/Aviso** (3)


</dt> <dd>

Deve ser usado quando apropriado para permitir que o usuário decida se a ação é necessária.

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Menor** (4)


</dt> <dd>

A ação é necessária, mas a situação não é grave no momento.

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)


</dt> <dd>

A ação é necessária AGORA.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)


</dt> <dd>

A ação é necessária agora e o escopo é amplo (talvez uma paralisação iminente para um recurso crítico resultará).

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/Não Recupeável** (7)


</dt> <dd>

ocorreu um erro, mas é tarde demais para tomar uma ação corretiva.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**SequenceContext**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Indicação CIM \_**.**SequenceNumber**")
</dt> </dl>

O contexto de sequência do identificador de sequência para a indicação. Se um serviço não dá suporte a identificadores de sequência para indicações, essa propriedade deve ser definida como **NULL.** Se a indicação for entregue de forma reprojetada, essa propriedade permanecerá a mesma.

> [!Note]  
> O identificador de sequência para a indicação permite que um ouvinte identifique indicações duplicadas quando o serviço tenta entregar indicações, reordenar indicações que chegam fora de ordem e detectar indicações perdidas.

 

Para garantir que **SequenceContext** seja exclusivo, ele deve usar o seguinte formato:

-   *indication-service-name* \# *cim-service-start-id* \# *listener-destination-creation-time*
-   *indication-service-name* é o valor da propriedade **Name** da instância **de Cim \_ IndicationService** que fornece a indicação.
-   *cim-service-start-id* é um identificador que identifica exclusivamente a operação de início de um serviço. Por exemplo, isso pode ser um data/hora da hora de início ou um contador que aumenta para cada início ou reinicialização do serviço.
-   *listener-destination-creation-time* é um timestamp da hora de criação da instância **\_ listenerDestination cim** que representa o ouvinte destination.nSince que esse formato é apenas uma recomendação, os clientes CIM devem tratar o valor como um identificador opaco para o contexto de sequência e não devem depender desse formato.

</dd> <dt>

**SequenceNumber**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Indicação CIM \_**.**SequenceContext**")
</dt> </dl>

O número de sequência do identificador de sequência para a indicação.

> [!Note]  
> O identificador de sequência para a indicação permite que um ouvinte identifique indicações duplicadas quando o serviço tenta entregar indicações, reordenar indicações que chegam fora de ordem e detectar indicações perdidas.

 

O número de sequência tem as seguintes características:

-   O número de sequência é redefinido para "0" sempre que **o valor SequenceContext** é muda.
-   Sempre que o destino do ouvinte recebe uma nova indicação, o número de sequência é aumentado em "1".
-   O número de sequência é wraps para "0" quando o intervalo de valor é excedido.
-   Se a indicação for entregue de forma reprojetada, **SequenceNumber** permanecerá o mesmo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_\_ExtrinsicEvent**](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

