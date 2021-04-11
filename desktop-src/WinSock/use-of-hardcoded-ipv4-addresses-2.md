---
description: A longevidade do IPv4 resultou em codificação rígida de muitos endereços IPv4 conhecidos, como endereços de loopback (127. x. x. x), constantes de inteiros como, por exemplo \_ , loopback de inaddr, entre outros.
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: Uso de endereços IPv4 codificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296340"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="9a05f-103">Uso de endereços IPv4 codificados</span><span class="sxs-lookup"><span data-stu-id="9a05f-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="9a05f-104">A longevidade do IPv4 resultou em codificação rígida de muitos endereços IPv4 conhecidos, como endereços de loopback (127. x. x. x), constantes de inteiros como, por exemplo \_ , loopback de inaddr, entre outros.</span><span class="sxs-lookup"><span data-stu-id="9a05f-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="9a05f-105">A prática de codificação rígida desses endereços apresenta problemas óbvios durante a modificação e o aplicativo existente para dar suporte ao IPv6 ou à criação de novos programas independentes de versão de IP.</span><span class="sxs-lookup"><span data-stu-id="9a05f-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="9a05f-106">Melhor prática</span><span class="sxs-lookup"><span data-stu-id="9a05f-106">Best Practice</span></span>

-   <span data-ttu-id="9a05f-107">A melhor abordagem é evitar o código de codificação de endereços.</span><span class="sxs-lookup"><span data-stu-id="9a05f-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="9a05f-108">Código a ser evitado</span><span class="sxs-lookup"><span data-stu-id="9a05f-108">Code To Avoid</span></span>

-   <span data-ttu-id="9a05f-109">Evite usar endereços codificados no código.</span><span class="sxs-lookup"><span data-stu-id="9a05f-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="9a05f-110">**Para modificar sua base de código existente de IPv4 para IPv4 e IPv6-interoperabilidade**</span><span class="sxs-lookup"><span data-stu-id="9a05f-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="9a05f-111">Adquira o utilitário *Checkv4.exe* .</span><span class="sxs-lookup"><span data-stu-id="9a05f-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="9a05f-112">O utilitário *Checkv4.exe* é instalado como parte do SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior.</span><span class="sxs-lookup"><span data-stu-id="9a05f-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="9a05f-113">O SDK do Windows está disponível por meio de uma assinatura do MSDN e também pode ser baixado do site da Microsoft ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="9a05f-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="9a05f-114">Execute o utilitário *Checkv4.exe* em relação ao seu código.</span><span class="sxs-lookup"><span data-stu-id="9a05f-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="9a05f-115">Saiba mais sobre como executar o utilitário de *Checkv4.exe* em seus arquivos na seção sobre como [usar o utilitário de Checkv4.exe](using-the-checkv4-exe-utility-2.md).</span><span class="sxs-lookup"><span data-stu-id="9a05f-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="9a05f-116">O utilitário *Checkv4.exe* alerta você sobre a presença de definições comuns para endereços IPv4, como inaddr \_ loopback.</span><span class="sxs-lookup"><span data-stu-id="9a05f-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="9a05f-117">Modifique qualquer código que use cadeias de caracteres literais com código que seja independente de versão de protocolo.</span><span class="sxs-lookup"><span data-stu-id="9a05f-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="9a05f-118">Pesquise sua base de código para outras possíveis cadeias de caracteres literais, conforme apropriado.</span><span class="sxs-lookup"><span data-stu-id="9a05f-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="9a05f-119">O utilitário *Checkv4.exe* pode ajudá-lo a encontrar cadeias de caracteres literais comuns, mas pode haver outros que são específicas do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9a05f-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="9a05f-120">Você deve executar a pesquisa e os testes completos para garantir que sua base de código tenha potencialmente possíveis problemas associados a cadeias de caracteres literais.</span><span class="sxs-lookup"><span data-stu-id="9a05f-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a05f-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9a05f-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a05f-122">Guia IPv6 para aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="9a05f-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="9a05f-123">Alterando estruturas de dados para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="9a05f-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="9a05f-124">Soquetes de pilha dupla para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="9a05f-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="9a05f-125">Chamadas de função para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="9a05f-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="9a05f-126">Problemas de interface do usuário para aplicativos Winsock do IPv6</span><span class="sxs-lookup"><span data-stu-id="9a05f-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="9a05f-127">Protocolos subjacentes para aplicativos Winsock IPv6</span><span class="sxs-lookup"><span data-stu-id="9a05f-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



