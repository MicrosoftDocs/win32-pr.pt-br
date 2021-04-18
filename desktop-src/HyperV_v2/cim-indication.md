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
ms.openlocfilehash: 46b8d50f2e90d9a51c8ffa0b93de9ac16c889340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785461"
---
# <a name="cim_indication-class"></a><span data-ttu-id="5fc5e-104">\_Classe de indicação CIM</span><span class="sxs-lookup"><span data-stu-id="5fc5e-104">CIM\_Indication class</span></span>

<span data-ttu-id="5fc5e-105">**CIM \_ A indicação** é a classe base abstrata para todas as notificações sobre alterações em objetos de esquema e dados de objeto de esquema, eventos detectados por provedores e instrumentação.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-105">**CIM\_Indication** is the abstract base class for all notifications about changes in schema objects, and schema object data, events detected by providers and instrumentation.</span></span> <span data-ttu-id="5fc5e-106">As subclasses **da \_ indicação CIM** representam tipos específicos de notificações.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-106">Subclasses of **CIM\_Indication** represent specific types of notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fc5e-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5fc5e-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="5fc5e-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5fc5e-108">Members</span></span>

<span data-ttu-id="5fc5e-109">A classe de **\_ indicação CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="5fc5e-109">The **CIM\_Indication** class has these types of members:</span></span>

-   [<span data-ttu-id="5fc5e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5fc5e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5fc5e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5fc5e-111">Properties</span></span>

<span data-ttu-id="5fc5e-112">A classe de **\_ indicação CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-112">The **CIM\_Indication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5fc5e-113">**CorrelatedIndications**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-113">**CorrelatedIndications**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-114">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-116">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Notificações correlacionadas "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicação CIM**.**IndicationIdentifier**")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-116">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Correlated notifications"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**IndicationIdentifier**")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-117">Uma matriz que contém valores **IndicationIdentifier** de notificações que estão relacionadas a este.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-117">A array that contains **IndicationIdentifier** values of notifications that are related this one.</span></span>

</dd> <dt>

<span data-ttu-id="5fc5e-118">**IndicationFilterName**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-118">**IndicationFilterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-121">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ IndicationFilter.Name")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_IndicationFilter.Name")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-122">O identificador do filtro de indicação que processa a indicação.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-122">The identifier of the indication filter that processes the indication.</span></span> <span data-ttu-id="5fc5e-123">O serviço de envio define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-123">The sending service sets this property.</span></span> <span data-ttu-id="5fc5e-124">Essa propriedade correlaciona com a propriedade **Name** do objeto **CIM \_ IndicationFilter** .</span><span class="sxs-lookup"><span data-stu-id="5fc5e-124">This property correlates with the **Name** property of the **CIM\_IndicationFilter** object.</span></span> <span data-ttu-id="5fc5e-125">O valor de **IndicationFilterName** deve usar o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5fc5e-125">The value of **IndicationFilterName** should use the following format:</span></span>

-   <span data-ttu-id="5fc5e-126">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="5fc5e-126">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="5fc5e-127">*<OrgID>* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que possui o objeto.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-127">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="5fc5e-128">*<OrgID>* Não deve conter dois-pontos (:)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-128">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="5fc5e-129">*<LocalID>* um identificador exclusivo escolhido pela entidade de negócios que possui o objeto.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-129">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>

</dd> <dt>

<span data-ttu-id="5fc5e-130">**IndicationIdentifier**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-130">**IndicationIdentifier**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-131">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-132">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-133">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Identificador de notificação ")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-133">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Notification identifier")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-134">Um identificador da indicação.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-134">An identifier of the indication.</span></span> <span data-ttu-id="5fc5e-135">Essa propriedade pode ser usada como um valor de chave na matriz da propriedade **CorrelatedIndications** .</span><span class="sxs-lookup"><span data-stu-id="5fc5e-135">This property can be used as a key value in the **CorrelatedIndications** property array.</span></span> <span data-ttu-id="5fc5e-136">Portanto, **IndicationIdentifier** deve ser um valor exclusivo dentro do namespace dessa instância de classe.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-136">Therefore, **IndicationIdentifier** should be a unique value within the namespace of this class instance.</span></span>

<span data-ttu-id="5fc5e-137">Para garantir que o **IndicationIdentifier** seja exclusivo, ele deve usar o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5fc5e-137">To ensure that **IndicationIdentifier** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="5fc5e-138">*<OrgID>*:*<LocalID>*</span><span class="sxs-lookup"><span data-stu-id="5fc5e-138">*<OrgID>*:*<LocalID>*</span></span>
-   <span data-ttu-id="5fc5e-139">*<OrgID>* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que possui o objeto.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-139">*<OrgID>* must include a copyrighted, trademarked, or unique name that is owned by the business entity that owns the object.</span></span>
-   <span data-ttu-id="5fc5e-140">*<OrgID>* Não deve conter dois-pontos (:)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-140">*<OrgID>* must not contain a colon (:)</span></span>
-   <span data-ttu-id="5fc5e-141">*<LocalID>* um identificador exclusivo escolhido pela entidade de negócios que possui o objeto.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-141">*<LocalID>* a unique identifier chosen by the business entity that owns the object.</span></span>
-   <span data-ttu-id="5fc5e-142">Para instâncias definidas por DMTF, *<OrgID>* deve ser definido como "CIM".</span><span class="sxs-lookup"><span data-stu-id="5fc5e-142">For DMTF-defined instances, *<OrgID>* should be set to "CIM".</span></span>

