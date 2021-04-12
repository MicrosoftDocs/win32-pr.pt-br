---
title: Diretrizes de hardware periférico
description: Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo force a desabilitação do redirecionamento do dispositivo usando uma política do sistema ou uma política de grupo.
ms.assetid: f033d469-a860-4968-b289-bc4eab23bd46
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8e8e6a81a75abdef76851fedcb979526e1653
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364240"
---
# <a name="peripheral-hardware-guidelines"></a><span data-ttu-id="916ad-103">Diretrizes de hardware periférico</span><span class="sxs-lookup"><span data-stu-id="916ad-103">Peripheral hardware guidelines</span></span>

<span data-ttu-id="916ad-104">Para um cliente Conexão de Área de Trabalho Remota (RDC), o servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) é o computador local.</span><span class="sxs-lookup"><span data-stu-id="916ad-104">To a Remote Desktop Connection (RDC) client, the Remote Desktop Session Host (RD Session Host) server is the local computer.</span></span> <span data-ttu-id="916ad-105">Consequentemente, dispositivos como unidades de disco e impressoras conectadas ao servidor aparecem como dispositivos locais para um cliente.</span><span class="sxs-lookup"><span data-stu-id="916ad-105">Consequently, devices such as disk drives and printers attached to the server appear as local devices to a client.</span></span> <span data-ttu-id="916ad-106">Por outro lado, as unidades e impressoras anexadas a um terminal de cliente podem parecer dispositivos remotos, dependendo das opções selecionadas para a conexão, do servidor usado e da versão do software cliente usado.</span><span class="sxs-lookup"><span data-stu-id="916ad-106">In contrast, drives and printers attached to a client terminal can appear to be remote devices, depending on the options selected for the connection, the server used, and the version of the client software used.</span></span>

<span data-ttu-id="916ad-107">Embora a versão inicial do Serviços de Área de Trabalho Remota não tivesse suporte a aplicativos que enviam a saída diretamente para portas seriais, paralelas e de som anexadas ao terminal do cliente, as versões atuais permitem que esses dispositivos apareçam como dispositivos locais em aplicativos em execução na sessão de Serviços de Área de Trabalho Remota.</span><span class="sxs-lookup"><span data-stu-id="916ad-107">While the initial release of Remote Desktop Services did not support applications that send output directly to serial, parallel, and sound ports attached to the client terminal, the current versions do allow these devices to appear as local devices to applications running in the Remote Desktop Services session.</span></span>

<span data-ttu-id="916ad-108">Se o dispositivo de hardware não for projetado para funcionar em uma sessão remota, os fornecedores deverão garantir que o software do driver de dispositivo force a desabilitação do redirecionamento do dispositivo usando uma política do sistema ou uma política de grupo.</span><span class="sxs-lookup"><span data-stu-id="916ad-108">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

 

 




