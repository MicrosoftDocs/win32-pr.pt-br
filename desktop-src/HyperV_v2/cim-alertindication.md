---
description: Uma superclasse concreta para notificações de alerta do CIM.
ms.assetid: ec4cf41d-decd-4f21-b805-90db4a61376d
title: Classe CIM_AlertIndication
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlertIndication
- CIM_AlertIndication.Description
- CIM_AlertIndication.AlertingManagedElement
- CIM_AlertIndication.AlertingElementFormat
- CIM_AlertIndication.OtherAlertingElementFormat
- CIM_AlertIndication.AlertType
- CIM_AlertIndication.OtherAlertType
- CIM_AlertIndication.PerceivedSeverity
- CIM_AlertIndication.ProbableCause
- CIM_AlertIndication.ProbableCauseDescription
- CIM_AlertIndication.Trending
- CIM_AlertIndication.RecommendedActions
- CIM_AlertIndication.EventID
- CIM_AlertIndication.EventTime
- CIM_AlertIndication.SystemCreationClassName
- CIM_AlertIndication.SystemName
- CIM_AlertIndication.ProviderName
- CIM_AlertIndication.Message
- CIM_AlertIndication.MessageArguments
- CIM_AlertIndication.MessageID
- CIM_AlertIndication.OwningEntity
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1a1916705ee696c949dba2a557f7077ade8db7ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761724"
---
# <a name="cim_alertindication-class"></a><span data-ttu-id="67a5c-103">\_Classe CIM AlertIndication</span><span class="sxs-lookup"><span data-stu-id="67a5c-103">CIM\_AlertIndication class</span></span>

<span data-ttu-id="67a5c-104">Uma superclasse concreta para notificações de alerta do CIM.</span><span class="sxs-lookup"><span data-stu-id="67a5c-104">A concrete superclass for CIM alert notifications.</span></span> <span data-ttu-id="67a5c-105">**CIM \_ AlertIndication** é um tipo especializado de classe de **\_ indicação CIM** que contém informações sobre a gravidade, a causa, as ações recomendadas e outros dados para um evento do mundo real.</span><span class="sxs-lookup"><span data-stu-id="67a5c-105">**CIM\_AlertIndication** is a specialized type of **CIM\_Indication** class that contains information about the severity, cause, recommended actions, and other data for a real world event.</span></span> <span data-ttu-id="67a5c-106">Esse evento e seus dados podem ou não ser modelados na hierarquia de classes CIM.</span><span class="sxs-lookup"><span data-stu-id="67a5c-106">This event and its data may or may not be modeled in the CIM class hierarchy.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a5c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="67a5c-107">Syntax</span></span>

``` syntax
[Indication, Version("2.22.0"), UMLPackagePath("CIM::Event"), AMENDMENT]
class CIM_AlertIndication : CIM_ProcessIndication
{
  string   Description;
  string   AlertingManagedElement;
  uint16   AlertingElementFormat = 0;
  string   OtherAlertingElementFormat;
  uint16   AlertType;
  string   OtherAlertType;
  uint16   PerceivedSeverity;
  uint16   ProbableCause;
  string   ProbableCauseDescription;
  uint16   Trending;
  string   RecommendedActions[];
  string   EventID;
  datetime EventTime;
  string   SystemCreationClassName;
  string   SystemName;
  string   ProviderName;
  string   Message;
  string   MessageArguments[];
  string   MessageID;
  string   OwningEntity;
};
```

## <a name="members"></a><span data-ttu-id="67a5c-108">Membros</span><span class="sxs-lookup"><span data-stu-id="67a5c-108">Members</span></span>

<span data-ttu-id="67a5c-109">A classe **CIM \_ AlertIndication** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="67a5c-109">The **CIM\_AlertIndication** class has these types of members:</span></span>

