---
description: A classe De erro CIM \_ contém informações sobre a falha de uma operação CIM.
ms.assetid: 35acecbd-b972-45b4-9616-2047bba8fd41
title: CIM_Error classe
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
ms.openlocfilehash: 1c7e7fba10cb507e1288344637c944bb56d62dc4c9eaaf909a980ceaf3250440
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695966"
---
# <a name="cim_error-class"></a>Classe de erro CIM \_

A **classe De \_ erro CIM** contém informações sobre a falha de uma operação CIM.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe De \_ erro CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ erro CIM** tem essas propriedades.

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. ERRO DE \| DMTF. CODE \| 2.3", "DSP0200. DMTF \| CIMError \| 1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**CIMStatusCodeDescription**")
</dt> </dl>

O código de status CIM que caracteriza essa instância. Essa propriedade define os códigos de status que podem ser retornadas por um servidor CIM ou ouvinte.

<dt>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>

<span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span>**CIM \_ ERR \_ FAILED** (1)


</dt> <dd>

Ocorreu um erro geral que não é coberto por um código de erro mais específico.

</dd> <dt>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>

<span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span>**CIM \_ ERR \_ ACCESS \_ NEGADO** (2)


</dt> <dd>

O acesso a um recurso CIM não estava disponível para o cliente.

</dd> <dt>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>

<span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span>**CIM \_ ERR \_ \_ NAMESPACE INVÁLIDO** (3)


</dt> <dd>

O namespace de destino não existe.

</dd> <dt>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>

<span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span>**CIM \_ PARÂMETRO \_ INVÁLIDO \_ ERR** (4)


</dt> <dd>

Um ou mais valores de parâmetro passados para o método eram inválidos.

</dd> <dt>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>

<span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span>**CIM \_ CLASSE \_ ERR \_ INVÁLIDA** (5)


</dt> <dd>

A Classe especificada não existe.

</dd> <dt>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>

<span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span>**CIM \_ ERR \_ NOT \_ FOUND** (6)


</dt> <dd>

Não foi possível encontrar o objeto solicitado.

</dd> <dt>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>

<span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span>**CIM \_ ERR \_ SEM \_ SUPORTE** (7)


</dt> <dd>

Não há suporte para a operação solicitada.

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>

<span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span>**CIM \_ A CLASSE ERR \_ \_ TEM \_ FILHOS** (8)


</dt> <dd>

A operação não pode ser executada nessa classe, pois ela tem instâncias.

</dd> <dt>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>

<span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span>**CIM \_ A CLASSE ERR \_ \_ TEM \_ INSTÂNCIAS** (9)


</dt> <dd>

A operação não pode ser executada nessa classe, pois ela tem instâncias.

</dd> <dt>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>

<span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span>**CIM \_ ERR \_ \_ INVALID SUPERCLASS** (10)


</dt> <dd>

A operação não pode ser executada, pois a superclasse especificada não existe.

</dd> <dt>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>

<span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span>**CIM \_ ERR \_ JÁ \_ EXISTE** (11)


</dt> <dd>

A operação não pode ser executada porque um objeto já existe.

</dd> <dt>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>

<span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span>**CIM \_ ERR \_ NO \_ SUCH \_ PROPERTY** (12)


</dt> <dd>

A Propriedade especificada não existe.

</dd> <dt>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>

<span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span>**CIM \_ ERR \_ TYPE \_ MISMATCH** (13)


</dt> <dd>

O valor fornecido é incompatível com o tipo .

</dd> <dt>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>

<span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span>**CIM \_ ERR \_ QUERY \_ LANGUAGE NOT \_ \_ SUPPORTED** (14)


</dt> <dd>

Não há suporte para a linguagem de consulta.

</dd> <dt>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>

<span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span>**CIM \_ CONSULTA \_ \_ INVÁLIDA ERR** (15)


</dt> <dd>

A consulta não é válida para a linguagem de consulta especificada.

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>

<span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span>**CIM \_ MÉTODO ERR \_ \_ NÃO \_ DISPONÍVEL** (16)


