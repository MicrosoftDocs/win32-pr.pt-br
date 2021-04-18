---
description: O uso da funcionalidade do IMM em seu aplicativo com reconhecimento de IME alivia os usuários da necessidade de se lembrar de todos os valores de caractere possíveis.
ms.assetid: 43b3e561-b844-4688-ab3d-d99f92ed140e
title: Sobre o Gerenciador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b96c64eba5ddfb6966c96d88792fd657f94aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105800050"
---
# <a name="about-input-method-manager"></a><span data-ttu-id="ed34a-103">Sobre o Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ed34a-103">About Input Method Manager</span></span>

<span data-ttu-id="ed34a-104">O uso da funcionalidade do IMM em seu aplicativo com reconhecimento de IME alivia os usuários da necessidade de se lembrar de todos os valores de caractere possíveis.</span><span class="sxs-lookup"><span data-stu-id="ed34a-104">Use of the IMM functionality in your IME-aware application relieves users of the need to remember all possible character values.</span></span> <span data-ttu-id="ed34a-105">Em vez disso, ele permite que o IME monitore os pressionamentos de tecla de um usuário, prevê os caracteres que o usuário pode desejar e apresenta uma lista de caracteres candidatos a partir dos quais escolher.</span><span class="sxs-lookup"><span data-stu-id="ed34a-105">Instead, it allows the IME to monitor a user's keystrokes, anticipates the characters the user might want, and presents a list of candidate characters from which to choose.</span></span>

> [!Note]  
> <span data-ttu-id="ed34a-106">O IMM executa operações semelhantes às da estrutura de [serviços de texto](../tsf/text-services-framework.md), usada por aplicativos que se comunicam com serviços de texto.</span><span class="sxs-lookup"><span data-stu-id="ed34a-106">The IMM performs similar operations to those of the [Text Services Framework](../tsf/text-services-framework.md), used by applications that communicate with text services.</span></span>

 

<span data-ttu-id="ed34a-107">Por padrão, o IMM fornece uma janela IME por meio da qual o usuário insere pressionamentos de teclas e exibições e seleciona candidatos.</span><span class="sxs-lookup"><span data-stu-id="ed34a-107">By default, the IMM provides an IME window through which the user enters keystrokes and views and selects candidates.</span></span> <span data-ttu-id="ed34a-108">Os aplicativos podem usar as funções e mensagens do IMM para criar e gerenciar suas próprias janelas do IME, fornecendo uma interface personalizada ao usar os recursos de conversão do IME.</span><span class="sxs-lookup"><span data-stu-id="ed34a-108">Applications can use the IMM functions and messages to create and manage their own IME windows, providing a custom interface while using the conversion capabilities of the IME.</span></span>

<span data-ttu-id="ed34a-109">O IMM é habilitado somente no Leste Asiático (chinês, japonês, coreano) sistemas operacionais Windows localizados.</span><span class="sxs-lookup"><span data-stu-id="ed34a-109">The IMM is only enabled on East Asian (Chinese, Japanese, Korean) localized Windows operating systems.</span></span> <span data-ttu-id="ed34a-110">Nesses sistemas, o aplicativo chama [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ DBCSENABLED para determinar se o IMM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed34a-110">On these systems, the application calls [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_DBCSENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="ed34a-111">**Windows 2000:** O suporte completo a IMM é fornecido em todas as versões de idiomas localizadas.</span><span class="sxs-lookup"><span data-stu-id="ed34a-111">**Windows 2000:** Full-featured IMM support is provided in all localized language versions.</span></span> <span data-ttu-id="ed34a-112">No entanto, o IMM é habilitado somente quando um pacote de idiomas asiático é instalado.</span><span class="sxs-lookup"><span data-stu-id="ed34a-112">However, the IMM is enabled only when an Asian language pack is installed.</span></span> <span data-ttu-id="ed34a-113">Um aplicativo com reconhecimento de IME pode chamar [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) com SM \_ IMMENABLED para determinar se o IMM está habilitado.</span><span class="sxs-lookup"><span data-stu-id="ed34a-113">An IME-aware application can call [GetSystemMetrics](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) with SM\_IMMENABLED to determine if the IMM is enabled.</span></span>

<span data-ttu-id="ed34a-114">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed34a-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ed34a-115">Listas de candidatos</span><span class="sxs-lookup"><span data-stu-id="ed34a-115">Candidate Lists</span></span>](candidate-lists.md)
-   [<span data-ttu-id="ed34a-116">Cadeia de caracteres de composição</span><span class="sxs-lookup"><span data-stu-id="ed34a-116">Composition String</span></span>](composition-string.md)
-   [<span data-ttu-id="ed34a-117">HexToUnicode IME</span><span class="sxs-lookup"><span data-stu-id="ed34a-117">HexToUnicode IME</span></span>](hextounicode-ime.md)
-   [<span data-ttu-id="ed34a-118">Teclas de Atalho</span><span class="sxs-lookup"><span data-stu-id="ed34a-118">Hot Keys</span></span>](hot-keys.md)
-   [<span data-ttu-id="ed34a-119">Mensagens do IME</span><span class="sxs-lookup"><span data-stu-id="ed34a-119">IME Messages</span></span>](ime-messages.md)
-   [<span data-ttu-id="ed34a-120">Classe da janela do IME</span><span class="sxs-lookup"><span data-stu-id="ed34a-120">IME Window Class</span></span>](ime-window-class.md)
-   [<span data-ttu-id="ed34a-121">Contexto de entrada</span><span class="sxs-lookup"><span data-stu-id="ed34a-121">Input Context</span></span>](input-context.md)
-   [<span data-ttu-id="ed34a-122">Janelas de status, composição e candidatos</span><span class="sxs-lookup"><span data-stu-id="ed34a-122">Status, Composition, and Candidates Windows</span></span>](status--composition--and-candidates-windows.md)

 

 
