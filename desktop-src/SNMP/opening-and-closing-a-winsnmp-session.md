---
title: Abrindo e fechando uma sessão WinSNMP
description: Para abrir uma sessão, um aplicativo chama a função SnmpCreateSession.
ms.assetid: 76650231-509b-45be-b156-09752b817854
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e006ffb81f6c2508b3505678b28c3ace8e60c85
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005842"
---
# <a name="opening-and-closing-a-winsnmp-session"></a><span data-ttu-id="a6003-103">Abrindo e fechando uma sessão WinSNMP</span><span class="sxs-lookup"><span data-stu-id="a6003-103">Opening and Closing a WinSNMP Session</span></span>

<span data-ttu-id="a6003-104">Para abrir uma sessão, um aplicativo chama a função [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) .</span><span class="sxs-lookup"><span data-stu-id="a6003-104">To open a session, an application calls the [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession) function.</span></span> <span data-ttu-id="a6003-105">Se a função for concluída com êxito, a implementação do Microsoft WinSNMP abrirá uma sessão e a função retornará um identificador de sessão na forma de um identificador de **\_ sessão HSNMP** .</span><span class="sxs-lookup"><span data-stu-id="a6003-105">If the function completes successfully, the Microsoft WinSNMP implementation opens a session, and the function returns a session identifier in the form of an **HSNMP\_SESSION** handle.</span></span> <span data-ttu-id="a6003-106">Todas as funções de WinSNMP que retornam variáveis de identificador incluem o identificador de sessão como um parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="a6003-106">All WinSNMP functions that return handle variables include the session identifier as an input parameter.</span></span> <span data-ttu-id="a6003-107">Isso permite que a implementação use o identificador para gerenciar com eficiência os recursos no nível da sessão.</span><span class="sxs-lookup"><span data-stu-id="a6003-107">This enables the implementation to use the handle to efficiently manage resources at the session level.</span></span>

<span data-ttu-id="a6003-108">Um aplicativo pode ter várias sessões abertas ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="a6003-108">An application can have multiple sessions open at one time.</span></span> <span data-ttu-id="a6003-109">Várias sessões em um aplicativo podem compartilhar variáveis de identificador.</span><span class="sxs-lookup"><span data-stu-id="a6003-109">Multiple sessions within an application can share handle variables.</span></span>

<span data-ttu-id="a6003-110">Se a implementação não puder abrir uma sessão devido a limitações de recursos, ela retornará SNMPAPI \_ falha quando o aplicativo chamar [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span><span class="sxs-lookup"><span data-stu-id="a6003-110">If the implementation cannot open a session because of resource limitations, it returns SNMPAPI\_FAILURE when the application calls [**SnmpCreateSession**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcreatesession).</span></span> <span data-ttu-id="a6003-111">Se o aplicativo chamar a função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) , ele retornará um erro de alocação de snmpapi \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a6003-111">If the application then calls the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function, it returns SNMPAPI\_ALLOC\_ERROR.</span></span>

<span data-ttu-id="a6003-112">Uma chamada para a função [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) permite que a implementação libere todos os recursos restantes e feche a sessão.</span><span class="sxs-lookup"><span data-stu-id="a6003-112">A call to the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function enables the implementation to free any remaining resources and to close the session.</span></span>

<span data-ttu-id="a6003-113">Para obter mais informações, consulte [objetos de manipulador de recursos](resource-handle-objects.md) e sessões de [WinSNMP](winsnmp-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="a6003-113">For more information, see [Resource Handle Objects](resource-handle-objects.md) and [WinSNMP Sessions](winsnmp-sessions.md).</span></span>

 

 




