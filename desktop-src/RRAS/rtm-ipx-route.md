---
title: Estrutura de RTM_IPX_ROUTE (RTM. h)
description: A \_ estrutura de rota IPX do RTM \_ contém informações que descrevem uma rota para a família de protocolos IPX.
ms.assetid: ffa0637c-2197-4ebd-a5ef-e174dd0ccb15
keywords:
- RAS da estrutura de RTM_IPX_ROUTE
- RAS de ponteiro de estrutura de PRTM_IPX_ROUTE
topic_type:
- apiref
api_name:
- RTM_IPX_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d32333dd6a6b53ee4600dda388a318bdf9404b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918224"
---
# <a name="rtm_ipx_route-structure"></a>\_Estrutura de rota IPX do RTM \_

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ \_ rota IPX do RTM** contém informações que descrevem uma rota para a família de protocolos IPX.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RTM_IPX_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IPX_NETWORK            RR_Network;
  IPX_NEXT_HOP_ADDRESS   RR_NextHopAddress;
  IPX_SPECIFIC_DATA      RR_FamilySpecificData;
} RTM_IPX_ROUTE, *PRTM_IPX_ROUTE;
```



## <a name="members"></a>Membros

<dl> <dt>

**\_Carimbo de data/hora RR**
</dt> <dd>

Especifica a hora em que a entrada de rota foi criada ou atualizada pela última vez. Esse membro é definido pelo Gerenciador de tabela de roteamento. O tempo é expresso como uma estrutura FILETIME.

</dd> <dt>

**\_ROUTINGPROTOCOL RR**
</dt> <dd>

Especifica o protocolo de roteamento que adicionou a rota.

</dd> <dt>

**Tipo de registro de recurso \_**
</dt> <dd>

Especifica a interface pela qual a rota foi obtida.

</dd> <dt>

**\_PROTOCOLSPECIFICDATA RR**
</dt> <dd>

Especifica uma estrutura de [**\_ \_ dados específica de protocolo**](protocol-specific-data.md) que contém a memória reservada para dados específicos para protocolos de roteamento.

</dd> <dt>

**\_Rede RR**
</dt> <dd>

Especifica uma estrutura de [**\_ rede IPX**](ipx-network.md) que contém um endereço de rede IP.

</dd> <dt>

**\_NEXTHOPADDRESS RR**
</dt> <dd>

Especifica uma estrutura de [**\_ endereço de próximo \_ salto \_ IPX**](ipx-next-hop-address.md) que contém o endereço do roteador de próximo salto.

</dd> <dt>

**\_FAMILYSPECIFICDATA RR**
</dt> <dd>

Especifica uma estrutura de [**\_ \_ dados específica de IPX**](ipx-specific-data.md) que contém dados específicos para a família de protocolo IPX.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros da estrutura **de \_ \_ rota IPX do RTM** são todos alinhados em **DWORD** .

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

[Estruturas da versão 1 do Gerenciador de tabela de roteamento \_ \_](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_rede IPX**](ipx-network.md)
</dt> <dt>

[**\_endereço do próximo \_ salto \_ IPX**](ipx-next-hop-address.md)
</dt> <dt>

[**\_dados específicos de IPX \_**](ipx-specific-data.md)
</dt> </dl>

 

 