</dd> <dt>

<span data-ttu-id="5fc5e-143">**Indicaçãotime**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-143">**IndicationTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-144">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-144">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-145">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-146">A data e a hora em que a indicação foi criada.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-146">The time and date when the indication was created.</span></span> <span data-ttu-id="5fc5e-147">A propriedade pode ser definida como **NULL** se a entidade que criou a indicação não for capaz de determinar essas informações.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-147">The property can be set to **NULL** if the entity that created the indication is not capable of determining this information.</span></span>

> [!Note]  
> <span data-ttu-id="5fc5e-148">O valor de **indicatime** pode ser o mesmo para indicações que são geradas em sucessão rápida.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-148">The **IndicationTime** value can be the same for indications that are generated in rapid succession.</span></span>

 

</dd> <dt>

<span data-ttu-id="5fc5e-149">**OtherSeverity**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-149">**OtherSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-150">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-152">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_AlertIndication**](cim-alertindication.md).**PerceivedSeverity**")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-153">A severidade da indicação do ponto de vista do notificador quando **PerceivedSeverity** é definido como "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="5fc5e-153">The severity of the indication from the notifier's point of view when **PerceivedSeverity** is set to "1" (Other).</span></span>

</dd> <dt>

<span data-ttu-id="5fc5e-154">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-154">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-155">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-157">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Severidade percebida ")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-157">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-158">A severidade da indicação do ponto de vista do notificador.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-158">The severity of the indication from the notifier's point of view.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="5fc5e-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-159"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-160">a severidade percebida da indicação é desconhecida ou indeterminada.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-160">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="5fc5e-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-161"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-162">Indica que o valor da severidade pode ser encontrado na propriedade **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="5fc5e-162">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="5fc5e-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-163"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-164">As informações devem ser usadas ao fornecer uma resposta informativa.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-164">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="5fc5e-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/aviso** (3)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-165"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-166">Deve ser usado quando apropriado para permitir que o usuário decida se a ação é necessária.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-166">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="5fc5e-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundária** (4)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-167"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-168">A ação é necessária, mas a situação não é séria no momento.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-168">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="5fc5e-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-169"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-170">A ação é necessária agora.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-170">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="5fc5e-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-171"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-172">A ação é necessária agora e o escopo é amplo (talvez uma interrupção iminente a um recurso crítico resulte).</span><span class="sxs-lookup"><span data-stu-id="5fc5e-172">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="5fc5e-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-173"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="5fc5e-174">ocorreu um erro, mas é tarde demais para realizar uma ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-174">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="5fc5e-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="5fc5e-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="5fc5e-176">**SequenceContext**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-176">**SequenceContext**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-179">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicação CIM**.**SequenceNumber**")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-179">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceNumber**")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-180">O contexto de sequência do identificador de sequência para a indicação.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-180">The sequence context of the sequence identifier for the indication.</span></span> <span data-ttu-id="5fc5e-181">Se um serviço não oferecer suporte a identificadores de sequência para indicações, essa propriedade deverá ser definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-181">If a service does not support sequence identifiers for indications, this property should be set to **NULL**.</span></span> <span data-ttu-id="5fc5e-182">Se a indicação for entregue novamente, essa propriedade permanecerá a mesma.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-182">If the indication is redelivered, this property remains the same.</span></span>

> [!Note]  
> <span data-ttu-id="5fc5e-183">O identificador de sequência para a indicação permite que um ouvinte identifique indicações duplicadas quando o serviço tenta entregar indicações novamente, reordenar as indicações que chegam fora de ordem e detectar indicações perdidas.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-183">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="5fc5e-184">Para garantir que o **SequenceContext** seja exclusivo, ele deve usar o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="5fc5e-184">To ensure that **SequenceContext** is unique, it should use the following format:</span></span>

