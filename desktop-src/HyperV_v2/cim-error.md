---
description: A \_ classe de erro CIM contém informações sobre a falha de uma operação CIM.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: Classe CIM_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Error
- CIM_Error.ErrorType
- CIM_Error.OtherErrorType
- CIM_Error.OwningEntity
- CIM_Error.MessageID
- CIM_Error.Message
- CIM_Error.MessageArguments
- CIM_Error.PerceivedSeverity
- CIM_Error.ProbableCause
- CIM_Error.ProbableCauseDescription
- CIM_Error.RecommendedActions
- CIM_Error.ErrorSource
- CIM_Error.ErrorSourceFormat
- CIM_Error.OtherErrorSourceFormat
- CIM_Error.CIMStatusCode
- CIM_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 59ae2527478235c14a8f856319178afe00c02a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296178"
---
# <a name="cim_error-class"></a><span data-ttu-id="d4af6-103">\_Classe de erro CIM</span><span class="sxs-lookup"><span data-stu-id="d4af6-103">CIM\_Error class</span></span>

<span data-ttu-id="d4af6-104">A classe de **\_ erro CIM** contém informações sobre a falha de uma operação CIM.</span><span class="sxs-lookup"><span data-stu-id="d4af6-104">The **CIM\_Error** class contains information about the failure of a CIM operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4af6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d4af6-105">Syntax</span></span>

``` syntax
[Indication, Abstract, Version("2.22.1"), Exception, UMLPackagePath("CIM::Interop"), AMENDMENT]
class CIM_Error
{
  uint16 ErrorType;
  string OtherErrorType;
  string OwningEntity;
  string MessageID;
  string Message;
  string MessageArguments[];
  uint16 PerceivedSeverity;
  uint16 ProbableCause;
  string ProbableCauseDescription;
  string RecommendedActions[];
  string ErrorSource;
  uint16 ErrorSourceFormat = 0;
  string OtherErrorSourceFormat;
  uint32 CIMStatusCode;
  string CIMStatusCodeDescription;
};
```

## <a name="members"></a><span data-ttu-id="d4af6-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d4af6-106">Members</span></span>

<span data-ttu-id="d4af6-107">A classe de **\_ erro CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d4af6-107">The **CIM\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="d4af6-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d4af6-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d4af6-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d4af6-109">Properties</span></span>

