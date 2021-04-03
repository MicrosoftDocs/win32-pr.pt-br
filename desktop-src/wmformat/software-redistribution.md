---
title: Redistribuição de software
description: Redistribuição de software
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- SDK do Windows Media Format, redistribuição de software
- Formato de sistema avançado (ASF), redistribuição de software
- ASF (formato de sistemas avançados), redistribuição de software
- SDK do Windows Media Format, redistribuição
- Formato de sistema avançado (ASF), redistribuição
- ASF (formato de sistemas avançados), redistribuição
- redistribuição de software, sobre
- redistribuição, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635560"
---
# <a name="software-redistribution"></a><span data-ttu-id="6cf9b-111">Redistribuição de software</span><span class="sxs-lookup"><span data-stu-id="6cf9b-111">Software Redistribution</span></span>

<span data-ttu-id="6cf9b-112">A inclusão do software Windows Media Format em uma instalação de aplicativo é conhecida como redistribuição.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="6cf9b-113">O SDK do Windows Media Format inclui um pacote de instalação que pode ser incluído na instalação do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="6cf9b-114">O pacote de instalação é um arquivo executável chamado wmfdist95.exe.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="6cf9b-115">Quando você instala o SDK do Windows Media Format, o pacote de instalação é copiado para a \\ pasta redist do diretório de instalação (c: \\ WMSDK \\ wmfsdk por padrão).</span><span class="sxs-lookup"><span data-stu-id="6cf9b-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="6cf9b-116">As seções a seguir fornecem procedimentos e outras informações para a configuração de redistribuição de software.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="6cf9b-117">Seção</span><span class="sxs-lookup"><span data-stu-id="6cf9b-117">Section</span></span>                                                                            | <span data-ttu-id="6cf9b-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="6cf9b-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6cf9b-119">Para criar uma configuração de redistribuição</span><span class="sxs-lookup"><span data-stu-id="6cf9b-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="6cf9b-120">Descreve o procedimento para criar uma instalação de aplicativo.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="6cf9b-121">Detectando o status da instalação</span><span class="sxs-lookup"><span data-stu-id="6cf9b-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="6cf9b-122">Fornece um código de exemplo que verifica o status de instalação do registro para determinar se o pacote de redistribuição precisa ser instalado.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="6cf9b-123">Exemplo de código para configuração de redistribuição</span><span class="sxs-lookup"><span data-stu-id="6cf9b-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="6cf9b-124">Fornece um código de exemplo que pode ser usado em sua rotina de instalação para executar os pacotes de redistribuição no modo silencioso e notificar sua rotina de instalação quando o computador precisar ser reiniciado.</span><span class="sxs-lookup"><span data-stu-id="6cf9b-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="6cf9b-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6cf9b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6cf9b-126">**Considerações sobre o projeto**</span><span class="sxs-lookup"><span data-stu-id="6cf9b-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




