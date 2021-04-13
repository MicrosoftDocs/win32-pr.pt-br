---
title: Estrutura de CB_TARGET_INFO (Cbclient. h)
description: Contém informações sobre o computador de destino e os endereços IP em que as conexões de entrada devem ser redirecionadas.
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- Estrutura de CB_TARGET_INFO Serviços de Área de Trabalho Remota
- Ponteiro de estrutura de PCB_TARGET_INFO Serviços de Área de Trabalho Remota
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369392"
---
# <a name="cb_target_info-structure"></a>Estrutura de informações de \_ destino CB \_

Contém informações sobre o computador de destino e os endereços IP em que as conexões de entrada devem ser redirecionadas. Essa estrutura é usada com o método [**IConnectionBrokerClient:: GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) .

## <a name="syntax"></a>Sintaxe


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>Membros

<dl> <dt>

**ServerName**
</dt> <dd>

Representa o nome de domínio totalmente qualificado do servidor de destino. Para um cenário de RDV (virtualização de Área de Trabalho Remota), esse membro é **nulo**. Para um cenário de RDSH (host de sessão Área de Trabalho Remota), esse membro contém o nome do servidor em que a conexão de entrada é redirecionada.

</dd> <dt>

**AddressCount**
</dt> <dd>

O número de entradas válidas na matriz de **endereços** .

</dd> <dt>

**Endereços**
</dt> <dd>

Uma matriz de cadeias de caracteres que contêm os endereços IP onde as conexões de entrada são redirecionadas. O número de elementos válidos nessa matriz é especificado no membro **AddressCount** .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Cbclient. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