<span data-ttu-id="d4af6-110">A classe de **\_ erro CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d4af6-110">The **CIM\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d4af6-111">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="d4af6-111">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-112">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d4af6-112">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-114">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. erro de DMTF \| . CÓDIGO \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro CIM**.**CIMStatusCodeDescription**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-114">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.CODE\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCodeDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-115">O código de status CIM que caracteriza essa instância.</span><span class="sxs-lookup"><span data-stu-id="d4af6-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="d4af6-116">Essa propriedade define os códigos de status que podem ser retornados por um servidor CIM ou um ouvinte.</span><span class="sxs-lookup"><span data-stu-id="d4af6-116">This property defines the status codes that can be return by a CIM server or listener.</span></span>

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span data-ttu-id="d4af6-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ \_Falha de erro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4af6-117"><span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM\_ERR\_FAILED** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-118">Ocorreu um erro geral que não é coberto por um código de erro mais específico.</span><span class="sxs-lookup"><span data-stu-id="d4af6-118">A general error occurred that is not covered by a more specific error code.</span></span>

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span data-ttu-id="d4af6-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ ERRO de \_ acesso \_ negado** (2)</span><span class="sxs-lookup"><span data-stu-id="d4af6-119"><span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM\_ERR\_ACCESS\_DENIED** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-120">O acesso a um recurso CIM não estava disponível para o cliente.</span><span class="sxs-lookup"><span data-stu-id="d4af6-120">Access to a CIM resource was not available to the client.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span data-ttu-id="d4af6-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ ERRO \_ de \_ namespace inválido** (3)</span><span class="sxs-lookup"><span data-stu-id="d4af6-121"><span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM\_ERR\_INVALID\_NAMESPACE** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-122">O namespace de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="d4af6-122">The target namespace does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span data-ttu-id="d4af6-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ ERRO \_ de \_ parâmetro inválido** (4)</span><span class="sxs-lookup"><span data-stu-id="d4af6-123"><span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM\_ERR\_INVALID\_PARAMETER** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-124">Um ou mais valores de parâmetro passados para o método eram inválidos.</span><span class="sxs-lookup"><span data-stu-id="d4af6-124">One or more parameter values passed to the method were invalid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span data-ttu-id="d4af6-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ \_ \_ Classe inválida de Err** (5)</span><span class="sxs-lookup"><span data-stu-id="d4af6-125"><span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM\_ERR\_INVALID\_CLASS** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-126">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="d4af6-126">The specified Class does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span data-ttu-id="d4af6-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ ERRO \_ não \_ encontrado** (6)</span><span class="sxs-lookup"><span data-stu-id="d4af6-127"><span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM\_ERR\_NOT\_FOUND** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-128">O objeto solicitado não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="d4af6-128">The requested object could not be found.</span></span>

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span data-ttu-id="d4af6-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ \_Não \_ há suporte para erro** (7)</span><span class="sxs-lookup"><span data-stu-id="d4af6-129"><span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM\_ERR\_NOT\_SUPPORTED** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-130">Não há suporte para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="d4af6-130">The requested operation is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span data-ttu-id="d4af6-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ A \_ classe Err \_ tem \_ filhos** (8)</span><span class="sxs-lookup"><span data-stu-id="d4af6-131"><span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM\_ERR\_CLASS\_HAS\_CHILDREN** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-132">A operação não pode ser executada nesta classe porque ela tem instâncias.</span><span class="sxs-lookup"><span data-stu-id="d4af6-132">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span data-ttu-id="d4af6-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ \_Classe Err \_ tem \_ instâncias** (9)</span><span class="sxs-lookup"><span data-stu-id="d4af6-133"><span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM\_ERR\_CLASS\_HAS\_INSTANCES** (9)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-134">A operação não pode ser executada nesta classe porque ela tem instâncias.</span><span class="sxs-lookup"><span data-stu-id="d4af6-134">Operation cannot be carried out on this class since it has instances.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span data-ttu-id="d4af6-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ Inclasse de erro \_ inválido \_** (10)</span><span class="sxs-lookup"><span data-stu-id="d4af6-135"><span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM\_ERR\_INVALID\_SUPERCLASS** (10)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-136">A operação não pode ser executada porque a superclasse especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="d4af6-136">Operation cannot be carried out since the specified superclass does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span data-ttu-id="d4af6-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ O erro \_ já \_ existe** (11)</span><span class="sxs-lookup"><span data-stu-id="d4af6-137"><span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM\_ERR\_ALREADY\_EXISTS** (11)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-138">A operação não pode ser executada porque já existe um objeto.</span><span class="sxs-lookup"><span data-stu-id="d4af6-138">Operation cannot be carried out because an object already exists.</span></span>

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span data-ttu-id="d4af6-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ \_Não erro \_ de \_ Propriedade** (12)</span><span class="sxs-lookup"><span data-stu-id="d4af6-139"><span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM\_ERR\_NO\_SUCH\_PROPERTY** (12)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-140">A propriedade especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="d4af6-140">The specified Property does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span data-ttu-id="d4af6-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ Tipo de erro \_ \_ incompatível** (13)</span><span class="sxs-lookup"><span data-stu-id="d4af6-141"><span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM\_ERR\_TYPE\_MISMATCH** (13)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-142">O valor fornecido é incompatível com o tipo.</span><span class="sxs-lookup"><span data-stu-id="d4af6-142">The value supplied is incompatible with the type.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span data-ttu-id="d4af6-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ Linguagem de consulta de erro \_ \_ \_ sem \_ suporte** (14)</span><span class="sxs-lookup"><span data-stu-id="d4af6-143"><span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED** (14)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-144">A linguagem de consulta não é reconhecida nem tem suporte.</span><span class="sxs-lookup"><span data-stu-id="d4af6-144">The query language is not recognized or supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span data-ttu-id="d4af6-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ ERRO \_ de \_ consulta inválida** (15)</span><span class="sxs-lookup"><span data-stu-id="d4af6-145"><span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM\_ERR\_INVALID\_QUERY** (15)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-146">A consulta não é válida para a linguagem de consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="d4af6-146">The query is not valid for the specified query language.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span data-ttu-id="d4af6-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ O \_ método Err \_ não \_ está disponível** (16)</span><span class="sxs-lookup"><span data-stu-id="d4af6-147"><span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE** (16)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-148">Não foi possível executar o método extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="d4af6-148">The extrinsic Method could not be executed.</span></span>

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span data-ttu-id="d4af6-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ \_Método Err \_ não \_ encontrado** (17)</span><span class="sxs-lookup"><span data-stu-id="d4af6-149"><span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM\_ERR\_METHOD\_NOT\_FOUND** (17)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-150">O método extrínsecos especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="d4af6-150">The specified extrinsic Method does not exist.</span></span>

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span data-ttu-id="d4af6-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ \_ \_ Resposta de erro inesperado** (18)</span><span class="sxs-lookup"><span data-stu-id="d4af6-151"><span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM\_ERR\_UNEXPECTED\_RESPONSE** (18)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-152">A resposta retornada para a operação assíncrona não era esperada.</span><span class="sxs-lookup"><span data-stu-id="d4af6-152">The returned response to the asynchronous operation was not expected.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span data-ttu-id="d4af6-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ ERRO \_ de \_ \_ destino de resposta inválido** (19)</span><span class="sxs-lookup"><span data-stu-id="d4af6-153"><span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION** (19)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-154">O destino especificado para a resposta assíncrona não é válido.</span><span class="sxs-lookup"><span data-stu-id="d4af6-154">The specified destination for the asynchronous response is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span data-ttu-id="d4af6-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ O \_ namespace de Err \_ não \_ está vazio** (20)</span><span class="sxs-lookup"><span data-stu-id="d4af6-155"><span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY** (20)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-156">O namespace especificado não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d4af6-156">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span data-ttu-id="d4af6-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ ERRO \_ de \_ \_ contexto de enumeração inválido** (21)</span><span class="sxs-lookup"><span data-stu-id="d4af6-157"><span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM\_ERR\_INVALID\_ENUMERATION\_CONTEXT** (21)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-158">O contexto de enumeração fornecido não é válido.</span><span class="sxs-lookup"><span data-stu-id="d4af6-158">The enumeration context supplied is not valid.</span></span>

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span data-ttu-id="d4af6-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ ERRO \_ de \_ \_ tempo limite de operação inválido** (22)</span><span class="sxs-lookup"><span data-stu-id="d4af6-159"><span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM\_ERR\_INVALID\_OPERATION\_TIMEOUT** (22)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-160">O namespace especificado não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d4af6-160">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span data-ttu-id="d4af6-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ A pull de ERR foi \_ \_ \_ \_ abandonada** (23)</span><span class="sxs-lookup"><span data-stu-id="d4af6-161"><span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM\_ERR\_PULL\_HAS\_BEEN\_ABANDONED** (23)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-162">O namespace especificado não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d4af6-162">The specified Namespace is not empty.</span></span>

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span data-ttu-id="d4af6-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ A \_ pull de Err \_ não pode \_ ser \_ abandonada** (24)</span><span class="sxs-lookup"><span data-stu-id="d4af6-163"><span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM\_ERR\_PULL\_CANNOT\_BE\_ABANDONED** (24)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-164">Falha na tentativa de abandonar uma operação de pull.</span><span class="sxs-lookup"><span data-stu-id="d4af6-164">The attempt to abandon a pull operation has failed.</span></span>

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span data-ttu-id="d4af6-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ \_Enumeração filtrada de erro \_ \_ não \_ suportada** (25)</span><span class="sxs-lookup"><span data-stu-id="d4af6-165"><span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM\_ERR\_FILTERED\_ENUMERATION\_NOT\_SUPPORTED** (25)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-166">Não há suporte para Enumeratrions filtrados.</span><span class="sxs-lookup"><span data-stu-id="d4af6-166">Filtered Enumeratrions are not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span data-ttu-id="d4af6-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ \_ \_ \_ \_ Não \_ há suporte para a continuação de erro** (26)</span><span class="sxs-lookup"><span data-stu-id="d4af6-167"><span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM\_ERR\_CONTINUATION\_ON\_ERROR\_NOT\_SUPPORTED** (26)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-168">Não há suporte para continuar em caso de erro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-168">Continue on error is not supported.</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span data-ttu-id="d4af6-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ Limites de servidor de erro \_ \_ \_ excedido** (27)</span><span class="sxs-lookup"><span data-stu-id="d4af6-169"><span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM\_ERR\_SERVER\_LIMITS\_EXCEEDED** (27)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-170">Os limites do servidor WBEM foram excedidos (por exemplo, memória, conexões,...).</span><span class="sxs-lookup"><span data-stu-id="d4af6-170">The WBEM Server limits have been exceeded (e.g. memory, connections, ...).</span></span>

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span data-ttu-id="d4af6-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ O \_ servidor de erro \_ está \_ sendo desligado \_** (28)</span><span class="sxs-lookup"><span data-stu-id="d4af6-171"><span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM\_ERR\_SERVER\_IS\_SHUTTING\_DOWN** (28)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-172">O servidor WBEM está sendo desligado.</span><span class="sxs-lookup"><span data-stu-id="d4af6-172">The WBEM Server is shutting down.</span></span>

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span data-ttu-id="d4af6-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ Recurso de consulta de erro \_ \_ \_ sem \_ suporte** (29)</span><span class="sxs-lookup"><span data-stu-id="d4af6-173"><span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM\_ERR\_QUERY\_FEATURE\_NOT\_SUPPORTED** (29)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-174">Não há suporte para o recurso de consulta especificado.</span><span class="sxs-lookup"><span data-stu-id="d4af6-174">The specified Query Feature is not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d4af6-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d4af6-175"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4af6-176">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="d4af6-176">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-177">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-178">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-178">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-179">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. erro de DMTF \| . Descrição \| 2,3 "," DSP0200. DMTF \| CIMError \| 1,3 "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro CIM**.**CIMStatusCode**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-179">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201.DMTF\|ERROR.DESCRIPTION\|2.3", "DSP0200.DMTF\|CIMError\|1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**CIMStatusCode**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-180">Uma cadeia de caracteres de forma livre que contém uma descrição legível do valor da propriedade **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="d4af6-180">A free-form string that contains a human-readable description of the **CIMStatusCode** property value.</span></span>

