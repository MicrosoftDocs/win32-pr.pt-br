---
description: Contém informações sobre a gravidade, a causa, as ações recomendadas e outros dados relacionados à falha de uma operação CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Classe Msvm_Error
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Error
- Msvm_Error.ErrorType
- Msvm_Error.OtherErrorType
- Msvm_Error.OwningEntity
- Msvm_Error.MessageID
- Msvm_Error.Message
- Msvm_Error.MessageArguments
- Msvm_Error.PerceivedSeverity
- Msvm_Error.ProbableCause
- Msvm_Error.ProbableCauseDescription
- Msvm_Error.RecommendedActions
- Msvm_Error.ErrorSource
- Msvm_Error.ErrorSourceFormat
- Msvm_Error.OtherErrorSourceFormat
- Msvm_Error.CIMStatusCode
- Msvm_Error.CIMStatusCodeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56b3b30f1d64146db2554d097b11104df09ba018
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011089"
---
# <a name="msvm_error-class"></a><span data-ttu-id="a557b-103">\_Classe de erro Msvm</span><span class="sxs-lookup"><span data-stu-id="a557b-103">Msvm\_Error class</span></span>

<span data-ttu-id="a557b-104">Uma classe especializada que contém informações sobre a gravidade, a causa, as ações recomendadas e outros dados relacionados à falha de uma operação CIM.</span><span class="sxs-lookup"><span data-stu-id="a557b-104">A specialized class that contains information about the severity, cause, recommended actions, and other data related to the failure of a CIM Operation.</span></span>

<span data-ttu-id="a557b-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a557b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a557b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a557b-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_Error : CIM_Error
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

## <a name="members"></a><span data-ttu-id="a557b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a557b-107">Members</span></span>

<span data-ttu-id="a557b-108">A classe de **\_ erro Msvm** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a557b-108">The **Msvm\_Error** class has these types of members:</span></span>

