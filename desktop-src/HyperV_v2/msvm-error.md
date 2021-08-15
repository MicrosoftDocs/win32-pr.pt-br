---
description: Contém informações sobre a severidade, a causa, as ações recomendadas e outros dados relacionados à falha de uma operação CIM.
ms.assetid: 128B9ECE-D26C-4A7D-BFB7-69CD986B0DBA
title: Msvm_Error classe
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
ms.openlocfilehash: 03ef036fc9c325b5087e597602fafec29abc484aa5a02a4395aaff3c25e59238
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117994493"
---
# <a name="msvm_error-class"></a>Classe de erro Msvm \_

Uma classe especializada que contém informações sobre a gravidade, a causa, as ações recomendadas e outros dados relacionados à falha de uma operação CIM.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

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

## <a name="members"></a>Membros

A **classe Msvm \_ Error** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ Error** tem essas propriedades.

<dl> <dt>

**CIMStatusCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O código de status CIM que caracteriza essa instância. Essa propriedade define os códigos de status que podem ser retornadas por um servidor CIM ou ouvinte compatível. Nem todos os códigos de status são válidos para cada operação. A especificação de cada operação deve definir os códigos de status que podem ser retornados por essa operação. Os valores a seguir para o código de status CIM são definidos. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).



| Valor                                                                                                                                                                                                                                                                                          | Significado                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="CIM_ERR_FAILED"></span><span id="cim_err_failed"></span><dl> <dt>**CIM \_ ERR \_ FAILED**</dt> <dt>1</dt> </dl>                                                                       | Ocorreu um erro geral que não é coberto por um código de erro mais específico.<br/>    |
| <span id="CIM_ERR_ACCESS_DENIED"></span><span id="cim_err_access_denied"></span><dl> <dt>**CIM \_ ERR \_ ACCESS \_ NEGADO**</dt> <dt>2</dt> </dl>                                                 | O acesso a um recurso CIM não estava disponível para o cliente.<br/>                      |
| <span id="CIM_ERR_INVALID_NAMESPACE"></span><span id="cim_err_invalid_namespace"></span><dl> <dt>**CIM \_ ERR \_ \_ NAMESPACE INVÁLIDO**</dt> <dt>3</dt> </dl>                                     | O namespace de destino não existe.<br/>                                           |
| <span id="CIM_ERR_INVALID_PARAMETER"></span><span id="cim_err_invalid_parameter"></span><dl> <dt>**CIM \_ ERRO \_ PARÂMETRO \_ INVÁLIDO**</dt> <dt>4</dt> </dl>                                     | Um ou mais valores de parâmetro passados para o método eram inválidos.<br/>                |
| <span id="CIM_ERR_INVALID_CLASS"></span><span id="cim_err_invalid_class"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ CLASS**</dt> <dt>5</dt> </dl>                                                 | A classe especificada não existe.<br/>                                            |
| <span id="CIM_ERR_NOT_FOUND"></span><span id="cim_err_not_found"></span><dl> <dt>**CIM \_ ERR \_ NÃO \_ ENCONTRADO**</dt> <dt>6</dt> </dl>                                                             | Não foi possível encontrar o objeto solicitado.<br/>                                       |
| <span id="CIM_ERR_NOT_SUPPORTED"></span><span id="cim_err_not_supported"></span><dl> <dt>**CIM \_ ERR \_ SEM \_ SUPORTE**</dt> <dt>7</dt> </dl>                                                 | Não há suporte para a operação solicitada.<br/>                                      |
| <span id="CIM_ERR_CLASS_HAS_CHILDREN"></span><span id="cim_err_class_has_children"></span><dl> <dt>**CIM \_ A CLASSE ERR \_ \_ TEM \_ FILHOS**</dt> <dt>8</dt> </dl>                                 | A operação não pode ser executada nessa classe porque ela tem instâncias.<br/>        |
| <span id="CIM_ERR_CLASS_HAS_INSTANCES"></span><span id="cim_err_class_has_instances"></span><dl> <dt>**CIM \_ A CLASSE ERR \_ \_ TEM \_ INSTÂNCIAS**</dt> <dt>9</dt> </dl>                              | A operação não pode ser executada nessa classe, pois ela tem instâncias.<br/>          |
| <span id="CIM_ERR_INVALID_SUPERCLASS"></span><span id="cim_err_invalid_superclass"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ SUPERCLASS**</dt> <dt>10</dt> </dl>                                 | A operação não pode ser executada, pois a superclasse especificada não existe.<br/> |
| <span id="CIM_ERR_ALREADY_EXISTS"></span><span id="cim_err_already_exists"></span><dl> <dt>**CIM \_ ERR \_ JÁ \_ EXISTE**</dt> <dt>11</dt> </dl>                                             | A operação não pode ser executada porque um objeto já existe.<br/>              |
| <span id="CIM_ERR_NO_SUCH_PROPERTY"></span><span id="cim_err_no_such_property"></span><dl> <dt>**CIM \_ ERR \_ NO \_ SUCH \_ PROPERTY**</dt> <dt>12</dt> </dl>                                      | A Propriedade especificada não existe.<br/>                                         |
| <span id="CIM_ERR_TYPE_MISMATCH"></span><span id="cim_err_type_mismatch"></span><dl> <dt>**CIM \_ ERR \_ TYPE \_ MISMATCH**</dt> <dt>13</dt> </dl>                                                | O valor fornecido é incompatível com o tipo .<br/>                              |
| <span id="CIM_ERR_QUERY_LANGUAGE_NOT_SUPPORTED"></span><span id="cim_err_query_language_not_supported"></span><dl> <dt>**CIM \_ ERR \_ QUERY \_ LANGUAGE NOT \_ \_ SUPPORTED**</dt> <dt>14</dt> </dl> | Não há suporte para a linguagem de consulta.<br/>                             |
| <span id="CIM_ERR_INVALID_QUERY"></span><span id="cim_err_invalid_query"></span><dl> <dt>**CIM \_ ERR \_ \_ INVALID QUERY**</dt> <dt>15</dt> </dl>                                                | A consulta não é válida para a linguagem de consulta especificada.<br/>                       |
| <span id="CIM_ERR_METHOD_NOT_AVAILABLE"></span><span id="cim_err_method_not_available"></span><dl> <dt>**CIM \_ MÉTODO ERR \_ \_ NÃO \_ DISPONÍVEL**</dt> <dt>16</dt> </dl>                          | Não foi possível executar o método extrídico.<br/>                                    |
| <span id="CIM_ERR_METHOD_NOT_FOUND"></span><span id="cim_err_method_not_found"></span><dl> <dt>**CIM \_ MÉTODO ERR \_ \_ NÃO \_ ENCONTRADO**</dt> <dt>17</dt> </dl>                                      | O método extrítico especificado não existe.<br/>                                 |
| <span id="CIM_ERR_UNEXPECTED_RESPONSE"></span><span id="cim_err_unexpected_response"></span><dl> <dt>**CIM \_ ERR \_ UNEXPECTED \_ RESPONSE**</dt> <dt>18</dt> </dl>                              | A resposta retornada à operação assíncrona não era esperada.<br/>          |
| <span id="CIM_ERR_INVALID_RESPONSE_DESTINATION"></span><span id="cim_err_invalid_response_destination"></span><dl> <dt>**CIM \_ ERR \_ INVALID \_ RESPONSE \_ DESTINATION**</dt> <dt>19</dt> </dl>  | O destino especificado para a resposta assíncrona não é válido.<br/>          |
| <span id="CIM_ERR_NAMESPACE_NOT_EMPTY"></span><span id="cim_err_namespace_not_empty"></span><dl> <dt>**CIM \_ NAMESPACE \_ ERR \_ NÃO \_ VAZIO**</dt> <dt>20</dt> </dl>                             | O namespace especificado não está vazio.<br/>                                          |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt>**DMTF Reservado**</dt> <dt>21 = *valor*</dt> </dl>                            | Valores reservados.<br/>                                                               |



 

