---
title: Escrevendo um driver para capturar quadros PPP
description: Este documento explica como desenvolver um driver que pode capturar quadros PPP no Windows Vista antes que eles sejam compactados/criptografados no caminho de envio ou depois de serem descompactados/descriptografados no caminho de recebimento.
ms.assetid: 1b3fe1b8-2b11-4aed-98e1-464b8c0821ec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d592596674cd64af5122303afefcfc81026dad27
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104007163"
---
# <a name="writing-a-driver-to-capture-ppp-frames"></a><span data-ttu-id="041fc-103">Escrevendo um driver para capturar quadros PPP</span><span class="sxs-lookup"><span data-stu-id="041fc-103">Writing a Driver to Capture PPP Frames</span></span>

<span data-ttu-id="041fc-104">Quando os quadros de protocolo PPP (PPP) são enviados por meio de um túnel PPTP com criptografia ativada, ou por meio de um túnel L2TP (protocolo de encapsulamento de camada 2) que usa IPSec para criptografia, o utilitário de captura de quadro PPP típico só pode capturar quadros PPP que tenham um campo de identidade de protocolo criptografado.</span><span class="sxs-lookup"><span data-stu-id="041fc-104">When Point-to-Point Protocol (PPP) frames are sent through a Point-to-Point Tunneling Protocol (PPTP) tunnel with encryption turned on, or through a Layer 2 Tunneling Protocol (L2TP) tunnel that uses IPSec for encryption, the typical PPP frame capture utility can only capture PPP frames that have an encrypted protocol identity field.</span></span> <span data-ttu-id="041fc-105">Este documento explica como desenvolver um driver que pode capturar quadros PPP no Windows Vista antes que eles sejam compactados/criptografados no caminho de envio ou depois de serem descompactados/descriptografados no caminho de recebimento.</span><span class="sxs-lookup"><span data-stu-id="041fc-105">This document explains how to develop a driver that can capture PPP frames in Windows Vista before they are compressed/encrypted in the send path or after they are decompressed/decrypted in the receive path.</span></span>

