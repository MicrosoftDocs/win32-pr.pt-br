---
title: APIs de servidor DVC
description: As APIs de servidor de canal virtual dinâmico (DVC) são implementadas pelo servidor de Conexão de Área de Trabalho Remota (RDC) da conexão.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f43ab4032e4500732e2f9ee6cfa9a2c17f8b1892e55973ba633758792f00bf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118353969"
---
# <a name="dvc-server-apis"></a>APIs de servidor DVC

As APIs de servidor de canal virtual dinâmico (DVC) são implementadas pelo servidor de Conexão de Área de Trabalho Remota (RDC) da conexão.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**IWTSServerChannel**](iwtsserverchannel.md)
</dt> <dd>

Não há suporte para essa interface.

</dd> <dt>

[**IWTSServerChannelManager**](iwtsserverchannelmanager.md)
</dt> <dd>

Não há suporte para essa interface.

</dd> <dt>

[**TPriority**](tpriority.md)
</dt> <dd>

Esta enumeração não é usada.

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a>Alterações no comportamento para outras APIs de servidor

-   A API do servidor foi estendida com uma chamada adicional que abre um canal virtual dinâmico (DVC). A chamada adicional é feita usando a função [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .
-   [**WTSVirtualChannelRead**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    Ao usar essa API com DVC, ela sempre precederá os dados lidos com o [**\_ \_ cabeçalho PDU do canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header). Isso significa que qualquer leitura deve ser feita com pelo menos o bloco de dados de **\_ \_ comprimento de PDU do canal** passado como o buffer de entrada.

-   [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    Se o identificador de arquivo para o DVC for recuperado chamando [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) com o parâmetro *WTSVirtualFileHandle*, a mesma regra será aplicada. Todas as leituras incluirão [**o \_ \_ cabeçalho PDU do canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)e o buffer de leitura deverá ter pelo menos o tamanho do **\_ \_ comprimento de PDU do canal** .

 

 