</dt> <dd>

Não foi possível executar o método extrídico.

</dd> <dt>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>

<span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span>**CIM \_ MÉTODO ERR \_ \_ NÃO \_ ENCONTRADO** (17)


</dt> <dd>

O Método extrítico especificado não existe.

</dd> <dt>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>

<span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span>**CIM \_ RESPOSTA \_ INESPERADA \_ ERR** (18)


</dt> <dd>

A resposta retornada à operação assíncrona não era esperada.

</dd> <dt>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>

<span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span>**CIM \_ ERR \_ INVALID \_ RESPONSE \_ DESTINATION** (19)


</dt> <dd>

O destino especificado para a resposta assíncrona não é válido.

</dd> <dt>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>

<span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span>**CIM \_ NAMESPACE \_ ERR \_ NÃO \_ VAZIO** (20)


</dt> <dd>

O Namespace especificado não está vazio.

</dd> <dt>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>

<span id="CIM_ERR_INVALID_ENUMERATION_CONTEXT"></span><span id="cim_err_invalid_enumeration_context"></span>**CIM \_ ERR \_ INVALID \_ ENUMERATION \_ CONTEXT** (21)


</dt> <dd>

O contexto de enumeração fornecido não é válido.

</dd> <dt>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>

<span id="CIM_ERR_INVALID_OPERATION_TIMEOUT"></span><span id="cim_err_invalid_operation_timeout"></span>**CIM \_ ERR \_ INVALID \_ OPERATION \_ TIMEOUT** (22)


</dt> <dd>

O Namespace especificado não está vazio.

</dd> <dt>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>

<span id="CIM_ERR_PULL_HAS_BEEN_ABANDONED"></span><span id="cim_err_pull_has_been_abandoned"></span>**CIM \_ ERR \_ PULL \_ FOI \_ \_ ABANDONADO** (23)


</dt> <dd>

O Namespace especificado não está vazio.

</dd> <dt>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>

<span id="CIM_ERR_PULL_CANNOT_BE_ABANDONED"></span><span id="cim_err_pull_cannot_be_abandoned"></span>**CIM \_ ERR \_ PULL NÃO PODE SER \_ \_ \_ ABANDONADO** (24)


</dt> <dd>

Falha na tentativa de abandonar uma operação de pull.

</dd> <dt>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>

<span id="CIM_ERR_FILTERED_ENUMERATION_NOT_SUPPORTED"></span><span id="cim_err_filtered_enumeration_not_supported"></span>**CIM \_ \_ENUMERAÇÃO \_ FILTRADA ERR \_ SEM \_ SUPORTE** (25)


</dt> <dd>

Não há suporte para Enumeratrions filtrados.

</dd> <dt>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>

<span id="CIM_ERR_CONTINUATION_ON_ERROR_NOT_SUPPORTED"></span><span id="cim_err_continuation_on_error_not_supported"></span>**CIM \_ ERR \_ CONTINUATION \_ ON ERROR \_ NOT \_ \_ SUPPORTED** (26)


</dt> <dd>

Não há suporte para continuar com o erro.

</dd> <dt>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>

<span id="CIM_ERR_SERVER_LIMITS_EXCEEDED"></span><span id="cim_err_server_limits_exceeded"></span>**CIM \_ LIMITES \_ DE SERVIDOR ERR \_ \_ EXCEDIDO** (27)


</dt> <dd>

Os limites do servidor WBEM foram excedido (por exemplo, memória, conexões, ...).

</dd> <dt>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>

<span id="CIM_ERR_SERVER_IS_SHUTTING_DOWN"></span><span id="cim_err_server_is_shutting_down"></span>**CIM \_ O \_ SERVIDOR ERR ESTÁ \_ \_ \_ DESLIGANDO** (28)


</dt> <dd>

O servidor WBEM está sendo desligado.

</dd> <dt>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>

<span id="CIM_ERR_QUERY_FEATURE_NOT_SUPPORTED"></span><span id="cim_err_query_feature_not_supported"></span>**CIM \_ RECURSO \_ ERR \_ QUERY NÃO TEM \_ \_ SUPORTE** (29)


