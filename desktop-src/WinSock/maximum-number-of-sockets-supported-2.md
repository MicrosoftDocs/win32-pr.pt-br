---
description: O número máximo de soquetes com suporte de um determinado provedor de serviços do Windows Sockets é específico da implementação.
ms.assetid: acf5ab29-3848-4dbc-afa7-a0f19045ddec
title: Número máximo de soquetes com suporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207893836a411a2465ffcefe10e838c2e8b59011
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768221"
---
# <a name="maximum-number-of-sockets-supported"></a><span data-ttu-id="65d4e-103">Número máximo de soquetes com suporte</span><span class="sxs-lookup"><span data-stu-id="65d4e-103">Maximum Number of Sockets Supported</span></span>

<span data-ttu-id="65d4e-104">O número máximo de soquetes com suporte de um determinado provedor de serviços do Windows Sockets é específico da implementação.</span><span class="sxs-lookup"><span data-stu-id="65d4e-104">The maximum number of sockets supported by a particular Windows Sockets service provider is implementation specific.</span></span> <span data-ttu-id="65d4e-105">O provedor Microsoft Winsock limita o número máximo de soquetes com suporte apenas pela memória disponível no computador local.</span><span class="sxs-lookup"><span data-stu-id="65d4e-105">The Microsoft Winsock provider limits the maximum number of sockets supported only by available memory on the local computer.</span></span> <span data-ttu-id="65d4e-106">No entanto, provedores de Winsock de terceiros podem ter limitações sobre os números de soquetes com suporte.</span><span class="sxs-lookup"><span data-stu-id="65d4e-106">However, third-party Winsock providers may have limitations on the numbers of sockets supported.</span></span> <span data-ttu-id="65d4e-107">Um aplicativo não deve fazer suposições sobre a disponibilidade de um determinado número de soquetes.</span><span class="sxs-lookup"><span data-stu-id="65d4e-107">An application should make no assumptions about the availability of a certain number of sockets.</span></span> <span data-ttu-id="65d4e-108">Para obter mais informações sobre este tópico, consulte [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span><span class="sxs-lookup"><span data-stu-id="65d4e-108">For more information on this topic see [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup).</span></span>

## <a name="fd_set-and-select"></a><span data-ttu-id="65d4e-109">FD \_ set e Select</span><span class="sxs-lookup"><span data-stu-id="65d4e-109">FD\_SET and select</span></span>

<span data-ttu-id="65d4e-110">Várias \_ macros do FD xxx são definidas no arquivo de cabeçalho *Winsock2. h* para uso na portabilidade de aplicativos para o Windows a partir do ambiente UNIX.</span><span class="sxs-lookup"><span data-stu-id="65d4e-110">A number of FD\_XXX macros are defined in the *Winsock2.h* header file for use in porting applications to Windows from the UNIX environment.</span></span> <span data-ttu-id="65d4e-111">Essas macros são usadas com as funções [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) e [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) para portar aplicativos para o Windows.</span><span class="sxs-lookup"><span data-stu-id="65d4e-111">These macros are used with the [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) and [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) functions for porting applications to Windows.</span></span> <span data-ttu-id="65d4e-112">O número máximo de soquetes que um aplicativo do Windows Sockets pode usar não é afetado pela constante de manifesto FD \_ SetSize.</span><span class="sxs-lookup"><span data-stu-id="65d4e-112">The maximum number of sockets that a Windows Sockets application can use is not affected by the manifest constant FD\_SETSIZE.</span></span> <span data-ttu-id="65d4e-113">Esse valor definido no arquivo de cabeçalho *Winsock2. h* é usado na construção das estruturas [**de \_ conjunto fd**](/windows/desktop/api/winsock/nf-winsock-fd_set) usadas com a função **Select** .</span><span class="sxs-lookup"><span data-stu-id="65d4e-113">This value defined in the *Winsock2.h* header file is used in constructing the [**FD\_SET**](/windows/desktop/api/winsock/nf-winsock-fd_set) structures used with **select** function.</span></span> <span data-ttu-id="65d4e-114">O valor padrão em Winsock2. h é 64.</span><span class="sxs-lookup"><span data-stu-id="65d4e-114">The default value in Winsock2.h is 64.</span></span> <span data-ttu-id="65d4e-115">Se um aplicativo for projetado para ser capaz de trabalhar com mais de 64 soquetes usando as funções **Select** e **WSAPoll** , o implementador deverá definir o manifesto FD \_ SetSize em todos os arquivos de origem antes de incluir o arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="65d4e-115">If an application is designed to be capable of working with more than 64 sockets using the **select** and **WSAPoll** functions, the implementor should define the manifest FD\_SETSIZE in every source file before including the *Winsock2.h* header file.</span></span> <span data-ttu-id="65d4e-116">Uma maneira de fazer isso pode ser incluir a definição nas opções do compilador no Makefile.</span><span class="sxs-lookup"><span data-stu-id="65d4e-116">One way of doing this may be to include the definition within the compiler options in the makefile.</span></span> <span data-ttu-id="65d4e-117">Por exemplo, você pode adicionar "-DFD \_ SetSize = 128" como uma opção para a linha de comando do compilador para Microsoft C++.</span><span class="sxs-lookup"><span data-stu-id="65d4e-117">For example, you could add "-DFD\_SETSIZE=128" as an option to the compiler command line for Microsoft C++.</span></span> <span data-ttu-id="65d4e-118">Deve-se enfatizar que definir FD \_ SetSize como um valor específico não tem nenhum efeito sobre o número real de soquetes fornecidos por um provedor de serviços do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="65d4e-118">It must be emphasized that defining FD\_SETSIZE as a particular value has no effect on the actual number of sockets provided by a Windows Sockets service provider.</span></span> <span data-ttu-id="65d4e-119">Esse valor afeta apenas as \_ macros do FD xxx usadas pelas funções **Select** e **WSAPoll** .</span><span class="sxs-lookup"><span data-stu-id="65d4e-119">This value only affects the FD\_XXX macros used by the **select** and **WSAPoll** functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65d4e-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65d4e-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65d4e-121">**conjunto de FD \_**</span><span class="sxs-lookup"><span data-stu-id="65d4e-121">**FD\_SET**</span></span>](/windows/desktop/api/winsock/nf-winsock-fd_set)
</dt> <dt>

[<span data-ttu-id="65d4e-122">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="65d4e-122">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="65d4e-123">**Não**</span><span class="sxs-lookup"><span data-stu-id="65d4e-123">**select**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-select)
</dt> <dt>

[<span data-ttu-id="65d4e-124">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="65d4e-124">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="65d4e-125">**WSAStartup**</span><span class="sxs-lookup"><span data-stu-id="65d4e-125">**WSAStartup**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsastartup)
</dt> <dt>

[<span data-ttu-id="65d4e-126">**WSAPoll**</span><span class="sxs-lookup"><span data-stu-id="65d4e-126">**WSAPoll**</span></span>](/windows/win32/api/winsock2/nf-winsock2-wsapoll)
</dt> </dl>

 

 
