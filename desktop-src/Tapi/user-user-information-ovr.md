---
description: Usuário – as informações do usuário são um buffer que pode ser transmitido de uma extremidade de uma conexão para outra. Essas informações são específicas para o padrão ISDN Q. 931. Consulte a documentação dos provedores de serviços sobre o significado e o uso desses dados.
ms.assetid: 7040ab51-184e-4ffc-9333-b82ae5a5a7f3
title: Usuário – informações do usuário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d4539db192b9c24b5d71dfb60a2129e66b6658b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506078"
---
# <a name="user-user-information"></a><span data-ttu-id="f7ebe-105">Usuário – informações do usuário</span><span class="sxs-lookup"><span data-stu-id="f7ebe-105">User-user information</span></span>

<span data-ttu-id="f7ebe-106">Usuário – as informações do usuário são um buffer que pode ser transmitido de uma extremidade de uma conexão para outra.</span><span class="sxs-lookup"><span data-stu-id="f7ebe-106">User-user information is a buffer that can be transmitted from one end of a connection to another.</span></span> <span data-ttu-id="f7ebe-107">Essas informações são específicas para o padrão ISDN Q. 931.</span><span class="sxs-lookup"><span data-stu-id="f7ebe-107">This information is specific to the ISDN Q.931 standard.</span></span> <span data-ttu-id="f7ebe-108">Consulte a documentação do provedor de serviços sobre o significado e o uso desses dados.</span><span class="sxs-lookup"><span data-stu-id="f7ebe-108">Please refer to your service provider's documentation on the meaning and use of this data.</span></span>

<span data-ttu-id="f7ebe-109">Nem todos os provedores de serviços dão suporte ao uso dessas informações.</span><span class="sxs-lookup"><span data-stu-id="f7ebe-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="f7ebe-110">\* \* TAPI 2. x: \* \*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** e **dwCallDataOffset** membros de [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="f7ebe-110">\*\*TAPI 2.x:  \*\*[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwCallDataSize** and **dwCallDataOffset** members of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo), [**lineSendUserUserInfo**](/windows/win32/api/tapi/nf-tapi-linesenduseruserinfo)</span></span>

<span data-ttu-id="f7ebe-111">\* \* TAPI 3. x: \* \*[**ITCallInfo:: GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), chamado com o **membro \_ UserUserInfo CIB** do [**\_ buffer CALLINFO**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo:: ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span><span class="sxs-lookup"><span data-stu-id="f7ebe-111">\*\*TAPI 3.x:  \*\*[**ITCallInfo::GetCallInfoBuffer**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-getcallinfobuffer), called with the **CIB\_USERUSERINFO** member of [**CALLINFO\_BUFFER**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_buffer), [**ITCallInfo::ReleaseUserUserInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-releaseuseruserinfo)</span></span>

 

 
