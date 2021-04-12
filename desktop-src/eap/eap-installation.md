---
title: Instalação do EAP
description: Os fornecedores implementam EAPs, também conhecidos como protocolos de autenticação, em DLLs (bibliotecas de vínculo dinâmico).
ms.assetid: af10b1e9-45c9-4640-ba79-fc9c23cc3c47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 619505a55108ebde0e14d7ff20c78394c6c90fad
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104365327"
---
# <a name="eap-installation"></a><span data-ttu-id="d6f10-103">Instalação do EAP</span><span class="sxs-lookup"><span data-stu-id="d6f10-103">EAP Installation</span></span>

<span data-ttu-id="d6f10-104">Os fornecedores implementam EAPs, também conhecidos como protocolos de autenticação, em DLLs (bibliotecas de vínculo dinâmico).</span><span class="sxs-lookup"><span data-stu-id="d6f10-104">Vendors implement EAPs, also known as authentication protocols, in dynamic-link libraries (DLLs).</span></span> <span data-ttu-id="d6f10-105">Uma DLL para o protocolo de autenticação deve residir nos computadores cliente e servidor.</span><span class="sxs-lookup"><span data-stu-id="d6f10-105">A DLL for the authentication protocol must reside on both the client and server computers.</span></span> <span data-ttu-id="d6f10-106">Para simplificar, as DLLs do cliente e do servidor podem ser idênticas; no entanto, isso não é um requisito.</span><span class="sxs-lookup"><span data-stu-id="d6f10-106">For simplicity, the client and server DLLs may be identical; however, this is not a requirement.</span></span> <span data-ttu-id="d6f10-107">Além disso, lembre-se de que a mesma DLL pode dar suporte a mais de um protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d6f10-107">Also, be aware that the same DLL may support more than one authentication protocol.</span></span>

<span data-ttu-id="d6f10-108">O fornecedor deve fornecer software de instalação para instalar e remover a DLL.</span><span class="sxs-lookup"><span data-stu-id="d6f10-108">The vendor should provide setup software to install and remove the DLL.</span></span> <span data-ttu-id="d6f10-109">O software de instalação também deve criar as chaves e os valores apropriados para o protocolo de autenticação no registro do sistema e removê-los após a desinstalação.</span><span class="sxs-lookup"><span data-stu-id="d6f10-109">The setup software should also create the appropriate keys and values for the authentication protocol in the system registry and remove them upon uninstall.</span></span>

<span data-ttu-id="d6f10-110">A instalação de cada DLL de EAP deve criar a seguinte chave do registro.</span><span class="sxs-lookup"><span data-stu-id="d6f10-110">The installation of each EAP DLL should create the following registry key.</span></span>

<span data-ttu-id="d6f10-111">**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Services** \\ **RASMAN** \\  \\  \\ **&lt; eaptypeid &gt;** PPP EAP</span><span class="sxs-lookup"><span data-stu-id="d6f10-111">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Rasman**\\**PPP**\\**EAP**\\**&lt;eaptypeid&gt;**</span></span>

<span data-ttu-id="d6f10-112">No caminho anterior, **&lt; eaptypeid &gt;** é a ID do protocolo de autenticação.</span><span class="sxs-lookup"><span data-stu-id="d6f10-112">In the preceding path, **&lt;eaptypeid&gt;** is the ID of the authentication protocol.</span></span> <span data-ttu-id="d6f10-113">O fornecedor deve obter essa ID da IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="d6f10-113">The vendor must obtain this ID from the Internet Assigned Numbers Authority (IANA).</span></span>

<span data-ttu-id="d6f10-114">Para obter mais informações e uma descrição dos valores com suporte para essa chave, consulte [valores do registro do protocolo de autenticação](authentication-protocol-registry-values.md).</span><span class="sxs-lookup"><span data-stu-id="d6f10-114">For more information and a description of the supported values for this key, see [Authentication Protocol Registry Values](authentication-protocol-registry-values.md).</span></span>

 

 




