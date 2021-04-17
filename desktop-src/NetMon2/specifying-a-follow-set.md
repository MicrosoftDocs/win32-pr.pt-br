---
description: Um conjunto de acompanhamento especifica os protocolos que seguem um protocolo. Monitor de Rede usa um conjunto de acompanhamento quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.
ms.assetid: 9e73c724-a540-42f8-b273-4f02c39d81c4
title: Especificando um conjunto de acompanhamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9e36268be82d2fed7c3d0c56a078e41dff1733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789629"
---
# <a name="specifying-a-follow-set"></a><span data-ttu-id="08bc8-104">Especificando um conjunto de acompanhamento</span><span class="sxs-lookup"><span data-stu-id="08bc8-104">Specifying a Follow Set</span></span>

<span data-ttu-id="08bc8-105">Um conjunto de acompanhamento especifica os protocolos que seguem um protocolo.</span><span class="sxs-lookup"><span data-stu-id="08bc8-105">A follow set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="08bc8-106">Monitor de Rede usa um conjunto de acompanhamento quando o analisador não pode identificar o próximo protocolo dos dados em uma instância de protocolo.</span><span class="sxs-lookup"><span data-stu-id="08bc8-106">Network Monitor uses a follow set when the parser cannot identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="08bc8-107">Por exemplo, o analisador NetBIOS especifica um conjunto de acompanhamento porque os dados no protocolo NetBIOS não identificam qual protocolo é o próximo.</span><span class="sxs-lookup"><span data-stu-id="08bc8-107">For example, the NetBIOS parser specifies a follow set because the data in the NetBIOS protocol does not identify which protocol is next.</span></span> <span data-ttu-id="08bc8-108">Como resultado, o analisador NetBIOS deve criar um conjunto de todos os protocolos que podem ser seguidos.</span><span class="sxs-lookup"><span data-stu-id="08bc8-108">As a result the NetBIOS parser must create a follow set of all the protocols that may follow.</span></span>

<span data-ttu-id="08bc8-109">O exemplo de código a seguir identifica o conjunto de acompanhamento de NetBIOS no arquivo de [*Parser.ini*](p.md) .</span><span class="sxs-lookup"><span data-stu-id="08bc8-109">The following code example identifies the NetBIOS follow set in the [*Parser.ini*](p.md) file.</span></span> <span data-ttu-id="08bc8-110">O conjunto de acompanhamento contém o protocolo SMB e os protocolos de chamada de procedimento remoto da Microsoft (MSRPC).</span><span class="sxs-lookup"><span data-stu-id="08bc8-110">The follow set contains server message block (SMB), and Microsoft remote procedure call (MSRPC) protocols.</span></span> <span data-ttu-id="08bc8-111">Esses são os únicos protocolos que podem seguir uma instância do protocolo NetBIOS.</span><span class="sxs-lookup"><span data-stu-id="08bc8-111">These are the only protocols that can follow an instance of the NetBIOS protocol.</span></span>

``` syntax
[NETBIOS]
   Comment    = "Network Basic Input/Output System protocol"
   FollowSet  = SMB, MSRPC
   HelpFile   =
```

<span data-ttu-id="08bc8-112">Um analisador especifica um conjunto de acompanhamento durante a implementação da função [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="08bc8-112">A parser specifies a follow set during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="08bc8-113">Um analisador pode especificar quais protocolos são precedidos e quais protocolos seguem.</span><span class="sxs-lookup"><span data-stu-id="08bc8-113">A parser can specify which protocols precede, and which protocols follow.</span></span> <span data-ttu-id="08bc8-114">Quando um analisador especifica os protocolos que precedem, Monitor de Rede adiciona o protocolo analisador aos seguintes conjuntos de protocolos especificados.</span><span class="sxs-lookup"><span data-stu-id="08bc8-114">When a parser specifies the protocols that precede, Network Monitor adds the parser protocol to the follow sets of the specified protocols.</span></span> <span data-ttu-id="08bc8-115">Quando um analisador especifica os protocolos a seguir, Monitor de Rede cria uma nova seção no arquivo de Parser.ini que inclui o conjunto de acompanhamento do analisador.</span><span class="sxs-lookup"><span data-stu-id="08bc8-115">When a parser specifies the protocols that follow, Network Monitor creates a new section in the Parser.ini file that includes the follow set of the parser.</span></span>

 

 