1.  <span data-ttu-id="041fc-106">Escreva um driver de protocolo NDIS.</span><span class="sxs-lookup"><span data-stu-id="041fc-106">Write an NDIS protocol driver.</span></span> <span data-ttu-id="041fc-107">Para obter detalhes, consulte [drivers de protocolo ndis 6,0](https://msdn.microsoft.com/library/ms795570.aspx) ou [drivers de protocolo ndis (NDIS 5,1)](https://msdn.microsoft.com/library/ms801145.aspx).</span><span class="sxs-lookup"><span data-stu-id="041fc-107">For details, see [NDIS 6.0 Protocol Drivers](https://msdn.microsoft.com/library/ms795570.aspx) or [NDIS Protocol Drivers (NDIS 5.1)](https://msdn.microsoft.com/library/ms801145.aspx).</span></span>
2.  <span data-ttu-id="041fc-108">Instale o driver com uma identidade de hardware de "MS \_ Netmon".</span><span class="sxs-lookup"><span data-stu-id="041fc-108">Install the driver with a hardware identity of "ms\_netmon".</span></span> <span data-ttu-id="041fc-109">Para obter instruções detalhadas sobre como instalar o driver com uma identidade de hardware específica, consulte a [seção modelos inf](https://msdn.microsoft.com/library/ms794357.aspx).</span><span class="sxs-lookup"><span data-stu-id="041fc-109">For detailed instructions on how to install the driver with a specific hardware identity, see [INF Models Section](https://msdn.microsoft.com/library/ms794357.aspx).</span></span>
    > [!Note]  
    > <span data-ttu-id="041fc-110">Cada computador com Windows Vista permite a instalação de apenas uma entidade de driver que tenha a \_ identidade de hardware "MS Netmon".</span><span class="sxs-lookup"><span data-stu-id="041fc-110">Each Windows Vista machine permits the installation of only one driver entity that has the "ms\_netmon" hardware identity.</span></span> <span data-ttu-id="041fc-111">Para instalar outro driver com essa identidade, o primeiro driver deve ser desinstalado.</span><span class="sxs-lookup"><span data-stu-id="041fc-111">To install another driver with this identity, the first driver must be uninstalled.</span></span> <span data-ttu-id="041fc-112">Um driver que é instalado sem usar a identidade de \_ hardware "MS Netmon" não pode executar a associação necessária para capturar quadros PPP.</span><span class="sxs-lookup"><span data-stu-id="041fc-112">A driver that is installed without using the "ms\_netmon" hardware identity cannot perform the binding needed to capture PPP frames.</span></span>

     

3.  <span data-ttu-id="041fc-113">O driver de protocolo deve especificar "ndiswanbh" como a interface de associação para capturar quadros PPP.</span><span class="sxs-lookup"><span data-stu-id="041fc-113">The protocol driver should specify "ndiswanbh" as the binding interface for capturing PPP frames.</span></span> <span data-ttu-id="041fc-114">Para obter instruções detalhadas, consulte [especificando interfaces de associação](https://msdn.microsoft.com/library/aa937923.aspx).</span><span class="sxs-lookup"><span data-stu-id="041fc-114">For detailed instructions, see [Specifying Binding Interfaces](https://msdn.microsoft.com/library/aa937923.aspx).</span></span>
4.  <span data-ttu-id="041fc-115">A implementação de [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) no driver deve dar suporte a "NdisMediumWan" como parte da matriz média, para que ele possa abrir a borda de miniporta ndiswanbh usando a função [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) .</span><span class="sxs-lookup"><span data-stu-id="041fc-115">The [ProtocolBindAdapter](https://msdn.microsoft.com/library/ms797311.aspx) implementation in the driver should support "NdisMediumWan" as a part of the medium array, so that it can open the ndiswanbh miniport edge using the [NdisOpenAdapter](https://msdn.microsoft.com/library/ms804862.aspx) function.</span></span>
5.  <span data-ttu-id="041fc-116">Se a função [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) for chamada com status êxito de status de NDIS \_ \_ , o driver de protocolo deverá definir o OID [Gen do \_ \_ \_ \_ filtro de pacotes atual](https://msdn.microsoft.com/library/bb314089.aspx) com os sinalizadores tipo de pacote de [NDIS \_ \_ \_ promíscuo](https://msdn.microsoft.com/library/bb314089.aspx) e [tipo de pacote de NDIS \_ \_ \_ todos os \_ locais](https://msdn.microsoft.com/library/bb314089.aspx) nessa associação.</span><span class="sxs-lookup"><span data-stu-id="041fc-116">If the [ProtocolOpenAdapterComplete](https://msdn.microsoft.com/library/ms797287.aspx) function is called with status NDIS\_STATUS\_SUCCESS, the protocol driver should set the [OID\_GEN\_CURRENT\_PACKET\_FILTER](https://msdn.microsoft.com/library/bb314089.aspx) OID with the flags [NDIS\_PACKET\_TYPE\_PROMISCUOUS](https://msdn.microsoft.com/library/bb314089.aspx) and [NDIS\_PACKET\_TYPE\_ALL\_LOCAL](https://msdn.microsoft.com/library/bb314089.aspx) over this binding.</span></span> <span data-ttu-id="041fc-117">Quando isso for feito, o driver de protocolo receberá os quadros PPP descriptografados da camada de enquadramento PPP em sua função [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) .</span><span class="sxs-lookup"><span data-stu-id="041fc-117">Once this is done, the protocol driver will receive the decrypted PPP frames from the PPP framing layer in its [ProtocolReceive](https://msdn.microsoft.com/library/ms797274.aspx) function.</span></span>

> [!Note]  
> <span data-ttu-id="041fc-118">Essas informações se aplicam somente a drivers em um computador com Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="041fc-118">This information only applies to drivers on a Windows Vista machine.</span></span>

 

 

 




