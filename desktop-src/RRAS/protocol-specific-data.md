---
title: Estrutura de PROTOCOL_SPECIFIC_DATA (RTM. h)
description: A \_ estrutura de dados específica de protocolo \_ contém memória reservada para dados específicos de um protocolo de roteamento específico.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- RAS da estrutura de PROTOCOL_SPECIFIC_DATA
- RAS de ponteiro de estrutura de PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644822"
---
# <a name="protocol_specific_data-structure"></a>\_Estrutura de dados específica de protocolo \_

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ \_ dados específica de protocolo** contém memória reservada para dados específicos de um protocolo de roteamento específico.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Dados PSD**
</dt> <dd>

Especifica uma matriz de variáveis **DWORD** . Essa memória é reservada para dados que são específicos para protocolos de roteamento.

</dd> </dl>

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
</dt> <dt>

[**\_rota IPX do RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