</dt> <dd>

Não há suporte para o Recurso de Consulta especificado.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("DSP0201. ERRO DE \| DMTF. DESCRIPTION \| 2.3", "DSP0200. DMTF \| CIMError \| 1.3"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**CIMStatusCode**")
</dt> </dl>

Uma cadeia de caracteres de forma livre que contém uma descrição acessível por humanos do **valor da propriedade CIMStatusCode.**

> [!Note]  
> Essa descrição pode se estender, mas deve ser consistente com a definição de **CIMStatusCode**.

 

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**ErrorSourceFormat**")
</dt> </dl>

Informações que identificam a entidade que gerou o erro. Se a entidade for modelada pelo esquema CIM, essa propriedade conterá o caminho para a instância codificada como um parâmetro de cadeia de caracteres. Caso contrário, a propriedade conterá uma cadeia de caracteres que nomeia a entidade que gerou o erro. O formato dessa propriedade é especificado pela **propriedade ErrorSourceFormat.**

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**ErrorSource**", "**Erro CIM \_**.**OtherErrorSourceFormat**")
</dt> </dl>

O formato da **propriedade ErrorSource.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

O formato é desconhecido ou não pode ser interpretado significativamente por um aplicativo cliente CIM.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd>

O formato é definido pelo valor da **propriedade OtherErrorSourceFormat.**

</dd> <dt>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>

<span id="CIMObjectPath"></span><span id="cimobjectpath"></span><span id="CIMOBJECTPATH"></span>**CIMObjectPath** (2)


</dt> <dd>

Um Caminho do Objeto CIM conforme definido na especificação da Infraestrutura cim.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**OtherErrorType**")
</dt> </dl>

O tipo de erro primário.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>

<span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span>**Erro de comunicação** (2)


</dt> <dd>

Erros desse tipo são associados principalmente aos procedimentos e/ou processos necessários para transmitir informações de um ponto para outro.

</dd> <dt>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>

<span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span>**Erro de qualidade de serviço** (3)


</dt> <dd>

Erros desse tipo são associados principalmente a falhas que resultam em funcionalidade ou desempenho reduzidos.

</dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Erro de software** (4)


</dt> <dd>

O erro desse tipo está associado principalmente a um software ou falha de processamento.

</dd> <dt>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>

<span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span>**Erro de hardware** (5)


</dt> <dd>

Erros desse tipo são associados principalmente a uma falha de equipamento ou hardware.

</dd> <dt>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>

<span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span>**Erro ambiental** (6)


</dt> <dd>

outras considerações sobre o ambiente.

</dd> <dt>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>

<span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span>**Erro de segurança** (7)


</dt> <dd>

Erros desse tipo estão associados a violações de segurança, detecção de vírus e problemas semelhantes.

</dd> <dt>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>

<span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span>**Erro de excesso de assinatura** (8)


</dt> <dd>

Os erros desse tipo estão principalmente associados à falha ao alocar recursos suficientes para concluir a operação.

</dd> <dt>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>

<span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span>**Erro de recurso indisponível** (9)


</dt> <dd>

Erros desse tipo são associados principalmente à falha ao acessar um recurso necessário.

</dd> <dt>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>

<span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span>**Erro de operação sem suporte** (10)


</dt> <dd>

Erros desse tipo são associados principalmente a solicitações sem suporte.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**MessageID**", "**Erro CIM \_**.**MessageArguments**")
</dt> </dl>

A mensagem formatada.

> [!Note]  
> Essa mensagem é criada combinando elementos dinâmicos da propriedade **MessageArguments** com os elementos estáticos da propriedade **MessageID** e, em seguida, adicionando-os a um registro ou catálogo de mensagens associado ao **OwningEntity**.

 

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**MessageID**", "**Erro CIM \_**.**Mensagem**")
</dt> </dl>

Uma matriz que contém o conteúdo dinâmico da mensagem.

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Obrigatório,**](/windows/desktop/WmiSdk/standard-qualifiers) [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**Mensagem**", "**Erro CIM \_**.**MessageArguments**")
</dt> </dl>

Uma cadeia de caracteres opaca que identifica exclusivamente, dentro do escopo de OwningEntity, o formato da Mensagem.

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**ErrorSourceFormat**")
</dt> </dl>

Uma cadeia de caracteres que define **o valor ErrorSourceFormat** **quando ErrorSourceFormat** é definido como "1" (outro).

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**ErrorType**")
</dt> </dl>

Uma cadeia de caracteres de forma livre que descreve o **valor errorType** quando ele é definido como "1" (outro).

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A ID exclusiva da entidade que possui o formato da mensagem descrita por esta instância.

> [!Note]  
> Essa propriedade deve incluir um nome protegido por direitos autorais, marcas comerciais ou exclusivos pertencentes à entidade de negócios ou ao corpo de padrões que definiu o formato da mensagem.

 

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Severidade percebida")
</dt> </dl>

Uma descrição da severidade do erro do ponto de vista do elemento que enviou a mensagem de erro.

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

**ProvávelCause**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Recommendation.ITU \| X733. Causa provável", "Recommendation.ITU \| M3100.probableCause", "ITU-IANA-ALARM-TC"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Cim \_ Error**.**ProbableCauseDescription**")
</dt> </dl>