> [!Note]  
> <span data-ttu-id="d4af6-181">Essa descrição pode ser estendida, mas deve ser consistente com a definição de **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="d4af6-181">This description may extend, but must be consistent with the definition of **CIMStatusCode**.</span></span>

 

</dd> <dt>

<span data-ttu-id="d4af6-182">**ErrorName**</span><span class="sxs-lookup"><span data-stu-id="d4af6-182">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-184">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-185">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-186">Informações que identificam a entidade que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-186">Information that identifies the entity that generated the error.</span></span> <span data-ttu-id="d4af6-187">Se a entidade for modelada pelo esquema CIM, essa propriedade conterá o caminho para a instância codificada como um parâmetro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="d4af6-187">If the entity is modeled by the CIM Schema, this property contains the path to the instance encoded as a string parameter.</span></span> <span data-ttu-id="d4af6-188">Caso contrário, a propriedade conterá uma cadeia de caracteres que nomeia a entidade que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-188">Otherwise, the property contains a string that names the entity that generated the error.</span></span> <span data-ttu-id="d4af6-189">O formato dessa propriedade é especificado pela propriedade **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="d4af6-189">The format of this property is specified by the **ErrorSourceFormat** property.</span></span>

</dd> <dt>

<span data-ttu-id="d4af6-190">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="d4af6-190">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-191">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4af6-191">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-192">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-193">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**ErrorName**","**\_ erro CIM**.**OtherErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-193">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSource**", "**CIM\_Error**.**OtherErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-194">O formato da propriedade **errorName** .</span><span class="sxs-lookup"><span data-stu-id="d4af6-194">The format of the **ErrorSource** property.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4af6-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d4af6-195"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-196">O formato é desconhecido ou não é de forma significativa interpretado por um aplicativo cliente CIM.</span><span class="sxs-lookup"><span data-stu-id="d4af6-196">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d4af6-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4af6-197"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-198">O formato é definido pelo valor da propriedade **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="d4af6-198">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span>

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span data-ttu-id="d4af6-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span><span class="sxs-lookup"><span data-stu-id="d4af6-199"><span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-200">Um caminho de objeto CIM, conforme definido na especificação de infraestrutura de CIM.</span><span class="sxs-lookup"><span data-stu-id="d4af6-200">A CIM Object Path as defined in the CIM Infrastructure specification.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d4af6-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d4af6-201"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4af6-202">**Error**</span><span class="sxs-lookup"><span data-stu-id="d4af6-202">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-203">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4af6-203">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-204">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-205">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**OtherErrorType**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-205">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**OtherErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-206">O tipo de erro primário.</span><span class="sxs-lookup"><span data-stu-id="d4af6-206">The primary error type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4af6-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d4af6-207"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d4af6-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4af6-208"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span data-ttu-id="d4af6-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Erro de comunicação** (2)</span><span class="sxs-lookup"><span data-stu-id="d4af6-209"><span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Communications Error** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-210">Os erros desse tipo estão associados principalmente aos procedimentos e/ou processos necessários para transmitir informações de um ponto para outro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-210">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span>

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span data-ttu-id="d4af6-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Erro de qualidade de serviço** (3)</span><span class="sxs-lookup"><span data-stu-id="d4af6-211"><span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Quality of Service Error** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-212">Os erros desse tipo são associados principalmente a falhas que resultam em redução na funcionalidade ou no desempenho.</span><span class="sxs-lookup"><span data-stu-id="d4af6-212">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span>

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="d4af6-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Erro de software** (4)</span><span class="sxs-lookup"><span data-stu-id="d4af6-213"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-214">O erro desse tipo está associado principalmente a um software ou a uma falha de processamento.</span><span class="sxs-lookup"><span data-stu-id="d4af6-214">Error of this type are principally associated with a software or processing fault.</span></span>

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span data-ttu-id="d4af6-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erro de hardware** (5)</span><span class="sxs-lookup"><span data-stu-id="d4af6-215"><span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Hardware Error** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-216">Os erros desse tipo estão associados principalmente a um equipamento ou falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="d4af6-216">Errors of this type are principally associated with an equipment or hardware failure.</span></span>

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span data-ttu-id="d4af6-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Erro ambiental** (6)</span><span class="sxs-lookup"><span data-stu-id="d4af6-217"><span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Environmental Error** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-218">outras considerações ambientais.</span><span class="sxs-lookup"><span data-stu-id="d4af6-218">other environmental considerations.</span></span>

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span data-ttu-id="d4af6-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Erro de segurança** (7)</span><span class="sxs-lookup"><span data-stu-id="d4af6-219"><span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Security Error** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-220">Erros desse tipo estão associados a violações de segurança, detecção de vírus e problemas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="d4af6-220">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span>

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span data-ttu-id="d4af6-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Erro de excesso de assinatura** (8)</span><span class="sxs-lookup"><span data-stu-id="d4af6-221"><span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Oversubscription Error** (8)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-222">Os erros desse tipo estão associados principalmente à falha na alocação de recursos suficientes para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="d4af6-222">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span>

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span data-ttu-id="d4af6-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Erro de recurso indisponível** (9)</span><span class="sxs-lookup"><span data-stu-id="d4af6-223"><span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Unavailable Resource Error** (9)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-224">Os erros desse tipo estão associados principalmente à falha ao acessar um recurso necessário.</span><span class="sxs-lookup"><span data-stu-id="d4af6-224">Errors of this type are principally associated with the failure to access a required resource.</span></span>

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span data-ttu-id="d4af6-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Erro de operação sem suporte** (10)</span><span class="sxs-lookup"><span data-stu-id="d4af6-225"><span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Unsupported Operation Error** (10)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-226">Os erros desse tipo estão associados principalmente às solicitações que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="d4af6-226">Errors of this type are principally associated with requests that are not supported.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d4af6-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d4af6-227"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4af6-228">**Message**</span><span class="sxs-lookup"><span data-stu-id="d4af6-228">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-229">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-229">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-230">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-230">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-231">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**MessageID**","**\_ erro de CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-231">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-232">A mensagem formatada.</span><span class="sxs-lookup"><span data-stu-id="d4af6-232">The formatted message.</span></span>

