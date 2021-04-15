---
title: Códigos de erro WinSNMP
description: Códigos de erro WinSNMP
ms.assetid: 03b13b82-a31c-47e2-8b4d-17dcc4d19e56
keywords:
- Códigos de erro WinSNMP SNMP
- Códigos de erro SNMP, WinSNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6d3cff7bd1e534f5f9c1fb0ae2ea2687d2ba99a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454277"
---
# <a name="winsnmp-error-codes"></a><span data-ttu-id="a8a5a-105">Códigos de erro WinSNMP</span><span class="sxs-lookup"><span data-stu-id="a8a5a-105">WinSNMP Error Codes</span></span>

<span data-ttu-id="a8a5a-106">\[O SNMP está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-106">\[SNMP is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="a8a5a-107">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-107">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="a8a5a-108">Em vez disso, use [gerenciamento remoto do Windows](/windows/desktop/WinRM/portal), que é a implementação da Microsoft do WS-Man.\]</span><span class="sxs-lookup"><span data-stu-id="a8a5a-108">Instead, use [Windows Remote Management](/windows/desktop/WinRM/portal), which is the Microsoft implementation of WS-Man.\]</span></span>

> [!Note]  
> <span data-ttu-id="a8a5a-109">Os erros descritos neste tópico são distintos dos códigos de erro SNMP definidos pelos RFCs relevantes.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-109">The errors described in this topic are distinct from the SNMP error codes defined by the relevant RFCs.</span></span>

 

<span data-ttu-id="a8a5a-110">Todas as funções WinSNMP retornarão o valor **snmpapi \_ falha** se a função falhar.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-110">All WinSNMP functions return the value **SNMPAPI\_FAILURE** if the function fails.</span></span> <span data-ttu-id="a8a5a-111">O aplicativo WinSNMP deve chamar imediatamente a função [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) para recuperar informações de erro estendidas quando uma função WinSNMP falhar.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-111">The WinSNMP application must immediately call the [**SnmpGetLastError**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpgetlasterror) function to retrieve extended error information when a WinSNMP function fails.</span></span> <span data-ttu-id="a8a5a-112">A tabela a seguir lista os tópicos que discutem os códigos de erro estendidos retornados pelas funções de WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-112">The following table lists topics that discuss extended error codes returned by WinSNMP functions.</span></span>



| <span data-ttu-id="a8a5a-113">Tópico</span><span class="sxs-lookup"><span data-stu-id="a8a5a-113">Topic</span></span>                                                        | <span data-ttu-id="a8a5a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a8a5a-114">Description</span></span>                                             |
|--------------------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="a8a5a-115">Códigos de erro de WinSNMP comuns</span><span class="sxs-lookup"><span data-stu-id="a8a5a-115">WinSNMP Common Error Codes</span></span>](winsnmp-common-error-codes.md) | <span data-ttu-id="a8a5a-116">Descreve os códigos de erro comuns para a API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-116">Describes common error codes for the WinSNMP API.</span></span>       |
| [<span data-ttu-id="a8a5a-117">Erros de transporte de rede</span><span class="sxs-lookup"><span data-stu-id="a8a5a-117">Network Transport Errors</span></span>](network-transport-errors.md)     | <span data-ttu-id="a8a5a-118">Descreve os erros de transporte de rede para a API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-118">Describes network transport errors for the WinSNMP API.</span></span> |



 

<span data-ttu-id="a8a5a-119">Os erros de WinSNMP que transmitem informações específicas do contexto são incluídos na página de referência da função.</span><span class="sxs-lookup"><span data-stu-id="a8a5a-119">The WinSNMP errors that convey context-specific information are included in the function reference page.</span></span>

 

 