</dd> <dt>

**CIMStatusCodeDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que contém uma descrição acessível pelo usuário da **propriedade CIMStatusCode.** Essa descrição pode estender, mas deve ser consistente com a definição de **CIMStatusCode**. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**ErrorSource**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As informações de identificação da entidade (a instância) gerando o erro. Se essa entidade for modelada no esquema CIM, essa propriedade conterá o caminho da instância codificada como um parâmetro de cadeia de caracteres. Se não for modelada, a propriedade conterá alguma cadeia de caracteres de identificação que nomeia a entidade que gerou o erro. O caminho ou a cadeia de caracteres de identificação é formatado de acordo com a **propriedade ErrorSourceFormat.** Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**ErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O formato da **propriedade ErrorSource** é interpretável com base no valor dessa propriedade. Essa propriedade é herdada do [**\_ erro CIM**](/previous-versions//cc150671(v=vs.85))e é sempre definida como 0.



| Valor                                                                                                                                                                                                                                                        | Significado                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconhecido**</dt> <dt>0</dt> </dl>                                  | O formato é desconhecido ou não pode ser interpretado significativamente por um aplicativo cliente CIM.<br/>                                         |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Outros**</dt> <dt>1</dt> </dl>                                          | O formato é definido pelo valor da **propriedade OtherErrorSourceFormat.**<br/>                                               |
| <span id="CIMObjectHandle"></span><span id="cimobjecthandle"></span><span id="CIMOBJECTHANDLE"></span><dl> <dt>**CIMObjectHandle**</dt> <dt>2</dt> </dl> | Um Identificador de Objeto CIM, codificado usando a sintaxe MOF definida para o objetoHandle não terminal, é usado para identificar a entidade.<br/> |



 

</dd> <dt>

**ErrorType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Classificação primária do erro. Os valores a seguir são definidos. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).



