---
description: Códigos de retorno do WMI que indicam o status e não indicam um erro.
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: Constantes de não erro do WMI (WbemCli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165322"
---
# <a name="wmi-non-error-constants"></a>Constantes de não erro do WMI

Códigos de retorno do WMI que indicam o status e não indicam um erro.

Se uma operação não resultar em um erro, o WMI retornará um dos códigos a seguir como um **HRESULT** que indica o status da operação.

> [!Note]  
> Alguns métodos em classes WMI podem retornar códigos de erro de sistema e rede (64, por exemplo). Você pode verificar a definição desses tipos de códigos de erro usando o comando **net helpmsg** na janela do prompt de comando. Por exemplo, o comando **net helpmsg 64** retorna a mensagem: o nome de rede especificado não está mais disponível.

 

Em C++, você pode chamar [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) e especificar **C: \\ Windows \\ System32 \\ WBEM \\wmiutils.dll** como o módulo de mensagem.

<dl> <dt>

<span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**\_ \_ não há erro no WBEM \_**
</dt> <dd> <dl> <dt>

0 (0x0)
</dt> <dt>



A operação foi bem-sucedida.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ falso**
</dt> <dd> <dl> <dt>

1 (0x1)
</dt> <dt>



Não há mais objetos disponíveis, o número de objetos retornados é menor que o número solicitado ou este é o final de uma enumeração. Esse valor também é retornado quando esse método é chamado com um valor de 0 para o parâmetro *uCount* .


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**o WBEM \_ S \_ já \_ existe**
</dt> <dd> <dl> <dt>

262145 (0x40001)
</dt> <dt>



Foi feita uma tentativa de criar um objeto ou classe que já existe.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM \_ S \_ Redefinir \_ para \_ padrão**
</dt> <dd> <dl> <dt>

262146 (0x40002)
</dt> <dt>



Uma propriedade substituída foi excluída. Esse valor é retornado para sinalizar que o valor original não substituído foi restaurado como resultado da exclusão.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ diferentes**
</dt> <dd> <dl> <dt>

262147 (0x40003)
</dt> <dt>



Os itens (objetos, classes e assim por diante) que estão sendo comparados não são idênticos.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S \_ TIMEDOUT**
</dt> <dd> <dl> <dt>

262148 (0x40004)
</dt> <dt>



Uma chamada atingiu o tempo limite. Essa não é uma condição de erro. Portanto, alguns resultados também podem ter sido retornados.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ não \_ mais \_ dados**
</dt> <dd> <dl> <dt>

262149 (0x40005)
</dt> <dt>



Não há mais dados disponíveis na enumeração e o usuário deve encerrar a enumeração.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**\_operação do \_ WBEM \_ cancelada**
</dt> <dd> <dl> <dt>

262150 (0x40006)
</dt> <dt>



A operação foi cancelada intencional ou não intencionalmente.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ pendentes**
</dt> <dd> <dl> <dt>

262151 (0x40007)
</dt> <dt>



Uma solicitação ainda está em andamento e os resultados ainda não estão disponíveis.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**\_ \_ objetos duplicados do WBEM S \_**
</dt> <dd> <dl> <dt>

262152 (0x40008)
</dt> <dt>



Foi detectada mais de uma cópia do mesmo objeto no conjunto de resultados de uma enumeração.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**\_ \_ acesso \_ NEGAdo a WBEM**
</dt> <dd> <dl> <dt>

262153 (0x40009)
</dt> <dt>



O usuário teve o acesso negado a alguns, mas não a todos os recursos.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**\_ \_ resultados parciais do WBEM \_**
</dt> <dd> <dl> <dt>

262160 (0x40010)
</dt> <dt>



O usuário não recebeu todos os objetos solicitados devido a recursos inacessíveis (que não sejam violações de segurança).


</dt> </dl> </dd> <dt>

<span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**\_ \_ serviço limitado do \_ WBEM**
</dt> <dd> <dl> <dt>

274433 (0x43001)
</dt> <dt>



O provedor é capaz de serviço limitado.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**o WBEM \_ S foi \_ atualizado indiretamente \_**
</dt> <dd> <dl> <dt>

274434 (0x43002)
</dt> <dt>



Reservado para uso futuro.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                         |
| parâmetro<br/>                   | <dl> <dt>WbemCli. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>WbemCli. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Códigos de retorno do WMI](wmi-return-codes.md)
</dt> </dl>

 

