---
description: Você pode controlar a capacidade de um processo de acessar objetos protegíveis ou executar tarefas de administração do sistema.
ms.assetid: a5d8eaaa-4585-44a3-ab92-2a323d9af80c
title: Especificando um descritor de segurança de um arquivo INF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a065a41db49385c7c95e683fd4aca4cfe7eb9cd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922729"
---
# <a name="specifying-a-security-descriptor-from-an-inf-file"></a><span data-ttu-id="04dc2-103">Especificando um descritor de segurança de um arquivo INF</span><span class="sxs-lookup"><span data-stu-id="04dc2-103">Specifying a Security Descriptor From an INF File</span></span>

<span data-ttu-id="04dc2-104">Você pode controlar a capacidade de um processo de acessar objetos protegíveis ou executar tarefas de administração do sistema.</span><span class="sxs-lookup"><span data-stu-id="04dc2-104">You can control the ability of a process to access securable objects or to perform system administration tasks.</span></span> <span data-ttu-id="04dc2-105">Um objeto protegível é um objeto que pode ter um descritor de segurança.</span><span class="sxs-lookup"><span data-stu-id="04dc2-105">A securable object is an object that can have a security descriptor.</span></span> <span data-ttu-id="04dc2-106">Todos os objetos nomeados são protegíveis.</span><span class="sxs-lookup"><span data-stu-id="04dc2-106">All named objects are securable.</span></span> <span data-ttu-id="04dc2-107">Alguns objetos sem nome, como objetos de processo e thread, também podem ter descritores de segurança.</span><span class="sxs-lookup"><span data-stu-id="04dc2-107">Some unnamed objects, such as process and thread objects, can have security descriptors too.</span></span> <span data-ttu-id="04dc2-108">Para obter mais informações sobre como controlar o acesso a objetos protegíveis, consulte [controle de acesso](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="04dc2-108">For more information about controlling access to securable objects see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="04dc2-109">[Descritores de segurança](/windows/desktop/SecAuthZ/security-descriptors) contêm as informações de segurança associadas a objetos protegíveis.</span><span class="sxs-lookup"><span data-stu-id="04dc2-109">[Security descriptors](/windows/desktop/SecAuthZ/security-descriptors) contain the security information associated with securable objects.</span></span> <span data-ttu-id="04dc2-110">Para a maioria dos objetos protegíveis, você pode especificar o descritor de segurança de um objeto na chamada de função que cria o objeto.</span><span class="sxs-lookup"><span data-stu-id="04dc2-110">For most securable objects, you can specify an object's security descriptor in the function call that creates the object.</span></span> <span data-ttu-id="04dc2-111">Por exemplo, você pode especificar um descritor de segurança nas funções [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) .</span><span class="sxs-lookup"><span data-stu-id="04dc2-111">For example, you can specify a security descriptor in the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) functions.</span></span>

<span data-ttu-id="04dc2-112">Para definir um descritor de segurança de um arquivo INF, adicione uma seção segurança de criação de INF-Writer imediatamente após a seção que instala o arquivo, a chave do registro ou o componente.</span><span class="sxs-lookup"><span data-stu-id="04dc2-112">To set a security descriptor from an INF file, add an INF-writer authored Security section immediately following the section that installs the file, registry key, or component.</span></span> <span data-ttu-id="04dc2-113">A seção de segurança deve conter uma linha com descritor de segurança de cadeia de caracteres escrito usando o formato para [cadeias de caracteres de descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-strings).</span><span class="sxs-lookup"><span data-stu-id="04dc2-113">The Security section should contain one line with the string security descriptor written on it using the format for [Security Descriptor Strings](/windows/desktop/SecAuthZ/security-descriptor-strings).</span></span> <span data-ttu-id="04dc2-114">A linha também deve ser colocada entre aspas (").</span><span class="sxs-lookup"><span data-stu-id="04dc2-114">The line should also be enclosed by quotation marks (").</span></span>

<span data-ttu-id="04dc2-115">Por exemplo, o seguinte trecho de arquivo INF criaria uma chave do registro para a qual somente os administradores e o sistema têm acesso.</span><span class="sxs-lookup"><span data-stu-id="04dc2-115">For example, the following INF file snippet would create a registry key to which only administrators and the system have access.</span></span> <span data-ttu-id="04dc2-116">Observe que este exemplo requer privilégios administrativos.</span><span class="sxs-lookup"><span data-stu-id="04dc2-116">Note that this example requires administrative privileges.</span></span>

``` syntax
[DDInstall]
AddReg=mydevice.reg
 
[mydevice.reg]
include Registry information here
 
[mydevice.reg.Security]
"D:P(A;CI;GA;;;BA)(A;CI;GA;;;SY)"
```

<span data-ttu-id="04dc2-117">Nesse caso, o significado da cadeia de caracteres é que os administradores têm controle total, o sistema tem controle total e o acesso é herdável para todas as subchaves.</span><span class="sxs-lookup"><span data-stu-id="04dc2-117">In this case, the meaning of the string is that administrators have full control, system has full control, and access is inheritable to all subkeys.</span></span> <span data-ttu-id="04dc2-118">Para obter mais informações, consulte [linguagem de definição do descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span><span class="sxs-lookup"><span data-stu-id="04dc2-118">For more information see [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-definition-language).</span></span>

 

 
