---
title: IP_SPECIFIC_DATA (Rtm.h)
description: A estrutura DADOS ESPECÍFICOS de IP \_ contém dados específicos de IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- ras IP_SPECIFIC_DATA estrutura de IP_SPECIFIC_DATA
- PIP_SPECIFIC_DATA RAS do ponteiro de estrutura
topic_type:
- apiref
api_name:
- IP_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 906ae9f2accb3d380227f08ad6b65642b96ce6bfa928591bd11a69c478f531b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036666"
---
# <a name="ip_specific_data-structure"></a>Estrutura \_ DE DADOS ESPECÍFICA DE \_ IP

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

A **estrutura \_ DADOS ESPECÍFICOS de IP** contém dados específicos de IP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _IP_SPECIFIC_DATA {
  DWORD FSD_Type;
  DWORD FSD_Policy;
  DWORD FSD_NextHopAS;
  DWORD FSD_Priority;
  DWORD FSD_Metric;
  DWORD FSD_Metric1;
  DWORD FSD_Metric2;
  DWORD FSD_Metric3;
  DWORD FSD_Metric4;
  DWORD FSD_Metric5;
  DWORD FSD_Flags;
} IP_SPECIFIC_DATA, *PIP_SPECIFIC_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Tipo \_ FSD**
</dt> <dd>

Especifica o tipo de rota conforme definido em [RFC 1354.](routing-protocols-request-for-comments.md) A tabela a seguir mostra os valores possíveis para esse membro.



| Membro                                                                                               | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | O tipo de rota não foi especificado. O tipo é diferente daqueles listados aqui.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | A rota é inválida. Normalmente, esse valor é usado para invalidar uma rota. No entanto, como a invalidação não é suportada pelo gerenciador de tabela de roteamento, a rota ainda é considerada em cálculos de melhor rota. Portanto, os protocolos de roteamento não devem usar esse valor.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | A rota é uma rota local, ou seja, o próximo salto é o destino final.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | A rota é uma rota remota, ou seja, o próximo salto não é o destino final.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**Política \_ FSD**
</dt> <dd>

Especifica o conjunto de condições que causaria a seleção de uma rota de vários caminhos. Normalmente, esse membro está no formato IP TOS. Para obter mais informações, [consulte RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**NextHopAS do FSD \_**
</dt> <dd>

Especifica o número do sistema autônomo do próximo salto.

</dd> <dt>

**Prioridade do \_ FSD**
</dt> <dd>

Especifica um valor de métrica. O gerenciador de tabela de roteamento usa esse valor para comparar essa entrada de rota com entradas de rota obtidas de outros protocolos de roteamento. O valor desse membro é definido pelo gerenciador de tabela de roteamento.

</dd> <dt>

**Métrica do \_ FSD**
</dt> <dd>

Especifica um valor de métrica. O gerenciador de tabela de roteamento usa esse valor para comparar essa entrada de rota com outras entradas de rota obtidas do mesmo protocolo de roteamento. O valor desse membro é definido pelo protocolo de roteamento.

</dd> <dt>

**FSD \_ Metric1**
</dt> <dd>

Especifica um valor de métrica específico do protocolo de roteamento. Esse valor de métrica está documentado [no RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**FSD \_ Metric2**
</dt> <dd>

Especifica um valor de métrica específico do protocolo de roteamento. Esse valor de métrica está documentado [no RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**FSD \_ Metric3**
</dt> <dd>

Especifica um valor de métrica específico do protocolo de roteamento. Esse valor de métrica está documentado [no RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**FSD \_ Metric4**
</dt> <dd>

Especifica um valor de métrica específico do protocolo de roteamento. Esse valor de métrica está documentado [no RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**FSD \_ Metric5**
</dt> <dd>

Especifica um valor de métrica específico do protocolo de roteamento. Esse valor de métrica está documentado [no RFC 1354.](routing-protocols-request-for-comments.md)

</dd> <dt>

**Sinalizadores \_ FSD**
</dt> <dd>

Especifica se a rota é válida. O protocolo de roteamento deve primeiro limpar esses sinalizadores e, em seguida, definir a rota como válida ou inválida. O protocolo de roteamento deve usar as **macros ClearRouteFlags(),** **SetRouteValid()** e **ClearRouteValid()** para executar essas operações. Essas macros são definidas em Rtm.h.

</dd> </dl>

## <a name="remarks"></a>Comentários

O gerenciador de tabelas de roteamento usa os **membros Prioridade do FSD \_** e Métrica **FSD \_** para calcular a melhor rota para uma rede de destino específica.

Os **membros da \_ \[ Métrica FSD de 1 a 5 \]** são para conformidade com o MIB II. Os agentes do MIB II exibem apenas esses valores de métrica. Eles não exibem o valor da métrica **\_ Métrica FSD.** Para que a Métrica **do \_ FSD** seja exibida, o protocolo de roteamento também deve armazenar o valor em um dos membros da **Métrica FSD \_ de \[ 1 a 5 \]** membros.

O gerenciador de tabela de roteamento não usa os valores de métrica nos membros **da Métrica FSD de 1 a \_ \[ 5 \]** ao calcular a melhor rota para uma rede de destino. Portanto, o protocolo de roteamento deve garantir que o **membro da Métrica FSD \_** tenha um valor de métrica apropriado.

Um protocolo de roteamento pode usar os **Sinalizadores FSD \_** para marcar uma rota como inválida, se a rota não deve ser usada por outros protocolos de roteamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Fim do suporte ao servidor<br/>    | Windows Server 2003<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estruturas do Gerenciador de Tabelas de Roteamento versão 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IP \_ ROUTE**](rtm-ip-route.md)
</dt> </dl>

 

 





