---
description: A ação de anúncio é uma ação de nível superior chamada para instalar ou remover componentes anunciados.
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: Ação de anúncio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103662070"
---
# <a name="advertise-action"></a><span data-ttu-id="dbbc6-103">Ação de anúncio</span><span class="sxs-lookup"><span data-stu-id="dbbc6-103">ADVERTISE Action</span></span>

<span data-ttu-id="dbbc6-104">A ação de anúncio é uma ação de nível superior chamada para instalar ou remover componentes anunciados.</span><span class="sxs-lookup"><span data-stu-id="dbbc6-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="dbbc6-105">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="dbbc6-105">Sequence Restrictions</span></span>

<span data-ttu-id="dbbc6-106">Não há restrições de sequência.</span><span class="sxs-lookup"><span data-stu-id="dbbc6-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="dbbc6-107">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="dbbc6-107">ActionData Messages</span></span>

<span data-ttu-id="dbbc6-108">Não há nenhuma mensagem ActionData.</span><span class="sxs-lookup"><span data-stu-id="dbbc6-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="dbbc6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbbc6-109">Remarks</span></span>

<span data-ttu-id="dbbc6-110">O [*anúncio*](a-gly.md) refere-se à capacidade do instalador de fornecer as interfaces de carregamento e inicialização de um aplicativo sem instalar fisicamente o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dbbc6-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="dbbc6-111">O instalador não instala os componentes necessários até que um usuário ou aplicativo ative uma interface anunciada.</span><span class="sxs-lookup"><span data-stu-id="dbbc6-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="dbbc6-112">Esse conceito é chamado de [*instalação sob demanda*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dbbc6-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="dbbc6-113">A ação de anúncio não é chamada de dentro da sequência da tabela de ações, a Windows Installer executa essa ação quando o executável da linha de comando Msiexec.exe é chamado com a opção de linha de comando "/j" ou quando [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) é chamado com o parâmetro *SZCOMMANDLINE* definido como Action = Advertise.</span><span class="sxs-lookup"><span data-stu-id="dbbc6-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbbc6-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dbbc6-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbbc6-115">Tabela AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="dbbc6-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



