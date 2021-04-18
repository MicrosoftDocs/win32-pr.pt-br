---
title: Estrutura de RTM_IP_ROUTE (RTM. h)
description: A \_ estrutura de rota de IP RTM \_ contém informações que descrevem uma rota de propriedade da família de protocolos IP.
ms.assetid: e752a4ae-a6bf-4cd3-9638-7615ff3901b7
keywords:
- RAS da estrutura de RTM_IP_ROUTE
- RAS de ponteiro de estrutura de PRTM_IP_ROUTE
topic_type:
- apiref
api_name:
- RTM_IP_ROUTE
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1978503a3ec37e0c39716569030d5ea6599e19d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778525"
---
# <a name="rtm_ip_route-structure"></a>Estrutura de rota de \_ IP RTM \_

\[Essa API foi substituída pela API do [Gerenciador de tabela de roteamento versão 2](about-routing-table-manager-version-2.md) e não estará disponível além do Windows Server 2003. Os aplicativos devem usar a API da versão 2 do Gerenciador de tabela de roteamento.\]

A estrutura de **\_ \_ rota de IP RTM** contém informações que descrevem uma rota de propriedade da família de protocolos IP.

## <a name="syntax"></a>Sintaxe


```C++
typedef struct _RTM_IP_ROUTE {
  FILETIME               RR_TimeStamp;
  DWORD                  RR_RoutingProtocol;
  DWORD                  RR_InterfaceID;
  PROTOCOL_SPECIFIC_DATA RR_ProtocolSpecificData;
  IP_NETWORK             RR_Network;
  IP_NEXT_HOP_ADDRESS    RR_NextHopAddress;
  IP_SPECIFIC_DATA       RR_FamilySpecificData;
} RTM_IP_ROUTE, *PRTM_IP_ROUTE;
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

Especifica uma estrutura de [**\_ \_ dados específica de protocolo**](protocol-specific-data.md) que contém memória reservada para dados específicos do protocolo de roteamento.

</dd> <dt>

**\_Rede RR**
</dt> <dd>

Especifica uma estrutura de [**\_ rede IP**](ip-network.md) que contém um endereço de rede IP.

</dd> <dt>

**\_NEXTHOPADDRESS RR**
</dt> <dd>

Especifica uma estrutura de [**\_ endereço de próximo \_ salto \_ IP**](ip-next-hop-address.md) que contém o endereço do roteador do próximo salto.

</dd> <dt>

**\_FAMILYSPECIFICDATA RR**
</dt> <dd>

Especifica uma estrutura de [**\_ \_ dados específica de IP**](ip-specific-data.md) que contém dados específicos da família de protocolos IP.

</dd> </dl>

## <a name="remarks"></a>Comentários

Os membros da estrutura **de \_ \_ rota de IP RTM** são alinhados em **DWORD** .

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

[**\_rede IP**](ip-network.md)
</dt> <dt>

[**\_endereço do próximo \_ salto \_ IP**](ip-next-hop-address.md)
</dt> <dt>

[**\_dados específicos de IP \_**](ip-specific-data.md)
</dt> </dl>

 

 





