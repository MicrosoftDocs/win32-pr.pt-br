---
title: Abrindo e fechando um aplicativo WinSNMP
description: O aplicativo WinSNMP deve chamar a função SnmpStartup com êxito antes de chamar qualquer outra função WinSNMP.
ms.assetid: ff2b99c9-c2fd-4bb7-8fd5-799e72c4560d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f960a22a6155d3f3eeec770af361fac2c0eb036e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005844"
---
# <a name="opening-and-closing-a-winsnmp-application"></a><span data-ttu-id="e61a6-103">Abrindo e fechando um aplicativo WinSNMP</span><span class="sxs-lookup"><span data-stu-id="e61a6-103">Opening and Closing a WinSNMP Application</span></span>

<span data-ttu-id="e61a6-104">O aplicativo WinSNMP deve chamar a função [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) com êxito antes de chamar qualquer outra função WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="e61a6-104">The WinSNMP application must call the [**SnmpStartup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstartup) function successfully before it calls any other WinSNMP function.</span></span> <span data-ttu-id="e61a6-105">A função **SnmpStartup** permite que a implementação do Microsoft WinSNMP execute procedimentos de inicialização.</span><span class="sxs-lookup"><span data-stu-id="e61a6-105">The **SnmpStartup** function enables the Microsoft WinSNMP implementation to perform initialization procedures.</span></span> <span data-ttu-id="e61a6-106">A função também retorna ao aplicativo a versão da API WinSNMP à qual a implementação dá suporte, o nível de comunicações SNMP que ele suporta e os modos de conversão e retransmissão padrão da implementação.</span><span class="sxs-lookup"><span data-stu-id="e61a6-106">The function also returns to the application the version of the WinSNMP API that the implementation supports, the level of SNMP communications it supports, and the implementation's default translation and retransmission modes.</span></span>

<span data-ttu-id="e61a6-107">O aplicativo WinSNMP deve chamar a função [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) quando o aplicativo não exigir mais os serviços da implementação.</span><span class="sxs-lookup"><span data-stu-id="e61a6-107">The WinSNMP application must call the [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) function when the application no longer requires the implementation's services.</span></span> <span data-ttu-id="e61a6-108">Embora o **SnmpCleanup** permita que a implementação desaloque todos os recursos alocados para o aplicativo, é recomendável que o aplicativo chame primeiro a função [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) uma vez para cada sessão WinSNMP aberta, a fim de maximizar o desempenho da implementação.</span><span class="sxs-lookup"><span data-stu-id="e61a6-108">Even though **SnmpCleanup** enables the implementation to deallocate all resources allocated to the application, it is recommended that the application first call the [**SnmpClose**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpclose) function once for each open WinSNMP session, to maximize the implementation's performance.</span></span> <span data-ttu-id="e61a6-109">O aplicativo WinSNMP deve chamar [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) como a última função WinSNMP antes de ser encerrado.</span><span class="sxs-lookup"><span data-stu-id="e61a6-109">The WinSNMP application must call [**SnmpCleanup**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcleanup) as the last WinSNMP function before it terminates.</span></span>

 

 




