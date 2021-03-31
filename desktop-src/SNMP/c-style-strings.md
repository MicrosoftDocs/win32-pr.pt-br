---
title: Cadeias de caracteres C-Style
description: Um aplicativo WinSNMP pode usar cadeias de estilo C com terminação nula para converter objetos de OID (identificador de objeto e entidade) de e para suas representações de cadeia de caracteres.
ms.assetid: df04071c-df46-410b-ad92-6adecbfcd454
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878398b6d8691982aa90b9f1376a38214030e52e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822167"
---
# <a name="c-style-strings"></a><span data-ttu-id="a69ca-103">Cadeias de caracteres C-Style</span><span class="sxs-lookup"><span data-stu-id="a69ca-103">C-Style Strings</span></span>

<span data-ttu-id="a69ca-104">Um aplicativo WinSNMP pode usar cadeias de estilo C com terminação **nula** para converter objetos de OID (identificador de objeto e entidade) de e para suas representações de cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a69ca-104">A WinSNMP application can use **NULL**-terminated C-style strings to convert entity and object identifier (OID) objects to and from their string representations.</span></span>

<span data-ttu-id="a69ca-105">As funções WinSNMP que manipulam cadeias de caracteres em estilo C incluem [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid)e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span><span class="sxs-lookup"><span data-stu-id="a69ca-105">The WinSNMP functions that manipulate C-style strings include [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity), [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr), [**SnmpStrToOid**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtooid), and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr).</span></span> <span data-ttu-id="a69ca-106">Como [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) e [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) retornam um ponteiro para uma variável de cadeia de caracteres de estilo C, o aplicativo WinSNMP deve passar um valor apropriado no parâmetro *size* quando ele faz chamadas para essas funções.</span><span class="sxs-lookup"><span data-stu-id="a69ca-106">Because [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) and [**SnmpOidToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpoidtostr) return a pointer to a C-style string variable, the WinSNMP application must pass an appropriate value in the *size* parameter when it makes calls to these functions.</span></span> <span data-ttu-id="a69ca-107">Para obter mais informações, consulte as páginas de referência para essas funções.</span><span class="sxs-lookup"><span data-stu-id="a69ca-107">For more information, see the reference pages for these functions.</span></span>

> [!Note]  
> <span data-ttu-id="a69ca-108">O parâmetro de *contexto* das funções [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) e [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) deve ser uma estrutura de cadeia de caracteres de octeto, ou seja, uma estrutura [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) .</span><span class="sxs-lookup"><span data-stu-id="a69ca-108">The *context* parameter of the [**SnmpStrToContext**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtocontext) and [**SnmpContextToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpcontexttostr) functions must be an octet string structure, that is, an [**smiOCTETS**](/windows/desktop/api/Winsnmp/ns-winsnmp-smioctets) structure.</span></span> <span data-ttu-id="a69ca-109">O parâmetro de *contexto* não pode ser uma cadeia de caracteres em estilo C.</span><span class="sxs-lookup"><span data-stu-id="a69ca-109">The *context* parameter cannot be a C-style string.</span></span> <span data-ttu-id="a69ca-110">A cadeia de caracteres contida em uma estrutura **smiOCTETS** não requer um byte de terminação **nula**.</span><span class="sxs-lookup"><span data-stu-id="a69ca-110">The string contained in an **smiOCTETS** structure does not require a **NULL**-terminating byte.</span></span>

 

 

 




