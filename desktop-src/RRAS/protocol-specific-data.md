---
title: PROTOCOL_SPECIFIC_DATA estrutura (Rtm.h)
description: A estrutura \_ PROTOCOL SPECIFIC DATA contém memória reservada para dados \_ específicos de um protocolo de roteamento específico.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- ras PROTOCOL_SPECIFIC_DATA estrutura de PROTOCOL_SPECIFIC_DATA
- PPROTOCOL_SPECIFIC_DATA ras de estrutura
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
ms.openlocfilehash: fe43e17827a4c6308c7bfd4499de60ec9105a9fa525ab5aad0226887d02ae8e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036456"
---
# <a name="protocol_specific_data-structure"></a>ESTRUTURA \_ DE DADOS ESPECÍFICA DO \_ PROTOCOLO

\[Essa API foi superada pela API do Gerenciador de Tabelas de Roteamento versão [2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API do Gerenciador de Tabelas de Roteamento versão 2.\]

A **estrutura PROTOCOL SPECIFIC \_ \_ DATA** contém memória reservada para dados específicos de um protocolo de roteamento específico.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Dados \_ PSD**
</dt> <dd>

Especifica uma matriz de **variáveis DWORD.** Essa memória é reservada para dados específicos aos protocolos de roteamento.

</dd> </dl>

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
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> </dl>

 

 





