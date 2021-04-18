---
description: Antes de começar a desenvolver um aplicativo do Microsoft Windows HTTP Services (WinHTTP), primeiro você deve decidir se usará a API C/C++ ou a interface COM.
ms.assetid: 451ad247-962f-4af1-bb21-0aed4ef5f93c
title: Escolhendo uma interface WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc529e6052b0de2de19a7c15ff1cfad226cee2cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765310"
---
# <a name="choosing-a-winhttp-interface"></a><span data-ttu-id="d7635-103">Escolhendo uma interface WinHTTP</span><span class="sxs-lookup"><span data-stu-id="d7635-103">Choosing a WinHTTP Interface</span></span>

<span data-ttu-id="d7635-104">Antes de começar a desenvolver um aplicativo do Microsoft Windows HTTP Services (WinHTTP), primeiro você deve decidir se usará a API C/C++ ou a interface COM.</span><span class="sxs-lookup"><span data-stu-id="d7635-104">Before you begin to develop a Microsoft Windows HTTP Services (WinHTTP) application, you must first decide whether to use the C/C++ API or the COM interface.</span></span> <span data-ttu-id="d7635-105">A tabela a seguir resume as vantagens e desvantagens associadas a cada uma dessas abordagens.</span><span class="sxs-lookup"><span data-stu-id="d7635-105">The following table summarizes the advantages and disadvantages associated with each of these approaches.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d7635-106">API C/C++</span><span class="sxs-lookup"><span data-stu-id="d7635-106">C/C++ API</span></span></th>
<th><span data-ttu-id="d7635-107">Interface COM</span><span class="sxs-lookup"><span data-stu-id="d7635-107">COM interface</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d7635-108">Vantagens</span><span class="sxs-lookup"><span data-stu-id="d7635-108">Advantages</span></span></td>
<td><ul>
<li><span data-ttu-id="d7635-109">As respostas podem ser processadas em partes, o que é mais eficiente.</span><span class="sxs-lookup"><span data-stu-id="d7635-109">Responses can be processed in chunks, which is more efficient.</span></span></li>
<li><span data-ttu-id="d7635-110">As operações POST também podem ser processadas em partes, acelerando o tempo de processamento.</span><span class="sxs-lookup"><span data-stu-id="d7635-110">POST operations can also be processed in chunks, speeding processing time.</span></span></li>
<li><span data-ttu-id="d7635-111">Suporte a AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="d7635-111">AutoProxy support.</span></span></li>
<li><span data-ttu-id="d7635-112">Acesso ao conjunto completo de recursos do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d7635-112">Access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="d7635-113">Dados binários podem ser facilmente manipulados.</span><span class="sxs-lookup"><span data-stu-id="d7635-113">Binary data can easily be handled.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d7635-114">A criação de um aplicativo é fácil e requer menos linhas de código do que a API C/C++.</span><span class="sxs-lookup"><span data-stu-id="d7635-114">Creating an application is easy and requires fewer lines of code than the C/C++ API.</span></span></li>
<li><span data-ttu-id="d7635-115">A interface pode ser usada por linguagens de script.</span><span class="sxs-lookup"><span data-stu-id="d7635-115">The interface can be used by scripting languages.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d7635-116">Desvantagens</span><span class="sxs-lookup"><span data-stu-id="d7635-116">Disadvantages</span></span></td>
<td><ul>
<li><span data-ttu-id="d7635-117">O processamento é mais complexo.</span><span class="sxs-lookup"><span data-stu-id="d7635-117">Processing is more complex.</span></span></li>
<li><span data-ttu-id="d7635-118">A API C/C++ requer mais etapas do que a interface COM para executar as mesmas ações.</span><span class="sxs-lookup"><span data-stu-id="d7635-118">The C/C++ API requires more steps than the COM interface to perform the same actions.</span></span></li>
<li><span data-ttu-id="d7635-119">A configuração de uma solicitação leva mais código.</span><span class="sxs-lookup"><span data-stu-id="d7635-119">Setting up a request takes more code.</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d7635-120">A interface COM não fornece acesso ao conjunto completo de recursos do WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="d7635-120">The COM interface does not provide access to the full feature set of WinHTTP.</span></span></li>
<li><span data-ttu-id="d7635-121">É difícil lidar com tipos de dados binários em algumas linguagens de script, como VBScript e JScript.</span><span class="sxs-lookup"><span data-stu-id="d7635-121">It is difficult to handle binary data types in some scripting languages, such as VBScript and JScript.</span></span></li>
<li><span data-ttu-id="d7635-122">A interface COM não oferece suporte a AutoProxy.</span><span class="sxs-lookup"><span data-stu-id="d7635-122">The COM interface does not support AutoProxy.</span></span></li>
<li><span data-ttu-id="d7635-123">Os aplicativos devem usar o modelo de APARTMENT_THREADED COM.</span><span class="sxs-lookup"><span data-stu-id="d7635-123">Applications must use the COM APARTMENT_THREADED model.</span></span></li>
<li><span data-ttu-id="d7635-124">Antes que uma resposta possa começar a ser processada, a resposta inteira deve primeiro ser recebida e armazenada em buffer.</span><span class="sxs-lookup"><span data-stu-id="d7635-124">Before a response can begin being processed, the entire response must first be received and buffered.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

 

 