> [!Note]  
> <span data-ttu-id="d4af6-233">Essa mensagem é criada combinando elementos dinâmicos da propriedade **MessageArguments** com os elementos estáticos da propriedade **MessageId** e, em seguida, adicionando-os a um registro de mensagem ou catálogo associado a **OwningEntity**.</span><span class="sxs-lookup"><span data-stu-id="d4af6-233">This message is created by combining dynamic elements of the **MessageArguments** property with the static elements of the **MessageID** property, and then adding them to a message registry or catalog associated with the **OwningEntity**.</span></span>

 

</dd> <dt>

<span data-ttu-id="d4af6-234">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="d4af6-234">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-235">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-235">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-236">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-236">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-237">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**MessageID**","**\_ erro de CIM**.**Mensagem**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-237">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**MessageID**", "**CIM\_Error**.**Message**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-238">Uma matriz que contém o conteúdo dinâmico da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4af6-238">An array that contains the dynamic content of the message.</span></span>

</dd> <dt>

<span data-ttu-id="d4af6-239">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="d4af6-239">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-240">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-240">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-241">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-241">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-242">Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro CIM**.**Mensagem**","**\_ erro de CIM**.**MessageArguments**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-242">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**Message**", "**CIM\_Error**.**MessageArguments**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-243">Uma cadeia de caracteres opaca que identifica exclusivamente, dentro do escopo de OwningEntity, o formato da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4af6-243">An opaque string that uniquely identifies, within the scope of the OwningEntity, the format of the Message.</span></span>

</dd> <dt>

<span data-ttu-id="d4af6-244">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="d4af6-244">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-245">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-245">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-246">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-246">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-247">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**ErrorSourceFormat**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-247">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorSourceFormat**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-248">Uma cadeia de caracteres que define o valor de **errorsourceformat** quando **errorsourceformat** é definido como "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="d4af6-248">A string that defines the **ErrorSourceFormat** value when **ErrorSourceFormat** is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="d4af6-249">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="d4af6-249">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-250">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-250">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-251">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-251">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-252">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**ErrorType**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-252">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ErrorType**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-253">Uma cadeia de caracteres de forma livre que descreve o valor de **ErrorType** quando ele é definido como "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="d4af6-253">A free-form string that describes the **ErrorType** value when it is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="d4af6-254">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="d4af6-254">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-255">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-255">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-257">A ID exclusiva da entidade que possui o formato da mensagem descrita por essa instância.</span><span class="sxs-lookup"><span data-stu-id="d4af6-257">The unique ID of the entity that owns the format of the message described by this instance.</span></span>

> [!Note]  
> <span data-ttu-id="d4af6-258">Essa propriedade deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios ou ao corpo de padrões que definiu o formato da mensagem.</span><span class="sxs-lookup"><span data-stu-id="d4af6-258">This property must include a copyrighted, trademarked, or unique name that is owned by the business entity or standards body that defined the message format.</span></span>

 

</dd> <dt>

<span data-ttu-id="d4af6-259">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="d4af6-259">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-260">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4af6-260">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-261">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-261">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-262">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Severidade percebida ")</span><span class="sxs-lookup"><span data-stu-id="d4af6-262">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Perceived severity")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-263">Uma descrição da severidade do erro do ponto de vista do elemento que enviou a mensagem de erro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-263">A description of the error severity from the point of view of the element that sent the error message.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4af6-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d4af6-264"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-265">a severidade percebida da indicação é desconhecida ou indeterminada.</span><span class="sxs-lookup"><span data-stu-id="d4af6-265">the Perceived Severity of the indication is unknown or indeterminate.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d4af6-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4af6-266"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-267">Indica que o valor da severidade pode ser encontrado na propriedade **OtherSeverity** .</span><span class="sxs-lookup"><span data-stu-id="d4af6-267">Indicates that the Severity's value can be found in the **OtherSeverity** property.</span></span>

</dd> <dt>

<span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>

<span data-ttu-id="d4af6-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Informações** (2)</span><span class="sxs-lookup"><span data-stu-id="d4af6-268"><span id="Information"></span><span id="information"></span><span id="INFORMATION"></span>**Information** (2)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-269">As informações devem ser usadas ao fornecer uma resposta informativa.</span><span class="sxs-lookup"><span data-stu-id="d4af6-269">Information should be used when providing an informative response.</span></span>

</dd> <dt>

<span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>

<span data-ttu-id="d4af6-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degradado/aviso** (3)</span><span class="sxs-lookup"><span data-stu-id="d4af6-270"><span id="Degraded_Warning"></span><span id="degraded_warning"></span><span id="DEGRADED_WARNING"></span>**Degraded/Warning** (3)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-271">Deve ser usado quando apropriado para permitir que o usuário decida se a ação é necessária.</span><span class="sxs-lookup"><span data-stu-id="d4af6-271">Should be used when its appropriate to let the user decide if action is needed.</span></span>

</dd> <dt>

<span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>

<span data-ttu-id="d4af6-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Secundária** (4)</span><span class="sxs-lookup"><span data-stu-id="d4af6-272"><span id="Minor"></span><span id="minor"></span><span id="MINOR"></span>**Minor** (4)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-273">A ação é necessária, mas a situação não é séria no momento.</span><span class="sxs-lookup"><span data-stu-id="d4af6-273">Action is needed, but the situation is not serious at this time.</span></span>

</dd> <dt>

<span id="Major"></span><span id="major"></span><span id="MAJOR"></span>

<span data-ttu-id="d4af6-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Principal** (5)</span><span class="sxs-lookup"><span data-stu-id="d4af6-274"><span id="Major"></span><span id="major"></span><span id="MAJOR"></span>**Major** (5)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-275">A ação é necessária agora.</span><span class="sxs-lookup"><span data-stu-id="d4af6-275">Action is needed NOW.</span></span>

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span data-ttu-id="d4af6-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (6)</span><span class="sxs-lookup"><span data-stu-id="d4af6-276"><span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Critical** (6)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-277">A ação é necessária agora e o escopo é amplo (talvez uma interrupção iminente a um recurso crítico resulte).</span><span class="sxs-lookup"><span data-stu-id="d4af6-277">Action is needed NOW and the scope is broad (perhaps an imminent outage to a critical resource will result).</span></span>

</dd> <dt>

<span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>

