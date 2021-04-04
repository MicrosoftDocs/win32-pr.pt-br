---
title: Modificar o padrão de redirecionamento de dispositivo
description: Como Área de Trabalho Remota servidores de gateway tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.
ms.assetid: 03F2617C-D478-4A51-9EEC-E9643CA831B7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 925099b94c75dca39d381bdf57ae9730fb840da7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822706"
---
# <a name="modify-device-redirection-default"></a><span data-ttu-id="df29d-103">Modificar o padrão de redirecionamento de dispositivo</span><span class="sxs-lookup"><span data-stu-id="df29d-103">Modify Device Redirection Default</span></span>

<span data-ttu-id="df29d-104">Como Área de Trabalho Remota servidores de gateway tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota, talvez seja necessário desabilitar esse padrão em alguns casos.</span><span class="sxs-lookup"><span data-stu-id="df29d-104">Because Remote Desktop Gateway servers attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server, you may need to disable this default in some cases.</span></span>

<span data-ttu-id="df29d-105">No Windows Server 2008 R2 e posterior, Área de Trabalho Remota servidores de gateway, por padrão, tentam impor políticas de redirecionamento de dispositivo seguro antes de passar a conexão do cliente para um servidor Host da Sessão da Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="df29d-105">On Windows Server 2008 R2 and later, Remote Desktop Gateway servers will by default attempt to enforce secure device redirection policies before passing the client connection through to a Remote Desktop Session Host server.</span></span> <span data-ttu-id="df29d-106">No entanto, esse recurso não tem suporte em alguns servidores.</span><span class="sxs-lookup"><span data-stu-id="df29d-106">However, this feature is not supported by some servers.</span></span> <span data-ttu-id="df29d-107">Por exemplo, isso não tem suporte para conexões com sessões de console do Hyper-V e pode ser necessário desabilitar o padrão para dar suporte à autenticação federada.</span><span class="sxs-lookup"><span data-stu-id="df29d-107">For example, this is not supported for connections to Hyper-V console sessions, and it may be necessary to disable the default to support federated authentication.</span></span> <span data-ttu-id="df29d-108">Nesses casos, esse recurso pode ser desabilitado com a criação da seguinte chave do registro para permitir que as conexões passem.</span><span class="sxs-lookup"><span data-stu-id="df29d-108">In these cases, this feature can be disabled by creating the following registry key to allow connections to go through.</span></span>

<span data-ttu-id="df29d-109">**HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Terminal Server gateway \\ preRDPDisableRegKey**</span><span class="sxs-lookup"><span data-stu-id="df29d-109">**HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Terminal Server Gateway\\preRDPDisableRegKey**</span></span>

<span data-ttu-id="df29d-110">Quando essa chave existir, o gateway de Área de Trabalho Remota não impedirá o redirecionamento de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="df29d-110">When this key exists, the Remote Desktop Gateway will not enforce device redirection.</span></span>

 

 