| Valor                                                                                                                                                                                                                                                                                                         | Significado                                                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconhecido**</dt> <dt>0</dt> </dl>                                                                                   |                                                                                                                                                          |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Outros**</dt> <dt>1</dt> </dl>                                                                                           |                                                                                                                                                          |
| <span id="Communications_Error"></span><span id="communications_error"></span><span id="COMMUNICATIONS_ERROR"></span><dl> <dt>**Erro de comunicação**</dt> <dt>2</dt> </dl>                               | Erros desse tipo são associados principalmente aos procedimentos e/ou processos necessários para transmitir informações de um ponto para outro.<br/> |
| <span id="Quality_of_Service_Error"></span><span id="quality_of_service_error"></span><span id="QUALITY_OF_SERVICE_ERROR"></span><dl> <dt>**Erro de qualidade de serviço**</dt> <dt>3</dt> </dl>               | Erros desse tipo são associados principalmente a falhas que resultam em funcionalidade ou desempenho reduzidos.<br/>                             |
| <span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span><dl> <dt>**Erro de software**</dt> <dt>4</dt> </dl>                                                       | O erro desse tipo está associado principalmente a um software ou falha de processamento.<br/>                                                            |
| <span id="Hardware_Error"></span><span id="hardware_error"></span><span id="HARDWARE_ERROR"></span><dl> <dt>**Erro de hardware**</dt> <dt>5</dt> </dl>                                                       | Erros desse tipo são associados principalmente a uma falha de equipamento ou hardware.<br/>                                                         |
| <span id="Environmental_Error"></span><span id="environmental_error"></span><span id="ENVIRONMENTAL_ERROR"></span><dl> <dt>**Erro ambiental**</dt> <dt>6</dt> </dl>                                   | Erros desse tipo são associados principalmente a uma condição de falha relacionada à instalação ou a outras considerações ambientais.<br/>      |
| <span id="Security_Error"></span><span id="security_error"></span><span id="SECURITY_ERROR"></span><dl> <dt>**Erro de segurança**</dt> <dt>7</dt> </dl>                                                       | Erros desse tipo estão associados a violações de segurança, detecção de vírus e problemas semelhantes.<br/>                                        |
| <span id="Oversubscription_Error"></span><span id="oversubscription_error"></span><span id="OVERSUBSCRIPTION_ERROR"></span><dl> <dt>**Erro de excesso de assinatura**</dt> <dt>8</dt> </dl>                       | Os erros desse tipo estão principalmente associados à falha ao alocar recursos suficientes para concluir a operação.<br/>                   |
| <span id="Unavailable_Resource_Error"></span><span id="unavailable_resource_error"></span><span id="UNAVAILABLE_RESOURCE_ERROR"></span><dl> <dt>**Erro de recurso não disponível**</dt> <dt>9</dt> </dl>       | Erros desse tipo são associados principalmente à falha ao acessar um recurso necessário.<br/>                                                |
| <span id="Unsupported_Operation_Error"></span><span id="unsupported_operation_error"></span><span id="UNSUPPORTED_OPERATION_ERROR"></span><dl> <dt>**Erro de operação sem suporte**</dt> <dt>10</dt> </dl> | Erros desse tipo são associados principalmente a solicitações sem suporte.<br/>                                                          |



 

</dd> <dt>

**Message**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A mensagem formatada. Essa mensagem é construída aplicando o conteúdo dinâmico da mensagem, descrito em **MessageArguments**, à cadeia de caracteres de formato identificada exclusivamente, dentro do escopo **de OwningEntity**, por **MessageID**. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**MessageArguments**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém o conteúdo dinâmico da mensagem. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**MessageID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres opaca que identifica exclusivamente, dentro do escopo **de OwningEntity**, o formato da mensagem. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**OtherErrorSourceFormat**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que define valores "Outros" **para ErrorSourceFormat.** Esse valor deve ser definido como um valor não NULL **quando ErrorSourceFormat** é definido como um valor de 1 (Outro). Para todos os outros valores **de ErrorSourceFormat**, o valor dessa cadeia de caracteres deve ser definido como **Null.** Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**OtherErrorType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve **o ErrorType** quando 1, (Outro) é especificado como **o ErrorType.** Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**OwningEntity**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que identifica exclusivamente a entidade que possui a definição do formato da mensagem descrita nesta instância. **OwningEntity** deve incluir um nome protegido por direitos autorais, marcas comerciais ou exclusivos pertencentes à entidade de negócios ou corpo de padrões que define o formato. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**PerceivedSeverity**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor enumerado que descreve a severidade do erro do ponto de vista do notificador: 2 – Baixo deve ser usado para problemas nãocríticos, como parâmetros inválidos, uso incorreto, funcionalidade sem suporte. 3 - Médio deve ser usado para indicar que a ação é necessária, mas a situação não é grave no momento. 4 - Alta deve ser usada para indicar que a ação é necessária agora. 5 - Fatal deve ser usado para indicar uma perda de dados ou falha de serviço ou sistema irrecuperável. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Baixo** (2)
</dt> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Médio** (3)
</dt> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Alto** (4)
</dt> <dt>

<span id="Fatal_"></span><span id="fatal_"></span><span id="FATAL_"></span>**Fatal** (5 )
</dt> </dl>

</dd> <dt>

**ProvávelCause**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor enumerado que descreve a causa provável do erro. Essa propriedade é herdada do [**erro CIM \_**](/previous-versions//cc150671(v=vs.85)).

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)
</dt> <dt>

<span id="Adapter_Card_Error"></span><span id="adapter_card_error"></span><span id="ADAPTER_CARD_ERROR"></span>**Erro de adaptador/cartão** (2)
</dt> <dt>

