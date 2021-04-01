---
title: Requisitos de software para a API WinSNMP
description: Um aplicativo WinSNMP deve acessar a API WinSNMP por meio da biblioteca de vínculo dinâmico WSNMP32.DLL.
ms.assetid: ba0b9443-3fcf-41e2-993e-54e042f9d785
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c30302f9f6d15cef221da46ce721dc4727a44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159286"
---
# <a name="software-requirements-for-the-winsnmp-api"></a><span data-ttu-id="87574-103">Requisitos de software para a API WinSNMP</span><span class="sxs-lookup"><span data-stu-id="87574-103">Software Requirements for the WinSNMP API</span></span>

<span data-ttu-id="87574-104">Um aplicativo WinSNMP deve acessar a API WinSNMP por meio da biblioteca de vínculo dinâmico WSNMP32.DLL.</span><span class="sxs-lookup"><span data-stu-id="87574-104">A WinSNMP application must access the WinSNMP API through the dynamic-link library WSNMP32.DLL.</span></span>

<span data-ttu-id="87574-105">Os arquivos a seguir são necessários para dar suporte à funcionalidade da API WinSNMP.</span><span class="sxs-lookup"><span data-stu-id="87574-105">The following files are required to support the functionality of the WinSNMP API.</span></span>



| <span data-ttu-id="87574-106">Nome de arquivo</span><span class="sxs-lookup"><span data-stu-id="87574-106">Filename</span></span>     | <span data-ttu-id="87574-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="87574-107">Description</span></span>                                                                                  |
|--------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="87574-108">WSNMP32. LIB</span><span class="sxs-lookup"><span data-stu-id="87574-108">WSNMP32.LIB</span></span>  | <span data-ttu-id="87574-109">Biblioteca WinSNMP</span><span class="sxs-lookup"><span data-stu-id="87574-109">WinSNMP Library</span></span>                                                                              |
| <span data-ttu-id="87574-110">WSNMP32.DLL</span><span class="sxs-lookup"><span data-stu-id="87574-110">WSNMP32.DLL</span></span>  | <span data-ttu-id="87574-111">Fornece a interface WinSNMP</span><span class="sxs-lookup"><span data-stu-id="87574-111">Provides WinSNMP interface</span></span>                                                                   |
| <span data-ttu-id="87574-112">WINSNMP. T</span><span class="sxs-lookup"><span data-stu-id="87574-112">WINSNMP.H</span></span>    | <span data-ttu-id="87574-113">Arquivo de cabeçalho WinSNMP</span><span class="sxs-lookup"><span data-stu-id="87574-113">WinSNMP header file</span></span>                                                                          |
| <span data-ttu-id="87574-114">SNMPTRAP.EXE</span><span class="sxs-lookup"><span data-stu-id="87574-114">SNMPTRAP.EXE</span></span> | <span data-ttu-id="87574-115">Recebe interceptações SNMP e as encaminha para MGMTAPI.DLL, a biblioteca de API do Gerenciador SNMP da Microsoft</span><span class="sxs-lookup"><span data-stu-id="87574-115">Receives SNMP traps and forwards them to MGMTAPI.DLL, the Microsoft SNMP Manager API library</span></span> |
| <span data-ttu-id="87574-116">SNMPAPI.DLL</span><span class="sxs-lookup"><span data-stu-id="87574-116">SNMPAPI.DLL</span></span>  | <span data-ttu-id="87574-117">Fornece utilitários SNMP</span><span class="sxs-lookup"><span data-stu-id="87574-117">Provides SNMP utilities</span></span>                                                                      |



 

 

 




