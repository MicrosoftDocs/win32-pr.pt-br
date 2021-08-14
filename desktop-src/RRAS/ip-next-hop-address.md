---
title: Estrutura de IP_NEXT_HOP_ADDRESS (RTM. h)
description: A \_ estrutura de endereço do próximo salto IP \_ \_ contém o endereço do roteador do próximo salto para uma rota IP.
ms.assetid: a97b3995-dfaa-4e53-be86-3ad46b8be691
keywords:
- RAS da estrutura de IP_NEXT_HOP_ADDRESS
- RAS da estrutura de PIP_NEXT_HOP_ADDRESS
topic_type:
- apiref
api_name:
- IP_NEXT_HOP_ADDRESS
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94f79b850c7d5f48e5f409e5380ad7345288187b8939b752b4f282b2274a99cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790960"
---
# <a name="ip_next_hop_address-structure"></a>\_Estrutura de endereço do próximo \_ salto IP \_

\[esta api foi substituída pela api do [gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ endereço do próximo \_ salto \_ IP** contém o endereço do roteador do próximo salto para uma rota IP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _IP_NEXT_HOP_ADDRESS {
  DWORD N_NetNumber;
  DWORD N_NetMask;
} IP_NEXT_HOP_ADDRESS, *PIP_NEXT_HOP_ADDRESS;
```



## <a name="members"></a>Membros

<dl> <dt>

**N \_ Netnumber**
</dt> <dd>

Especifica o endereço de rede IP expresso como um endereço IP na ordem de bytes de máquina.

</dd> <dt>

**N \_ máscara de rede**
</dt> <dd>

Especifica a máscara de rede. Aplique essa máscara ao endereço IP para extrair o endereço de rede. A máscara de rede está na ordem de bytes de máquina.

</dd> </dl>

## <a name="remarks"></a>Comentários

A estrutura de **\_ endereço do próximo \_ salto \_ IP** é um typedef da estrutura de [**\_ rede IP**](ip-network.md) . O TypeDef está no RTM. h.

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

[**\_rede IP**](ip-network.md)
</dt> <dt>

[**\_rota de IP RTM \_**](rtm-ip-route.md)
</dt> </dl>

 

 