<span id="Application_Subsystem_Failure"></span><span id="application_subsystem_failure"></span><span id="APPLICATION_SUBSYSTEM_FAILURE"></span>**Falha do subsistema do aplicativo** (3)
</dt> <dt>

<span id="Bandwidth_Reduced"></span><span id="bandwidth_reduced"></span><span id="BANDWIDTH_REDUCED"></span>**Largura de banda** reduzida (4)
</dt> <dt>

<span id="Connection_Establishment_Error"></span><span id="connection_establishment_error"></span><span id="CONNECTION_ESTABLISHMENT_ERROR"></span>**Erro de estabelecimento de** conexão (5)
</dt> <dt>

<span id="Communications_Protocol_Error"></span><span id="communications_protocol_error"></span><span id="COMMUNICATIONS_PROTOCOL_ERROR"></span>**Erro de protocolo de** comunicações (6)
</dt> <dt>

<span id="Communications_Subsystem_Failure"></span><span id="communications_subsystem_failure"></span><span id="COMMUNICATIONS_SUBSYSTEM_FAILURE"></span>**Falha do subsistema de comunicações** (7)
</dt> <dt>

<span id="Configuration_Customization_Error"></span><span id="configuration_customization_error"></span><span id="CONFIGURATION_CUSTOMIZATION_ERROR"></span>**Erro de configuração/personalização** (8)
</dt> <dt>

<span id="Congestion"></span><span id="congestion"></span><span id="CONGESTION"></span>**Congestionamento** (9)
</dt> <dt>

<span id="Corrupt_Data"></span><span id="corrupt_data"></span><span id="CORRUPT_DATA"></span>**Dados corrompidos** (10)
</dt> <dt>

<span id="CPU_Cycles_Limit_Exceeded"></span><span id="cpu_cycles_limit_exceeded"></span><span id="CPU_CYCLES_LIMIT_EXCEEDED"></span>**Limite de ciclos de CPU excedido** (11)
</dt> <dt>

<span id="Dataset_Modem_Error"></span><span id="dataset_modem_error"></span><span id="DATASET_MODEM_ERROR"></span>**Erro de conjuntos de dados/modem** (12)
</dt> <dt>

<span id="Degraded_Signal"></span><span id="degraded_signal"></span><span id="DEGRADED_SIGNAL"></span>**Sinal degradado** (13)
</dt> <dt>

<span id="DTE-DCE_Interface_Error"></span><span id="dte-dce_interface_error"></span><span id="DTE-DCE_INTERFACE_ERROR"></span>**Erro de interface DTE-DCE** (14)
</dt> <dt>

<span id="Enclosure_Door_Open"></span><span id="enclosure_door_open"></span><span id="ENCLOSURE_DOOR_OPEN"></span>**Porta do compartimento aberta** (15)
</dt> <dt>

<span id="Equipment_Malfunction"></span><span id="equipment_malfunction"></span><span id="EQUIPMENT_MALFUNCTION"></span>**Funcionamento do equipamento** (16)
</dt> <dt>

<span id="Excessive_Vibration"></span><span id="excessive_vibration"></span><span id="EXCESSIVE_VIBRATION"></span>**Vibração excessiva** (17)
</dt> <dt>

<span id="File_Format_Error"></span><span id="file_format_error"></span><span id="FILE_FORMAT_ERROR"></span>**Erro de formato de** arquivo (18)
</dt> <dt>

<span id="Fire_Detected"></span><span id="fire_detected"></span><span id="FIRE_DETECTED"></span>**Fire Detected** (19)
</dt> <dt>

<span id="Flood_Detected"></span><span id="flood_detected"></span><span id="FLOOD_DETECTED"></span>**Inundação detectada** (20)
</dt> <dt>

<span id="Framing_Error"></span><span id="framing_error"></span><span id="FRAMING_ERROR"></span>**Erro de enquadramento** (21)
</dt> <dt>

<span id="HVAC_Problem"></span><span id="hvac_problem"></span><span id="HVAC_PROBLEM"></span>**Problema de HVAC** (22)
</dt> <dt>

<span id="Humidity_Unacceptable"></span><span id="humidity_unacceptable"></span><span id="HUMIDITY_UNACCEPTABLE"></span>**Umidade inaceitável** (23)
</dt> <dt>

<span id="I_O_Device_Error"></span><span id="i_o_device_error"></span><span id="I_O_DEVICE_ERROR"></span>**Erro de dispositivo de E/S** (24)
</dt> <dt>

<span id="Input_Device_Error"></span><span id="input_device_error"></span><span id="INPUT_DEVICE_ERROR"></span>**Erro de dispositivo de** entrada (25)
</dt> <dt>

<span id="LAN_Error"></span><span id="lan_error"></span><span id="LAN_ERROR"></span>**Erro de LAN** (26)
</dt> <dt>

<span id="Non-Toxic_Leak_Detected"></span><span id="non-toxic_leak_detected"></span><span id="NON-TOXIC_LEAK_DETECTED"></span>**Vazamento não detectado** (27)
</dt> <dt>

