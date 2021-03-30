---
title: Suporte para cadeias de caracteres de Endereço IPX em WinSNMP
description: WinSNMP 2,0 formalizes o uso de cadeias de caracteres de Endereço IPX.
ms.assetid: b90b8e95-dab0-483b-9336-07e20c122cba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc33c3ff3b589f9614b139260cef993e232f4343
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634839"
---
# <a name="support-for-ipx-address-strings-in-winsnmp"></a><span data-ttu-id="bfb8d-103">Suporte para cadeias de caracteres de Endereço IPX em WinSNMP</span><span class="sxs-lookup"><span data-stu-id="bfb8d-103">Support for IPX Address Strings in WinSNMP</span></span>

<span data-ttu-id="bfb8d-104">WinSNMP 2,0 formalizes o uso de cadeias de caracteres de Endereço IPX.</span><span class="sxs-lookup"><span data-stu-id="bfb8d-104">WinSNMP 2.0 formalizes the use of IPX address strings.</span></span> <span data-ttu-id="bfb8d-105">Se você especificar uma cadeia de caracteres de Endereço IPX como um parâmetro de entrada para a função [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) , deverá Formatar a cadeia de caracteres usando os seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="bfb8d-105">If you specify an IPX address string as an input parameter to the [**SnmpStrToEntity**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpstrtoentity) function, you must format the string using the following standards:</span></span>

-   <span data-ttu-id="bfb8d-106">Um número de rede que consiste em oito dígitos hexadecimais (preenchido com zero, se necessário)</span><span class="sxs-lookup"><span data-stu-id="bfb8d-106">A network number that consists of eight hexadecimal digits (zero-filled if necessary)</span></span>
-   <span data-ttu-id="bfb8d-107">Um separador (":", "." ou "–")</span><span class="sxs-lookup"><span data-stu-id="bfb8d-107">A separator (either ":", "." or " – ")</span></span>
-   <span data-ttu-id="bfb8d-108">Um número de nó que consiste em 12 dígitos hexadecimais (preenchido com zero, se necessário)</span><span class="sxs-lookup"><span data-stu-id="bfb8d-108">A node number that consists of 12 hexadecimal digits (zero-filled if necessary)</span></span>

<span data-ttu-id="bfb8d-109">Por exemplo, 00000001:00081A0D01C2 ou 00000001.00081 a0d01c2.</span><span class="sxs-lookup"><span data-stu-id="bfb8d-109">For example, 00000001:00081A0D01C2 or 00000001.00081a0d01c2.</span></span> <span data-ttu-id="bfb8d-110">Os dígitos hexadecimais podem ser maiúsculos ou minúsculos.</span><span class="sxs-lookup"><span data-stu-id="bfb8d-110">Hexadecimal digits can be uppercase or lowercase.</span></span>

<span data-ttu-id="bfb8d-111">Esse é o formato que a função [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) usa para retornar uma cadeia de caracteres de Endereço IPX.</span><span class="sxs-lookup"><span data-stu-id="bfb8d-111">This is the format the [**SnmpEntityToStr**](/windows/desktop/api/Winsnmp/nf-winsnmp-snmpentitytostr) function uses to return an IPX address string.</span></span> <span data-ttu-id="bfb8d-112">A cadeia de caracteres é retornada quando um aplicativo que está operando em um dos \_ modos não traduzidos do snmpapi chama a função **SnmpEntityToStr** .</span><span class="sxs-lookup"><span data-stu-id="bfb8d-112">The string is returned when an application that is operating in one of the SNMPAPI\_UNTRANSLATED modes calls the **SnmpEntityToStr** function.</span></span> <span data-ttu-id="bfb8d-113">A cadeia de caracteres também pode ser retornada quando o aplicativo estiver operando no \_ modo traduzido do snmpapi e nenhum nome amigável estiver disponível para a entidade.</span><span class="sxs-lookup"><span data-stu-id="bfb8d-113">The string can also be returned when the application is operating in SNMPAPI\_TRANSLATED mode and no user-friendly name is available for the entity.</span></span>

 

 




