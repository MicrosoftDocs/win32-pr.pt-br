---
title: Estrutura de IPX_SPECIFIC_DATA (RTM. h)
description: A \_ estrutura de dados específica de IPX \_ contém dados específicos de IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- RAS da estrutura de IPX_SPECIFIC_DATA
- RAS de ponteiro de estrutura de PIPX_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917958"
---
# <a name="ipx_specific_data-structure"></a>\_Estrutura de dados específica de IPX \_

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ \_ dados específica de IPX** contém dados específicos de IPX.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Membros

<dl> <dt>

**Sinalizadores de FSD \_**
</dt> <dd>

Especifica sinalizadores que descrevem a rota. Atualmente, esse membro é zero ou o seguinte valor de sinalizador.



| Valor                                                                                                                                                                                                      | Significado                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**\_rota de \_ WAN do cliente global \_ IPX \_**</dt> </dl> | Especifica que essa rota é para a rede global alocada para todos os clientes WAN.<br/> |



 

</dd> <dt>

**FSD \_**
</dt> <dd>

Especifica o número de tiques que leva para alcançar a rede de destino. Protocolos de roteamento diferentes do RIP devem converter suas métricas em tiques.

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

Especifica a contagem de saltos associada à rota.

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

[**\_rota IPX do RTM \_**](rtm-ipx-route.md)
</dt> </dl>

 

 





