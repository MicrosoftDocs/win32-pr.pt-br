---
description: Alguns pacotes de segurança dão suporte a mensagens de erro estendidas que permitem que os lados de um link de comunicação se comuniquem por qualquer motivo de falha.
ms.assetid: a15c61f0-03cc-462f-b5c1-8e7f062e9523
title: Informações de erro estendidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a4f59c53da452a3254ff6faaebeb30983498161
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105748874"
---
# <a name="extended-error-information"></a><span data-ttu-id="73efb-103">Informações de erro estendidas</span><span class="sxs-lookup"><span data-stu-id="73efb-103">Extended Error Information</span></span>

<span data-ttu-id="73efb-104">Alguns [*pacotes de segurança*](/windows/desktop/SecGloss/s-gly) dão suporte a mensagens de erro estendidas que permitem que os lados de um link de comunicação se comuniquem por qualquer motivo de falha.</span><span class="sxs-lookup"><span data-stu-id="73efb-104">Some [*security packages*](/windows/desktop/SecGloss/s-gly) support extended error messages that allow the sides of a communication link to communicate any reasons for a failure.</span></span> <span data-ttu-id="73efb-105">Por exemplo, o [*protocolo Kerberos*](/windows/desktop/SecGloss/k-gly) pode falhar devido a uma discrepância de tempo entre a hora da solicitação de um tíquete Kerberos e a hora do problema do tíquete.</span><span class="sxs-lookup"><span data-stu-id="73efb-105">For example, the [*Kerberos protocol*](/windows/desktop/SecGloss/k-gly) could fail because of a time discrepancy between the time of request for a Kerberos ticket and the ticket's time of issue.</span></span> <span data-ttu-id="73efb-106">Com informações de informações de erro estendidas retornadas, um cliente pode ressincronizar seu relógio e gerar uma nova mensagem de conexão.</span><span class="sxs-lookup"><span data-stu-id="73efb-106">With information from returned extended error information, a client can resynchronize its clock and generate a new connection message.</span></span>

<span data-ttu-id="73efb-107">Um pacote de segurança que define \_ o \_ sinalizador de erro estendido do sinalizador SECPKG \_ no membro **FCapabilities** de uma estrutura [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) indica que o pacote de segurança dá suporte a mensagens de erro estendidas.</span><span class="sxs-lookup"><span data-stu-id="73efb-107">A security package setting the SECPKG\_FLAG\_EXTENDED\_ERROR flag in the **fCapabilities** member of a [**SecPkgInfo**](/windows/desktop/api/Sspi/ns-sspi-secpkginfoa) structure indicates that the security package supports extended error messages.</span></span>

<span data-ttu-id="73efb-108">Aplicativos cliente que exigem mensagens de erro estendidas especificam o sinalizador de erro estendido de solicitação de ISC \_ \_ \_ ao chamar a função [**InitializeSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) .</span><span class="sxs-lookup"><span data-stu-id="73efb-108">Client applications requiring extended error messages specify the ISC\_REQ\_EXTENDED\_ERROR flag when calling the [**InitializeSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) function.</span></span> <span data-ttu-id="73efb-109">Aplicativos de servidor que exigem mensagens de erro estendidas definem o \_ \_ sinalizador de erro estendido de ASC req \_ ao chamar [**AcceptSecurityContext (geral)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span><span class="sxs-lookup"><span data-stu-id="73efb-109">Server applications requiring extended error messages set the ASC\_REQ\_EXTENDED\_ERROR flag when calling [**AcceptSecurityContext (General)**](/windows/win32/api/sspi/nf-sspi-acceptsecuritycontext).</span></span>

 

 
