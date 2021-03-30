---
description: O provedor WMI do coletor de eventos de inicialização fornece acesso a informações de conexão e configuração para o recurso de coleta de eventos de instalação e inicialização no Windows Server.
ms.assetid: ab9ac8f0-69a5-4a2d-8ee5-1f003aa1bb5b
ms.tgt_platform: multiple
title: Provedor WMI do coletor de eventos de inicialização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38ef27b2989f856fdcfda82d4ee0e68c3913167
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826110"
---
# <a name="boot-event-collector-wmi-provider"></a>Provedor WMI do coletor de eventos de inicialização

## <a name="purpose"></a>Finalidade

O provedor WMI do coletor de eventos de inicialização fornece acesso a informações de conexão e configuração para o recurso de coleta de eventos de instalação e inicialização no Windows Server. Isso permite que você exiba uma lista das conexões atuais e o histórico de conexão entre um servidor de coletor e seus computadores de destino. Além disso, esse provedor permite que você gerencie a configuração de um servidor coletor.

> [!Note]  
> O provedor WMI do coletor de eventos de inicialização é implementado no BEvtCol.exe.

 

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**TargetForwarding**](targetforwarding.md)
</dt> <dd>

Recupera os dados de encaminhamento de um computador de destino.

</dd> <dt>

[**TargetForwardingDestination**](targetforwardingdestination.md)
</dt> <dd>

Os destinos conhecidos que contêm os dados coletados. Disponível somente se o coletor estiver em execução com o log de status habilitado.

</dd> <dt>

[**TargetForwardingHistory**](targetforwardinghistory.md)
</dt> <dd>

O histórico recente de alterações nos dados de encaminhamento de um computador de destino.

</dd> <dt>

[**Control**](control.md)
</dt> <dd>

Controle da instância do coletor. Requer os privilégios de administrador (BA).

</dd> </dl>

 

 



