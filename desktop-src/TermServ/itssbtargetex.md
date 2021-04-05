---
title: Interface ITsSbTargetEx
description: Expõe propriedades que armazenam informações de configuração e estado sobre um destino.
ms.assetid: 3f0f26fb-e8bc-47eb-8038-e51792ad4376
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface ITsSbTargetEx
- Serviços de Área de Trabalho Remota da interface ITsSbTargetEx, descrita
topic_type:
- apiref
api_name:
- ITsSbTargetEx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d53d126d9419f87d91b027b0d69847f67de84be6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919110"
---
# <a name="itssbtargetex-interface"></a>Interface ITsSbTargetEx

Expõe propriedades que armazenam informações de configuração e estado sobre um destino.

Essa interface só está disponível no Windows Server 2012 R2 com o [KB3091411](https://support.microsoft.com/kb/3091411) instalado. A propriedade [**TargetLoad**](itssbtarget-targetload.md) da interface [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) está disponível a partir do Windows Server 2016.

## <a name="members"></a>Membros

A interface **ITsSbTargetEx** herda de [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget). **ITsSbTargetEx** também tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A interface **ITsSbTargetEx** tem essas propriedades.



| Propriedade                                                                      | Tipo de acesso           | Descrição                                                                               |
|:------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------|
| [**EnvironmentName**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_environmentname)<br/>             | Leitura/gravação<br/> | Recupera ou especifica o nome do ambiente associado ao destino.<br/> |
| [**Farmname**](itssbtarget-farmname.md)<br/>                           | Leitura/gravação<br/> | Especifica ou recupera o nome do farm ao qual esse destino está associado.<br/>    |
| [**IpAddresses**](itssbtarget-ipaddresses.md)<br/>                     | Leitura/gravação<br/> | Recupera ou especifica os endereços IP externos do destino.<br/>                |
| [**NumPendingConnections**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numpendingconnections)<br/> | Somente leitura<br/>  | Recupera o número de conexões de usuário pendentes para o destino.<br/>               |
| [**NumSessions**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_numsessions)<br/>                     | Somente leitura<br/>  | Recupera o número de sessões mantidas pelo Broker para o destino.<br/>          |
| [**TargetFQDN**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetfqdn)<br/>                       | Leitura/gravação<br/> | Especifica ou recupera o nome de domínio totalmente qualificado do destino.<br/>          |
| [**TargetLoad**](/previous-versions/windows/desktop/legacy/mt703468(v=vs.85))<br/>                     | Somente leitura<br/>  | Recupera a carga relativa em um destino.<br/>                                       |
| [**TargetName**](itssbtarget-targetname.md)<br/>                       | Leitura/gravação<br/> | Especifica ou recupera o nome do destino.<br/>                                 |
| [**TargetNetbios**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetnetbios)<br/>                 | Leitura/gravação<br/> | Especifica ou recupera o nome NetBIOS do destino.<br/>                         |
| [**TargetSet**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetpropertyset)<br/>         | Leitura/gravação<br/> | Especifica ou recupera o conjunto de propriedades para o destino.<br/>                        |
| [**Destinostate**](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtarget-get_targetstate)<br/>                     | Leitura/gravação<br/> | Especifica ou recupera o estado de destino.<br/>                                       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Nenhum compatível<br/>                                                        |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                |
| Fim do suporte do servidor<br/>    | Windows Server 2012 R2<br/>                                                |
| IID<br/>                      | IID \_ ITsSbTargetEx é definido como 74f99987-625d-11e5-bea1-a0481c7e9064<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dt>

[Interfaces de virtualização Área de Trabalho Remota](remote-desktop-virtualization-interfaces.md)
</dt> </dl>

 