-   <span data-ttu-id="5fc5e-185">*indicação-nome* \# -do-serviço *CIM-Service-Start-ID* \# *ouvinte-destino-criação-de-tempo*</span><span class="sxs-lookup"><span data-stu-id="5fc5e-185">*indication-service-name*\#*cim-service-start-id* \#*listener-destination-creation-time*</span></span>
-   <span data-ttu-id="5fc5e-186">*indica-Service-Name* é o valor da propriedade **Name** da instância **\_ IndicationService do CIM** que fornece a indicação.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-186">*indication-service-name* is the value of the **Name** property of the **CIM\_IndicationService** instance that delivers the indication.</span></span>
-   <span data-ttu-id="5fc5e-187">*CIM-Service-Start-ID* é um identificador que identifica exclusivamente a operação de início de um serviço.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-187">*cim-service-start-id* is an identifier that uniquely identifies the start operation of a service.</span></span> <span data-ttu-id="5fc5e-188">Por exemplo, isso pode ser um carimbo de hora da hora de início ou um contador que aumenta para cada início ou reinício do serviço.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-188">For example, this could be a timestamp of the start time, or a counter that increases for each start or restart of the service.</span></span>
-   <span data-ttu-id="5fc5e-189">*Listener-destino-Creation-time* é um carimbo de data/hora do tempo de criação da instância **\_ ListenerDestination do CIM** que representa o destino do ouvinte. nSince esse formato é apenas uma recomendação, os clientes CIM devem tratar o valor como um identificador opaco para o contexto de sequência e não devem depender desse formato.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-189">*listener-destination-creation-time* is a timestamp of the creation time of the **CIM\_ListenerDestination** instance representing the listener destination.nSince this format is only a recommendation, CIM clients shall treat the value as an opaque identifier for the sequence context and shall not rely on this format.</span></span>

</dd> <dt>

<span data-ttu-id="5fc5e-190">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-190">**SequenceNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5fc5e-191">Tipo de dados: **sint64**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-191">Data type: **sint64**</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="5fc5e-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5fc5e-193">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ indicação CIM**.**SequenceContext**")</span><span class="sxs-lookup"><span data-stu-id="5fc5e-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Indication**.**SequenceContext**")</span></span>
</dt> </dl>

<span data-ttu-id="5fc5e-194">O número de sequência do identificador de sequência para a indicação.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-194">The sequence number of the sequence identifier for the indication.</span></span>

> [!Note]  
> <span data-ttu-id="5fc5e-195">O identificador de sequência para a indicação permite que um ouvinte identifique indicações duplicadas quando o serviço tenta entregar indicações novamente, reordenar as indicações que chegam fora de ordem e detectar indicações perdidas.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-195">The sequence identifier for the indication enables a listener to identify duplicate indications when the service attempts to redeliver indications, reorder indications that arrive out of order, and detect lost indications.</span></span>

 

<span data-ttu-id="5fc5e-196">O número de sequência tem as seguintes características:</span><span class="sxs-lookup"><span data-stu-id="5fc5e-196">The sequence number has the following characteristics:</span></span>

-   <span data-ttu-id="5fc5e-197">O número de sequência é redefinido como "0" sempre que o valor de **SequenceContext** é alterado.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-197">The sequence number is reset to "0" whenever the **SequenceContext** value changes.</span></span>
-   <span data-ttu-id="5fc5e-198">Sempre que o destino do ouvinte receber uma nova indicação, o número de sequência será aumentado por "1".</span><span class="sxs-lookup"><span data-stu-id="5fc5e-198">Whenever the listener destination receives a new indication, the sequence number is increased by "1".</span></span>
-   <span data-ttu-id="5fc5e-199">O número de sequência é quebrado em "0" quando o intervalo de valores é excedido.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-199">The sequence number wraps to "0" when the value range is exceeded.</span></span>
-   <span data-ttu-id="5fc5e-200">Se a indicação for entregue novamente, **SequenceNumber** permanecerá o mesmo.</span><span class="sxs-lookup"><span data-stu-id="5fc5e-200">If the indication is redelivered, the **SequenceNumber** remains the same.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5fc5e-201">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5fc5e-201">Requirements</span></span>



| <span data-ttu-id="5fc5e-202">Requisito</span><span class="sxs-lookup"><span data-stu-id="5fc5e-202">Requirement</span></span> | <span data-ttu-id="5fc5e-203">Valor</span><span class="sxs-lookup"><span data-stu-id="5fc5e-203">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5fc5e-204">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc5e-204">Minimum supported client</span></span><br/> | <span data-ttu-id="5fc5e-205">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5fc5e-205">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5fc5e-206">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5fc5e-206">Minimum supported server</span></span><br/> | <span data-ttu-id="5fc5e-207">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5fc5e-207">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5fc5e-208">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fc5e-208">Namespace</span></span><br/>                | <span data-ttu-id="5fc5e-209">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="5fc5e-209">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5fc5e-210">MOF</span><span class="sxs-lookup"><span data-stu-id="5fc5e-210">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5fc5e-211"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5fc5e-211"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5fc5e-212">DLL</span><span class="sxs-lookup"><span data-stu-id="5fc5e-212">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fc5e-213"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5fc5e-213"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5fc5e-214">Confira também</span><span class="sxs-lookup"><span data-stu-id="5fc5e-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fc5e-215">**\_\_ExtrinsicEvent**</span><span class="sxs-lookup"><span data-stu-id="5fc5e-215">**\_\_ExtrinsicEvent**</span></span>](/windows/desktop/WmiSdk/--extrinsicevent)
</dt> </dl>

 

