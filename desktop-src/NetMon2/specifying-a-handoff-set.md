---
description: Um conjunto de entregas especifica os protocolos que seguem um protocolo. O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: Especificando um conjunto de entrega
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9acb421963bea3ffaa70b6165c6ffceee138e38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780199"
---
# <a name="specifying-a-handoff-set"></a><span data-ttu-id="c85d0-104">Especificando um conjunto de entrega</span><span class="sxs-lookup"><span data-stu-id="c85d0-104">Specifying a Handoff Set</span></span>

<span data-ttu-id="c85d0-105">Um conjunto de entregas especifica os protocolos que seguem um protocolo.</span><span class="sxs-lookup"><span data-stu-id="c85d0-105">A handoff set specifies the protocols that follow a protocol.</span></span> <span data-ttu-id="c85d0-106">O analisador usa um conjunto de entrega somente quando o analisador pode identificar o próximo protocolo dos dados em uma instância de protocolo.</span><span class="sxs-lookup"><span data-stu-id="c85d0-106">The parser uses a handoff set only when the parser can identify the next protocol from the data in a protocol instance.</span></span>

<span data-ttu-id="c85d0-107">Por exemplo, o protocolo TCP tem uma propriedade Port que identifica o protocolo que segue o protocolo TCP.</span><span class="sxs-lookup"><span data-stu-id="c85d0-107">For example, the TCP protocol has a port property that identifies the protocol that follows the TCP protocol.</span></span> <span data-ttu-id="c85d0-108">Um valor de propriedade de 20 indica que o próximo protocolo é FTP.</span><span class="sxs-lookup"><span data-stu-id="c85d0-108">A property value of 20 indicates that the next protocol is FTP.</span></span> <span data-ttu-id="c85d0-109">Um valor de propriedade de 53 indica que o próximo protocolo é DNS.</span><span class="sxs-lookup"><span data-stu-id="c85d0-109">A property value of 53 indicates that the next protocol is DNS.</span></span> <span data-ttu-id="c85d0-110">Como a propriedade Port identifica o protocolo a seguir, o analisador TCP pode usar o seguinte conjunto de entrega para obter um identificador para o protocolo que a propriedade Port especifica.</span><span class="sxs-lookup"><span data-stu-id="c85d0-110">Because the port property identifies the protocol that follows, the TCP parser can use the following handoff set to get a handle for the protocol that the port property specifies.</span></span>

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

<span data-ttu-id="c85d0-111">Os conjuntos de entrega são armazenados no arquivo INI do analisador.</span><span class="sxs-lookup"><span data-stu-id="c85d0-111">Handoff sets are stored in the parser INI file.</span></span> <span data-ttu-id="c85d0-112">Por exemplo, o conjunto de entrega TCP anterior está localizado no arquivo tcpip.ini.</span><span class="sxs-lookup"><span data-stu-id="c85d0-112">For example, the preceding TCP handoff set is located in tcpip.ini file.</span></span> <span data-ttu-id="c85d0-113">Observe que, se uma DLL do analisador der suporte a vários protocolos, cada analisador que usa um conjunto de entrega terá seu próprio local no arquivo INI.</span><span class="sxs-lookup"><span data-stu-id="c85d0-113">Note that if a parser DLL supports multiple protocols, each parser that uses a handoff set has its own location in the INI file.</span></span>

<span data-ttu-id="c85d0-114">As informações do conjunto de entrega são especificadas durante a implementação da função [**ParserAutoInstallInfo**](parserautoinstallinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="c85d0-114">Handoff set information is specified during the implementation of the [**ParserAutoInstallInfo**](parserautoinstallinfo.md) function.</span></span> <span data-ttu-id="c85d0-115">O analisador pode especificar os protocolos que precedem o protocolo do analisador e os protocolos que seguem o protocolo do analisador.</span><span class="sxs-lookup"><span data-stu-id="c85d0-115">The parser can specify the protocols that precede the parser protocol, and the protocols that follow the parser protocol.</span></span> <span data-ttu-id="c85d0-116">Monitor de Rede usa todos os protocolos precedidos e adiciona o protocolo analisador às seções do conjunto de acompanhamento a seguir do arquivo INI do analisador — para cada protocolo anterior.</span><span class="sxs-lookup"><span data-stu-id="c85d0-116">Network Monitor takes all the protocols that precede, and adds the parser protocol to the follow set sections of the parser INI file — for each preceding protocol.</span></span> <span data-ttu-id="c85d0-117">Monitor de Rede armazena a lista de protocolos que seguem na seção conjunto de entrega do arquivo INI do analisador.</span><span class="sxs-lookup"><span data-stu-id="c85d0-117">Network Monitor stores the list of protocols that follow in the handoff set section of the parser INI file.</span></span>

<span data-ttu-id="c85d0-118">O Monitor de Rede armazena as informações de conjunto de entrega no arquivo INI do analisador, mas o analisador não acessa os arquivos INI diretamente.</span><span class="sxs-lookup"><span data-stu-id="c85d0-118">Network Monitor stores the handoff set information in the parser INI file, but the parser does not access the INI files directly.</span></span> <span data-ttu-id="c85d0-119">Para usar as informações no conjunto de entrega, o analisador chama a função [**Createentregatable**](createhandofftable.md) para criar uma tabela de entrega.</span><span class="sxs-lookup"><span data-stu-id="c85d0-119">To use the information in the handoff set, the parser calls the [**CreateHandoffTable**](createhandofftable.md) function to create a handoff table.</span></span> <span data-ttu-id="c85d0-120">Normalmente, a tabela de entrega é criada quando o analisador registra o protocolo.</span><span class="sxs-lookup"><span data-stu-id="c85d0-120">Typically, the handoff table is created when the parser registers the protocol.</span></span> <span data-ttu-id="c85d0-121">Depois que o protocolo é registrado, o Monitor de Rede cria uma tabela de conjunto de entrega que o analisador pode usar.</span><span class="sxs-lookup"><span data-stu-id="c85d0-121">After the protocol is registered, Network Monitor creates a handoff set table that the parser can use.</span></span>

<span data-ttu-id="c85d0-122">O analisador usa seu conjunto de entregas ao reconhecer dados.</span><span class="sxs-lookup"><span data-stu-id="c85d0-122">The parser uses its handoff set when recognizing data.</span></span> <span data-ttu-id="c85d0-123">Primeiro, o analisador lê o valor da propriedade que identifica o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="c85d0-123">First the parser reads the value of the property that identifies the next protocol.</span></span> <span data-ttu-id="c85d0-124">Em seguida, o analisador chama o [**GetProtocolFromTable**](getprotocolfromtable.md) para obter um identificador para o próximo protocolo.</span><span class="sxs-lookup"><span data-stu-id="c85d0-124">Then the parser calls the [**GetProtocolFromTable**](getprotocolfromtable.md) to get a handle to the next protocol.</span></span> <span data-ttu-id="c85d0-125">Por fim, o analisador retorna um ponteiro para o identificador no parâmetro *phNextProtocol* de [**RecognizeFrame**](recognizeframe.md).</span><span class="sxs-lookup"><span data-stu-id="c85d0-125">Last, the parser returns a pointer to the handle in the *phNextProtocol* parameter of [**RecognizeFrame**](recognizeframe.md).</span></span>

 

 