<span id="Local_Node_Transmission_Error"></span><span id="local_node_transmission_error"></span><span id="LOCAL_NODE_TRANSMISSION_ERROR"></span>**Erro de transmissão de nó local** (28)
</dt> <dt>

<span id="Loss_of_Frame"></span><span id="loss_of_frame"></span><span id="LOSS_OF_FRAME"></span>**Perda de quadro** (29)
</dt> <dt>

<span id="Loss_of_Signal"></span><span id="loss_of_signal"></span><span id="LOSS_OF_SIGNAL"></span>**Perda de sinal** (30)
</dt> <dt>

<span id="__31____________Material_Supply_Exhausted"></span><span id="__31____________material_supply_exhausted"></span><span id="__31____________MATERIAL_SUPPLY_EXHAUSTED"></span>**//31 Fornecimento de material esgotado** (31)
</dt> <dt>

<span id="Multiplexer_Problem"></span><span id="multiplexer_problem"></span><span id="MULTIPLEXER_PROBLEM"></span>**Problema de multiplexador** (32)
</dt> <dt>

<span id="Out_of_Memory"></span><span id="out_of_memory"></span><span id="OUT_OF_MEMORY"></span>**Memória sem** memória (33)
</dt> <dt>

<span id="Output_Device_Error"></span><span id="output_device_error"></span><span id="OUTPUT_DEVICE_ERROR"></span>**Erro de dispositivo de saída** (34)
</dt> <dt>

<span id="Performance_Degraded"></span><span id="performance_degraded"></span><span id="PERFORMANCE_DEGRADED"></span>**Desempenho degradado** (35)
</dt> <dt>

<span id="Power_Problem"></span><span id="power_problem"></span><span id="POWER_PROBLEM"></span>**Problema de energia** (36)
</dt> <dt>

<span id="Pressure_Unacceptable"></span><span id="pressure_unacceptable"></span><span id="PRESSURE_UNACCEPTABLE"></span>**Pressão inaceitável** (37)
</dt> <dt>

<span id="Processor_Problem__Internal_Machine_Error_"></span><span id="processor_problem__internal_machine_error_"></span><span id="PROCESSOR_PROBLEM__INTERNAL_MACHINE_ERROR_"></span>**Problema do processador (erro interno do computador)** (38)
</dt> <dt>

<span id="Pump_Failure"></span><span id="pump_failure"></span><span id="PUMP_FAILURE"></span>**Falha de bomba** (39)
</dt> <dt>

<span id="Queue_Size_Exceeded"></span><span id="queue_size_exceeded"></span><span id="QUEUE_SIZE_EXCEEDED"></span>**Tamanho da fila excedido** (40)
</dt> <dt>

<span id="Receive_Failure"></span><span id="receive_failure"></span><span id="RECEIVE_FAILURE"></span>**Falha de recebimento** (41)
</dt> <dt>

<span id="Receiver_Failure"></span><span id="receiver_failure"></span><span id="RECEIVER_FAILURE"></span>**Falha do receptor** (42)
</dt> <dt>

<span id="Remote_Node_Transmission_Error"></span><span id="remote_node_transmission_error"></span><span id="REMOTE_NODE_TRANSMISSION_ERROR"></span>**Erro de transmissão de nó remoto** (43)
</dt> <dt>

<span id="Resource_at_or_Nearing_Capacity"></span><span id="resource_at_or_nearing_capacity"></span><span id="RESOURCE_AT_OR_NEARING_CAPACITY"></span>**Recurso em ou capacidade de aproximação** (44)
</dt> <dt>

<span id="Response_Time_Excessive"></span><span id="response_time_excessive"></span><span id="RESPONSE_TIME_EXCESSIVE"></span>**Tempo de resposta excessivo** (45)
</dt> <dt>

<span id="Retransmission_Rate_Excessive"></span><span id="retransmission_rate_excessive"></span><span id="RETRANSMISSION_RATE_EXCESSIVE"></span>**Taxa de retransmissão excessiva** (46)
</dt> <dt>

<span id="Software_Error"></span><span id="software_error"></span><span id="SOFTWARE_ERROR"></span>**Erro de software** (47)
</dt> <dt>

<span id="Software_Program_Abnormally_Terminated"></span><span id="software_program_abnormally_terminated"></span><span id="SOFTWARE_PROGRAM_ABNORMALLY_TERMINATED"></span>**Programa de Software encerrado de forma anormal** (48)
</dt> <dt>

<span id="Software_Program_Error__Incorrect_Results_"></span><span id="software_program_error__incorrect_results_"></span><span id="SOFTWARE_PROGRAM_ERROR__INCORRECT_RESULTS_"></span>**Erro do programa de software (resultados incorretos)** (49)
</dt> <dt>

<span id="Storage_Capacity_Problem"></span><span id="storage_capacity_problem"></span><span id="STORAGE_CAPACITY_PROBLEM"></span>**Armazenamento de capacidade** (50)
</dt> <dt>

<span id="Temperature_Unacceptable"></span><span id="temperature_unacceptable"></span><span id="TEMPERATURE_UNACCEPTABLE"></span>**Temperatura inaceitável** (51)
</dt> <dt>

