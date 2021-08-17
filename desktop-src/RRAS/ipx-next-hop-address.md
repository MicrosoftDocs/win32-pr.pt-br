---
title: Estrutura de IPX_NEXT_HOP_ADDRESS (RTM. h)
description: A \_ estrutura de endereço do próximo salto IPX \_ \_ contém o endereço do roteador do próximo salto para uma rota IPX.
ms.assetid: 079e3284-6238-4bcf-a17f-68ff86775f18
keywords:
- RAS da estrutura de IPX_NEXT_HOP_ADDRESS
- RAS de ponteiro de estrutura de PIPX_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IPX_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8abbb67f916960d015b26337734ffcff6f8e6551ab664bd4f4cc0d7511630a7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790754"
---
# <a name="ipx_next_hop_address-structure"></a>\_Estrutura de endereço do próximo salto do IPX \_ \_

\[esta api foi substituída pela api do [gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ endereço do próximo \_ salto \_ IPX** contém o endereço do roteador do próximo salto para uma rota IPX.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _IPX_NEXT_HOP_ADDRESS {
  BYTE NHA_Mac[6];
} IPX_NEXT_HOP_ADDRESS, *PIPX_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**NHA \_ Mac**
</dt> <dd>

Especifica o endereço MAC do roteador do próximo salto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                   |
| Cabeçalho<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estruturas da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_rota IPX do RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