-   [<span data-ttu-id="67a5c-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67a5c-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="67a5c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="67a5c-111">Properties</span></span>

<span data-ttu-id="67a5c-112">A classe **CIM \_ AlertIndication** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="67a5c-112">The **CIM\_AlertIndication** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="67a5c-113">**AlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="67a5c-113">**AlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67a5c-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-116">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingManagedElement**","**CIM \_ AlertIndication**.**OtherAlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingManagedElement**", "**CIM\_AlertIndication**.**OtherAlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-117">O formato da propriedade **AlertingManagedElement** .</span><span class="sxs-lookup"><span data-stu-id="67a5c-117">The format of the **AlertingManagedElement** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67a5c-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="67a5c-118"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-119">O formato é desconhecido ou não é de forma significativa interpretado por um aplicativo cliente CIM.</span><span class="sxs-lookup"><span data-stu-id="67a5c-119">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67a5c-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="67a5c-120"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-121">O formato é definido pelo valor da propriedade OtherAlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="67a5c-121">The format is defined by the value of the OtherAlertingElementFormat property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="67a5c-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="67a5c-122"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-123">O formato é um CIMObjectPath, especificando uma instância no esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="67a5c-123">The format is a CIMObjectPath, specifying an instance in the CIM Schema.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67a5c-124">**AlertingManagedElement**</span><span class="sxs-lookup"><span data-stu-id="67a5c-124">**AlertingManagedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-127">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-128">As informações de identificação da entidade (isto é, a instância) para as quais essa indicação é gerada.</span><span class="sxs-lookup"><span data-stu-id="67a5c-128">The identifying information of the entity (ie, the instance) for which this Indication is generated.</span></span> <span data-ttu-id="67a5c-129">A propriedade contém o caminho de uma instância, codificada como um parâmetro de cadeia de caracteres-se a instância for modelada no esquema CIM.</span><span class="sxs-lookup"><span data-stu-id="67a5c-129">The property contains the path of an instance, encoded as a string parameter - if the instance is modeled in the CIM Schema.</span></span> <span data-ttu-id="67a5c-130">Se não for uma instância CIM, a propriedade conterá uma cadeia de caracteres de identificação que nomeia a entidade para a qual o alerta é gerado.</span><span class="sxs-lookup"><span data-stu-id="67a5c-130">If not a CIM instance, the property contains some identifying string that names the entity for which the Alert is generated.</span></span> <span data-ttu-id="67a5c-131">O caminho ou a cadeia de caracteres de identificação é formatado de acordo com a propriedade AlertingElementFormat.</span><span class="sxs-lookup"><span data-stu-id="67a5c-131">The path or identifying string is formatted per the AlertingElementFormat property.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-132">**AlertType**</span><span class="sxs-lookup"><span data-stu-id="67a5c-132">**AlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-133">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67a5c-133">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-135">Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Tipo de evento ")</span><span class="sxs-lookup"><span data-stu-id="67a5c-135">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Event type")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-136">A classificação primária da indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-136">The primary classification of the indication.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67a5c-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="67a5c-137"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-138">\- Outros.</span><span class="sxs-lookup"><span data-stu-id="67a5c-138">\- Other.</span></span> <span data-ttu-id="67a5c-139">A propriedade OtherAlertType da indicação transmite sua classificação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-139">The Indication's OtherAlertType property conveys its classification.</span></span> <span data-ttu-id="67a5c-140">O uso de "other" em uma enumeração é uma convenção CIM padrão.</span><span class="sxs-lookup"><span data-stu-id="67a5c-140">Use of "Other" in an enumeration is a standard CIM convention.</span></span> <span data-ttu-id="67a5c-141">Isso significa que a indicação atual não se encaixa nas categorias descritas por essa enumeração.</span><span class="sxs-lookup"><span data-stu-id="67a5c-141">It means that the current Indication does not fit into the categories described by this enumeration.</span></span>

</dd> <dt>

<span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>

<span data-ttu-id="67a5c-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Alerta de comunicações** (2)</span><span class="sxs-lookup"><span data-stu-id="67a5c-142"><span id="Communications_Alert"></span><span id="communications_alert"></span><span id="COMMUNICATIONS_ALERT"></span>**Communications Alert** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-143">Uma indicação desse tipo está associada principalmente aos procedimentos e/ou processos necessários para transmitir informações de um ponto para outro.</span><span class="sxs-lookup"><span data-stu-id="67a5c-143">An Indication of this type is principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>

<span data-ttu-id="67a5c-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Alerta de qualidade de serviço** (3)</span><span class="sxs-lookup"><span data-stu-id="67a5c-144"><span id="Quality_of_Service_Alert"></span><span id="quality_of_service_alert"></span><span id="QUALITY_OF_SERVICE_ALERT"></span>**Quality of Service Alert** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-145">Uma indicação desse tipo está associada principalmente a uma degradação ou a erros no desempenho ou na função de uma entidade.</span><span class="sxs-lookup"><span data-stu-id="67a5c-145">An Indication of this type is principally associated with a degradation or errors in the performance or function of an entity.</span></span>

</dd> <dt>

<span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>

<span data-ttu-id="67a5c-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Erro de processamento** (4)</span><span class="sxs-lookup"><span data-stu-id="67a5c-146"><span id="Processing_Error"></span><span id="processing_error"></span><span id="PROCESSING_ERROR"></span>**Processing Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-147">Uma indicação desse tipo está associada principalmente a um software ou a uma falha de processamento.</span><span class="sxs-lookup"><span data-stu-id="67a5c-147">An Indication of this type is principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>

<span data-ttu-id="67a5c-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Alerta de dispositivo** (5)</span><span class="sxs-lookup"><span data-stu-id="67a5c-148"><span id="Device_Alert"></span><span id="device_alert"></span><span id="DEVICE_ALERT"></span>**Device Alert** (5)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-149">Uma indicação desse tipo está associada principalmente a um equipamento ou a uma falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="67a5c-149">An Indication of this type is principally associated with an equipment or hardware fault.</span></span>

</dd> <dt>

<span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>

<span data-ttu-id="67a5c-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Alerta ambiental** (6)</span><span class="sxs-lookup"><span data-stu-id="67a5c-150"><span id="Environmental_Alert"></span><span id="environmental_alert"></span><span id="ENVIRONMENTAL_ALERT"></span>**Environmental Alert** (6)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-151">Alerta ambiental.</span><span class="sxs-lookup"><span data-stu-id="67a5c-151">Environmental Alert.</span></span> <span data-ttu-id="67a5c-152">Uma indicação desse tipo está associada principalmente a uma condição relacionada a um compartimento no qual o hardware reside ou outras considerações ambientais.</span><span class="sxs-lookup"><span data-stu-id="67a5c-152">An Indication of this type is principally associated with a condition relating to an enclosure in which the hardware resides, or other environmental considerations.</span></span>