<span id="Threshold_Crossed"></span><span id="threshold_crossed"></span><span id="THRESHOLD_CROSSED"></span>**Limite cruzado** (52)
</dt> <dt>

<span id="Timing_Problem"></span><span id="timing_problem"></span><span id="TIMING_PROBLEM"></span>**Problema de tempo** (53)
</dt> <dt>

<span id="Toxic_Leak_Detected"></span><span id="toxic_leak_detected"></span><span id="TOXIC_LEAK_DETECTED"></span>**Vazamento de resíduos detectado** (54)
</dt> <dt>

<span id="Transmit_Failure"></span><span id="transmit_failure"></span><span id="TRANSMIT_FAILURE"></span>**Falha de transmissão** (55)
</dt> <dt>

<span id="Transmitter_Failure"></span><span id="transmitter_failure"></span><span id="TRANSMITTER_FAILURE"></span>**Falha do transmissor** (56)
</dt> <dt>

<span id="Underlying_Resource_Unavailable"></span><span id="underlying_resource_unavailable"></span><span id="UNDERLYING_RESOURCE_UNAVAILABLE"></span>**Recurso subjacente indisponível** (57)
</dt> <dt>

<span id="Version_Mismatch"></span><span id="version_mismatch"></span><span id="VERSION_MISMATCH"></span>**Incompatibilidade de versão** (58)
</dt> <dt>

<span id="Previous_Alert_Cleared"></span><span id="previous_alert_cleared"></span><span id="PREVIOUS_ALERT_CLEARED"></span>**Alerta anterior limpo** (59)
</dt> <dt>

<span id="__60____________Login_Attempts_Failed"></span><span id="__60____________login_attempts_failed"></span><span id="__60____________LOGIN_ATTEMPTS_FAILED"></span>**//60 Tentativas de logon com falha** (60)
</dt> <dt>

<span id="Software_Virus_Detected"></span><span id="software_virus_detected"></span><span id="SOFTWARE_VIRUS_DETECTED"></span>**Vírus de software detectados** (61)
</dt> <dt>

<span id="Hardware_Security_Breached"></span><span id="hardware_security_breached"></span><span id="HARDWARE_SECURITY_BREACHED"></span>**Segurança de hardware violada** (62)
</dt> <dt>

<span id="Denial_of_Service_Detected"></span><span id="denial_of_service_detected"></span><span id="DENIAL_OF_SERVICE_DETECTED"></span>**Negação de serviço detectada** (63)
</dt> <dt>

<span id="Security_Credential_Mismatch"></span><span id="security_credential_mismatch"></span><span id="SECURITY_CREDENTIAL_MISMATCH"></span>**Incompatibilidade de credenciais de segurança** (64)
</dt> <dt>

<span id="Unauthorized_Access"></span><span id="unauthorized_access"></span><span id="UNAUTHORIZED_ACCESS"></span>**Acesso não autorizado** (65)
</dt> <dt>

<span id="Alarm_Received"></span><span id="alarm_received"></span><span id="ALARM_RECEIVED"></span>**Alarme recebido** (66)
</dt> <dt>

<span id="Loss_of_Pointer"></span><span id="loss_of_pointer"></span><span id="LOSS_OF_POINTER"></span>**Perda de ponteiro** (67)
</dt> <dt>

<span id="Payload_Mismatch"></span><span id="payload_mismatch"></span><span id="PAYLOAD_MISMATCH"></span>**Incompatibilidade de carga** (68)
</dt> <dt>

<span id="Transmission_Error"></span><span id="transmission_error"></span><span id="TRANSMISSION_ERROR"></span>**Erro de** transmissão (69)
</dt> <dt>

<span id="Excessive_Error_Rate"></span><span id="excessive_error_rate"></span><span id="EXCESSIVE_ERROR_RATE"></span>**Taxa de erro excessiva** (70)
</dt> <dt>

<span id="Trace_Problem"></span><span id="trace_problem"></span><span id="TRACE_PROBLEM"></span>**Problema de rastreamento** (71)
</dt> <dt>

<span id="Element_Unavailable"></span><span id="element_unavailable"></span><span id="ELEMENT_UNAVAILABLE"></span>**Elemento Indisponível** (72)
</dt> <dt>

<span id="Element_Missing"></span><span id="element_missing"></span><span id="ELEMENT_MISSING"></span>**Elemento Missing** (73)
</dt> <dt>

<span id="Loss_of_Multi_Frame"></span><span id="loss_of_multi_frame"></span><span id="LOSS_OF_MULTI_FRAME"></span>**Perda de vários quadros** (74)
</dt> <dt>

<span id="Broadcast_Channel_Failure"></span><span id="broadcast_channel_failure"></span><span id="BROADCAST_CHANNEL_FAILURE"></span>**Falha de canal de** difusão (75)
</dt> <dt>

<span id="Invalid_Message_Received"></span><span id="invalid_message_received"></span><span id="INVALID_MESSAGE_RECEIVED"></span>**Mensagem inválida recebida** (76)
</dt> <dt>

<span id="Routing_Failure"></span><span id="routing_failure"></span><span id="ROUTING_FAILURE"></span>**Falha de roteamento** (77)
</dt> <dt>

