---
description: A tabela a seguir descreve \_ \_ as opções de soquete do tipo de tráfego IP DSCP \_ .
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
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748730"
---
# <a name="ip_dscp_traffic_type"></a>\_tipo de \_ tráfego IP DSCP \_

A tabela a seguir descreve \_ \_ as opções de soquete do tipo de tráfego IP DSCP \_ .

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_tipo de \_ tráfego IP DSCP \_**</dt> <dd> <dl> <dt> 

| Opção              | Obter | Definir | Tipo de optval | Descrição                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo de tráfego DSCP \_ | Sim | Sim | DWORD       | Ao definir esse valor como valores definidos no **\_ \_ tipo de tráfego DSCP**, um aplicativo poderá solicitar que seus pacotes de rede sejam tratados de acordo com o tipo de serviço que está sendo solicitado. Chamadas semelhantes a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) podem ser usadas para obter a configuração atual para o tipo de tráfego solicitado no soquete especificado |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------------------|--------------------------------------------------------------------------------|
| Fim do suporte do cliente<br/> | Windows 10<br/>                                                          |
| Fim do suporte do servidor<br/> | Windows Server 2016<br/>                                                 |
| parâmetro<br/>                | <dl> <dt>N/A</dt> </dl> |



 

 




