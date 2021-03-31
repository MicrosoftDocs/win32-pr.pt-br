---
title: Estrutura de IPX_NETWORK (RTM. h)
description: A \_ estrutura de rede IPX descreve um endereço de rede IPX.
ms.assetid: 83fc4022-8515-4a51-ac47-f92572447fbf
keywords:
- RAS da estrutura de IPX_NETWORK
- RAS de ponteiro de estrutura de PIPX_NETWORK
topic_type:
- apiref
api_name:
- IPX_NETWORK
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04aabf363c0152ba520bb5c8894142715b5bff56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917959"
---
# <a name="ipx_network-structure"></a>\_Estrutura de rede IPX

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ rede IPX** descreve um endereço de rede IPX.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _IPX_NETWORK {
  DWORD N_NetNumber;
} IPX_NETWORK, *PIPX_NETWORK;
```



## <a name="members"></a>Membros

<dl> <dt>

**N \_ Netnumber**
</dt> <dd>

Contém o número de rede IPX na ordem de bytes de máquina.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                        |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Fim do suporte do servidor<br/>    | Windows Server 2003<br/>                                                   |
| parâmetro<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[Referência da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Estruturas da versão 1 do Gerenciador de tabela de roteamento](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_rota IPX do RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