<span id="Backplane_Failure"></span><span id="backplane_failure"></span><span id="BACKPLANE_FAILURE"></span>**Falha de backplane** (78)
</dt> <dt>

<span id="Identifier_Duplication"></span><span id="identifier_duplication"></span><span id="IDENTIFIER_DUPLICATION"></span>**Duplicação do identificador** (79)
</dt> <dt>

<span id="Protection_Path_Failure"></span><span id="protection_path_failure"></span><span id="PROTECTION_PATH_FAILURE"></span>**Falha no caminho de** proteção (80)
</dt> <dt>

<span id="Sync_Loss_or_Mismatch"></span><span id="sync_loss_or_mismatch"></span><span id="SYNC_LOSS_OR_MISMATCH"></span>**Perda de sincronização ou incompatibilidade** (81)
</dt> <dt>

<span id="Terminal_Problem"></span><span id="terminal_problem"></span><span id="TERMINAL_PROBLEM"></span>**Problema de terminal** (82)
</dt> <dt>

<span id="Real_Time_Clock_Failure"></span><span id="real_time_clock_failure"></span><span id="REAL_TIME_CLOCK_FAILURE"></span>**Falha no relógio em tempo real** (83)
</dt> <dt>

<span id="Antenna_Failure"></span><span id="antenna_failure"></span><span id="ANTENNA_FAILURE"></span>**Falha de antena** (84)
</dt> <dt>

<span id="Battery_Charging_Failure"></span><span id="battery_charging_failure"></span><span id="BATTERY_CHARGING_FAILURE"></span>**Falha de carregamento da bateria** (85)
</dt> <dt>

<span id="Disk_Failure"></span><span id="disk_failure"></span><span id="DISK_FAILURE"></span>**Falha de** disco (86)
</dt> <dt>

<span id="Frequency_Hopping_Failure"></span><span id="frequency_hopping_failure"></span><span id="FREQUENCY_HOPPING_FAILURE"></span>**Falha de salto de frequência** (87)
</dt> <dt>

<span id="Loss_of_Redundancy"></span><span id="loss_of_redundancy"></span><span id="LOSS_OF_REDUNDANCY"></span>**Perda de redundância** (88)
</dt> <dt>

<span id="Power_Supply_Failure"></span><span id="power_supply_failure"></span><span id="POWER_SUPPLY_FAILURE"></span>**Falha na fonte de** alimentação (89)
</dt> <dt>

<span id="Signal_Quality_Problem"></span><span id="signal_quality_problem"></span><span id="SIGNAL_QUALITY_PROBLEM"></span>**Problema de qualidade do sinal** (90)
</dt> <dt>

<span id="__91____________Battery_Discharging"></span><span id="__91____________battery_discharging"></span><span id="__91____________BATTERY_DISCHARGING"></span>**//91 Compartilhamento de Bateria** (91)
</dt> <dt>

<span id="Battery_Failure"></span><span id="battery_failure"></span><span id="BATTERY_FAILURE"></span>**Falha de bateria** (92)
</dt> <dt>

<span id="Commercial_Power_Problem"></span><span id="commercial_power_problem"></span><span id="COMMERCIAL_POWER_PROBLEM"></span>**Problema de energia comercial** (93)
</dt> <dt>

<span id="Fan_Failure"></span><span id="fan_failure"></span><span id="FAN_FAILURE"></span>**Falha do ventilador** (94)
</dt> <dt>

<span id="Engine_Failure"></span><span id="engine_failure"></span><span id="ENGINE_FAILURE"></span>**Falha do** mecanismo (95)
</dt> <dt>

<span id="Sensor_Failure"></span><span id="sensor_failure"></span><span id="SENSOR_FAILURE"></span>**Falha do sensor** (96)
</dt> <dt>

<span id="Fuse_Failure"></span><span id="fuse_failure"></span><span id="FUSE_FAILURE"></span>**Falha de fuse** (97)
</dt> <dt>

<span id="Generator_Failure"></span><span id="generator_failure"></span><span id="GENERATOR_FAILURE"></span>**Falha do gerador** (98)
</dt> <dt>

<span id="Low_Battery"></span><span id="low_battery"></span><span id="LOW_BATTERY"></span>**Bateria fraca** (99)
</dt> <dt>

<span id="Low_Fuel"></span><span id="low_fuel"></span><span id="LOW_FUEL"></span>**Baixo combustível** (100)
</dt> <dt>

<span id="Low_Water"></span><span id="low_water"></span><span id="LOW_WATER"></span>**Baixa água** (101)
</dt> <dt>

<span id="Explosive_Gas"></span><span id="explosive_gas"></span><span id="EXPLOSIVE_GAS"></span>**Gás de artefato** (102)
</dt> <dt>

<span id="High_Winds"></span><span id="high_winds"></span><span id="HIGH_WINDS"></span>**Altos danos** (103)
</dt> <dt>

<span id="Ice_Buildup"></span><span id="ice_buildup"></span><span id="ICE_BUILDUP"></span>**Buildup ice** (104)
</dt> <dt>

<span id="Smoke"></span><span id="smoke"></span><span id="SMOKE"></span>**Smoke** (105)
</dt> <dt>

