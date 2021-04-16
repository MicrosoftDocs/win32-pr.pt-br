---
description: Você pode especificar um descritor de segurança para um pipe anônimo ao chamar a função CreatePipe. O descritor de segurança controla o acesso às extremidades de leitura e gravação do pipe.
ms.assetid: 17813ce1-b3f6-408f-9c55-5caa7eda6738
title: Segurança de pipe anônimo e direitos de acesso
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02935a3b2bc5ea31d88aab3f23f23c348c054e5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758083"
---
# <a name="anonymous-pipe-security-and-access-rights"></a><span data-ttu-id="40053-104">Segurança de pipe anônimo e direitos de acesso</span><span class="sxs-lookup"><span data-stu-id="40053-104">Anonymous Pipe Security and Access Rights</span></span>

<span data-ttu-id="40053-105">A segurança do Windows permite que você controle o acesso a Pipes anônimos.</span><span class="sxs-lookup"><span data-stu-id="40053-105">Windows security enables you to control access to anonymous pipes.</span></span> <span data-ttu-id="40053-106">Para obter mais informações sobre segurança, consulte [modelo de controle de acesso](/windows/desktop/SecAuthZ/access-control-model).</span><span class="sxs-lookup"><span data-stu-id="40053-106">For more information about security, see [Access-Control Model](/windows/desktop/SecAuthZ/access-control-model).</span></span>

<span data-ttu-id="40053-107">Você pode especificar um [descritor de segurança](/windows/desktop/SecAuthZ/security-descriptors) para um pipe ao chamar a função [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) .</span><span class="sxs-lookup"><span data-stu-id="40053-107">You can specify a [security descriptor](/windows/desktop/SecAuthZ/security-descriptors) for a pipe when you call the [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function.</span></span> <span data-ttu-id="40053-108">O descritor de segurança controla o acesso às extremidades de leitura e gravação do pipe.</span><span class="sxs-lookup"><span data-stu-id="40053-108">The security descriptor controls access to both the read and write ends of the pipe.</span></span> <span data-ttu-id="40053-109">Se você especificar **NULL**, o pipe obterá um descritor de segurança padrão.</span><span class="sxs-lookup"><span data-stu-id="40053-109">If you specify **NULL**, the pipe gets a default security descriptor.</span></span> <span data-ttu-id="40053-110">As ACLs no descritor de segurança padrão para um pipe são provenientes do token de representação ou primário do criador.</span><span class="sxs-lookup"><span data-stu-id="40053-110">The ACLs in the default security descriptor for a pipe come from the primary or impersonation token of the creator.</span></span>

<span data-ttu-id="40053-111">Para recuperar o descritor de segurança de um pipe, chame a função [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="40053-111">To retrieve a pipe's security descriptor, call the [**GetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-getsecurityinfo) function.</span></span> <span data-ttu-id="40053-112">Para alterar o descritor de segurança de um pipe, chame a função [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) .</span><span class="sxs-lookup"><span data-stu-id="40053-112">To change a pipe's security descriptor, call the [**SetSecurityInfo**](/windows/desktop/api/aclapi/nf-aclapi-setsecurityinfo) function.</span></span>

<span data-ttu-id="40053-113">A função [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) retorna dois identificadores para o pipe anônimo: um identificador de leitura com \_ acesso genérico de leitura e sincronização; e um identificador de gravação com acesso genérico de \_ gravação e sincronização.</span><span class="sxs-lookup"><span data-stu-id="40053-113">The [**CreatePipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) function returns two handles to the anonymous pipe: a read handle with GENERIC\_READ and SYNCHRONIZE access; and a write handle with GENERIC\_WRITE and SYNCHRONIZE access.</span></span> <span data-ttu-id="40053-114">\_A leitura genérica e o \_ acesso de gravação genérico usam o mesmo mapeamento de direitos de acesso para pipes nomeados.</span><span class="sxs-lookup"><span data-stu-id="40053-114">GENERIC\_READ and GENERIC\_WRITE access use the same access rights mapping as for named pipes.</span></span>

<span data-ttu-id="40053-115">\_O acesso de leitura genérico para um pipe anônimo combina os direitos de leitura de dados do pipe, leitura de atributos de pipe, leitura de atributos estendidos e leitura da DACL do pipe.</span><span class="sxs-lookup"><span data-stu-id="40053-115">GENERIC\_READ access for an anonymous pipe combines the rights to read data from the pipe, read pipe attributes, read extended attributes, and read the pipe's DACL.</span></span>

<span data-ttu-id="40053-116">\_O acesso de gravação genérico para um pipe anônimo combina os direitos de gravar dados no pipe, acrescentar dados a ele, gravar atributos de pipe, gravar atributos estendidos e ler a DACL do pipe.</span><span class="sxs-lookup"><span data-stu-id="40053-116">GENERIC\_WRITE access for an anonymous pipe combines the rights to write data to the pipe, append data to it, write pipe attributes, write extended attributes, and read the pipe's DACL.</span></span>

 

 