<span data-ttu-id="d4af6-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/não recuperável** (7)</span><span class="sxs-lookup"><span data-stu-id="d4af6-278"><span id="Fatal_NonRecoverable"></span><span id="fatal_nonrecoverable"></span><span id="FATAL_NONRECOVERABLE"></span>**Fatal/NonRecoverable** (7)</span></span>


</dt> <dd>

<span data-ttu-id="d4af6-279">ocorreu um erro, mas é tarde demais para realizar uma ação corretiva.</span><span class="sxs-lookup"><span data-stu-id="d4af6-279">an error occurred, but it's too late to take remedial action.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d4af6-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d4af6-280"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4af6-281">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="d4af6-281">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-282">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="d4af6-282">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-283">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-283">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-284">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("recomendação. ITU \| X733. Causa provável "," recomendação. ITU \| M3100. probableCause "," ITU-IANA-Alarm-TC "), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro CIM**.**ProbableCauseDescription**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-284">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU\|X733.Probable cause", "Recommendation.ITU\|M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCauseDescription**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-285">Uma descrição da causa provável do erro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-285">A description of te probable cause of the error.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="d4af6-286">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="d4af6-286">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="d4af6-287">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="d4af6-287">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

<span data-ttu-id="d4af6-288">**Erro de adaptador/placa** (2)</span><span class="sxs-lookup"><span data-stu-id="d4af6-288">**Adapter/Card Error** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="d4af6-289">**Falha no subsistema do aplicativo** (3)</span><span class="sxs-lookup"><span data-stu-id="d4af6-289">**Application Subsystem Failure** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

<span data-ttu-id="d4af6-290">**Largura de banda reduzida** (4)</span><span class="sxs-lookup"><span data-stu-id="d4af6-290">**Bandwidth Reduced** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

<span data-ttu-id="d4af6-291">**Erro de estabelecimento de conexão** (5)</span><span class="sxs-lookup"><span data-stu-id="d4af6-291">**Connection Establishment Error** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

<span data-ttu-id="d4af6-292">**Erro de protocolo de comunicação** (6)</span><span class="sxs-lookup"><span data-stu-id="d4af6-292">**Communications Protocol Error** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

<span data-ttu-id="d4af6-293">**Falha no subsistema de comunicações** (7)</span><span class="sxs-lookup"><span data-stu-id="d4af6-293">**Communications Subsystem Failure** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

<span data-ttu-id="d4af6-294">**Erro de configuração/personalização** (8)</span><span class="sxs-lookup"><span data-stu-id="d4af6-294">**Configuration/Customization Error** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

<span data-ttu-id="d4af6-295">**Congestionamento** (9)</span><span class="sxs-lookup"><span data-stu-id="d4af6-295">**Congestion** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

<span data-ttu-id="d4af6-296">**Dados corrompidos** (10)</span><span class="sxs-lookup"><span data-stu-id="d4af6-296">**Corrupt Data** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

<span data-ttu-id="d4af6-297">**Limite de ciclos de CPU excedido** (11)</span><span class="sxs-lookup"><span data-stu-id="d4af6-297">**CPU Cycles Limit Exceeded** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

<span data-ttu-id="d4af6-298">**Erro de conjunto de/DataSet** (12)</span><span class="sxs-lookup"><span data-stu-id="d4af6-298">**Dataset/Modem Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

<span data-ttu-id="d4af6-299">**Sinal degradado** (13)</span><span class="sxs-lookup"><span data-stu-id="d4af6-299">**Degraded Signal** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

<span data-ttu-id="d4af6-300">**DTE-erro de interface de DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="d4af6-300">**DTE-DCE Interface Error** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

<span data-ttu-id="d4af6-301">**Porta do compartimento aberta** (15)</span><span class="sxs-lookup"><span data-stu-id="d4af6-301">**Enclosure Door Open** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

<span data-ttu-id="d4af6-302">**Mau funcionamento do equipamento** (16)</span><span class="sxs-lookup"><span data-stu-id="d4af6-302">**Equipment Malfunction** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

<span data-ttu-id="d4af6-303">**Vibração excessiva** (17)</span><span class="sxs-lookup"><span data-stu-id="d4af6-303">**Excessive Vibration** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

<span data-ttu-id="d4af6-304">**Erro de formato de arquivo** (18)</span><span class="sxs-lookup"><span data-stu-id="d4af6-304">**File Format Error** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

<span data-ttu-id="d4af6-305">**Incêndio detectado** (19)</span><span class="sxs-lookup"><span data-stu-id="d4af6-305">**Fire Detected** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

<span data-ttu-id="d4af6-306">**Inundação detectada** (20)</span><span class="sxs-lookup"><span data-stu-id="d4af6-306">**Flood Detected** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

<span data-ttu-id="d4af6-307">**Erro de enquadramento** (21)</span><span class="sxs-lookup"><span data-stu-id="d4af6-307">**Framing Error** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

<span data-ttu-id="d4af6-308">**Problema de HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="d4af6-308">**HVAC Problem** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

<span data-ttu-id="d4af6-309">**Umidade inaceitável** (23)</span><span class="sxs-lookup"><span data-stu-id="d4af6-309">**Humidity Unacceptable** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

<span data-ttu-id="d4af6-310">**Erro de dispositivo de e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="d4af6-310">**I/O Device Error** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

<span data-ttu-id="d4af6-311">**Erro de dispositivo de entrada** (25)</span><span class="sxs-lookup"><span data-stu-id="d4af6-311">**Input Device Error** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

<span data-ttu-id="d4af6-312">**Erro de LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="d4af6-312">**LAN Error** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="d4af6-313">**Vazamento não tóxicos detectado** (27)</span><span class="sxs-lookup"><span data-stu-id="d4af6-313">**Non-Toxic Leak Detected** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="d4af6-314">**Erro de transmissão do nó local** (28)</span><span class="sxs-lookup"><span data-stu-id="d4af6-314">**Local Node Transmission Error** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

<span data-ttu-id="d4af6-315">**Perda de quadro** (29)</span><span class="sxs-lookup"><span data-stu-id="d4af6-315">**Loss of Frame** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

<span data-ttu-id="d4af6-316">**Perda de sinal** (30)</span><span class="sxs-lookup"><span data-stu-id="d4af6-316">**Loss of Signal** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

<span data-ttu-id="d4af6-317">**Fornecimento de material esgotado** (31)</span><span class="sxs-lookup"><span data-stu-id="d4af6-317">**Material Supply Exhausted** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

<span data-ttu-id="d4af6-318">**Problema do Multiplexador** (32)</span><span class="sxs-lookup"><span data-stu-id="d4af6-318">**Multiplexer Problem** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

<span data-ttu-id="d4af6-319">**Memória insuficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="d4af6-319">**Out of Memory** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

<span data-ttu-id="d4af6-320">**Erro do dispositivo de saída** (34)</span><span class="sxs-lookup"><span data-stu-id="d4af6-320">**Output Device Error** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

