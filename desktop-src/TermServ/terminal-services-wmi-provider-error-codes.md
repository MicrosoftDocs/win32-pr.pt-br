---
title: Serviços de Área de Trabalho Remota códigos de erro do provedor WMI (Wbemcli. h)
description: Erros retornados pelo provedor WMI de Serviços de Área de Trabalho Remota. Para obter uma lista de outros erros de WMI, consulte constantes de erro WMI.
ms.assetid: 1e68c41d-f321-4bc5-ba30-b69f5ba741eb
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WBEM_E_FAILED
- WBEM_E_NOT_FOUND
- WBEM_E_PROVIDER_FAILURE
- WBEM_E_TYPE_MISMATCH
- WBEM_E_OUT_OF_MEMORY
- WBEM_E_INVALID_PARAMETER
- WBEM_E_NOT_AVAILABLE
- WBEM_E_NOT_SUPPORTED
- WBEM_E_INVALID_NAMESPACE
- WBEM_E_INVALID_OBJECT
- WBEM_E_INITIALIZATION_FAILURE
- WBEM_E_INVALID_OPERATION
- WBEM_E_INVALID_QUERY
- WBEM_E_INVALID_QUERY_TYPE
- WBEM_E_ALREADY_EXISTS
- WBEM_E_INVALID_SYNTAX
- WBEM_E_READ_ONLY
- WBEM_E_PROVIDER_NOT_CAPABLE
- WBEM_E_ILLEGAL_NULL
- WBEM_E_VALUE_OUT_OF_RANGE
- WBEM_E_INVALID_METHOD
- WBEM_E_INVALID_METHOD_PARAMETERS
- WBEM_E_INVALID_OBJECT_PATH
api_location:
- Wbemcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 252015a5d80a1487033ad285ce3080f4d666f0c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499778"
---
# <a name="remote-desktop-services-wmi-provider-error-codes"></a>Serviços de Área de Trabalho Remota códigos de erro do provedor WMI

A lista a seguir lista os erros do WMI retornados pelo provedor WMI Serviços de Área de Trabalho Remota. Para obter uma lista de outros erros de WMI, consulte [**constantes de erro WMI**](/windows/desktop/WmiSdk/wmi-error-constants).

<dl> <dt>

<span id="WBEM_E_FAILED"></span><span id="wbem_e_failed"></span>**falha de WBEM \_ E \_**
</dt> <dd> <dl> <dt>

2147749889 (0x80041001)
</dt> <dt>



Falha na chamada do método.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_FOUND"></span><span id="wbem_e_not_found"></span>**WBEM \_ E \_ não \_ encontrado**
</dt> <dd> <dl> <dt>

2147749890 (0x80041002)
</dt> <dt>



Não foi possível encontrar o objeto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_FAILURE"></span><span id="wbem_e_provider_failure"></span>**\_falha do \_ provedor WBEM E \_**
</dt> <dd> <dl> <dt>

2147749892 (0x80041004)
</dt> <dt>



O provedor falhou em algum momento além de durante a inicialização.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_TYPE_MISMATCH"></span><span id="wbem_e_type_mismatch"></span>**incompatibilidade de \_ tipo WBEM E \_ \_**
</dt> <dd> <dl> <dt>

2147749893 (0x80041005)
</dt> <dt>



Ocorreu uma incompatibilidade de tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_OUT_OF_MEMORY"></span><span id="wbem_e_out_of_memory"></span>**WBEM \_ E \_ memória insuficiente \_ \_**
</dt> <dd> <dl> <dt>

2147749894 (0x80041006)
</dt> <dt>



Não havia memória suficiente para a operação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_PARAMETER"></span><span id="wbem_e_invalid_parameter"></span>**parâmetro de WBEM \_ E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749896 (0x80041008)
</dt> <dt>



Um dos parâmetros para a chamada não está correto.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_AVAILABLE"></span><span id="wbem_e_not_available"></span>**WBEM \_ E \_ não \_ disponível**
</dt> <dd> <dl> <dt>

2147749897 (0x80041009)
</dt> <dt>



O recurso, normalmente um servidor remoto, não está disponível no momento.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_NOT_SUPPORTED"></span><span id="wbem_e_not_supported"></span>**\_ \_ não \_ há suporte para o WBEM E**
</dt> <dd> <dl> <dt>

2147749900 (0x8004100C)
</dt> <dt>



Não há suporte para o recurso ou operação.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_NAMESPACE"></span><span id="wbem_e_invalid_namespace"></span>**WBEM \_ E \_ \_ namespace inválido**
</dt> <dd> <dl> <dt>

2147749902 (0x8004100E)
</dt> <dt>



O namespace especificado não foi encontrado.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT"></span><span id="wbem_e_invalid_object"></span>**\_objeto WBEM E \_ inválido \_**
</dt> <dd> <dl> <dt>

