---
description: Lojas de pessoas ao meu redor
ms.assetid: 3f2aa9bd-49ca-4fa6-b718-7cbeeef857c7
title: Lojas de pessoas ao meu redor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d18bf60e43aba278862fbd19f3c8909e344bc67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829177"
---
# <a name="people-near-me-stores"></a><span data-ttu-id="b0fd3-103">Lojas de pessoas ao meu redor</span><span class="sxs-lookup"><span data-stu-id="b0fd3-103">People Near Me Stores</span></span>

<span data-ttu-id="b0fd3-104">Aplicativos capazes de [pessoas ao meu redor](about-people-near-me.md) (PNM) podem usar os seguintes armazenamentos de dados:</span><span class="sxs-lookup"><span data-stu-id="b0fd3-104">Applications capable of [People Near Me](about-people-near-me.md) (PNM) can use the following data stores:</span></span>

### <a name="windows-address-book"></a><span data-ttu-id="b0fd3-105">Catálogo de endereços do Windows</span><span class="sxs-lookup"><span data-stu-id="b0fd3-105">Windows Address Book</span></span>

<span data-ttu-id="b0fd3-106">O catálogo de endereços do Windows armazena informações sobre contatos e seus certificados digitais.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-106">The Windows Address Book stores information on contacts and their digital certificates.</span></span> <span data-ttu-id="b0fd3-107">O contato '**me**', que representa o usuário conectado no momento, também é armazenado no catálogo de endereços do Windows.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-107">The '**Me**' contact, representing the currently logged in user, is also stored in the Windows Address Book.</span></span>

### <a name="certificate-store"></a><span data-ttu-id="b0fd3-108">Repositório de certificados</span><span class="sxs-lookup"><span data-stu-id="b0fd3-108">Certificate Store</span></span>

<span data-ttu-id="b0fd3-109">O repositório de certificados contém o certificado autoassinado para o contato '**me**'.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-109">The Certificate Store contains the self-signed certificate for the '**Me**' contact.</span></span>

### <a name="application-store"></a><span data-ttu-id="b0fd3-110">Repositório de aplicativos</span><span class="sxs-lookup"><span data-stu-id="b0fd3-110">Application Store</span></span>

<span data-ttu-id="b0fd3-111">Um instalador de aplicativo registra um aplicativo com o PNM durante o processo de instalação.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-111">An application installer registers an application with PNM during the installation process.</span></span> <span data-ttu-id="b0fd3-112">Esses são os objetos que podem ser pesquisados por outros usuários ao tentar se conectar a um usuário com um aplicativo comum, como um jogo de computador.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-112">These are the objects that can be searched for by other users when attempting to connect to a user with a common application, such as a computer game.</span></span> <span data-ttu-id="b0fd3-113">Para cada aplicativo, a loja de aplicativos contém o nome do aplicativo, um GUID (identificador global exclusivo), um escopo do aplicativo, uma descrição e um caminho para o arquivo executável do programa.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-113">For each application, the Application Store contains the name of the application, a globally unique identifier (GUID), a scope of the application, a description, and a path to the executable file of the program.</span></span> <span data-ttu-id="b0fd3-114">O escopo de um aplicativo pode ser definido como nenhum (não anunciado), pessoas ao meu redor (anunciados na sub-rede local), contatos (anunciados apenas para contatos) ou todos (anunciados na sub-rede local e para contatos).</span><span class="sxs-lookup"><span data-stu-id="b0fd3-114">The scope of an application can be set to None (not advertised), People Near Me (advertised on the local subnet), Contacts (advertised just for contacts), or All (advertised on the local subnet and for contacts).</span></span> <span data-ttu-id="b0fd3-115">A loja de aplicativos está localizada no registro do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b0fd3-115">The Application Store is located in the Windows Vista registry.</span></span>

 

 