<span data-ttu-id="d4af6-321">**Desempenho degradado** (35)</span><span class="sxs-lookup"><span data-stu-id="d4af6-321">**Performance Degraded** (35)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

<span data-ttu-id="d4af6-322">**Problema de energia** (36)</span><span class="sxs-lookup"><span data-stu-id="d4af6-322">**Power Problem** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

<span data-ttu-id="d4af6-323">**Pressão inaceitável** (37)</span><span class="sxs-lookup"><span data-stu-id="d4af6-323">**Pressure Unacceptable** (37)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

<span data-ttu-id="d4af6-324">**Problema do processador (erro interno da máquina)** (38)</span><span class="sxs-lookup"><span data-stu-id="d4af6-324">**Processor Problem (Internal Machine Error)** (38)</span></span>


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

<span data-ttu-id="d4af6-325">**Falha de bomba** (39)</span><span class="sxs-lookup"><span data-stu-id="d4af6-325">**Pump Failure** (39)</span></span>


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

<span data-ttu-id="d4af6-326">**Tamanho da fila excedido** (40)</span><span class="sxs-lookup"><span data-stu-id="d4af6-326">**Queue Size Exceeded** (40)</span></span>


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

<span data-ttu-id="d4af6-327">**Falha de recebimento** (41)</span><span class="sxs-lookup"><span data-stu-id="d4af6-327">**Receive Failure** (41)</span></span>


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

<span data-ttu-id="d4af6-328">**Falha do receptor** (42)</span><span class="sxs-lookup"><span data-stu-id="d4af6-328">**Receiver Failure** (42)</span></span>


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

<span data-ttu-id="d4af6-329">**Erro de transmissão de nó remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="d4af6-329">**Remote Node Transmission Error** (43)</span></span>


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

<span data-ttu-id="d4af6-330">**Recurso na capacidade ou perto** (44)</span><span class="sxs-lookup"><span data-stu-id="d4af6-330">**Resource at or Nearing Capacity** (44)</span></span>


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

<span data-ttu-id="d4af6-331">**Tempo de resposta excessivo** (45)</span><span class="sxs-lookup"><span data-stu-id="d4af6-331">**Response Time Excessive** (45)</span></span>


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

<span data-ttu-id="d4af6-332">**Taxa de retransmissão excessiva** (46)</span><span class="sxs-lookup"><span data-stu-id="d4af6-332">**Retransmission Rate Excessive** (46)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span data-ttu-id="d4af6-333">**Erro de software** (47)</span><span class="sxs-lookup"><span data-stu-id="d4af6-333">**Software Error** (47)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

<span data-ttu-id="d4af6-334">**Programa de software encerrado** de forma anormal (48)</span><span class="sxs-lookup"><span data-stu-id="d4af6-334">**Software Program Abnormally Terminated** (48)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

<span data-ttu-id="d4af6-335">**Erro do programa de software (resultados incorretos)** (49)</span><span class="sxs-lookup"><span data-stu-id="d4af6-335">**Software Program Error (Incorrect Results)** (49)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

<span data-ttu-id="d4af6-336">**Problema de capacidade de armazenamento** (50)</span><span class="sxs-lookup"><span data-stu-id="d4af6-336">**Storage Capacity Problem** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

<span data-ttu-id="d4af6-337">**Temperatura inaceitável** (51)</span><span class="sxs-lookup"><span data-stu-id="d4af6-337">**Temperature Unacceptable** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

<span data-ttu-id="d4af6-338">**Limite ultrapassado** (52)</span><span class="sxs-lookup"><span data-stu-id="d4af6-338">**Threshold Crossed** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

<span data-ttu-id="d4af6-339">**Problema de tempo** (53)</span><span class="sxs-lookup"><span data-stu-id="d4af6-339">**Timing Problem** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

<span data-ttu-id="d4af6-340">**Vazamento de tóxicos detectado** (54)</span><span class="sxs-lookup"><span data-stu-id="d4af6-340">**Toxic Leak Detected** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

<span data-ttu-id="d4af6-341">**Falha de transmissão** (55)</span><span class="sxs-lookup"><span data-stu-id="d4af6-341">**Transmit Failure** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

<span data-ttu-id="d4af6-342">**Falha do transmissor** (56)</span><span class="sxs-lookup"><span data-stu-id="d4af6-342">**Transmitter Failure** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

<span data-ttu-id="d4af6-343">**Recurso subjacente não disponível** (57)</span><span class="sxs-lookup"><span data-stu-id="d4af6-343">**Underlying Resource Unavailable** (57)</span></span>


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

<span data-ttu-id="d4af6-344">**Incompatibilidade de versão** (58)</span><span class="sxs-lookup"><span data-stu-id="d4af6-344">**Version Mismatch** (58)</span></span>


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

<span data-ttu-id="d4af6-345">**Alerta anterior limpo** (59)</span><span class="sxs-lookup"><span data-stu-id="d4af6-345">**Previous Alert Cleared** (59)</span></span>


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

<span data-ttu-id="d4af6-346">**Tentativas de logon com falha** (60)</span><span class="sxs-lookup"><span data-stu-id="d4af6-346">**Login Attempts Failed** (60)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

<span data-ttu-id="d4af6-347">**Vírus de software detectado** (61)</span><span class="sxs-lookup"><span data-stu-id="d4af6-347">**Software Virus Detected** (61)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

<span data-ttu-id="d4af6-348">**Segurança de hardware violada** (62)</span><span class="sxs-lookup"><span data-stu-id="d4af6-348">**Hardware Security Breached** (62)</span></span>


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

<span data-ttu-id="d4af6-349">**Negação de serviço detectada** (63)</span><span class="sxs-lookup"><span data-stu-id="d4af6-349">**Denial of Service Detected** (63)</span></span>


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

<span data-ttu-id="d4af6-350">**Incompatibilidade de credencial de segurança** (64)</span><span class="sxs-lookup"><span data-stu-id="d4af6-350">**Security Credential Mismatch** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

<span data-ttu-id="d4af6-351">**Acesso não autorizado** (65)</span><span class="sxs-lookup"><span data-stu-id="d4af6-351">**Unauthorized Access** (65)</span></span>


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

<span data-ttu-id="d4af6-352">**Alarme recebido** (66)</span><span class="sxs-lookup"><span data-stu-id="d4af6-352">**Alarm Received** (66)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

<span data-ttu-id="d4af6-353">**Perda de ponteiro** (67)</span><span class="sxs-lookup"><span data-stu-id="d4af6-353">**Loss of Pointer** (67)</span></span>


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

<span data-ttu-id="d4af6-354">**Incompatibilidade de carga** (68)</span><span class="sxs-lookup"><span data-stu-id="d4af6-354">**Payload Mismatch** (68)</span></span>


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

