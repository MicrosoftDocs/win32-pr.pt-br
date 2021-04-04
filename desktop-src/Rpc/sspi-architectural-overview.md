---
title: Visão geral da arquitetura SSPI
description: O SSPI é uma interface de software.
ms.assetid: 2497afea-33dd-45ae-891b-bacf390ef338
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 910cef52def2f398606fd541b8ed170f7e216078
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007894"
---
# <a name="sspi-architectural-overview"></a><span data-ttu-id="5113b-103">Visão geral da arquitetura SSPI</span><span class="sxs-lookup"><span data-stu-id="5113b-103">SSPI Architectural Overview</span></span>

<span data-ttu-id="5113b-104">O SSPI é uma interface de software.</span><span class="sxs-lookup"><span data-stu-id="5113b-104">SSPI is a software interface.</span></span> <span data-ttu-id="5113b-105">Bibliotecas de programação distribuídas, como RPC, podem usá-las para comunicações autenticadas.</span><span class="sxs-lookup"><span data-stu-id="5113b-105">Distributed programming libraries such as RPC can use it for authenticated communications.</span></span> <span data-ttu-id="5113b-106">Um ou mais módulos de software fornecem os recursos de autenticação reais.</span><span class="sxs-lookup"><span data-stu-id="5113b-106">One or more software modules provide the actual authentication capabilities.</span></span> <span data-ttu-id="5113b-107">Cada módulo, chamado de SSP (provedor de suporte de segurança), é implementado como uma DLL (biblioteca de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="5113b-107">Each module, called a security support provider (SSP), is implemented as a dynamic link library (DLL).</span></span> <span data-ttu-id="5113b-108">Um SSP fornece um ou mais pacotes de segurança.</span><span class="sxs-lookup"><span data-stu-id="5113b-108">An SSP provides one or more security packages.</span></span>

<span data-ttu-id="5113b-109">Uma variedade de SSPs e pacotes estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="5113b-109">A variety of SSPs and packages are available.</span></span> <span data-ttu-id="5113b-110">O Windows é fornecido com o pacote de segurança do NTLM e o pacote de segurança do protocolo Microsoft Kerberos.</span><span class="sxs-lookup"><span data-stu-id="5113b-110">Windows ships with the NTLM security package and the Microsoft Kerberos protocol security package.</span></span> <span data-ttu-id="5113b-111">Além disso, você pode optar por instalar o pacote de segurança SSL (Secure Socket Layer) ou qualquer outro SSP compatível com o SSPI.</span><span class="sxs-lookup"><span data-stu-id="5113b-111">In addition, you may choose to install the Secure Socket Layer (SSL) security package, or any other SSPI-compatible SSP.</span></span>

<span data-ttu-id="5113b-112">O uso de SSPI garante que, independentemente do SSP que você selecionar, seu aplicativo acesse os recursos de autenticação de maneira uniforme.</span><span class="sxs-lookup"><span data-stu-id="5113b-112">Using SSPI ensures that no matter which SSP you select, your application accesses the authentication features in a uniform manner.</span></span> <span data-ttu-id="5113b-113">Esse recurso fornece ao seu aplicativo maior independência da implementação da rede do que estava disponível no passado.</span><span class="sxs-lookup"><span data-stu-id="5113b-113">This capability provides your application greater independence from the implementation of the network than was available in the past.</span></span>

<span data-ttu-id="5113b-114">Os aplicativos distribuídos se comunicam através da interface RPC.</span><span class="sxs-lookup"><span data-stu-id="5113b-114">Distributed applications communicate through the RPC interface.</span></span> <span data-ttu-id="5113b-115">O software RPC, por sua vez, acessa os recursos de autenticação de um SSP por meio do SSPI.</span><span class="sxs-lookup"><span data-stu-id="5113b-115">The RPC software in turn, accesses the authentication features of an SSP through the SSPI.</span></span>

<span data-ttu-id="5113b-116">Para obter mais informações, consulte [SSPI](/windows/desktop/SecAuthN/sspi).</span><span class="sxs-lookup"><span data-stu-id="5113b-116">For more information, see [SSPI](/windows/desktop/SecAuthN/sspi).</span></span>

 

 