</dd> <dt>

<span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>

<span data-ttu-id="67a5c-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Alteração de modelo** (7)</span><span class="sxs-lookup"><span data-stu-id="67a5c-153"><span id="Model_Change"></span><span id="model_change"></span><span id="MODEL_CHANGE"></span>**Model Change** (7)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-154">A indicação aborda as alterações no modelo de informações.</span><span class="sxs-lookup"><span data-stu-id="67a5c-154">The Indication addresses changes in the Information Model.</span></span> <span data-ttu-id="67a5c-155">Por exemplo, ele pode inserir uma indicação de ciclo de vida para transmitir a alteração de modelo específica que está sendo alertada.</span><span class="sxs-lookup"><span data-stu-id="67a5c-155">For example, it may embed a Lifecycle Indication to convey the specific model change being alerted.</span></span>

</dd> <dt>

<span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>

<span data-ttu-id="67a5c-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Alerta de segurança** (8)</span><span class="sxs-lookup"><span data-stu-id="67a5c-156"><span id="Security_Alert"></span><span id="security_alert"></span><span id="SECURITY_ALERT"></span>**Security Alert** (8)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-157">.</span><span class="sxs-lookup"><span data-stu-id="67a5c-157">.</span></span> <span data-ttu-id="67a5c-158">Uma indicação desse tipo está associada.</span><span class="sxs-lookup"><span data-stu-id="67a5c-158">An Indication of this type is associated.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67a5c-159">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="67a5c-159">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-162">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Texto adicional ")</span><span class="sxs-lookup"><span data-stu-id="67a5c-162">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Additional text")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-163">Uma breve descrição da indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-163">A short description of the Indication.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-164">**EventID**</span><span class="sxs-lookup"><span data-stu-id="67a5c-164">**EventID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-165">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-166">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-167">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-167">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-168">Um valor específico de instrumentação ou provedor que descreve o evento do mundo real subjacente representado pela indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-168">An instrumentation or provider specific value that describes the underlying real-world event represented by the indication.</span></span> <span data-ttu-id="67a5c-169">As indicações com o mesmo valor de **EventID** não nulo são consideradas, pela entidade de criação, para representar o mesmo evento.</span><span class="sxs-lookup"><span data-stu-id="67a5c-169">Indications with the same non-NULL **EventID** value are considered, by the creating entity, to represent the same event.</span></span> <span data-ttu-id="67a5c-170">A comparação de dois valores de **EventID** só é definida para indicações de alerta com valores idênticos e não nulos das propriedades **SystemCreateClassName**, **SystemName** e **ProviderName** .</span><span class="sxs-lookup"><span data-stu-id="67a5c-170">The comparison of two **EventID** values is only defined for alert indications with identical, non-NULL values of **SystemCreateClassName**, **SystemName** and **ProviderName** properties.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-171">**EventTime**</span><span class="sxs-lookup"><span data-stu-id="67a5c-171">**EventTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-172">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="67a5c-172">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-174">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-174">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-175">A hora e a data que indicam quando o evento subjacente foi detectado pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="67a5c-175">The time and date that indicates when the underlying event was first detected.</span></span> <span data-ttu-id="67a5c-176">Se esses valores forem especificados e a entidade de criação não for capaz de fornecer essas informações, essa propriedade deverá ser definida como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="67a5c-176">If this values is specified and the creating entity is not capable of providing this information, this property must be set to **NULL**.</span></span> <span data-ttu-id="67a5c-177">Esse valor se baseia na noção da data e hora local do objeto **CIM \_ ManageSystemElement** que gerou a indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-177">This value is based on the notion of the local date and time of the **CIM\_ManageSystemElement** object that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-178">**Message**</span><span class="sxs-lookup"><span data-stu-id="67a5c-178">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-179">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-179">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-181">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**MessageID**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-181">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**MessageID**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-182">A mensagem formatada para a indicação de alerta.</span><span class="sxs-lookup"><span data-stu-id="67a5c-182">The formatted message for the alert indication.</span></span> <span data-ttu-id="67a5c-183">Essa mensagem é formatada pela combinação de um ou mais elementos dinâmicos especificados na propriedade **MessageArguments** e com os elementos estáticos identificados exclusivamente pela propriedade **MessageId** .</span><span class="sxs-lookup"><span data-stu-id="67a5c-183">This message is formatted by combining one or more of the dynamic elements specified in the **MessageArguments** property, and with the static elements uniquely identified by the **MessageID** property.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-184">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="67a5c-184">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-185">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-185">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-187">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Message**","**CIM \_ AlertIndication**.**MessageID**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-187">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageID**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-188">Uma matriz que contém o conteúdo dinâmico da mensagem para a indicação de alerta.</span><span class="sxs-lookup"><span data-stu-id="67a5c-188">An array that contains the dynamic content of the message for the alert indication.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-189">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="67a5c-189">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-190">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-191">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-192">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**Message**","**CIM \_ AlertIndication**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-192">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**Message**", "**CIM\_AlertIndication**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-193">A ID exclusiva do formato de mensagem, com o escopo da organização especificado em **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="67a5c-193">The unique ID of the message format, withing the scope of the organization specified in **OwningEntity**.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-194">**OtherAlertingElementFormat**</span><span class="sxs-lookup"><span data-stu-id="67a5c-194">**OtherAlertingElementFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-195">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-195">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-196">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-196">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-197">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertingElementFormat**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-197">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertingElementFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-198">Define o formato da propriedade **AlertingManagedElement** quando a propriedade **AlertingElementFormat** é definida como "1" (outra); caso contrário, esse valor deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="67a5c-198">Defines the format of the **AlertingManagedElement** property when the **AlertingElementFormat** property is set to "1" (other); otherwise, this value must be set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-199">**OtherAlertType**</span><span class="sxs-lookup"><span data-stu-id="67a5c-199">**OtherAlertType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-200">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-200">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-201">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-201">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-202">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**AlertType**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-202">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**AlertType**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-203">Uma cadeia de caracteres que descreve o valor **AlertType** quando a propriedade **AlertType** é definida como "1" (outra alteração de estado).</span><span class="sxs-lookup"><span data-stu-id="67a5c-203">A string that describes the **AlertType** value when the **AlertType** property is set to "1" (Other State Change).</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-204">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="67a5c-204">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-205">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-205">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-206">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-206">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-207">A ID exclusiva da organização que possui a definição do formato da propriedade de **mensagem** .</span><span class="sxs-lookup"><span data-stu-id="67a5c-207">The unique ID of the organization that owns the definition of the format of the **Message** property.</span></span> <span data-ttu-id="67a5c-208">**OwningEntity** deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios ou ao corpo de padrões que definiu o formato da mensagem.</span><span class="sxs-lookup"><span data-stu-id="67a5c-208">**OwningEntity** must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-209">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="67a5c-209">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-210">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67a5c-210">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-211">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-211">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-212">Qualificadores: [**obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MAPPINGSTRINGS**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Severidade percebida ")</span><span class="sxs-lookup"><span data-stu-id="67a5c-212">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PerceivedSeverity"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-213">A severidade da indicação de alerta do ponto de vista do elemento que gerou o alerta.</span><span class="sxs-lookup"><span data-stu-id="67a5c-213">The severity of the alert indication from the point of view of the element that raised the alert.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67a5c-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="67a5c-214"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-215">Segue o uso comum.</span><span class="sxs-lookup"><span data-stu-id="67a5c-215">Follows common usage.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67a5c-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="67a5c-216"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-217">Indica que o valor da severidade pode ser encontrado na propriedade OtherSeverity.</span><span class="sxs-lookup"><span data-stu-id="67a5c-217">Indicates that the Severity's value can be found in the OtherSeverity property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="67a5c-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)</span><span class="sxs-lookup"><span data-stu-id="67a5c-218"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-219">Segue o uso comum.</span><span class="sxs-lookup"><span data-stu-id="67a5c-219">Follows common usage.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="67a5c-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/aviso** (3)</span><span class="sxs-lookup"><span data-stu-id="67a5c-220"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-221">Deve ser usado quando apropriado para permitir que o usuário decida se a ação é necessária.</span><span class="sxs-lookup"><span data-stu-id="67a5c-221">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="67a5c-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundária** (4)</span><span class="sxs-lookup"><span data-stu-id="67a5c-222"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-223">Indica que a ação é necessária, mas a situação não é séria no momento.</span><span class="sxs-lookup"><span data-stu-id="67a5c-223">Indicates action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="67a5c-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="67a5c-224"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-225">Indica que a ação é necessária agora.</span><span class="sxs-lookup"><span data-stu-id="67a5c-225">Indicates action is needed now.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="67a5c-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)</span><span class="sxs-lookup"><span data-stu-id="67a5c-226"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-227">A ação é necessária agora e o escopo é amplo (talvez uma interrupção iminente a um recurso crítico resulte).</span><span class="sxs-lookup"><span data-stu-id="67a5c-227">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="67a5c-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="67a5c-228"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="67a5c-229">Indica que ocorreu um erro, mas é tarde demais para realizar uma ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="67a5c-229">Indicates an error occurred, but it's too late to take remedial action.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="67a5c-230">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="67a5c-230">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-231">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67a5c-231">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-232">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-233">Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Causa provável "," recomendação. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCauseDescription**","**CIM \_ AlertIndication**.**EventID**","**CIM \_ AlertIndication**.**EventTime**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-233">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCauseDescription**", "**CIM\_AlertIndication**.**EventID**", "**CIM\_AlertIndication**.**EventTime**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-234">A causa provável da situação que resultou na indicação do alerta.</span><span class="sxs-lookup"><span data-stu-id="67a5c-234">The probable cause of the situation which resulted in the alert indication.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67a5c-235">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="67a5c-235">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="67a5c-236">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="67a5c-236">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="67a5c-237">**Erro de adaptador/placa** (2)</span><span class="sxs-lookup"><span data-stu-id="67a5c-237">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="67a5c-238">**Falha no subsistema do aplicativo** (3)</span><span class="sxs-lookup"><span data-stu-id="67a5c-238">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="67a5c-239">**Largura de banda reduzida** (4)</span><span class="sxs-lookup"><span data-stu-id="67a5c-239">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="67a5c-240">**Erro de estabelecimento de conexão** (5)</span><span class="sxs-lookup"><span data-stu-id="67a5c-240">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="67a5c-241">**Erro de protocolo de comunicação** (6)</span><span class="sxs-lookup"><span data-stu-id="67a5c-241">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="67a5c-242">**Falha no subsistema de comunicações** (7)</span><span class="sxs-lookup"><span data-stu-id="67a5c-242">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="67a5c-243">**Erro de configuração/personalização** (8)</span><span class="sxs-lookup"><span data-stu-id="67a5c-243">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="67a5c-244">**Congestionamento** (9)</span><span class="sxs-lookup"><span data-stu-id="67a5c-244">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="67a5c-245">**Dados corrompidos** (10)</span><span class="sxs-lookup"><span data-stu-id="67a5c-245">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="67a5c-246">**Limite de ciclos de CPU excedido** (11)</span><span class="sxs-lookup"><span data-stu-id="67a5c-246">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="67a5c-247">**Erro de conjunto de/DataSet** (12)</span><span class="sxs-lookup"><span data-stu-id="67a5c-247">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="67a5c-248">**Sinal degradado** (13)</span><span class="sxs-lookup"><span data-stu-id="67a5c-248">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="67a5c-249">**DTE-erro de interface de DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="67a5c-249">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="67a5c-250">**Porta do compartimento aberta** (15)</span><span class="sxs-lookup"><span data-stu-id="67a5c-250">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="67a5c-251">**Mau funcionamento do equipamento** (16)</span><span class="sxs-lookup"><span data-stu-id="67a5c-251">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="67a5c-252">**Vibração excessiva** (17)</span><span class="sxs-lookup"><span data-stu-id="67a5c-252">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="67a5c-253">**Erro de formato de arquivo** (18)</span><span class="sxs-lookup"><span data-stu-id="67a5c-253">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="67a5c-254">**Incêndio detectado** (19)</span><span class="sxs-lookup"><span data-stu-id="67a5c-254">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="67a5c-255">**Inundação detectada** (20)</span><span class="sxs-lookup"><span data-stu-id="67a5c-255">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="67a5c-256">**Erro de enquadramento** (21)</span><span class="sxs-lookup"><span data-stu-id="67a5c-256">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="67a5c-257">**Problema de HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="67a5c-257">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="67a5c-258">**Umidade inaceitável** (23)</span><span class="sxs-lookup"><span data-stu-id="67a5c-258">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="67a5c-259">**Erro de dispositivo de e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="67a5c-259">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="67a5c-260">**Erro de dispositivo de entrada** (25)</span><span class="sxs-lookup"><span data-stu-id="67a5c-260">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="67a5c-261">**Erro de LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="67a5c-261">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="67a5c-262">**Vazamento não tóxicos detectado** (27)</span><span class="sxs-lookup"><span data-stu-id="67a5c-262">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="67a5c-263">**Erro de transmissão do nó local** (28)</span><span class="sxs-lookup"><span data-stu-id="67a5c-263">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="67a5c-264">**Perda de quadro** (29)</span><span class="sxs-lookup"><span data-stu-id="67a5c-264">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="67a5c-265">**Perda de sinal** (30)</span><span class="sxs-lookup"><span data-stu-id="67a5c-265">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="67a5c-266">**Fornecimento de material esgotado** (31)</span><span class="sxs-lookup"><span data-stu-id="67a5c-266">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="67a5c-267">**Problema do Multiplexador** (32)</span><span class="sxs-lookup"><span data-stu-id="67a5c-267">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="67a5c-268">**Memória insuficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="67a5c-268">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="67a5c-269">**Erro do dispositivo de saída** (34)</span><span class="sxs-lookup"><span data-stu-id="67a5c-269">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="67a5c-270">**Desempenho degradado** (35)</span><span class="sxs-lookup"><span data-stu-id="67a5c-270">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="67a5c-271">**Problema de energia** (36)</span><span class="sxs-lookup"><span data-stu-id="67a5c-271">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="67a5c-272">**Pressão inaceitável** (37)</span><span class="sxs-lookup"><span data-stu-id="67a5c-272">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="67a5c-273">**Problema do processador (erro interno da máquina)** (38)</span><span class="sxs-lookup"><span data-stu-id="67a5c-273">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="67a5c-274">**Falha de bomba** (39)</span><span class="sxs-lookup"><span data-stu-id="67a5c-274">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="67a5c-275">**Tamanho da fila excedido** (40)</span><span class="sxs-lookup"><span data-stu-id="67a5c-275">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="67a5c-276">**Falha de recebimento** (41)</span><span class="sxs-lookup"><span data-stu-id="67a5c-276">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="67a5c-277">**Falha do receptor** (42)</span><span class="sxs-lookup"><span data-stu-id="67a5c-277">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="67a5c-278">**Erro de transmissão de nó remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="67a5c-278">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="67a5c-279">**Recurso na capacidade ou perto** (44)</span><span class="sxs-lookup"><span data-stu-id="67a5c-279">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="67a5c-280">**Tempo de resposta excessivo** (45)</span><span class="sxs-lookup"><span data-stu-id="67a5c-280">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="67a5c-281">**Taxa de retransmissão excessiva** (46)</span><span class="sxs-lookup"><span data-stu-id="67a5c-281">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="67a5c-282">**Erro de software** (47)</span><span class="sxs-lookup"><span data-stu-id="67a5c-282">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="67a5c-283">**Programa de software encerrado** de forma anormal (48)</span><span class="sxs-lookup"><span data-stu-id="67a5c-283">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="67a5c-284">**Erro do programa de software (resultados incorretos)** (49)</span><span class="sxs-lookup"><span data-stu-id="67a5c-284">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="67a5c-285">**Problema de capacidade de armazenamento** (50)</span><span class="sxs-lookup"><span data-stu-id="67a5c-285">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="67a5c-286">**Temperatura inaceitável** (51)</span><span class="sxs-lookup"><span data-stu-id="67a5c-286">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="67a5c-287">**Limite ultrapassado** (52)</span><span class="sxs-lookup"><span data-stu-id="67a5c-287">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="67a5c-288">**Problema de tempo** (53)</span><span class="sxs-lookup"><span data-stu-id="67a5c-288">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="67a5c-289">**Vazamento de tóxicos detectado** (54)</span><span class="sxs-lookup"><span data-stu-id="67a5c-289">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="67a5c-290">**Falha de transmissão** (55)</span><span class="sxs-lookup"><span data-stu-id="67a5c-290">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="67a5c-291">**Falha do transmissor** (56)</span><span class="sxs-lookup"><span data-stu-id="67a5c-291">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="67a5c-292">**Recurso subjacente não disponível** (57)</span><span class="sxs-lookup"><span data-stu-id="67a5c-292">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_MisMatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="67a5c-293">**Incompatibilidade de versão** (58)</span><span class="sxs-lookup"><span data-stu-id="67a5c-293">**Version MisMatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="67a5c-294">**Alerta anterior limpo** (59)</span><span class="sxs-lookup"><span data-stu-id="67a5c-294">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="67a5c-295">**Tentativas de logon com falha** (60)</span><span class="sxs-lookup"><span data-stu-id="67a5c-295">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="67a5c-296">**Vírus de software detectado** (61)</span><span class="sxs-lookup"><span data-stu-id="67a5c-296">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="67a5c-297">**Segurança de hardware violada** (62)</span><span class="sxs-lookup"><span data-stu-id="67a5c-297">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="67a5c-298">**Negação de serviço detectada** (63)</span><span class="sxs-lookup"><span data-stu-id="67a5c-298">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_MisMatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="67a5c-299">**Incompatibilidade de credencial de segurança** (64)</span><span class="sxs-lookup"><span data-stu-id="67a5c-299">**Security Credential MisMatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="67a5c-300">**Acesso não autorizado** (65)</span><span class="sxs-lookup"><span data-stu-id="67a5c-300">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="67a5c-301">**Alarme recebido** (66)</span><span class="sxs-lookup"><span data-stu-id="67a5c-301">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="67a5c-302">**Perda de ponteiro** (67)</span><span class="sxs-lookup"><span data-stu-id="67a5c-302">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="67a5c-303">**Incompatibilidade de carga** (68)</span><span class="sxs-lookup"><span data-stu-id="67a5c-303">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="67a5c-304">**Erro de transmissão** (69)</span><span class="sxs-lookup"><span data-stu-id="67a5c-304">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="67a5c-305">**Taxa de erros excessivas** (70)</span><span class="sxs-lookup"><span data-stu-id="67a5c-305">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="67a5c-306">**Problema de rastreamento** (71)</span><span class="sxs-lookup"><span data-stu-id="67a5c-306">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="67a5c-307">**Elemento não disponível** (72)</span><span class="sxs-lookup"><span data-stu-id="67a5c-307">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="67a5c-308">**Elemento ausente** (73)</span><span class="sxs-lookup"><span data-stu-id="67a5c-308">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="67a5c-309">**Perda de vários quadros** (74)</span><span class="sxs-lookup"><span data-stu-id="67a5c-309">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="67a5c-310">**Falha no canal de difusão** (75)</span><span class="sxs-lookup"><span data-stu-id="67a5c-310">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="67a5c-311">**Mensagem inválida recebida** (76)</span><span class="sxs-lookup"><span data-stu-id="67a5c-311">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="67a5c-312">**Falha de roteamento** (77)</span><span class="sxs-lookup"><span data-stu-id="67a5c-312">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="67a5c-313">**Falha no backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="67a5c-313">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="67a5c-314">**Duplicação de identificador** (79)</span><span class="sxs-lookup"><span data-stu-id="67a5c-314">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="67a5c-315">**Falha no caminho de proteção** (80)</span><span class="sxs-lookup"><span data-stu-id="67a5c-315">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="67a5c-316">**Perda de sincronização ou incompatibilidade** (81)</span><span class="sxs-lookup"><span data-stu-id="67a5c-316">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="67a5c-317">**Problema de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="67a5c-317">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="67a5c-318">**Falha no relógio em tempo real** (83)</span><span class="sxs-lookup"><span data-stu-id="67a5c-318">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="67a5c-319">**Falha de antena** (84)</span><span class="sxs-lookup"><span data-stu-id="67a5c-319">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="67a5c-320">**Falha no carregamento da bateria** (85)</span><span class="sxs-lookup"><span data-stu-id="67a5c-320">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="67a5c-321">**Falha de disco** (86)</span><span class="sxs-lookup"><span data-stu-id="67a5c-321">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="67a5c-322">**Falha de salto de frequência** (87)</span><span class="sxs-lookup"><span data-stu-id="67a5c-322">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="67a5c-323">**Perda de redundância** (88)</span><span class="sxs-lookup"><span data-stu-id="67a5c-323">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="67a5c-324">**Falha da fonte de energia** (89)</span><span class="sxs-lookup"><span data-stu-id="67a5c-324">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="67a5c-325">**Problema de qualidade de sinal** (90)</span><span class="sxs-lookup"><span data-stu-id="67a5c-325">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="67a5c-326">**Descarregamento da bateria** (91)</span><span class="sxs-lookup"><span data-stu-id="67a5c-326">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="67a5c-327">**Falha da bateria** (92)</span><span class="sxs-lookup"><span data-stu-id="67a5c-327">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="67a5c-328">**Problema de energia comercial** (93)</span><span class="sxs-lookup"><span data-stu-id="67a5c-328">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="67a5c-329">**Falha do ventilador** (94)</span><span class="sxs-lookup"><span data-stu-id="67a5c-329">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="67a5c-330">**Falha do mecanismo** (95)</span><span class="sxs-lookup"><span data-stu-id="67a5c-330">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="67a5c-331">**Falha do sensor** (96)</span><span class="sxs-lookup"><span data-stu-id="67a5c-331">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="67a5c-332">**Falha de fusível** (97)</span><span class="sxs-lookup"><span data-stu-id="67a5c-332">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="67a5c-333">**Falha do gerador** (98)</span><span class="sxs-lookup"><span data-stu-id="67a5c-333">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="67a5c-334">**Bateria fraca** (99)</span><span class="sxs-lookup"><span data-stu-id="67a5c-334">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="67a5c-335">**Baixo combustível** (100)</span><span class="sxs-lookup"><span data-stu-id="67a5c-335">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="67a5c-336">**Água inferior** (101)</span><span class="sxs-lookup"><span data-stu-id="67a5c-336">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="67a5c-337">**Gás explosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="67a5c-337">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="67a5c-338">**Altos ventos** (103)</span><span class="sxs-lookup"><span data-stu-id="67a5c-338">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="67a5c-339">**Acúmulo de gelo** (104)</span><span class="sxs-lookup"><span data-stu-id="67a5c-339">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="67a5c-340">**Fumaça** (105)</span><span class="sxs-lookup"><span data-stu-id="67a5c-340">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="67a5c-341">**Incompatibilidade de memória** (106)</span><span class="sxs-lookup"><span data-stu-id="67a5c-341">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="67a5c-342">**Ciclos de CPU insuficientes** (107)</span><span class="sxs-lookup"><span data-stu-id="67a5c-342">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="67a5c-343">**Problema de ambiente de software** (108)</span><span class="sxs-lookup"><span data-stu-id="67a5c-343">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="67a5c-344">**Falha de download de software** (109)</span><span class="sxs-lookup"><span data-stu-id="67a5c-344">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="67a5c-345">**Elemento reinicializado** (110)</span><span class="sxs-lookup"><span data-stu-id="67a5c-345">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="67a5c-346">**Tempo limite** (111)</span><span class="sxs-lookup"><span data-stu-id="67a5c-346">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="67a5c-347">**Problemas de log** (112)</span><span class="sxs-lookup"><span data-stu-id="67a5c-347">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="67a5c-348">**Vazamento detectado** (113)</span><span class="sxs-lookup"><span data-stu-id="67a5c-348">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="67a5c-349">**Falha no mecanismo de proteção** (114)</span><span class="sxs-lookup"><span data-stu-id="67a5c-349">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="67a5c-350">**Proteção de falha de recurso** (115)</span><span class="sxs-lookup"><span data-stu-id="67a5c-350">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="67a5c-351">**Inconsistência do banco de dados** (116)</span><span class="sxs-lookup"><span data-stu-id="67a5c-351">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="67a5c-352">**Falha de autenticação** (117)</span><span class="sxs-lookup"><span data-stu-id="67a5c-352">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="67a5c-353">**Violação de confidencialidade** (118)</span><span class="sxs-lookup"><span data-stu-id="67a5c-353">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="67a5c-354">**Adulteração de cabo** (119)</span><span class="sxs-lookup"><span data-stu-id="67a5c-354">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="67a5c-355">**Informações atrasadas** (120)</span><span class="sxs-lookup"><span data-stu-id="67a5c-355">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="67a5c-356">**Informações duplicadas** (121)</span><span class="sxs-lookup"><span data-stu-id="67a5c-356">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="67a5c-357">**Informações ausentes** (122)</span><span class="sxs-lookup"><span data-stu-id="67a5c-357">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="67a5c-358">**Modificação de informações** (123)</span><span class="sxs-lookup"><span data-stu-id="67a5c-358">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="67a5c-359">**Informações fora de sequência** (124)</span><span class="sxs-lookup"><span data-stu-id="67a5c-359">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="67a5c-360">**Chave expirada** (125)</span><span class="sxs-lookup"><span data-stu-id="67a5c-360">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="67a5c-361">**Falha de não repúdio** (126)</span><span class="sxs-lookup"><span data-stu-id="67a5c-361">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="67a5c-362">**Atividade fora de horas** (127)</span><span class="sxs-lookup"><span data-stu-id="67a5c-362">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="67a5c-363">**Fora de serviço** (128)</span><span class="sxs-lookup"><span data-stu-id="67a5c-363">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="67a5c-364">**Erro de procedimento** (129)</span><span class="sxs-lookup"><span data-stu-id="67a5c-364">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="67a5c-365">**Informações inesperadas** (130)</span><span class="sxs-lookup"><span data-stu-id="67a5c-365">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="67a5c-366">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="67a5c-366">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-367">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-367">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-368">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-368">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-369">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AlertIndication**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="67a5c-369">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_AlertIndication**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-370">Informações adicionais relacionadas à propriedade **ProbableCause** .</span><span class="sxs-lookup"><span data-stu-id="67a5c-370">Additional information related to the **ProbableCause** property.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-371">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="67a5c-371">**ProviderName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-372">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-372">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-373">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-373">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-374">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67a5c-374">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-375">O nome do provedor que gerou a indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-375">The name of the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-376">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="67a5c-376">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-377">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-377">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-378">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-378">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-379">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Ações de reparo propostas ")</span><span class="sxs-lookup"><span data-stu-id="67a5c-379">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Proposed repair actions")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-380">Descrições de forma livre das ações recomendadas a serem executadas para resolver a causa da notificação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-380">Free form descriptions of the recommended actions to take to resolve the cause of the notification.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-381">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="67a5c-381">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-382">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-382">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-383">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-383">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-384">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67a5c-384">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-385">O valor de **CreationClassName** do sistema de escopo para o provedor que gerou a indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-385">The **CreationClassName** value of the scoping system for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-386">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="67a5c-386">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-387">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="67a5c-387">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-388">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-388">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-389">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="67a5c-389">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-390">O nome do sistema de escopo para o provedor que gerou a indicação.</span><span class="sxs-lookup"><span data-stu-id="67a5c-390">The scoping system name for the provider that generated the indication.</span></span>