<span data-ttu-id="d4af6-355">**Erro de transmissão** (69)</span><span class="sxs-lookup"><span data-stu-id="d4af6-355">**Transmission Error** (69)</span></span>


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

<span data-ttu-id="d4af6-356">**Taxa de erros excessivas** (70)</span><span class="sxs-lookup"><span data-stu-id="d4af6-356">**Excessive Error Rate** (70)</span></span>


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

<span data-ttu-id="d4af6-357">**Problema de rastreamento** (71)</span><span class="sxs-lookup"><span data-stu-id="d4af6-357">**Trace Problem** (71)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

<span data-ttu-id="d4af6-358">**Elemento não disponível** (72)</span><span class="sxs-lookup"><span data-stu-id="d4af6-358">**Element Unavailable** (72)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

<span data-ttu-id="d4af6-359">**Elemento ausente** (73)</span><span class="sxs-lookup"><span data-stu-id="d4af6-359">**Element Missing** (73)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

<span data-ttu-id="d4af6-360">**Perda de vários quadros** (74)</span><span class="sxs-lookup"><span data-stu-id="d4af6-360">**Loss of Multi Frame** (74)</span></span>


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

<span data-ttu-id="d4af6-361">**Falha no canal de difusão** (75)</span><span class="sxs-lookup"><span data-stu-id="d4af6-361">**Broadcast Channel Failure** (75)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

<span data-ttu-id="d4af6-362">**Mensagem inválida recebida** (76)</span><span class="sxs-lookup"><span data-stu-id="d4af6-362">**Invalid Message Received** (76)</span></span>


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

<span data-ttu-id="d4af6-363">**Falha de roteamento** (77)</span><span class="sxs-lookup"><span data-stu-id="d4af6-363">**Routing Failure** (77)</span></span>


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

<span data-ttu-id="d4af6-364">**Falha no backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="d4af6-364">**Backplane Failure** (78)</span></span>


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

<span data-ttu-id="d4af6-365">**Duplicação de identificador** (79)</span><span class="sxs-lookup"><span data-stu-id="d4af6-365">**Identifier Duplication** (79)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

<span data-ttu-id="d4af6-366">**Falha no caminho de proteção** (80)</span><span class="sxs-lookup"><span data-stu-id="d4af6-366">**Protection Path Failure** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

<span data-ttu-id="d4af6-367">**Perda de sincronização ou incompatibilidade** (81)</span><span class="sxs-lookup"><span data-stu-id="d4af6-367">**Sync Loss or Mismatch** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

<span data-ttu-id="d4af6-368">**Problema de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="d4af6-368">**Terminal Problem** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

<span data-ttu-id="d4af6-369">**Falha no relógio em tempo real** (83)</span><span class="sxs-lookup"><span data-stu-id="d4af6-369">**Real Time Clock Failure** (83)</span></span>


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

<span data-ttu-id="d4af6-370">**Falha de antena** (84)</span><span class="sxs-lookup"><span data-stu-id="d4af6-370">**Antenna Failure** (84)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

<span data-ttu-id="d4af6-371">**Falha no carregamento da bateria** (85)</span><span class="sxs-lookup"><span data-stu-id="d4af6-371">**Battery Charging Failure** (85)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

<span data-ttu-id="d4af6-372">**Falha de disco** (86)</span><span class="sxs-lookup"><span data-stu-id="d4af6-372">**Disk Failure** (86)</span></span>


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

<span data-ttu-id="d4af6-373">**Falha de salto de frequência** (87)</span><span class="sxs-lookup"><span data-stu-id="d4af6-373">**Frequency Hopping Failure** (87)</span></span>


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

<span data-ttu-id="d4af6-374">**Perda de redundância** (88)</span><span class="sxs-lookup"><span data-stu-id="d4af6-374">**Loss of Redundancy** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

<span data-ttu-id="d4af6-375">**Falha da fonte de energia** (89)</span><span class="sxs-lookup"><span data-stu-id="d4af6-375">**Power Supply Failure** (89)</span></span>


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

<span data-ttu-id="d4af6-376">**Problema de qualidade de sinal** (90)</span><span class="sxs-lookup"><span data-stu-id="d4af6-376">**Signal Quality Problem** (90)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

<span data-ttu-id="d4af6-377">**Descarregamento da bateria** (91)</span><span class="sxs-lookup"><span data-stu-id="d4af6-377">**Battery Discharging** (91)</span></span>


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

<span data-ttu-id="d4af6-378">**Falha da bateria** (92)</span><span class="sxs-lookup"><span data-stu-id="d4af6-378">**Battery Failure** (92)</span></span>


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

<span data-ttu-id="d4af6-379">**Problema de energia comercial** (93)</span><span class="sxs-lookup"><span data-stu-id="d4af6-379">**Commercial Power Problem** (93)</span></span>


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

<span data-ttu-id="d4af6-380">**Falha do ventilador** (94)</span><span class="sxs-lookup"><span data-stu-id="d4af6-380">**Fan Failure** (94)</span></span>


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

<span data-ttu-id="d4af6-381">**Falha do mecanismo** (95)</span><span class="sxs-lookup"><span data-stu-id="d4af6-381">**Engine Failure** (95)</span></span>


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

<span data-ttu-id="d4af6-382">**Falha do sensor** (96)</span><span class="sxs-lookup"><span data-stu-id="d4af6-382">**Sensor Failure** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

<span data-ttu-id="d4af6-383">**Falha de fusível** (97)</span><span class="sxs-lookup"><span data-stu-id="d4af6-383">**Fuse Failure** (97)</span></span>


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

<span data-ttu-id="d4af6-384">**Falha do gerador** (98)</span><span class="sxs-lookup"><span data-stu-id="d4af6-384">**Generator Failure** (98)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

<span data-ttu-id="d4af6-385">**Bateria fraca** (99)</span><span class="sxs-lookup"><span data-stu-id="d4af6-385">**Low Battery** (99)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

<span data-ttu-id="d4af6-386">**Baixo combustível** (100)</span><span class="sxs-lookup"><span data-stu-id="d4af6-386">**Low Fuel** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

<span data-ttu-id="d4af6-387">**Água inferior** (101)</span><span class="sxs-lookup"><span data-stu-id="d4af6-387">**Low Water** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

<span data-ttu-id="d4af6-388">**Gás explosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="d4af6-388">**Explosive Gas** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

<span data-ttu-id="d4af6-389">**Altos ventos** (103)</span><span class="sxs-lookup"><span data-stu-id="d4af6-389">**High Winds** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

<span data-ttu-id="d4af6-390">**Acúmulo de gelo** (104)</span><span class="sxs-lookup"><span data-stu-id="d4af6-390">**Ice Buildup** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

<span data-ttu-id="d4af6-391">**Fumaça** (105)</span><span class="sxs-lookup"><span data-stu-id="d4af6-391">**Smoke** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

