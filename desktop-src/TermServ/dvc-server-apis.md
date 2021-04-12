---
title: APIs de servidor DVC
description: As APIs de servidor de canal virtual dinâmico (DVC) são implementadas pelo servidor de Conexão de Área de Trabalho Remota (RDC) da conexão.
ms.assetid: 9743ce32-9262-4af3-b013-668e834e279c
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3bc413cb6bc60f5b6a16f282fe3d4d1aa830272
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366586"
---
# <a name="dvc-server-apis"></a><span data-ttu-id="9b666-103">APIs de servidor DVC</span><span class="sxs-lookup"><span data-stu-id="9b666-103">DVC Server APIs</span></span>

<span data-ttu-id="9b666-104">As APIs de servidor de canal virtual dinâmico (DVC) são implementadas pelo servidor de Conexão de Área de Trabalho Remota (RDC) da conexão.</span><span class="sxs-lookup"><span data-stu-id="9b666-104">The dynamic virtual channel (DVC) server APIs are implemented by the Remote Desktop Connection (RDC) server of the connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b666-105">Nesta seção</span><span class="sxs-lookup"><span data-stu-id="9b666-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="9b666-106">**IWTSServerChannel**</span><span class="sxs-lookup"><span data-stu-id="9b666-106">**IWTSServerChannel**</span></span>](iwtsserverchannel.md)
</dt> <dd>

<span data-ttu-id="9b666-107">Não há suporte para essa interface.</span><span class="sxs-lookup"><span data-stu-id="9b666-107">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="9b666-108">**IWTSServerChannelManager**</span><span class="sxs-lookup"><span data-stu-id="9b666-108">**IWTSServerChannelManager**</span></span>](iwtsserverchannelmanager.md)
</dt> <dd>

<span data-ttu-id="9b666-109">Não há suporte para essa interface.</span><span class="sxs-lookup"><span data-stu-id="9b666-109">This interface is not supported.</span></span>

</dd> <dt>

[<span data-ttu-id="9b666-110">**TPriority**</span><span class="sxs-lookup"><span data-stu-id="9b666-110">**TPriority**</span></span>](tpriority.md)
</dt> <dd>

<span data-ttu-id="9b666-111">Esta enumeração não é usada.</span><span class="sxs-lookup"><span data-stu-id="9b666-111">This enumeration is not used.</span></span>

</dd> </dl>

## <a name="changes-in-behavior-for-other-server-apis"></a><span data-ttu-id="9b666-112">Alterações no comportamento para outras APIs de servidor</span><span class="sxs-lookup"><span data-stu-id="9b666-112">Changes in Behavior for Other Server APIs</span></span>

-   <span data-ttu-id="9b666-113">A API do servidor foi estendida com uma chamada adicional que abre um canal virtual dinâmico (DVC).</span><span class="sxs-lookup"><span data-stu-id="9b666-113">The server API has been extended with an additional call which opens a dynamic virtual channel (DVC).</span></span> <span data-ttu-id="9b666-114">A chamada adicional é feita usando a função [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) .</span><span class="sxs-lookup"><span data-stu-id="9b666-114">The additional call is made using the [**WTSVirtualChannelOpenEx**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopenex) function.</span></span>
-   [<span data-ttu-id="9b666-115">**WTSVirtualChannelRead**</span><span class="sxs-lookup"><span data-stu-id="9b666-115">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)

    <span data-ttu-id="9b666-116">Ao usar essa API com DVC, ela sempre precederá os dados lidos com o [**\_ \_ cabeçalho PDU do canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span><span class="sxs-lookup"><span data-stu-id="9b666-116">When using this API with DVC, it will always prepend the data read with [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header).</span></span> <span data-ttu-id="9b666-117">Isso significa que qualquer leitura deve ser feita com pelo menos o bloco de dados de **\_ \_ comprimento de PDU do canal** passado como o buffer de entrada.</span><span class="sxs-lookup"><span data-stu-id="9b666-117">This means that any read must be done with at least the **CHANNEL\_PDU\_LENGTH** data block passed as the input buffer.</span></span>

-   [<span data-ttu-id="9b666-118">**ReadFile**</span><span class="sxs-lookup"><span data-stu-id="9b666-118">**ReadFile**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-readfile)

    <span data-ttu-id="9b666-119">Se o identificador de arquivo para o DVC for recuperado chamando [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) com o parâmetro *WTSVirtualFileHandle*, a mesma regra será aplicada.</span><span class="sxs-lookup"><span data-stu-id="9b666-119">If the file handle to the DVC is retrieved by calling [**WTSVirtualChannelQuery**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery) with parameter *WTSVirtualFileHandle*, the same rule will apply.</span></span> <span data-ttu-id="9b666-120">Todas as leituras incluirão [**o \_ \_ cabeçalho PDU do canal**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)e o buffer de leitura deverá ter pelo menos o tamanho do **\_ \_ comprimento de PDU do canal** .</span><span class="sxs-lookup"><span data-stu-id="9b666-120">All reads will include the [**CHANNEL\_PDU\_HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header), and the read buffer has to be at least **CHANNEL\_PDU\_LENGTH** size.</span></span>

 

 