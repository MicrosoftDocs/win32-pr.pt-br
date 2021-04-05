---
title: Componentes do Windows instalados sob demanda
description: Componentes do Windows instalados sob demanda
ms.assetid: 14865DD7-167C-462C-B85A-BD07C929D7B8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09d2c3c3fee1cd12d7b12900e41dc006badcf53f
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104008496"
---
# <a name="windows-components-installed-on-demand"></a><span data-ttu-id="f1b58-103">Componentes do Windows instalados sob demanda</span><span class="sxs-lookup"><span data-stu-id="f1b58-103">Windows components installed on demand</span></span>

## <a name="platform"></a><span data-ttu-id="f1b58-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="f1b58-104">Platform</span></span>

<span data-ttu-id="f1b58-105">**Clientes-** Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f1b58-105">**Clients -** Windows 8.1</span></span>  







## <a name="description"></a><span data-ttu-id="f1b58-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1b58-106">Description</span></span>

<span data-ttu-id="f1b58-107">Dois componentes do Windows serão instalados sob demanda no Windows 8.1: DirectPlay e NTVDM.</span><span class="sxs-lookup"><span data-stu-id="f1b58-107">Two Windows components will be installed on demand in Windows 8.1: DirectPlay and NTVDM.</span></span> <span data-ttu-id="f1b58-108">Esses componentes são listados em componentes opcionais no nó "componentes herdados".</span><span class="sxs-lookup"><span data-stu-id="f1b58-108">These components are listed within Optional Components under the “Legacy Components” node.</span></span> <span data-ttu-id="f1b58-109">Esses componentes são instalados localmente como parte do sistema operacional e compactados como componentes opcionais.</span><span class="sxs-lookup"><span data-stu-id="f1b58-109">These components are installed locally as part of the operating system, and compressed as optional components.</span></span> <span data-ttu-id="f1b58-110">Quando um aplicativo referencia ou chama um desses componentes (normalmente na primeira inicialização do aplicativo), a instalação é disparada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="f1b58-110">When an app references or calls one of these components (usually at first launch of the app), installation is triggered automatically.</span></span> <span data-ttu-id="f1b58-111">Os usuários serão notificados de que o componente será instalado e deverão confirmar a ação para continuar.</span><span class="sxs-lookup"><span data-stu-id="f1b58-111">Users will be notified that the component will be installed, and they must confirm the action in order to proceed.</span></span> <span data-ttu-id="f1b58-112">A elevação será necessária para que isso tenha sucesso se o usuário não for um administrador.</span><span class="sxs-lookup"><span data-stu-id="f1b58-112">Elevation is required for this to succeed if the user is not an administrator.</span></span> <span data-ttu-id="f1b58-113">Após a instalação inicial, o usuário não precisa executar nenhuma outra ação para usar o componente novamente.</span><span class="sxs-lookup"><span data-stu-id="f1b58-113">After the initial installation, the user does not need to perform any other actions to use the component again.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f1b58-114">Manifestação</span><span class="sxs-lookup"><span data-stu-id="f1b58-114">Manifestation</span></span>

<span data-ttu-id="f1b58-115">Quando um aplicativo referencia ou chama um componente herdado em componentes opcionais (na primeira inicialização), o aplicativo será suspenso e a caixa de diálogo recurso sob demanda será aberta, solicitando permissão do usuário para instalar o componente.</span><span class="sxs-lookup"><span data-stu-id="f1b58-115">When an app references or calls a legacy component in optional components (at first launch), the app will be suspended and the Feature on Demand dialog will open, requesting user permission to install the component.</span></span> <span data-ttu-id="f1b58-116">Se os usuários clicarem em OK, eles também poderão ver um prompt de elevação em que eles deverão inserir suas credenciais.</span><span class="sxs-lookup"><span data-stu-id="f1b58-116">If users click OK, they may also see an elevation prompt where they must enter their credentials.</span></span> <span data-ttu-id="f1b58-117">O componente será instalado e o aplicativo será retomado.</span><span class="sxs-lookup"><span data-stu-id="f1b58-117">The component will then be installed and the app will resume.</span></span>

## <a name="mitigation"></a><span data-ttu-id="f1b58-118">Atenuação</span><span class="sxs-lookup"><span data-stu-id="f1b58-118">Mitigation</span></span>

<span data-ttu-id="f1b58-119">Para impedir que os recursos da interface do usuário sob demanda sejam abertos, você pode pré-instalar o DirectPlay e o NTVDM usando o DISM ou a interface do usuário de componentes opcionais.</span><span class="sxs-lookup"><span data-stu-id="f1b58-119">To keep the Features on Demand UI from opening, you can pre-install DirectPlay and NTVDM using DISM or the Optional Components UI.</span></span>

## <a name="solution"></a><span data-ttu-id="f1b58-120">Solução</span><span class="sxs-lookup"><span data-stu-id="f1b58-120">Solution</span></span>

<span data-ttu-id="f1b58-121">É altamente recomendável evitar a referência ou a chamada de componentes que foram listados como componentes opcionais herdados no Windows em versões futuras do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1b58-121">You are strongly encouraged to avoid referencing or calling components that have been listed as Legacy Optional Components in Windows in future versions of your app.</span></span> <span data-ttu-id="f1b58-122">Os componentes opcionais herdados incluirão apenas componentes mais antigos e menos usados que possam causar problemas de desempenho e segurança para os usuários.</span><span class="sxs-lookup"><span data-stu-id="f1b58-122">Legacy Optional Components will only include older, lesser-used components that could potentially cause performance and security issues for users.</span></span>

## <a name="tests"></a><span data-ttu-id="f1b58-123">Testes</span><span class="sxs-lookup"><span data-stu-id="f1b58-123">Tests</span></span>

<span data-ttu-id="f1b58-124">Nenhuma acomodações de teste adicional é necessária para compatibilidade.</span><span class="sxs-lookup"><span data-stu-id="f1b58-124">No additional test accommodations are necessary for compatibility.</span></span> <span data-ttu-id="f1b58-125">É importante estar ciente de que essa caixa de diálogo será exibida quando o componente opcional for chamado ou referenciado e essa instalação exigir elevação.</span><span class="sxs-lookup"><span data-stu-id="f1b58-125">It is important to be aware that this dialog will appear when the optional component is called or referenced, and this installation requires elevation.</span></span>

 

 




