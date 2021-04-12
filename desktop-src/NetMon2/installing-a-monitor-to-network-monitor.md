---
description: A instalação de uma DLL de monitor é um processo simples.
ms.assetid: f2c18faa-0010-4d26-b7e9-e8a7b5d11981
title: Instalando um monitor para Monitor de Rede
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7fb6847d1ea93895b190ce2377247c586c06f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172332"
---
# <a name="installing-a-monitor-to-network-monitor"></a><span data-ttu-id="5bf49-103">Instalando um monitor para Monitor de Rede</span><span class="sxs-lookup"><span data-stu-id="5bf49-103">Installing a Monitor to Network Monitor</span></span>

<span data-ttu-id="5bf49-104">A instalação de uma DLL de monitor é um processo simples.</span><span class="sxs-lookup"><span data-stu-id="5bf49-104">Installing a monitor DLL is a simple process.</span></span> <span data-ttu-id="5bf49-105">Primeiro, copie a DLL e o formulário de configuração HTML associado para o subdiretório de monitores do NPP (por exemplo, C: \\ Windows \\ System32 \\ NPP \\ monitores).</span><span class="sxs-lookup"><span data-stu-id="5bf49-105">First, copy the DLL and the associated HTML configuration form to your NPP Monitors subdirectory (for example, C:\\Windows\\System32\\Npp\\Monitors).</span></span> <span data-ttu-id="5bf49-106">Quando copiado para o diretório, o monitor será reconhecido e estará disponível na próxima vez que a ferramenta de controle de monitor ou o serviço de controle de monitor (MCSVC) for ativado.</span><span class="sxs-lookup"><span data-stu-id="5bf49-106">When copied to the directory, the monitor will be recognized and available the next time the Monitor Control Tool or Monitor Control Service (MCSVC) is activated.</span></span>

<span data-ttu-id="5bf49-107">Por exemplo, se a variável de ambiente,% SystemRoot% for C: \\ Windows, o subdiretório monitor será c: \\ Windows \\ System32 \\ NPP \\ monitores.</span><span class="sxs-lookup"><span data-stu-id="5bf49-107">For example, if the environment variable, %SystemRoot% is C:\\Windows, then the monitor subdirectory is C:\\Windows\\System32\\Npp\\Monitors.</span></span>

 

 