Uma descrição da causa provável do erro.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outros** (1)


</dt> <dd></dd> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>

**Erro de adaptador/cartão** (2)


</dt> <dd></dd> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>

**Falha do subsistema do aplicativo** (3)


</dt> <dd></dd> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>

**Largura de banda** reduzida (4)


</dt> <dd></dd> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>

**Erro de estabelecimento de** conexão (5)


</dt> <dd></dd> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>

**Erro de protocolo de** comunicações (6)


</dt> <dd></dd> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>

**Falha do subsistema de comunicações** (7)


</dt> <dd></dd> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>

**Erro de configuração/personalização** (8)


</dt> <dd></dd> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>

**Congestionamento** (9)


</dt> <dd></dd> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>

**Dados corrompidos** (10)


</dt> <dd></dd> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>

**Limite de ciclos de CPU excedido** (11)


</dt> <dd></dd> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>

**Erro de conjuntos de dados/modem** (12)


</dt> <dd></dd> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>

**Sinal degradado** (13)


</dt> <dd></dd> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>

**Erro de interface DTE-DCE** (14)


</dt> <dd></dd> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>

**Porta do compartimento aberta** (15)


</dt> <dd></dd> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>

**Funcionamento do equipamento** (16)


</dt> <dd></dd> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>

**Vibração excessiva** (17)


</dt> <dd></dd> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>

**Erro de formato de** arquivo (18)


</dt> <dd></dd> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>

**Fire Detected** (19)


</dt> <dd></dd> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>

**Inundação detectada** (20)


</dt> <dd></dd> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>

**Erro de enquadramento** (21)


</dt> <dd></dd> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>

**Problema de HVAC** (22)


</dt> <dd></dd> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>

**Umidade inaceitável** (23)


</dt> <dd></dd> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>

**Erro de dispositivo de E/S** (24)


</dt> <dd></dd> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>

**Erro de dispositivo de** entrada (25)


</dt> <dd></dd> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>

**Erro de LAN** (26)


</dt> <dd></dd> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>

**Vazamento não detectado** (27)


</dt> <dd></dd> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>

**Erro de transmissão de nó local** (28)


</dt> <dd></dd> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>

**Perda de quadro** (29)


</dt> <dd></dd> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>

**Perda de sinal** (30)


</dt> <dd></dd> <dt>

<span id="Material_Supply_Exhausted"></span><span id="material_supply_exhausted"></span><span id="MATERIAL_SUPPLY_EXHAUSTED"></span>

**Fornecimento de material esgotado** (31)


</dt> <dd></dd> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>

**Problema de multiplexador** (32)


</dt> <dd></dd> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>

**Memória sem** memória (33)


