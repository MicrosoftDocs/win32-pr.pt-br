---
description: A tabela a seguir descreve opções de \_ soquete IP DSCP \_ TRAFFIC \_ TYPE.
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 87915dc214b0ba306b4f38dbd833b27199277564fa8c2815b9147e0d82253589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097846"
---
# <a name="ip_dscp_traffic_type"></a>TIPO \_ DE TRÁFEGO IP DSCP \_ \_

A tabela a seguir descreve opções de \_ soquete IP DSCP \_ TRAFFIC \_ TYPE.

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**TIPO \_ DE TRÁFEGO IP DSCP \_ \_**</dt> <dd> <dl> <dt> 

| Opção              | Obter | Definir | Tipo de aceitação | Descrição                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DE TRÁFEGO \_ \_ DSCP | Sim | Sim | DWORD       | Ao definir esse valor como valores definidos em **TIPO DE TRÁFEGO DSCP, \_ \_** um aplicativo poderá solicitar que seus pacotes de rede sejam tratados de acordo com o tipo de serviço que está sendo solicitado. Da mesma forma, chamadas [**para getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) podem ser usadas para obter a configuração atual para o tipo de tráfego solicitado no soquete determinado |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|--------------------------------------------------------------------------------|
| Fim do suporte ao cliente<br/> | Windows 10<br/>                                                          |
| Fim do suporte ao servidor<br/> | Windows Server 2016<br/>                                                 |
| Cabeçalho<br/>                | <dl> <dt>N/A</dt> </dl> |



 

 