<span data-ttu-id="d4af6-392">**Incompatibilidade de memória** (106)</span><span class="sxs-lookup"><span data-stu-id="d4af6-392">**Memory Mismatch** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

<span data-ttu-id="d4af6-393">**Ciclos de CPU insuficientes** (107)</span><span class="sxs-lookup"><span data-stu-id="d4af6-393">**Out of CPU Cycles** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

<span data-ttu-id="d4af6-394">**Problema de ambiente de software** (108)</span><span class="sxs-lookup"><span data-stu-id="d4af6-394">**Software Environment Problem** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

<span data-ttu-id="d4af6-395">**Falha de download de software** (109)</span><span class="sxs-lookup"><span data-stu-id="d4af6-395">**Software Download Failure** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

<span data-ttu-id="d4af6-396">**Elemento reinicializado** (110)</span><span class="sxs-lookup"><span data-stu-id="d4af6-396">**Element Reinitialized** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

<span data-ttu-id="d4af6-397">**Tempo limite** (111)</span><span class="sxs-lookup"><span data-stu-id="d4af6-397">**Timeout** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

<span data-ttu-id="d4af6-398">**Problemas de log** (112)</span><span class="sxs-lookup"><span data-stu-id="d4af6-398">**Logging Problems** (112)</span></span>


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

<span data-ttu-id="d4af6-399">**Vazamento detectado** (113)</span><span class="sxs-lookup"><span data-stu-id="d4af6-399">**Leak Detected** (113)</span></span>


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

<span data-ttu-id="d4af6-400">**Falha no mecanismo de proteção** (114)</span><span class="sxs-lookup"><span data-stu-id="d4af6-400">**Protection Mechanism Failure** (114)</span></span>


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

<span data-ttu-id="d4af6-401">**Proteção de falha de recurso** (115)</span><span class="sxs-lookup"><span data-stu-id="d4af6-401">**Protecting Resource Failure** (115)</span></span>


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

<span data-ttu-id="d4af6-402">**Inconsistência do banco de dados** (116)</span><span class="sxs-lookup"><span data-stu-id="d4af6-402">**Database Inconsistency** (116)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

<span data-ttu-id="d4af6-403">**Falha de autenticação** (117)</span><span class="sxs-lookup"><span data-stu-id="d4af6-403">**Authentication Failure** (117)</span></span>


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

<span data-ttu-id="d4af6-404">**Violação de confidencialidade** (118)</span><span class="sxs-lookup"><span data-stu-id="d4af6-404">**Breach of Confidentiality** (118)</span></span>


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

<span data-ttu-id="d4af6-405">**Adulteração de cabo** (119)</span><span class="sxs-lookup"><span data-stu-id="d4af6-405">**Cable Tamper** (119)</span></span>


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

<span data-ttu-id="d4af6-406">**Informações atrasadas** (120)</span><span class="sxs-lookup"><span data-stu-id="d4af6-406">**Delayed Information** (120)</span></span>


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

<span data-ttu-id="d4af6-407">**Informações duplicadas** (121)</span><span class="sxs-lookup"><span data-stu-id="d4af6-407">**Duplicate Information** (121)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

<span data-ttu-id="d4af6-408">**Informações ausentes** (122)</span><span class="sxs-lookup"><span data-stu-id="d4af6-408">**Information Missing** (122)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

<span data-ttu-id="d4af6-409">**Modificação de informações** (123)</span><span class="sxs-lookup"><span data-stu-id="d4af6-409">**Information Modification** (123)</span></span>


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

<span data-ttu-id="d4af6-410">**Informações fora de sequência** (124)</span><span class="sxs-lookup"><span data-stu-id="d4af6-410">**Information Out of Sequence** (124)</span></span>


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

<span data-ttu-id="d4af6-411">**Chave expirada** (125)</span><span class="sxs-lookup"><span data-stu-id="d4af6-411">**Key Expired** (125)</span></span>


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

<span data-ttu-id="d4af6-412">**Falha de não repúdio** (126)</span><span class="sxs-lookup"><span data-stu-id="d4af6-412">**Non-Repudiation Failure** (126)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

<span data-ttu-id="d4af6-413">**Atividade fora de horas** (127)</span><span class="sxs-lookup"><span data-stu-id="d4af6-413">**Out of Hours Activity** (127)</span></span>


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

<span data-ttu-id="d4af6-414">**Fora de serviço** (128)</span><span class="sxs-lookup"><span data-stu-id="d4af6-414">**Out of Service** (128)</span></span>


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

<span data-ttu-id="d4af6-415">**Erro de procedimento** (129)</span><span class="sxs-lookup"><span data-stu-id="d4af6-415">**Procedural Error** (129)</span></span>


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

<span data-ttu-id="d4af6-416">**Informações inesperadas** (130)</span><span class="sxs-lookup"><span data-stu-id="d4af6-416">**Unexpected Information** (130)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="d4af6-417">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="d4af6-417">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="d4af6-418">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="d4af6-418">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-419">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-420">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-420">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-421">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**\_ erro de CIM**.**ProbableCause**")</span><span class="sxs-lookup"><span data-stu-id="d4af6-421">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_Error**.**ProbableCause**")</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-422">Uma cadeia de caracteres de forma livre que descreve a causa provável do erro, quando a propriedade **ProbableCause** é definida como "1" (outra).</span><span class="sxs-lookup"><span data-stu-id="d4af6-422">A free-form string that describes the probable cause of the error, when the **ProbableCause** property is set to "1" (other).</span></span>

</dd> <dt>

<span data-ttu-id="d4af6-423">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="d4af6-423">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d4af6-424">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="d4af6-424">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="d4af6-425">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d4af6-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d4af6-426">Uma matriz de cadeias de caracteres de forma livre que descrevem as ações recomendadas a serem executadas para resolver o erro.</span><span class="sxs-lookup"><span data-stu-id="d4af6-426">An array of free-form strings that describe the recommended actions to take to resolve the error.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4af6-427">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4af6-427">Requirements</span></span>



| <span data-ttu-id="d4af6-428">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4af6-428">Requirement</span></span> | <span data-ttu-id="d4af6-429">Valor</span><span class="sxs-lookup"><span data-stu-id="d4af6-429">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4af6-430">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4af6-430">Minimum supported client</span></span><br/> | <span data-ttu-id="d4af6-431">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d4af6-431">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d4af6-432">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4af6-432">Minimum supported server</span></span><br/> | <span data-ttu-id="d4af6-433">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d4af6-433">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d4af6-434">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4af6-434">Namespace</span></span><br/>                | <span data-ttu-id="d4af6-435">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d4af6-435">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d4af6-436">MOF</span><span class="sxs-lookup"><span data-stu-id="d4af6-436">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4af6-437"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d4af6-437"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4af6-438">DLL</span><span class="sxs-lookup"><span data-stu-id="d4af6-438">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4af6-439"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d4af6-439"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