</dt> <dd></dd> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>

**Erro de dispositivo de saída** (34)


</dt> <dd></dd> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>

**Desempenho degradado** (35)


</dt> <dd></dd> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>

**Problema de energia** (36)


</dt> <dd></dd> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>

**Pressão inaceitável** (37)


</dt> <dd></dd> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>

**Problema do processador (erro interno do computador)** (38)


</dt> <dd></dd> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>

**Falha de bomba** (39)


</dt> <dd></dd> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>

**Tamanho da fila excedido** (40)


</dt> <dd></dd> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>

**Falha de recebimento** (41)


</dt> <dd></dd> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>

**Falha do receptor** (42)


</dt> <dd></dd> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>

**Erro de transmissão de nó remoto** (43)


</dt> <dd></dd> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>

**Recurso em ou capacidade de aproximação** (44)


</dt> <dd></dd> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>

**Tempo de resposta excessivo** (45)


</dt> <dd></dd> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>

**Taxa de retransmissão excessiva** (46)


</dt> <dd></dd> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>

**Erro de software** (47)


</dt> <dd></dd> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>

**Programa de Software encerrado de forma anormal** (48)


</dt> <dd></dd> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>

**Erro do programa de software (resultados incorretos)** (49)


</dt> <dd></dd> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>

**Armazenamento de capacidade** (50)


</dt> <dd></dd> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>

**Temperatura inaceitável** (51)


</dt> <dd></dd> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>

**Limite cruzado** (52)


</dt> <dd></dd> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>

**Problema de tempo** (53)


</dt> <dd></dd> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>

**Vazamento de resíduos detectado** (54)


</dt> <dd></dd> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>

**Falha de transmissão** (55)


</dt> <dd></dd> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>

**Falha do transmissor** (56)


</dt> <dd></dd> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>

**Recurso subjacente indisponível** (57)


</dt> <dd></dd> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>

**Incompatibilidade de versão** (58)


</dt> <dd></dd> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>

**Alerta anterior limpo** (59)


</dt> <dd></dd> <dt>

<span id="Login_Attempts_Failed"></span><span id="login_attempts_failed"></span><span id="LOGIN_ATTEMPTS_FAILED"></span>

**Tentativas de logon com** falha (60)


</dt> <dd></dd> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>

**Vírus de software detectados** (61)


</dt> <dd></dd> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>

**Segurança de hardware violada** (62)


</dt> <dd></dd> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>

**Negação de serviço detectada** (63)


</dt> <dd></dd> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>

**Incompatibilidade de credenciais de segurança** (64)


</dt> <dd></dd> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>

**Acesso não autorizado** (65)


</dt> <dd></dd> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>

**Alarme recebido** (66)


</dt> <dd></dd> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>

**Perda de ponteiro** (67)


</dt> <dd></dd> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>

**Incompatibilidade de carga** (68)


</dt> <dd></dd> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>

**Erro de** transmissão (69)


</dt> <dd></dd> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>

**Taxa de erro excessiva** (70)


</dt> <dd></dd> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>

**Problema de rastreamento** (71)


</dt> <dd></dd> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>

**Elemento Indisponível** (72)


</dt> <dd></dd> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>

**Elemento Missing** (73)


</dt> <dd></dd> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>

**Perda de vários quadros** (74)


</dt> <dd></dd> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>

**Falha de canal de** difusão (75)


</dt> <dd></dd> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>

**Mensagem inválida recebida** (76)


</dt> <dd></dd> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>

**Falha de roteamento** (77)


</dt> <dd></dd> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>

**Falha de backplane** (78)


</dt> <dd></dd> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>

**Duplicação do identificador** (79)


</dt> <dd></dd> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>

**Falha no caminho de** proteção (80)


</dt> <dd></dd> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>

**Perda de sincronização ou incompatibilidade** (81)


</dt> <dd></dd> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>

**Problema de terminal** (82)


</dt> <dd></dd> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>

**Falha no relógio em tempo real** (83)


</dt> <dd></dd> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>

**Falha de antena** (84)