-   [<span data-ttu-id="a557b-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a557b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a557b-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a557b-110">Properties</span></span>

<span data-ttu-id="a557b-111">A classe de **\_ erro Msvm** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a557b-111">The **Msvm\_Error** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a557b-112">**CIMStatusCode**</span><span class="sxs-lookup"><span data-stu-id="a557b-112">**CIMStatusCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-113">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a557b-113">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-115">O código de status CIM que caracteriza essa instância.</span><span class="sxs-lookup"><span data-stu-id="a557b-115">The CIM status code that characterizes this instance.</span></span> <span data-ttu-id="a557b-116">Essa propriedade define os códigos de status que podem ser retornados por um ouvinte ou servidor CIM em conformidade.</span><span class="sxs-lookup"><span data-stu-id="a557b-116">This property defines the status codes that may be return by a conforming CIM Server or Listener.</span></span> <span data-ttu-id="a557b-117">Nem todos os códigos de status são válidos para cada operação.</span><span class="sxs-lookup"><span data-stu-id="a557b-117">Not all status codes are valid for each operation.</span></span> <span data-ttu-id="a557b-118">A especificação para cada operação deve definir os códigos de status que podem ser retornados por essa operação.</span><span class="sxs-lookup"><span data-stu-id="a557b-118">The specification for each operation should define the status codes that may be returned by that operation.</span></span> <span data-ttu-id="a557b-119">Os valores a seguir para o código de status CIM são definidos.</span><span class="sxs-lookup"><span data-stu-id="a557b-119">The following values for CIM status code are defined.</span></span> <span data-ttu-id="a557b-120">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-120">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="a557b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="a557b-121">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="a557b-122">Significado</span><span class="sxs-lookup"><span data-stu-id="a557b-122">Meaning</span></span>                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <span data-ttu-id="a557b-123"><dt>**CIM \_ \_Falha de Err**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-123"><dt>**CIM\_ERR\_FAILED**</dt> <dt>1</dt></span></span> </dl>                                                                       | <span data-ttu-id="a557b-124">Ocorreu um erro geral que não é coberto por um código de erro mais específico.</span><span class="sxs-lookup"><span data-stu-id="a557b-124">A general error occurred that is not covered by a more specific error code.</span></span><br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <span data-ttu-id="a557b-125"><dt>**CIM \_ ERRO de \_ acesso \_ negado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-125"><dt>**CIM\_ERR\_ACCESS\_DENIED**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="a557b-126">O acesso a um recurso CIM não estava disponível para o cliente.</span><span class="sxs-lookup"><span data-stu-id="a557b-126">Access to a CIM resource was not available to the client.</span></span><br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <span data-ttu-id="a557b-127"><dt>**CIM \_ ERRO \_ de \_ namespace inválido**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-127"><dt>**CIM\_ERR\_INVALID\_NAMESPACE**</dt> <dt>3</dt></span></span> </dl>                                     | <span data-ttu-id="a557b-128">O namespace de destino não existe.</span><span class="sxs-lookup"><span data-stu-id="a557b-128">The target namespace does not exist.</span></span><br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <span data-ttu-id="a557b-129"><dt>**CIM \_ \_ \_ Parâmetro inválido**</dt> <dt>4</dt> do erro</span><span class="sxs-lookup"><span data-stu-id="a557b-129"><dt>**CIM\_ERR\_INVALID\_PARAMETER**</dt> <dt>4</dt></span></span> </dl>                                     | <span data-ttu-id="a557b-130">Um ou mais valores de parâmetro passados para o método eram inválidos.</span><span class="sxs-lookup"><span data-stu-id="a557b-130">One or more parameter values passed to the method were invalid.</span></span><br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <span data-ttu-id="a557b-131"><dt>**CIM \_ ERRO \_ \_ classe 5 inválida**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a557b-131"><dt>**CIM\_ERR\_INVALID\_CLASS**</dt> <dt>5</dt></span></span> </dl>                                                 | <span data-ttu-id="a557b-132">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="a557b-132">The specified class does not exist.</span></span><br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <span data-ttu-id="a557b-133"><dt>**CIM \_ ERRO \_ não \_ encontrado**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-133"><dt>**CIM\_ERR\_NOT\_FOUND**</dt> <dt>6</dt></span></span> </dl>                                                             | <span data-ttu-id="a557b-134">O objeto solicitado não pôde ser encontrado.</span><span class="sxs-lookup"><span data-stu-id="a557b-134">The requested object could not be found.</span></span><br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <span data-ttu-id="a557b-135"><dt>**CIM \_ \_Não \_ há suporte para o erro**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-135"><dt>**CIM\_ERR\_NOT\_SUPPORTED**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="a557b-136">Não há suporte para a operação solicitada.</span><span class="sxs-lookup"><span data-stu-id="a557b-136">The requested operation is not supported.</span></span><br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <span data-ttu-id="a557b-137"><dt>**CIM \_ A \_ classe Err \_ tem \_ filhos**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-137"><dt>**CIM\_ERR\_CLASS\_HAS\_CHILDREN**</dt> <dt>8</dt></span></span> </dl>                                 | <span data-ttu-id="a557b-138">A operação não pode ser executada nesta classe porque ela tem instâncias.</span><span class="sxs-lookup"><span data-stu-id="a557b-138">Operation cannot be carried out on this class because it has instances.</span></span><br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <span data-ttu-id="a557b-139"><dt>**CIM \_ A \_ classe Err \_ tem \_ instâncias**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-139"><dt>**CIM\_ERR\_CLASS\_HAS\_INSTANCES**</dt> <dt>9</dt></span></span> </dl>                              | <span data-ttu-id="a557b-140">A operação não pode ser executada nesta classe porque ela tem instâncias.</span><span class="sxs-lookup"><span data-stu-id="a557b-140">Operation cannot be carried out on this class since it has instances.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <span data-ttu-id="a557b-141"><dt>**CIM \_ \_Inclasse \_ inválida de Err**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-141"><dt>**CIM\_ERR\_INVALID\_SUPERCLASS**</dt> <dt>10</dt></span></span> </dl>                                 | <span data-ttu-id="a557b-142">A operação não pode ser executada porque a superclasse especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="a557b-142">Operation cannot be carried out since the specified superclass does not exist.</span></span><br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <span data-ttu-id="a557b-143"><dt>**CIM \_ O erro \_ já \_ existe**</dt> <dt>11</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-143"><dt>**CIM\_ERR\_ALREADY\_EXISTS**</dt> <dt>11</dt></span></span> </dl>                                             | <span data-ttu-id="a557b-144">A operação não pode ser executada porque já existe um objeto.</span><span class="sxs-lookup"><span data-stu-id="a557b-144">Operation cannot be carried out because an object already exists.</span></span><br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <span data-ttu-id="a557b-145"><dt>**CIM \_ \_Não erro \_ , \_ Propriedade**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-145"><dt>**CIM\_ERR\_NO\_SUCH\_PROPERTY**</dt> <dt>12</dt></span></span> </dl>                                      | <span data-ttu-id="a557b-146">A propriedade especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="a557b-146">The specified Property does not exist.</span></span><br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <span data-ttu-id="a557b-147"><dt>**CIM \_ Tipo de erro \_ \_ incompatível**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-147"><dt>**CIM\_ERR\_TYPE\_MISMATCH**</dt> <dt>13</dt></span></span> </dl>                                                | <span data-ttu-id="a557b-148">O valor fornecido é incompatível com o tipo.</span><span class="sxs-lookup"><span data-stu-id="a557b-148">The value supplied is incompatible with the type.</span></span><br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <span data-ttu-id="a557b-149"><dt>**CIM \_ \_Linguagem de consulta Err \_ \_ sem \_ suporte**</dt> <dt>14</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-149"><dt>**CIM\_ERR\_QUERY\_LANGUAGE\_NOT\_SUPPORTED**</dt> <dt>14</dt></span></span> </dl> | <span data-ttu-id="a557b-150">A linguagem de consulta não é reconhecida nem tem suporte.</span><span class="sxs-lookup"><span data-stu-id="a557b-150">The query language is not recognized or supported.</span></span><br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <span data-ttu-id="a557b-151"><dt>**CIM \_ ERRO \_ de \_ consulta inválida**</dt> <dt>15</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-151"><dt>**CIM\_ERR\_INVALID\_QUERY**</dt> <dt>15</dt></span></span> </dl>                                                | <span data-ttu-id="a557b-152">A consulta não é válida para a linguagem de consulta especificada.</span><span class="sxs-lookup"><span data-stu-id="a557b-152">The query is not valid for the specified query language.</span></span><br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <span data-ttu-id="a557b-153"><dt>**CIM \_ O \_ método Err \_ não \_ está disponível**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-153"><dt>**CIM\_ERR\_METHOD\_NOT\_AVAILABLE**</dt> <dt>16</dt></span></span> </dl>                          | <span data-ttu-id="a557b-154">Não foi possível executar o método extrínsecos.</span><span class="sxs-lookup"><span data-stu-id="a557b-154">The extrinsic method could not be executed.</span></span><br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <span data-ttu-id="a557b-155"><dt>**CIM \_ \_Método Err \_ não \_ encontrado**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-155"><dt>**CIM\_ERR\_METHOD\_NOT\_FOUND**</dt> <dt>17</dt></span></span> </dl>                                      | <span data-ttu-id="a557b-156">O método extrínsecos especificado não existe.</span><span class="sxs-lookup"><span data-stu-id="a557b-156">The specified extrinsic method does not exist.</span></span><br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <span data-ttu-id="a557b-157"><dt>**CIM \_ \_ \_ Resposta INESPERADA de erro**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-157"><dt>**CIM\_ERR\_UNEXPECTED\_RESPONSE**</dt> <dt>18</dt></span></span> </dl>                              | <span data-ttu-id="a557b-158">A resposta retornada para a operação assíncrona não era esperada.</span><span class="sxs-lookup"><span data-stu-id="a557b-158">The returned response to the asynchronous operation was not expected.</span></span><br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <span data-ttu-id="a557b-159"><dt>**CIM \_ ERRO \_ de \_ \_ destino de resposta inválido**</dt> <dt>19</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-159"><dt>**CIM\_ERR\_INVALID\_RESPONSE\_DESTINATION**</dt> <dt>19</dt></span></span> </dl>  | <span data-ttu-id="a557b-160">O destino especificado para a resposta assíncrona não é válido.</span><span class="sxs-lookup"><span data-stu-id="a557b-160">The specified destination for the asynchronous response is not valid.</span></span><br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <span data-ttu-id="a557b-161"><dt>**CIM \_ O \_ namespace de Err \_ não \_ está vazio**</dt> <dt>20</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-161"><dt>**CIM\_ERR\_NAMESPACE\_NOT\_EMPTY**</dt> <dt>20</dt></span></span> </dl>                             | <span data-ttu-id="a557b-162">O namespace especificado não está vazio.</span><span class="sxs-lookup"><span data-stu-id="a557b-162">The specified namespace is not empty.</span></span><br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <span data-ttu-id="a557b-163"><dt>**DMTF reservado**</dt> <dt>21 = *valor*</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-163"><dt>**DMTF Reserved**</dt> <dt>21 = *value* </dt></span></span> </dl>                            | <span data-ttu-id="a557b-164">Valores reservados.</span><span class="sxs-lookup"><span data-stu-id="a557b-164">Reserved values.</span></span><br/>                                                               |



 

</dd> <dt>

<span data-ttu-id="a557b-165">**CIMStatusCodeDescription**</span><span class="sxs-lookup"><span data-stu-id="a557b-165">**CIMStatusCodeDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-166">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-167">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-168">Uma cadeia de caracteres que contém uma descrição legível pelo usuário da propriedade **CIMStatusCode** .</span><span class="sxs-lookup"><span data-stu-id="a557b-168">A string containing a user-readable description of the **CIMStatusCode** property.</span></span> <span data-ttu-id="a557b-169">Essa descrição pode estender, mas deve ser consistente com a definição de **CIMStatusCode**.</span><span class="sxs-lookup"><span data-stu-id="a557b-169">This description may extend, but must be consistent with, the definition of **CIMStatusCode**.</span></span> <span data-ttu-id="a557b-170">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-170">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-171">**ErrorName**</span><span class="sxs-lookup"><span data-stu-id="a557b-171">**ErrorSource**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-172">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-173">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-173">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-174">As informações de identificação da entidade (a instância) que geram o erro.</span><span class="sxs-lookup"><span data-stu-id="a557b-174">The identifying information of the entity (the instance) generating the error.</span></span> <span data-ttu-id="a557b-175">Se essa entidade for modelada no esquema CIM, essa propriedade conterá o caminho da instância codificada como um parâmetro de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a557b-175">If this entity is modeled in the CIM Schema, this property contains the path of the instance encoded as a string parameter.</span></span> <span data-ttu-id="a557b-176">Se não for modelado, a propriedade conterá uma cadeia de caracteres de identificação que nomeia a entidade que gerou o erro.</span><span class="sxs-lookup"><span data-stu-id="a557b-176">If not modeled, the property contains some identifying string that names the entity that generated the error.</span></span> <span data-ttu-id="a557b-177">O caminho ou a cadeia de caracteres de identificação é formatado de acordo com a propriedade **ErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="a557b-177">The path or identifying string is formatted per the **ErrorSourceFormat** property.</span></span> <span data-ttu-id="a557b-178">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-178">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-179">**ErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="a557b-179">**ErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-180">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a557b-180">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-181">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-182">O formato da propriedade **errorName** é interpretável com base no valor dessa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a557b-182">The format of the **ErrorSource** property is interpretable based on the value of this property.</span></span> <span data-ttu-id="a557b-183">Essa propriedade é herdada [**do \_ erro CIM**](/previous-versions//cc150671(v=vs.85))e é sempre definida como 0.</span><span class="sxs-lookup"><span data-stu-id="a557b-183">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)), and it is always set to 0.</span></span>



| <span data-ttu-id="a557b-184">Valor</span><span class="sxs-lookup"><span data-stu-id="a557b-184">Value</span></span>                                                                                                                                                                                                                                                        | <span data-ttu-id="a557b-185">Significado</span><span class="sxs-lookup"><span data-stu-id="a557b-185">Meaning</span></span>                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a557b-186"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="a557b-186"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="a557b-187">O formato é desconhecido ou não é de forma significativa interpretado por um aplicativo cliente CIM.</span><span class="sxs-lookup"><span data-stu-id="a557b-187">The format is unknown or not meaningfully interpretable by a CIM client application.</span></span><br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a557b-188"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-188"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="a557b-189">O formato é definido pelo valor da propriedade **OtherErrorSourceFormat** .</span><span class="sxs-lookup"><span data-stu-id="a557b-189">The format is defined by the value of the **OtherErrorSourceFormat** property.</span></span><br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <span data-ttu-id="a557b-190"><dt>**CIMObjectHandle**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-190"><dt>**CIMObjectHandle**</dt> <dt>2 </dt></span></span> </dl> | <span data-ttu-id="a557b-191">Um identificador de objeto CIM, codificado usando a sintaxe de MOF definida para o não terminal objectHandle, é usado para identificar a entidade.</span><span class="sxs-lookup"><span data-stu-id="a557b-191">A CIM Object Handle, encoded using the MOF syntax defined for the objectHandle non-terminal, is used to identify the entity.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="a557b-192">**Error**</span><span class="sxs-lookup"><span data-stu-id="a557b-192">**ErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-193">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a557b-193">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-195">Classificação primária do erro.</span><span class="sxs-lookup"><span data-stu-id="a557b-195">Primary classification of the error.</span></span> <span data-ttu-id="a557b-196">Os valores a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="a557b-196">The following values are defined.</span></span> <span data-ttu-id="a557b-197">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-197">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>



| <span data-ttu-id="a557b-198">Valor</span><span class="sxs-lookup"><span data-stu-id="a557b-198">Value</span></span>                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="a557b-199">Significado</span><span class="sxs-lookup"><span data-stu-id="a557b-199">Meaning</span></span>                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="a557b-200"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="a557b-200"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="a557b-201"><dt>**Outros**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-201"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <span data-ttu-id="a557b-202"><dt>**Erro de comunicação**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-202"><dt>**Communications Error**</dt> <dt>2</dt></span></span> </dl>                               | <span data-ttu-id="a557b-203">Os erros desse tipo estão associados principalmente aos procedimentos e/ou processos necessários para transmitir informações de um ponto para outro.</span><span class="sxs-lookup"><span data-stu-id="a557b-203">Errors of this type are principally associated with the procedures and/or processes required to convey information from one point to another.</span></span><br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <span data-ttu-id="a557b-204"><dt>**Erro de qualidade de serviço**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-204"><dt>**Quality of Service Error**</dt> <dt>3</dt></span></span> </dl>               | <span data-ttu-id="a557b-205">Os erros desse tipo são associados principalmente a falhas que resultam em redução na funcionalidade ou no desempenho.</span><span class="sxs-lookup"><span data-stu-id="a557b-205">Errors of this type are principally associated with failures that result in reduced functionality or performance.</span></span><br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <span data-ttu-id="a557b-206"><dt>**Erro de software**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-206"><dt>**Software Error**</dt> <dt>4</dt></span></span> </dl>                                                       | <span data-ttu-id="a557b-207">O erro desse tipo está associado principalmente a um software ou a uma falha de processamento.</span><span class="sxs-lookup"><span data-stu-id="a557b-207">Error of this type are principally associated with a software or processing fault.</span></span><br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <span data-ttu-id="a557b-208"><dt>**Erro de hardware**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-208"><dt>**Hardware Error**</dt> <dt>5</dt></span></span> </dl>                                                       | <span data-ttu-id="a557b-209">Os erros desse tipo estão associados principalmente a um equipamento ou falha de hardware.</span><span class="sxs-lookup"><span data-stu-id="a557b-209">Errors of this type are principally associated with an equipment or hardware failure.</span></span><br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <span data-ttu-id="a557b-210"><dt>**Erro ambiental**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-210"><dt>**Environmental Error**</dt> <dt>6</dt></span></span> </dl>                                   | <span data-ttu-id="a557b-211">Os erros desse tipo estão associados principalmente a uma condição de falha relacionada à instalação ou a outras considerações ambientais.</span><span class="sxs-lookup"><span data-stu-id="a557b-211">Errors of this type are principally associated with a failure condition relating to the facility, or other environmental considerations.</span></span><br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <span data-ttu-id="a557b-212"><dt>**Erro de segurança**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-212"><dt>**Security Error**</dt> <dt>7</dt></span></span> </dl>                                                       | <span data-ttu-id="a557b-213">Erros desse tipo estão associados a violações de segurança, detecção de vírus e problemas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="a557b-213">Errors of this type are associated with security violations, detection of viruses, and similar issues.</span></span><br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <span data-ttu-id="a557b-214"><dt>**Erro de assinatura em excesso**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-214"><dt>**Oversubscription Error**</dt> <dt>8</dt></span></span> </dl>                       | <span data-ttu-id="a557b-215">Os erros desse tipo estão associados principalmente à falha na alocação de recursos suficientes para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="a557b-215">Errors of this type are principally associated with the failure to allocate sufficient resources to complete the operation.</span></span><br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <span data-ttu-id="a557b-216"><dt>**Erro de recurso indisponível**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-216"><dt>**Unavailable Resource Error**</dt> <dt>9</dt></span></span> </dl>       | <span data-ttu-id="a557b-217">Os erros desse tipo estão associados principalmente à falha ao acessar um recurso necessário.</span><span class="sxs-lookup"><span data-stu-id="a557b-217">Errors of this type are principally associated with the failure to access a required resource.</span></span><br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <span data-ttu-id="a557b-218"><dt>**Erro de operação sem suporte**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-218"><dt>**Unsupported Operation Error**</dt> <dt>10 </dt></span></span> </dl> | <span data-ttu-id="a557b-219">Os erros desse tipo estão associados principalmente às solicitações que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="a557b-219">Errors of this type are principally associated with requests that are not supported.</span></span><br/>                                                          |



 

</dd> <dt>

<span data-ttu-id="a557b-220">**Message**</span><span class="sxs-lookup"><span data-stu-id="a557b-220">**Message**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-221">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-221">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-222">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-222">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-223">A mensagem formatada.</span><span class="sxs-lookup"><span data-stu-id="a557b-223">The formatted message.</span></span> <span data-ttu-id="a557b-224">Essa mensagem é construída aplicando o conteúdo dinâmico da mensagem, descrito em **MessageArguments**, à cadeia de caracteres de formato identificada exclusivamente, dentro do escopo de **OwningEntity**, por **MessageId**.</span><span class="sxs-lookup"><span data-stu-id="a557b-224">This message is constructed by applying the dynamic content of the message, described in **MessageArguments**, to the format string uniquely identified, within the scope of the **OwningEntity**, by **MessageID**.</span></span> <span data-ttu-id="a557b-225">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-225">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-226">**MessageArguments**</span><span class="sxs-lookup"><span data-stu-id="a557b-226">**MessageArguments**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-227">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-227">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a557b-228">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-229">Uma matriz que contém o conteúdo dinâmico da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a557b-229">An array containing the dynamic content of the message.</span></span> <span data-ttu-id="a557b-230">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-230">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-231">**MessageID**</span><span class="sxs-lookup"><span data-stu-id="a557b-231">**MessageID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-232">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-233">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-234">Uma cadeia de caracteres opaca que identifica exclusivamente, dentro do escopo de **OwningEntity**, o formato da mensagem.</span><span class="sxs-lookup"><span data-stu-id="a557b-234">An opaque string that uniquely identifies, within the scope of the **OwningEntity**, the format of the message.</span></span> <span data-ttu-id="a557b-235">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-235">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-236">**OtherErrorSourceFormat**</span><span class="sxs-lookup"><span data-stu-id="a557b-236">**OtherErrorSourceFormat**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-237">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-238">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-239">Uma cadeia de caracteres que define "other" valores para **ErrorSourceFormat**.</span><span class="sxs-lookup"><span data-stu-id="a557b-239">A string defining "Other" values for **ErrorSourceFormat**.</span></span> <span data-ttu-id="a557b-240">Esse valor deve ser definido como um valor não nulo quando **ErrorSourceFormat** é definido como um valor de 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="a557b-240">This value must be set to a non-NULL value when **ErrorSourceFormat** is set to a value of 1 (Other).</span></span> <span data-ttu-id="a557b-241">Para todos os outros valores de **ErrorSourceFormat**, o valor dessa cadeia de caracteres deve ser definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="a557b-241">For all other values of **ErrorSourceFormat**, the value of this string must be set to **Null**.</span></span> <span data-ttu-id="a557b-242">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-242">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-243">**OtherErrorType**</span><span class="sxs-lookup"><span data-stu-id="a557b-243">**OtherErrorType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-244">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-244">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-245">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-245">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-246">Uma cadeia de caracteres que descreve o **ErrorType** quando 1, (Other), é especificado como **ErrorType**.</span><span class="sxs-lookup"><span data-stu-id="a557b-246">A string that describes the **ErrorType** when 1, (Other), is specified as the **ErrorType**.</span></span> <span data-ttu-id="a557b-247">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-247">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-248">**OwningEntity**</span><span class="sxs-lookup"><span data-stu-id="a557b-248">**OwningEntity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-249">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-249">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-250">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-250">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-251">Uma cadeia de caracteres que identifica exclusivamente a entidade que possui a definição do formato da mensagem descrita nesta instância.</span><span class="sxs-lookup"><span data-stu-id="a557b-251">A string that uniquely identifies the entity that owns the definition of the format of the message described in this instance.</span></span> <span data-ttu-id="a557b-252">**OwningEntity** deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios ou ao corpo de padrões que define o formato.</span><span class="sxs-lookup"><span data-stu-id="a557b-252">**OwningEntity** must include a copyrighted, trademarked, or otherwise unique name that is owned by the business entity or standards body defining the format.</span></span> <span data-ttu-id="a557b-253">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-253">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-254">**PerceivedSeverity**</span><span class="sxs-lookup"><span data-stu-id="a557b-254">**PerceivedSeverity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-255">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a557b-255">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-256">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-256">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-257">Um valor enumerado que descreve a severidade do erro do ponto de vista do notificador: 2-baixo deve ser usado para problemas não críticos, como parâmetros inválidos, uso incorreto e funcionalidade sem suporte.</span><span class="sxs-lookup"><span data-stu-id="a557b-257">An enumerated value that describes the severity of the error from the notifier's point of view: 2 - Low should be used for noncritical issues such as invalid parameters, incorrect usage, unsupported functionality.</span></span> <span data-ttu-id="a557b-258">3-médio deve ser usado para indicar que a ação é necessária, mas a situação não é séria no momento.</span><span class="sxs-lookup"><span data-stu-id="a557b-258">3 - Medium should be used to indicate action is needed, but the situation is not serious at this time.</span></span> <span data-ttu-id="a557b-259">4-alto deve ser usado para indicar que a ação é necessária agora.</span><span class="sxs-lookup"><span data-stu-id="a557b-259">4 - High should be used to indicate action is needed now.</span></span> <span data-ttu-id="a557b-260">5-fatal deve ser usado para indicar uma perda de dados ou falha de serviço ou sistema irrecuperável.</span><span class="sxs-lookup"><span data-stu-id="a557b-260">5 - Fatal should be used to indicate a loss of data or unrecoverable system or service failure.</span></span> <span data-ttu-id="a557b-261">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-261">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a557b-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a557b-262"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (2)</span><span class="sxs-lookup"><span data-stu-id="a557b-263"><span id="Low"></span><span id="low"></span><span id="LOW"></span>**Low** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Médio** (3)</span><span class="sxs-lookup"><span data-stu-id="a557b-264"><span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Medium** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alta** (4)</span><span class="sxs-lookup"><span data-stu-id="a557b-265"><span id="High"></span><span id="high"></span><span id="HIGH"></span>**High** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5)</span><span class="sxs-lookup"><span data-stu-id="a557b-266"><span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a557b-267">**ProbableCause**</span><span class="sxs-lookup"><span data-stu-id="a557b-267">**ProbableCause**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-268">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a557b-268">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-269">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-270">Um valor enumerado que descreve a causa provável do erro.</span><span class="sxs-lookup"><span data-stu-id="a557b-270">An enumerated value that describes the probable cause of the error.</span></span> <span data-ttu-id="a557b-271">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-271">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="a557b-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="a557b-272"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="a557b-273"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Erro de adaptador/placa** (2)</span><span class="sxs-lookup"><span data-stu-id="a557b-274"><span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Adapter/Card Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Falha no subsistema do aplicativo** (3)</span><span class="sxs-lookup"><span data-stu-id="a557b-275"><span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Application Subsystem Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Largura de banda reduzida** (4)</span><span class="sxs-lookup"><span data-stu-id="a557b-276"><span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Bandwidth Reduced** (4)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Erro de estabelecimento de conexão** (5)</span><span class="sxs-lookup"><span data-stu-id="a557b-277"><span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Connection Establishment Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Erro de protocolo de comunicação** (6)</span><span class="sxs-lookup"><span data-stu-id="a557b-278"><span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Communications Protocol Error** (6)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Falha no subsistema de comunicações** (7)</span><span class="sxs-lookup"><span data-stu-id="a557b-279"><span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Communications Subsystem Failure** (7)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Erro de configuração/personalização** (8)</span><span class="sxs-lookup"><span data-stu-id="a557b-280"><span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Configuration/Customization Error** (8)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestionamento** (9)</span><span class="sxs-lookup"><span data-stu-id="a557b-281"><span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestion** (9)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Dados corrompidos** (10)</span><span class="sxs-lookup"><span data-stu-id="a557b-282"><span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Corrupt Data** (10)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Limite de ciclos de CPU excedido** (11)</span><span class="sxs-lookup"><span data-stu-id="a557b-283"><span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**CPU Cycles Limit Exceeded** (11)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Erro de conjunto de/DataSet** (12)</span><span class="sxs-lookup"><span data-stu-id="a557b-284"><span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Dataset/Modem Error** (12)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Sinal degradado** (13)</span><span class="sxs-lookup"><span data-stu-id="a557b-285"><span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Degraded Signal** (13)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-erro de interface de DCE** (14)</span><span class="sxs-lookup"><span data-stu-id="a557b-286"><span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**DTE-DCE Interface Error** (14)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Porta do compartimento aberta** (15)</span><span class="sxs-lookup"><span data-stu-id="a557b-287"><span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Enclosure Door Open** (15)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Mau funcionamento do equipamento** (16)</span><span class="sxs-lookup"><span data-stu-id="a557b-288"><span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Equipment Malfunction** (16)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Vibração excessiva** (17)</span><span class="sxs-lookup"><span data-stu-id="a557b-289"><span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Excessive Vibration** (17)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Erro de formato de arquivo** (18)</span><span class="sxs-lookup"><span data-stu-id="a557b-290"><span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**File Format Error** (18)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Incêndio detectado** (19)</span><span class="sxs-lookup"><span data-stu-id="a557b-291"><span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Inundação detectada** (20)</span><span class="sxs-lookup"><span data-stu-id="a557b-292"><span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Flood Detected** (20)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Erro de enquadramento** (21)</span><span class="sxs-lookup"><span data-stu-id="a557b-293"><span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Framing Error** (21)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Problema de HVAC** (22)</span><span class="sxs-lookup"><span data-stu-id="a557b-294"><span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**HVAC Problem** (22)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Umidade inaceitável** (23)</span><span class="sxs-lookup"><span data-stu-id="a557b-295"><span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Humidity Unacceptable** (23)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Erro de dispositivo de e/s** (24)</span><span class="sxs-lookup"><span data-stu-id="a557b-296"><span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**I/O Device Error** (24)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Erro de dispositivo de entrada** (25)</span><span class="sxs-lookup"><span data-stu-id="a557b-297"><span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Input Device Error** (25)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Erro de LAN** (26)</span><span class="sxs-lookup"><span data-stu-id="a557b-298"><span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**LAN Error** (26)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Vazamento não tóxicos detectado** (27)</span><span class="sxs-lookup"><span data-stu-id="a557b-299"><span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Non-Toxic Leak Detected** (27)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Erro de transmissão do nó local** (28)</span><span class="sxs-lookup"><span data-stu-id="a557b-300"><span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Local Node Transmission Error** (28)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Perda de quadro** (29)</span><span class="sxs-lookup"><span data-stu-id="a557b-301"><span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Loss of Frame** (29)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Perda de sinal** (30)</span><span class="sxs-lookup"><span data-stu-id="a557b-302"><span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Loss of Signal** (30)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**31 fornecimento de material esgotado** (31)</span><span class="sxs-lookup"><span data-stu-id="a557b-303"><span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Material Supply Exhausted** (31)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Problema do Multiplexador** (32)</span><span class="sxs-lookup"><span data-stu-id="a557b-304"><span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Multiplexer Problem** (32)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Memória insuficiente** (33)</span><span class="sxs-lookup"><span data-stu-id="a557b-305"><span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Out of Memory** (33)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Erro do dispositivo de saída** (34)</span><span class="sxs-lookup"><span data-stu-id="a557b-306"><span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Output Device Error** (34)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Desempenho degradado** (35)</span><span class="sxs-lookup"><span data-stu-id="a557b-307"><span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Performance Degraded** (35)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Problema de energia** (36)</span><span class="sxs-lookup"><span data-stu-id="a557b-308"><span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Power Problem** (36)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressão inaceitável** (37)</span><span class="sxs-lookup"><span data-stu-id="a557b-309"><span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressure Unacceptable** (37)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Problema do processador (erro interno da máquina)** (38)</span><span class="sxs-lookup"><span data-stu-id="a557b-310"><span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Processor Problem (Internal Machine Error)** (38)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Falha de bomba** (39)</span><span class="sxs-lookup"><span data-stu-id="a557b-311"><span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Pump Failure** (39)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Tamanho da fila excedido** (40)</span><span class="sxs-lookup"><span data-stu-id="a557b-312"><span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Queue Size Exceeded** (40)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Falha de recebimento** (41)</span><span class="sxs-lookup"><span data-stu-id="a557b-313"><span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Receive Failure** (41)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Falha do receptor** (42)</span><span class="sxs-lookup"><span data-stu-id="a557b-314"><span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Receiver Failure** (42)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Erro de transmissão de nó remoto** (43)</span><span class="sxs-lookup"><span data-stu-id="a557b-315"><span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Remote Node Transmission Error** (43)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Recurso na capacidade ou perto** (44)</span><span class="sxs-lookup"><span data-stu-id="a557b-316"><span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Resource at or Nearing Capacity** (44)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Tempo de resposta excessivo** (45)</span><span class="sxs-lookup"><span data-stu-id="a557b-317"><span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Response Time Excessive** (45)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Taxa de retransmissão excessiva** (46)</span><span class="sxs-lookup"><span data-stu-id="a557b-318"><span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Retransmission Rate Excessive** (46)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Erro de software** (47)</span><span class="sxs-lookup"><span data-stu-id="a557b-319"><span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Software Error** (47)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Programa de software encerrado** de forma anormal (48)</span><span class="sxs-lookup"><span data-stu-id="a557b-320"><span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Software Program Abnormally Terminated** (48)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Erro do programa de software (resultados incorretos)** (49)</span><span class="sxs-lookup"><span data-stu-id="a557b-321"><span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Software Program Error (Incorrect Results)** (49)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Problema de capacidade de armazenamento** (50)</span><span class="sxs-lookup"><span data-stu-id="a557b-322"><span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Storage Capacity Problem** (50)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatura inaceitável** (51)</span><span class="sxs-lookup"><span data-stu-id="a557b-323"><span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperature Unacceptable** (51)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Limite ultrapassado** (52)</span><span class="sxs-lookup"><span data-stu-id="a557b-324"><span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Threshold Crossed** (52)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Problema de tempo** (53)</span><span class="sxs-lookup"><span data-stu-id="a557b-325"><span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Timing Problem** (53)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Vazamento de tóxicos detectado** (54)</span><span class="sxs-lookup"><span data-stu-id="a557b-326"><span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Toxic Leak Detected** (54)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Falha de transmissão** (55)</span><span class="sxs-lookup"><span data-stu-id="a557b-327"><span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Transmit Failure** (55)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Falha do transmissor** (56)</span><span class="sxs-lookup"><span data-stu-id="a557b-328"><span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Transmitter Failure** (56)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Recurso subjacente não disponível** (57)</span><span class="sxs-lookup"><span data-stu-id="a557b-329"><span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Underlying Resource Unavailable** (57)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Incompatibilidade de versão** (58)</span><span class="sxs-lookup"><span data-stu-id="a557b-330"><span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Version Mismatch** (58)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior limpo** (59)</span><span class="sxs-lookup"><span data-stu-id="a557b-331"><span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Previous Alert Cleared** (59)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**60 tentativas de logon com falha** (60)</span><span class="sxs-lookup"><span data-stu-id="a557b-332"><span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Login Attempts Failed** (60)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Vírus de software detectado** (61)</span><span class="sxs-lookup"><span data-stu-id="a557b-333"><span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Software Virus Detected** (61)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Segurança de hardware violada** (62)</span><span class="sxs-lookup"><span data-stu-id="a557b-334"><span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Hardware Security Breached** (62)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Negação de serviço detectada** (63)</span><span class="sxs-lookup"><span data-stu-id="a557b-335"><span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Denial of Service Detected** (63)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Incompatibilidade de credencial de segurança** (64)</span><span class="sxs-lookup"><span data-stu-id="a557b-336"><span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Security Credential Mismatch** (64)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Acesso não autorizado** (65)</span><span class="sxs-lookup"><span data-stu-id="a557b-337"><span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Unauthorized Access** (65)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarme recebido** (66)</span><span class="sxs-lookup"><span data-stu-id="a557b-338"><span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarm Received** (66)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Perda de ponteiro** (67)</span><span class="sxs-lookup"><span data-stu-id="a557b-339"><span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Loss of Pointer** (67)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Incompatibilidade de carga** (68)</span><span class="sxs-lookup"><span data-stu-id="a557b-340"><span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Payload Mismatch** (68)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Erro de transmissão** (69)</span><span class="sxs-lookup"><span data-stu-id="a557b-341"><span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Transmission Error** (69)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Taxa de erros excessivas** (70)</span><span class="sxs-lookup"><span data-stu-id="a557b-342"><span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Excessive Error Rate** (70)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Problema de rastreamento** (71)</span><span class="sxs-lookup"><span data-stu-id="a557b-343"><span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Trace Problem** (71)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Elemento não disponível** (72)</span><span class="sxs-lookup"><span data-stu-id="a557b-344"><span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Element Unavailable** (72)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Elemento ausente** (73)</span><span class="sxs-lookup"><span data-stu-id="a557b-345"><span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Element Missing** (73)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Perda de vários quadros** (74)</span><span class="sxs-lookup"><span data-stu-id="a557b-346"><span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Loss of Multi Frame** (74)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Falha no canal de difusão** (75)</span><span class="sxs-lookup"><span data-stu-id="a557b-347"><span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Broadcast Channel Failure** (75)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Mensagem inválida recebida** (76)</span><span class="sxs-lookup"><span data-stu-id="a557b-348"><span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Invalid Message Received** (76)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Falha de roteamento** (77)</span><span class="sxs-lookup"><span data-stu-id="a557b-349"><span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Routing Failure** (77)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Falha no backplane** (78)</span><span class="sxs-lookup"><span data-stu-id="a557b-350"><span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Backplane Failure** (78)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Duplicação de identificador** (79)</span><span class="sxs-lookup"><span data-stu-id="a557b-351"><span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Identifier Duplication** (79)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Falha no caminho de proteção** (80)</span><span class="sxs-lookup"><span data-stu-id="a557b-352"><span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Protection Path Failure** (80)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Perda de sincronização ou incompatibilidade** (81)</span><span class="sxs-lookup"><span data-stu-id="a557b-353"><span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Sync Loss or Mismatch** (81)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Problema de terminal** (82)</span><span class="sxs-lookup"><span data-stu-id="a557b-354"><span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Terminal Problem** (82)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Falha no relógio em tempo real** (83)</span><span class="sxs-lookup"><span data-stu-id="a557b-355"><span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Real Time Clock Failure** (83)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Falha de antena** (84)</span><span class="sxs-lookup"><span data-stu-id="a557b-356"><span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Antenna Failure** (84)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Falha no carregamento da bateria** (85)</span><span class="sxs-lookup"><span data-stu-id="a557b-357"><span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Battery Charging Failure** (85)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Falha de disco** (86)</span><span class="sxs-lookup"><span data-stu-id="a557b-358"><span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Disk Failure** (86)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Falha de salto de frequência** (87)</span><span class="sxs-lookup"><span data-stu-id="a557b-359"><span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Frequency Hopping Failure** (87)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Perda de redundância** (88)</span><span class="sxs-lookup"><span data-stu-id="a557b-360"><span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Loss of Redundancy** (88)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Falha da fonte de energia** (89)</span><span class="sxs-lookup"><span data-stu-id="a557b-361"><span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Power Supply Failure** (89)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Problema de qualidade de sinal** (90)</span><span class="sxs-lookup"><span data-stu-id="a557b-362"><span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Signal Quality Problem** (90)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>(91) **descarregamento da bateria de 91**</span><span class="sxs-lookup"><span data-stu-id="a557b-363"><span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Battery Discharging** (91)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Falha da bateria** (92)</span><span class="sxs-lookup"><span data-stu-id="a557b-364"><span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Battery Failure** (92)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Problema de energia comercial** (93)</span><span class="sxs-lookup"><span data-stu-id="a557b-365"><span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Commercial Power Problem** (93)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Falha do ventilador** (94)</span><span class="sxs-lookup"><span data-stu-id="a557b-366"><span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Fan Failure** (94)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Falha do mecanismo** (95)</span><span class="sxs-lookup"><span data-stu-id="a557b-367"><span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Engine Failure** (95)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Falha do sensor** (96)</span><span class="sxs-lookup"><span data-stu-id="a557b-368"><span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Sensor Failure** (96)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Falha de fusível** (97)</span><span class="sxs-lookup"><span data-stu-id="a557b-369"><span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Fuse Failure** (97)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Falha do gerador** (98)</span><span class="sxs-lookup"><span data-stu-id="a557b-370"><span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Generator Failure** (98)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Bateria fraca** (99)</span><span class="sxs-lookup"><span data-stu-id="a557b-371"><span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Low Battery** (99)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Baixo combustível** (100)</span><span class="sxs-lookup"><span data-stu-id="a557b-372"><span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Low Fuel** (100)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Água inferior** (101)</span><span class="sxs-lookup"><span data-stu-id="a557b-373"><span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Low Water** (101)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gás explosivo** (102)</span><span class="sxs-lookup"><span data-stu-id="a557b-374"><span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Explosive Gas** (102)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Altos ventos** (103)</span><span class="sxs-lookup"><span data-stu-id="a557b-375"><span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**High Winds** (103)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Acúmulo de gelo** (104)</span><span class="sxs-lookup"><span data-stu-id="a557b-376"><span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Ice Buildup** (104)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Fumaça** (105)</span><span class="sxs-lookup"><span data-stu-id="a557b-377"><span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Incompatibilidade de memória** (106)</span><span class="sxs-lookup"><span data-stu-id="a557b-378"><span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Memory Mismatch** (106)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Ciclos de CPU insuficientes** (107)</span><span class="sxs-lookup"><span data-stu-id="a557b-379"><span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Out of CPU Cycles** (107)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Problema de ambiente de software** (108)</span><span class="sxs-lookup"><span data-stu-id="a557b-380"><span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Software Environment Problem** (108)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Falha de download de software** (109)</span><span class="sxs-lookup"><span data-stu-id="a557b-381"><span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Software Download Failure** (109)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Elemento reinicializado** (110)</span><span class="sxs-lookup"><span data-stu-id="a557b-382"><span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Element Reinitialized** (110)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Tempo limite** (111)</span><span class="sxs-lookup"><span data-stu-id="a557b-383"><span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Timeout** (111)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Problemas de log** (112)</span><span class="sxs-lookup"><span data-stu-id="a557b-384"><span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Logging Problems** (112)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Vazamento detectado** (113)</span><span class="sxs-lookup"><span data-stu-id="a557b-385"><span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Leak Detected** (113)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Falha no mecanismo de proteção** (114)</span><span class="sxs-lookup"><span data-stu-id="a557b-386"><span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Protection Mechanism Failure** (114)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**115 proteção de falha de recurso** (115)</span><span class="sxs-lookup"><span data-stu-id="a557b-387"><span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protecting Resource Failure** (115)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Inconsistência do banco de dados** (116)</span><span class="sxs-lookup"><span data-stu-id="a557b-388"><span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Database Inconsistency** (116)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Falha de autenticação** (117)</span><span class="sxs-lookup"><span data-stu-id="a557b-389"><span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Authentication Failure** (117)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Violação de confidencialidade** (118)</span><span class="sxs-lookup"><span data-stu-id="a557b-390"><span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Breach of Confidentiality** (118)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Adulteração de cabo** (119)</span><span class="sxs-lookup"><span data-stu-id="a557b-391"><span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Cable Tamper** (119)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Informações atrasadas** (120)</span><span class="sxs-lookup"><span data-stu-id="a557b-392"><span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Delayed Information** (120)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Informações duplicadas** (121)</span><span class="sxs-lookup"><span data-stu-id="a557b-393"><span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Duplicate Information** (121)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Informações ausentes** (122)</span><span class="sxs-lookup"><span data-stu-id="a557b-394"><span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Information Missing** (122)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Modificação de informações** (123)</span><span class="sxs-lookup"><span data-stu-id="a557b-395"><span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Information Modification** (123)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informações fora de sequência** (124)</span><span class="sxs-lookup"><span data-stu-id="a557b-396"><span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Information Out of Sequence** (124)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Chave expirada** (125)</span><span class="sxs-lookup"><span data-stu-id="a557b-397"><span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Key Expired** (125)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Falha de não repúdio** (126)</span><span class="sxs-lookup"><span data-stu-id="a557b-398"><span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Non-Repudiation Failure** (126)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Atividade fora de horas** (127)</span><span class="sxs-lookup"><span data-stu-id="a557b-399"><span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Out of Hours Activity** (127)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Fora de serviço** (128)</span><span class="sxs-lookup"><span data-stu-id="a557b-400"><span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Out of Service** (128)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Erro de procedimento** (129)</span><span class="sxs-lookup"><span data-stu-id="a557b-401"><span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Procedural Error** (129)</span></span>
</dt> <dt>

<span data-ttu-id="a557b-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Informações inesperadas** (130)</span><span class="sxs-lookup"><span data-stu-id="a557b-402"><span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Unexpected Information** (130 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a557b-403">**ProbableCauseDescription**</span><span class="sxs-lookup"><span data-stu-id="a557b-403">**ProbableCauseDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-404">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-404">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a557b-405">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-405">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-406">Uma cadeia de caracteres que descreve a causa provável do erro.</span><span class="sxs-lookup"><span data-stu-id="a557b-406">A string that describes the probable cause of the error.</span></span> <span data-ttu-id="a557b-407">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-407">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a557b-408">**RecommendedActions**</span><span class="sxs-lookup"><span data-stu-id="a557b-408">**RecommendedActions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a557b-409">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a557b-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a557b-410">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a557b-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a557b-411">Uma cadeia de caracteres que descreve as ações recomendadas a serem executadas para resolver o erro.</span><span class="sxs-lookup"><span data-stu-id="a557b-411">A string that describes recommended actions to take to resolve the error.</span></span> <span data-ttu-id="a557b-412">Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a557b-412">This property is inherited from [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a557b-413">Comentários</span><span class="sxs-lookup"><span data-stu-id="a557b-413">Remarks</span></span>

<span data-ttu-id="a557b-414">O acesso à classe de **\_ erro Msvm** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="a557b-414">Access to the **Msvm\_Error** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a557b-415">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a557b-415">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="a557b-416">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a557b-416">Requirements</span></span>



| <span data-ttu-id="a557b-417">Requisito</span><span class="sxs-lookup"><span data-stu-id="a557b-417">Requirement</span></span> | <span data-ttu-id="a557b-418">Valor</span><span class="sxs-lookup"><span data-stu-id="a557b-418">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a557b-419">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a557b-419">Minimum supported client</span></span><br/> | <span data-ttu-id="a557b-420">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a557b-420">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a557b-421">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a557b-421">Minimum supported server</span></span><br/> | <span data-ttu-id="a557b-422">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a557b-422">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a557b-423">Namespace</span><span class="sxs-lookup"><span data-stu-id="a557b-423">Namespace</span></span><br/>                | <span data-ttu-id="a557b-424">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a557b-424">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a557b-425">MOF</span><span class="sxs-lookup"><span data-stu-id="a557b-425">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a557b-426"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-426"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a557b-427">DLL</span><span class="sxs-lookup"><span data-stu-id="a557b-427">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a557b-428"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a557b-428"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a557b-429">Confira também</span><span class="sxs-lookup"><span data-stu-id="a557b-429">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a557b-430">**Erro de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="a557b-430">**CIM\_Error**</span></span>](cim-error.md)
</dt> <dt>

<span data-ttu-id="a557b-431">[**Erro de CIM \_**](/previous-versions//cc150671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a557b-431">[**CIM\_Error**](/previous-versions//cc150671(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="a557b-432">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="a557b-432">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

