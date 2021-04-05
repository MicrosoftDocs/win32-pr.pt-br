---
title: Estrutura de IP_SPECIFIC_DATA (RTM. h)
description: A \_ estrutura de dados específica de IP contém dados específicos de IP.
ms.assetid: 68f2f4cc-141b-4f22-94ac-cc72e8dcca0a
keywords:
- RAS da estrutura de IP_SPECIFIC_DATA
- RAS de ponteiro de estrutura de PIP_SPECIFIC_DATA
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
ms.openlocfilehash: 2a3ed319f7cf42295bf918ed3ec67f5d59fe5d80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085888"
---
# <a name="ip_specific_data-structure"></a>\_Estrutura de dados específica de IP \_

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ dados específica de IP** contém dados específicos de IP.

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

**Tipo de FSD \_**
</dt> <dd>

Especifica o tipo de rota conforme definido no [RFC 1354](routing-protocols-request-for-comments.md). A tabela a seguir mostra os valores possíveis para esse membro.



| Membro                                                                                               | Significado                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | O tipo de rota não foi especificado. O tipo é diferente daqueles listados aqui.<br/>                                                                                                                                                                                         |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | A rota é inválida. Normalmente, esse valor é usado para invalidar uma rota. No entanto, como a invalidação não é suportada pelo Gerenciador de tabelas de roteamento, a rota ainda é considerada em cálculos de melhor rota. Portanto, os protocolos de roteamento não devem usar esse valor.<br/> |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | A rota é uma rota local, ou seja, o próximo salto é o destino final.<br/>                                                                                                                                                                                            |
| <span id="4"></span><dl> <dt>**quatro**</dt> </dl> | A rota é uma rota remota, ou seja, o próximo salto não é o destino final.<br/>                                                                                                                                                                                       |



 

</dd> <dt>

**Política de FSD \_**
</dt> <dd>

Especifica o conjunto de condições que causaria a seleção de uma rota de vários caminhos. Esse membro normalmente está no formato IP TOS. Para obter mais informações, consulte [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ NextHopAS**
</dt> <dd>

Especifica o número do sistema autônomo do próximo salto.

</dd> <dt>

**\_Prioridade FSD**
</dt> <dd>

Especifica um valor de métrica. O Gerenciador de tabela de roteamento usa esse valor para comparar essa entrada de rota com entradas de rota obtidas de outros protocolos de roteamento. O valor desse membro é definido pelo Gerenciador de tabela de roteamento.

</dd> <dt>

**\_Métrica FSD**
</dt> <dd>

Especifica um valor de métrica. O Gerenciador de tabela de roteamento usa esse valor para comparar essa entrada de rota com outras entradas de rota obtidas do mesmo protocolo de roteamento. O valor desse membro é definido pelo protocolo de roteamento.

</dd> <dt>

**FSD \_ Metric1**
</dt> <dd>

Especifica um valor de métrica específico de protocolo de roteamento. Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric2**
</dt> <dd>

Especifica um valor de métrica específico de protocolo de roteamento. Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric3**
</dt> <dd>

Especifica um valor de métrica específico de protocolo de roteamento. Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric4**
</dt> <dd>

Especifica um valor de métrica específico de protocolo de roteamento. Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**FSD \_ Metric5**
</dt> <dd>

Especifica um valor de métrica específico de protocolo de roteamento. Esse valor de métrica está documentado em [RFC 1354](routing-protocols-request-for-comments.md).

</dd> <dt>

**Sinalizadores de FSD \_**
</dt> <dd>

Especifica se a rota é válida. O protocolo de roteamento deve primeiro limpar esses sinalizadores e, em seguida, definir a rota como válida ou inválida. O protocolo de roteamento deve usar as macros **ClearRouteFlags ()**, **SetRouteValid ()** e **ClearRouteValid ()** para executar essas operações. Essas macros são definidas no RTM. h.

</dd> </dl>

## <a name="remarks"></a>Comentários

O Gerenciador de tabela de roteamento usa a **\_ prioridade FSD** e os membros da **\_ métrica FSD** para calcular a melhor rota para uma rede de destino específica.

Os membros da **\_ métrica \[ 1-5 \] do FSD** são para conformidade com MIB II. Os agentes MIB II exibem apenas esses valores de métrica. Eles não exibem o valor da métrica **\_ métrica FSD** . Para que a **\_ métrica FSD** seja exibida, o protocolo de roteamento também deve armazenar o valor em um dos membros **FSD \_ métrica \[ 1-5 \]** .

O Gerenciador de tabela de roteamento não usa os valores de métrica nos membros da **métrica do FSD \_ \[ 1-5 \]** ao calcular a melhor rota para uma rede de destino. Portanto, o protocolo de roteamento deve garantir que o membro de **\_ métrica FSD** tenha um valor de métrica apropriado.

Um protocolo de roteamento pode usar **os \_ sinalizadores FSD** para marcar uma rota como inválida, se a rota não deve ser usada por outros protocolos de roteamento.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estruturas da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_rota de IP RTM \_**](rtm-ip-route.md)
</dt> </dl>

 

 