</dd> <dt>

<span data-ttu-id="67a5c-391">**Mais populares**</span><span class="sxs-lookup"><span data-stu-id="67a5c-391">**Trending**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="67a5c-392">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="67a5c-392">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-393">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="67a5c-393">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="67a5c-394">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. TrendIndication")</span><span class="sxs-lookup"><span data-stu-id="67a5c-394">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.TrendIndication")</span></span>
</dt> </dl>

<span data-ttu-id="67a5c-395">Fornece informações sobre tendências – tendência verticalmente ou nenhuma alteração.</span><span class="sxs-lookup"><span data-stu-id="67a5c-395">Provides information on trending - trending up, down or no change.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="67a5c-396">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="67a5c-396">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="67a5c-397">**Não aplicável** (1)</span><span class="sxs-lookup"><span data-stu-id="67a5c-397">**Not Applicable** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Up"></span><span id="trending_up"></span><span id="TRENDING_UP"></span>

<span data-ttu-id="67a5c-398">**Tendência** vertical (2)</span><span class="sxs-lookup"><span data-stu-id="67a5c-398">**Trending Up** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Trending_Down"></span><span id="trending_down"></span><span id="TRENDING_DOWN"></span>

<span data-ttu-id="67a5c-399">**Tendência para baixo** (3)</span><span class="sxs-lookup"><span data-stu-id="67a5c-399">**Trending Down** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="No_Change"></span><span id="no_change"></span><span id="NO_CHANGE"></span>