</dt> <dd></dd> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>

**Falha de carregamento da bateria** (85)


</dt> <dd></dd> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>

**Falha de** disco (86)


</dt> <dd></dd> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>

**Falha de salto de frequência** (87)


</dt> <dd></dd> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>

**Perda de redundância** (88)


</dt> <dd></dd> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>

**Falha na fonte de** alimentação (89)


</dt> <dd></dd> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>

**Problema de qualidade do sinal** (90)


</dt> <dd></dd> <dt>

<span id="Battery_Discharging"></span><span id="battery_discharging"></span><span id="BATTERY_DISCHARGING"></span>

**Descarregamento de bateria** (91)


</dt> <dd></dd> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>

**Falha de bateria** (92)


</dt> <dd></dd> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>

**Problema de energia comercial** (93)


</dt> <dd></dd> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>

**Falha do ventilador** (94)


</dt> <dd></dd> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>

**Falha do** mecanismo (95)


</dt> <dd></dd> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>

**Falha do sensor** (96)


</dt> <dd></dd> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>

**Falha de fuse** (97)


</dt> <dd></dd> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>

**Falha do gerador** (98)


</dt> <dd></dd> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>

**Bateria fraca** (99)


</dt> <dd></dd> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>

**Baixo combustível** (100)


</dt> <dd></dd> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>

**Baixa água** (101)


</dt> <dd></dd> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>

**Gás de artefato** (102)


</dt> <dd></dd> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>

**Altos danos** (103)


</dt> <dd></dd> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>

**Buildup ice** (104)


</dt> <dd></dd> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>

**Smoke** (105)


</dt> <dd></dd> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>

**Incompatibilidade de memória** (106)


</dt> <dd></dd> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>

**Ciclos de CPU fora** (107)


</dt> <dd></dd> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>

**Problema de ambiente de software** (108)


</dt> <dd></dd> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>

**Falha de download de software** (109)


</dt> <dd></dd> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>

**Elemento Reinicializado** (110)


</dt> <dd></dd> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>

**Tempoout** (111)


</dt> <dd></dd> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>

**Problemas de registro** em log (112)


</dt> <dd></dd> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>

**Vazamento detectado** (113)


</dt> <dd></dd> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>

**Falha do mecanismo de** proteção (114)


</dt> <dd></dd> <dt>

<span id="Protecting_Resource_Failure"></span><span id="protecting_resource_failure"></span><span id="PROTECTING_RESOURCE_FAILURE"></span>

**Protegendo a falha de** recursos (115)


</dt> <dd></dd> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>

**Inconsistência** de banco de dados (116)


</dt> <dd></dd> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>

**Falha de autenticação** (117)


</dt> <dd></dd> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>

**Violação de confidencialidade** (118)


</dt> <dd></dd> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>

**Adulteração de** cabo (119)


</dt> <dd></dd> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>

**Informações atrasadas** (120)


</dt> <dd></dd> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>

**Informações duplicadas** (121)


</dt> <dd></dd> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>

**Informações ausentes** (122)


</dt> <dd></dd> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>

**Modificação de** informações (123)


</dt> <dd></dd> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>

**Informações fora de sequência** (124)


</dt> <dd></dd> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>

**Chave expirada** (125)


</dt> <dd></dd> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>

**Falha de não repúdio** (126)


</dt> <dd></dd> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>

**Atividade fora do horário** comercial (127)


</dt> <dd></dd> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>

**Fora de serviço** (128)


</dt> <dd></dd> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>

**Erro de procedimento** (129)


</dt> <dd></dd> <dt>

<span id="Unexpected_Information"></span><span id="unexpected_information"></span><span id="UNEXPECTED_INFORMATION"></span>

**Informações inesperadas** (130)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF Reservado** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Erro CIM \_**.**ProbableCause**")
</dt> </dl>

Uma cadeia de caracteres de forma livre que descreve a causa provável do erro, quando a propriedade **ProbableCause** é definida como "1" (outro).

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que descrevem as ações recomendadas a ser tomadas para resolver o erro.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