2147749903 (0x8004100F)
</dt> <dt>



A instância especificada é inválida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INITIALIZATION_FAILURE"></span><span id="wbem_e_initialization_failure"></span>**\_ \_ falha na inicialização do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749908 (0x80041014)
</dt> <dt>



Um módulo, como um provedor, não pôde ser inicializado por motivos internos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OPERATION"></span><span id="wbem_e_invalid_operation"></span>**operação de WBEM \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749910 (0x80041016)
</dt> <dt>



A operação solicitada é inválida. Esse erro geralmente se aplica a tentativas inválidas para excluir classes ou propriedades. Esse erro é retornado em uma tentativa de modificar uma propriedade de substituição de servidor por meio do controle de diretiva de grupo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY"></span><span id="wbem_e_invalid_query"></span>**WBEM \_ E \_ consulta inválida \_**
</dt> <dd> <dl> <dt>

2147749911 (0x80041017)
</dt> <dt>



A consulta não era sintaticamente válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_QUERY_TYPE"></span><span id="wbem_e_invalid_query_type"></span>**\_tipo de consulta WBEM E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

2147749912 (0x80041018)
</dt> <dt>



O idioma de consulta solicitado não tem suporte.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ALREADY_EXISTS"></span><span id="wbem_e_already_exists"></span>**o WBEM \_ E \_ já \_ existe**
</dt> <dd> <dl> <dt>

2147749913 (0x80041019)
</dt> <dt>



Em uma operação put, o sinalizador **wbemChangeFlagCreateOnly** foi especificado, mas a instância já existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_SYNTAX"></span><span id="wbem_e_invalid_syntax"></span>**sintaxe de WBEM \_ E \_ inválida \_**
</dt> <dd> <dl> <dt>

2147749921 (0x80041021)
</dt> <dt>



A consulta não é sintaticamente válida.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_READ_ONLY"></span><span id="wbem_e_read_only"></span>**WBEM \_ E \_ \_ somente leitura**
</dt> <dd> <dl> <dt>

2147749923 (0x80041023)
</dt> <dt>



A propriedade que você está tentando modificar é somente leitura.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_PROVIDER_NOT_CAPABLE"></span><span id="wbem_e_provider_not_capable"></span>**\_provedor WBEM \_ E \_ não \_ compatível**
</dt> <dd> <dl> <dt>

2147749924 (0x80041024)
</dt> <dt>



O provedor não pode executar a operação solicitada. A operação pode incluir uma consulta que é muito complexa, recuperando uma instância, criando uma classe, atualizando uma classe, excluindo uma classe ou enumerando uma classe.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_ILLEGAL_NULL"></span><span id="wbem_e_illegal_null"></span>**WBEM \_ E \_ \_ nulo inválido**
</dt> <dd> <dl> <dt>

2147749928 (0x80041028)
</dt> <dt>



Um valor de **nada** / **nulo** foi especificado para uma propriedade que não pode **ser** / **nulo**, como um que esteja marcado por um qualificador de [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**indexado**](/windows/desktop/WmiSdk/optional-qualifiers)ou [**não \_ nulo**](/windows/desktop/WmiSdk/optional-qualifiers) .


</dt> </dl> </dd> <dt>

<span id="WBEM_E_VALUE_OUT_OF_RANGE"></span><span id="wbem_e_value_out_of_range"></span>**WBEM \_ E \_ valor \_ fora \_ do \_ intervalo**
</dt> <dd> <dl> <dt>

2147749931 (0x8004102B)
</dt> <dt>



A solicitação foi feita com um valor fora do intervalo ou é incompatível com o tipo.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD"></span><span id="wbem_e_invalid_method"></span>**\_ \_ método inválido do WBEM E \_**
</dt> <dd> <dl> <dt>

2147749934 (0x8004102E)
</dt> <dt>



O método não está disponível.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_METHOD_PARAMETERS"></span><span id="wbem_e_invalid_method_parameters"></span>**\_parâmetros de \_ \_ método inválido E WBEM \_**
</dt> <dd> <dl> <dt>

2147749935 (0x8004102F)
</dt> <dt>



Os parâmetros fornecidos para o método são inválidos.


</dt> </dl> </dd> <dt>

<span id="WBEM_E_INVALID_OBJECT_PATH"></span><span id="wbem_e_invalid_object_path"></span>**caminho de objeto do WBEM \_ E \_ inválido \_ \_**
</dt> <dd> <dl> <dt>

2147749946 (0x8004103A)
</dt> <dt>



O caminho do objeto especificado não era válido.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                       |
| parâmetro<br/>                   | <dl> <dt>Wbemcli. h</dt> </dl> |



 