<span data-ttu-id="67a5c-400">**Nenhuma alteração** (4)</span><span class="sxs-lookup"><span data-stu-id="67a5c-400">**No Change** (4)</span></span>


<span data-ttu-id="67a5c-401"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="67a5c-401"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="67a5c-402">Requisitos</span><span class="sxs-lookup"><span data-stu-id="67a5c-402">Requirements</span></span>



| <span data-ttu-id="67a5c-403">Requisito</span><span class="sxs-lookup"><span data-stu-id="67a5c-403">Requirement</span></span> | <span data-ttu-id="67a5c-404">Valor</span><span class="sxs-lookup"><span data-stu-id="67a5c-404">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5c-405">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67a5c-405">Minimum supported client</span></span><br/> | <span data-ttu-id="67a5c-406">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="67a5c-406">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="67a5c-407">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="67a5c-407">Minimum supported server</span></span><br/> | <span data-ttu-id="67a5c-408">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="67a5c-408">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="67a5c-409">Namespace</span><span class="sxs-lookup"><span data-stu-id="67a5c-409">Namespace</span></span><br/>                | <span data-ttu-id="67a5c-410">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="67a5c-410">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="67a5c-411">MOF</span><span class="sxs-lookup"><span data-stu-id="67a5c-411">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67a5c-412"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-412"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="67a5c-413">DLL</span><span class="sxs-lookup"><span data-stu-id="67a5c-413">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67a5c-414"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-414"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="67a5c-415">Confira também</span><span class="sxs-lookup"><span data-stu-id="67a5c-415">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a5c-416">**\_PROCESSINDICATION CIM**</span><span class="sxs-lookup"><span data-stu-id="67a5c-416">**CIM\_ProcessIndication**</span></span>](cim-processindication.md)
</dt> </dl>

 

