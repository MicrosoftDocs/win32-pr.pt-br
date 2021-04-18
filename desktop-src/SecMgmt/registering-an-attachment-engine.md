---
description: Antes que o mecanismo de configuração de segurança possa chamar seu mecanismo de anexo para processar tarefas específicas do serviço, você deve instalar o mecanismo de anexo e registrá-lo no mecanismo de configuração de segurança.
ms.assetid: f7376a79-97cd-4607-9e1b-5b8c7cd76a32
title: Registrando um mecanismo de anexo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f50827fe27e86328e7e914bfc98740fa5e15060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760195"
---
# <a name="registering-an-attachment-engine"></a><span data-ttu-id="d0181-103">Registrando um mecanismo de anexo</span><span class="sxs-lookup"><span data-stu-id="d0181-103">Registering an Attachment Engine</span></span>

<span data-ttu-id="d0181-104">Antes que o mecanismo de configuração de segurança possa chamar seu mecanismo de anexo para processar tarefas específicas do serviço, você deve instalar o mecanismo de anexo e registrá-lo no mecanismo de configuração de segurança.</span><span class="sxs-lookup"><span data-stu-id="d0181-104">Before the Security Configuration Engine can call your attachment engine to process service-specific tasks, you must install your attachment engine and register it with the Security Configuration Engine.</span></span>

<span data-ttu-id="d0181-105">**Para instalar e registrar a DLL do mecanismo de anexo**</span><span class="sxs-lookup"><span data-stu-id="d0181-105">**To install and register the attachment engine DLL**</span></span>

1.  <span data-ttu-id="d0181-106">Copie a DLL do mecanismo de anexo para um diretório no sistema.</span><span class="sxs-lookup"><span data-stu-id="d0181-106">Copy the attachment engine DLL to a directory on the system.</span></span> <span data-ttu-id="d0181-107">O diretório preferencial são os anexos de% windir% \\ secedit \\ .</span><span class="sxs-lookup"><span data-stu-id="d0181-107">The preferred directory is %windir%\\secedit\\attachments.</span></span> <span data-ttu-id="d0181-108">Se esse diretório não existir, você deverá criá-lo.</span><span class="sxs-lookup"><span data-stu-id="d0181-108">If this directory does not exist, you should create it.</span></span>
2.  <span data-ttu-id="d0181-109">Crie uma chave do registro no nó a seguir.</span><span class="sxs-lookup"><span data-stu-id="d0181-109">Create a registry key under the following node.</span></span> <span data-ttu-id="d0181-110">O *nome do serviço* é o nome registrado para o anexo e deve ser o mesmo nome de serviço usado no Gerenciador de controle de serviço, um módulo que gerencia a interrupção e o início dos serviços.</span><span class="sxs-lookup"><span data-stu-id="d0181-110">The *service name* is the registered name for the attachment, and must be the same service name used in the Service Control Manager, a module which manages the stopping and starting of services.</span></span> <span data-ttu-id="d0181-111">O nome também deve ser exclusivo para que não entre em conflito com os nomes de outros anexos.</span><span class="sxs-lookup"><span data-stu-id="d0181-111">The name must also be unique so it does not conflict with the names of other attachments.</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Microsoft
          Windows NT
             CurrentVersion
                SeCEdit
                   Service
                      service name
    ```

3.  <span data-ttu-id="d0181-112">Crie o seguinte valor de cadeia de caracteres na nova chave do registro.</span><span class="sxs-lookup"><span data-stu-id="d0181-112">Create the following string value in the new registry key.</span></span> <span data-ttu-id="d0181-113">*caminho do mecanismo de anexo* é o caminho completo para o módulo do mecanismo de anexo.</span><span class="sxs-lookup"><span data-stu-id="d0181-113">*attachment engine path* is the full path to the attachment engine module.</span></span><dl> <dd><span data-ttu-id="d0181-114">**ServiceAttachmentPath**  =  *caminho do mecanismo de anexo*</span><span class="sxs-lookup"><span data-stu-id="d0181-114">**ServiceAttachmentPath** = *attachment engine path*</span></span><dl> <dt>

<span data-ttu-id="d0181-115">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="d0181-115">Data type</span></span>
</dt> <dd><span data-ttu-id="d0181-116">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="d0181-116">REG_SZ</span></span></dd> </dl> </dd> </dl>

 

 