<span id="Memory_Mismatch"></span><span id="memory_mismatch"></span><span id="MEMORY_MISMATCH"></span>**Incompatibilidade de memória** (106)
</dt> <dt>

<span id="Out_of_CPU_Cycles"></span><span id="out_of_cpu_cycles"></span><span id="OUT_OF_CPU_CYCLES"></span>**Ciclos de CPU fora** (107)
</dt> <dt>

<span id="Software_Environment_Problem"></span><span id="software_environment_problem"></span><span id="SOFTWARE_ENVIRONMENT_PROBLEM"></span>**Problema de ambiente de software** (108)
</dt> <dt>

<span id="Software_Download_Failure"></span><span id="software_download_failure"></span><span id="SOFTWARE_DOWNLOAD_FAILURE"></span>**Falha de download de software** (109)
</dt> <dt>

<span id="Element_Reinitialized"></span><span id="element_reinitialized"></span><span id="ELEMENT_REINITIALIZED"></span>**Elemento Reinicializado** (110)
</dt> <dt>

<span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>**Tempoout** (111)
</dt> <dt>

<span id="Logging_Problems"></span><span id="logging_problems"></span><span id="LOGGING_PROBLEMS"></span>**Problemas de registro** em log (112)
</dt> <dt>

<span id="Leak_Detected"></span><span id="leak_detected"></span><span id="LEAK_DETECTED"></span>**Vazamento detectado** (113)
</dt> <dt>

<span id="Protection_Mechanism_Failure"></span><span id="protection_mechanism_failure"></span><span id="PROTECTION_MECHANISM_FAILURE"></span>**Falha do mecanismo de** proteção (114)
</dt> <dt>

<span id="__115____________Protecting_Resource_Failure"></span><span id="__115____________protecting_resource_failure"></span><span id="__115____________PROTECTING_RESOURCE_FAILURE"></span>**//115 Protegendo a falha de recursos** (115)
</dt> <dt>

<span id="Database_Inconsistency"></span><span id="database_inconsistency"></span><span id="DATABASE_INCONSISTENCY"></span>**Inconsistência** de banco de dados (116)
</dt> <dt>

<span id="Authentication_Failure"></span><span id="authentication_failure"></span><span id="AUTHENTICATION_FAILURE"></span>**Falha de autenticação** (117)
</dt> <dt>

<span id="Breach_of_Confidentiality"></span><span id="breach_of_confidentiality"></span><span id="BREACH_OF_CONFIDENTIALITY"></span>**Violação de confidencialidade** (118)
</dt> <dt>

<span id="Cable_Tamper"></span><span id="cable_tamper"></span><span id="CABLE_TAMPER"></span>**Adulteração de** cabo (119)
</dt> <dt>

<span id="Delayed_Information"></span><span id="delayed_information"></span><span id="DELAYED_INFORMATION"></span>**Informações atrasadas** (120)
</dt> <dt>

<span id="Duplicate_Information"></span><span id="duplicate_information"></span><span id="DUPLICATE_INFORMATION"></span>**Informações duplicadas** (121)
</dt> <dt>

<span id="Information_Missing"></span><span id="information_missing"></span><span id="INFORMATION_MISSING"></span>**Informações ausentes** (122)
</dt> <dt>

<span id="Information_Modification"></span><span id="information_modification"></span><span id="INFORMATION_MODIFICATION"></span>**Modificação de** informações (123)
</dt> <dt>

<span id="Information_Out_of_Sequence"></span><span id="information_out_of_sequence"></span><span id="INFORMATION_OUT_OF_SEQUENCE"></span>**Informações fora de sequência** (124)
</dt> <dt>

<span id="Key_Expired"></span><span id="key_expired"></span><span id="KEY_EXPIRED"></span>**Chave expirada** (125)
</dt> <dt>

<span id="Non-Repudiation_Failure"></span><span id="non-repudiation_failure"></span><span id="NON-REPUDIATION_FAILURE"></span>**Falha de não repúdio** (126)
</dt> <dt>

<span id="Out_of_Hours_Activity"></span><span id="out_of_hours_activity"></span><span id="OUT_OF_HOURS_ACTIVITY"></span>**Atividade fora do horário** comercial (127)
</dt> <dt>

<span id="Out_of_Service"></span><span id="out_of_service"></span><span id="OUT_OF_SERVICE"></span>**Fora de serviço** (128)
</dt> <dt>

<span id="Procedural_Error"></span><span id="procedural_error"></span><span id="PROCEDURAL_ERROR"></span>**Erro de procedimento** (129)
</dt> <dt>

<span id="Unexpected_Information_"></span><span id="unexpected_information_"></span><span id="UNEXPECTED_INFORMATION_"></span>**Informações inesperadas** (130)
</dt> </dl>

</dd> <dt>

**ProbableCauseDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve a causa provável do erro. Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> <dt>

**RecommendedActions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve as ações recomendadas a serem executadas para resolver o erro. Essa propriedade é herdada [**de \_ erro CIM**](/previous-versions//cc150671(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe de **\_ erro Msvm** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Erro de CIM \_**](cim-error.md)
</dt> <dt>

[**Erro de CIM \_**](/previous-versions//cc150671(v=vs.85))
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> </dl>

 

