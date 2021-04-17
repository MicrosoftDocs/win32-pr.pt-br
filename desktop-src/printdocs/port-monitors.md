---
description: Depois que um driver de dispositivo converteu um arquivo de diário inteiro em comandos de dispositivo bruto, o arquivo dos comandos convertidos é passado de volta para o spooler.
ms.assetid: 149e44d0-052a-48ba-8f65-59eab193c785
title: Monitores de porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4b00e4171b3fd6e366a66deae8f5e70578ca92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811555"
---
# <a name="port-monitors"></a><span data-ttu-id="bf575-103">Monitores de porta</span><span class="sxs-lookup"><span data-stu-id="bf575-103">Port Monitors</span></span>

<span data-ttu-id="bf575-104">Depois que um driver de dispositivo converteu um arquivo de diário inteiro em comandos de dispositivo bruto, o arquivo dos comandos convertidos é passado de volta para o spooler.</span><span class="sxs-lookup"><span data-stu-id="bf575-104">Once a device driver has converted an entire journal file into raw device commands, the file of converted commands is passed back to the spooler.</span></span> <span data-ttu-id="bf575-105">O spooler envia esses comandos de baixo nível para um monitor.</span><span class="sxs-lookup"><span data-stu-id="bf575-105">The spooler sends these low-level commands to a monitor.</span></span> <span data-ttu-id="bf575-106">Um monitor de porta é um. dll que passa os comandos de dispositivo brutos pela rede, por meio de uma porta paralela, ou por meio de uma porta serial para o dispositivo de impressora.</span><span class="sxs-lookup"><span data-stu-id="bf575-106">A port monitor is a .dll that passes the raw device commands over the network, through a parallel port, or through a serial port to the printer device.</span></span> <span data-ttu-id="bf575-107">Monitores de porta personalizados podem ser instalados para dar suporte à passagem de dados de dispositivo por meio de outras portas de comunicação.</span><span class="sxs-lookup"><span data-stu-id="bf575-107">Custom port monitors can be installed to support passing device data through other communication ports.</span></span>

<span data-ttu-id="bf575-108">Use as funções a seguir para trabalhar com monitores de porta.</span><span class="sxs-lookup"><span data-stu-id="bf575-108">Use the following functions to work with port monitors.</span></span>



| <span data-ttu-id="bf575-109">Função</span><span class="sxs-lookup"><span data-stu-id="bf575-109">Function</span></span>                               | <span data-ttu-id="bf575-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf575-110">Description</span></span>                                                                         |
|----------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="bf575-111">**Addmonitor**</span><span class="sxs-lookup"><span data-stu-id="bf575-111">**AddMonitor**</span></span>](addmonitor.md)       | <span data-ttu-id="bf575-112">Instala um monitor de porta local e vincula a configuração, os dados e os arquivos de monitoramento.</span><span class="sxs-lookup"><span data-stu-id="bf575-112">Installs a local port monitor and links the configuration, data, and monitor files.</span></span> |
| [<span data-ttu-id="bf575-113">**DeleteMonitor**</span><span class="sxs-lookup"><span data-stu-id="bf575-113">**DeleteMonitor**</span></span>](deletemonitor.md) | <span data-ttu-id="bf575-114">Remove um monitor de porta adicionado pela função [**addmonitor**](addmonitor.md) .</span><span class="sxs-lookup"><span data-stu-id="bf575-114">Removes a port monitor added by the [**AddMonitor**](addmonitor.md) function.</span></span>      |
| [<span data-ttu-id="bf575-115">**EnumMonitors**</span><span class="sxs-lookup"><span data-stu-id="bf575-115">**EnumMonitors**</span></span>](enummonitors.md)   | <span data-ttu-id="bf575-116">Enumera os monitores de porta instalados em um servidor especificado.</span><span class="sxs-lookup"><span data-stu-id="bf575-116">Enumerates the port monitors installed on a specified server.</span></span>                       |



 

 

 



