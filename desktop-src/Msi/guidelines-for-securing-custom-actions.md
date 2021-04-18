---
description: Para ajudar a manter uma instalação de software segura, siga estas diretrizes ao criar uma Windows Installer ação personalizada.
ms.assetid: f7081b0c-bfa2-47a1-840b-28881ad97071
title: Diretrizes para proteger ações personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119c045833b165222756702244cf65bb2225a8f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170237"
---
# <a name="guidelines-for-securing-custom-actions"></a><span data-ttu-id="61d07-103">Diretrizes para proteger ações personalizadas</span><span class="sxs-lookup"><span data-stu-id="61d07-103">Guidelines for Securing Custom Actions</span></span>

<span data-ttu-id="61d07-104">A adesão às seguintes diretrizes ao criar um pacote de Windows Installer com ações personalizadas ajuda a manter um ambiente seguro durante a instalação:</span><span class="sxs-lookup"><span data-stu-id="61d07-104">Adherence to the following guidelines when authoring a Windows Installer package with custom actions helps maintain a secure environment during installation:</span></span>

-   <span data-ttu-id="61d07-105">Proteja todos os arquivos adicionais gravados por sua ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="61d07-105">Secure any additional files written by your custom action.</span></span>
-   <span data-ttu-id="61d07-106">Verifique os comprimentos do buffer e a validade de todos os dados lidos por sua ação personalizada.</span><span class="sxs-lookup"><span data-stu-id="61d07-106">Check buffer lengths and validity of all data read by your custom action.</span></span> <span data-ttu-id="61d07-107">Isso inclui propriedades que podem fornecer dados para sua ação personalizada, particularmente aquelas que usam propriedades públicas fornecidas por um usuário.</span><span class="sxs-lookup"><span data-stu-id="61d07-107">This includes properties that may supply data to your custom action, particularly those that use public properties provided by a user.</span></span>
-   <span data-ttu-id="61d07-108">Não confie em DLLs externas que não são confiáveis pelo sistema em todas as plataformas nas quais o pacote de instalação deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="61d07-108">Do not rely on external DLLs that are not trusted by the system on all platforms on which your installation package is intended to run.</span></span>
-   <span data-ttu-id="61d07-109">Considere atentamente se as ações personalizadas que usam privilégios [*elevados*](e-gly.md) ou representação devem ser usadas.</span><span class="sxs-lookup"><span data-stu-id="61d07-109">Carefully consider whether to use custom actions that use [*elevated*](e-gly.md) privileges or impersonation.</span></span> <span data-ttu-id="61d07-110">As ações personalizadas, como "abrir uma URL após a instalação, são concluídas", "iniciar o software após a instalação concluída" ou "iniciar o Leiame após a instalação concluída", normalmente, não exigiria privilégios elevados para funcionar.</span><span class="sxs-lookup"><span data-stu-id="61d07-110">Custom actions such as “open a URL after installation is completed,” “launch the software after installation is complete,” or “launch ReadMe after installation is complete” would not usually require elevated privileges to function.</span></span> <span data-ttu-id="61d07-111">Se a ação personalizada deve ser executada com privilégios *elevados* , certifique-se de que o código de ação personalizado protege contra estouros de buffer e carregamento inadvertido de código não seguro.</span><span class="sxs-lookup"><span data-stu-id="61d07-111">If your custom action must run with *elevated* privileges, be sure that the custom action code guards against buffer overruns and inadvertent loading of unsafe code.</span></span> <span data-ttu-id="61d07-112">Observe que durante a fase de execução da instalação, o instalador passa informações para um processo com privilégios *elevados* e executa o script.</span><span class="sxs-lookup"><span data-stu-id="61d07-112">Note that during the execution phase of the installation, the installer passes information to a process with *elevated* privileges and runs the script.</span></span> <span data-ttu-id="61d07-113">Todas as ações personalizadas executadas durante a fase de execução podem ser executadas com privilégios *elevados* .</span><span class="sxs-lookup"><span data-stu-id="61d07-113">Any custom actions that run during the execution phase may run with *elevated* privileges.</span></span>
-   <span data-ttu-id="61d07-114">Reúna todas as informações fornecidas pelo usuário durante a sequência de interface</span><span class="sxs-lookup"><span data-stu-id="61d07-114">Gather all information provided by the user during the UI sequence.</span></span> <span data-ttu-id="61d07-115">Não solicite ao usuário nenhuma informação que não possa ser definida usando uma propriedade pública.</span><span class="sxs-lookup"><span data-stu-id="61d07-115">Do not prompt the user for any information that can't be set using a public property.</span></span>
-   <span data-ttu-id="61d07-116">Se a ação personalizada do script expandir as propriedades, tome precauções de que a ação personalizada é protegida contra a possibilidade de injeção de script.</span><span class="sxs-lookup"><span data-stu-id="61d07-116">If your script custom action expands properties, take precautions that the custom action is secured against the possibility of script injection.</span></span> <span data-ttu-id="61d07-117">O script pode ser registrado em texto não criptografado.</span><span class="sxs-lookup"><span data-stu-id="61d07-117">Script may be logged in clear text.</span></span>

<span data-ttu-id="61d07-118">Consulte também [segurança de ação personalizada](custom-action-security.md).</span><span class="sxs-lookup"><span data-stu-id="61d07-118">See also [Custom Action Security](custom-action-security.md).</span></span>

 

 



