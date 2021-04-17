---
description: O Windows Sockets 2 é um conjunto de funções que padroniza a maneira como os aplicativos acessam e usam os vários serviços de nomes de rede.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registro e resolução de nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773032"
---
# <a name="registration-and-name-resolution"></a><span data-ttu-id="ee316-103">Registro e resolução de nome</span><span class="sxs-lookup"><span data-stu-id="ee316-103">Registration and Name Resolution</span></span>

<span data-ttu-id="ee316-104">O Windows Sockets 2 é um conjunto de funções que padroniza a maneira como os aplicativos acessam e usam os vários serviços de nomes de rede.</span><span class="sxs-lookup"><span data-stu-id="ee316-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="ee316-105">Ao usar essas funções, os aplicativos não precisam distinguir os protocolos amplamente diferentes associados aos serviços de nome, como DNS, NIS, X. 500, SAP, etc. Para manter a compatibilidade com versões anteriores com o Windows Sockets 1,1, as funções de pesquisa de banco de dados **getXbyY** e assíncronas **WSAAsyncGetXbyY** continuam a ser suportadas, mas são implementadas na interface do provedor de serviços do Windows Sockets em termos de novos recursos de resolução de nomes.</span><span class="sxs-lookup"><span data-stu-id="ee316-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="ee316-106">Para obter mais informações, consulte as funções [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) .</span><span class="sxs-lookup"><span data-stu-id="ee316-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="ee316-107">Além disso, consulte [resolução de nome compatível para TCP/IP no SPI do Windows sockets 1,1](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span><span class="sxs-lookup"><span data-stu-id="ee316-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="ee316-108">Esta seção descreve os recursos de registro e resolução de nomes disponíveis para desenvolvedores de Winsock.</span><span class="sxs-lookup"><span data-stu-id="ee316-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="ee316-109">A lista a seguir descreve os tópicos nesta seção:</span><span class="sxs-lookup"><span data-stu-id="ee316-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="ee316-110">Resolução de nomes independente de protocolo</span><span class="sxs-lookup"><span data-stu-id="ee316-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="ee316-111">Resolução de nomes compatível com TCP/IP na API do Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="ee316-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="ee316-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ee316-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee316-113">Sobre o Winsock</span><span class="sxs-lookup"><span data-stu-id="ee316-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="ee316-114">Usando o Winsock</span><span class="sxs-lookup"><span data-stu-id="ee316-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



