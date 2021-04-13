---
description: Os desenvolvedores de bancos de dados de instalação precisam estar cientes de duas limitações na manipulação de fluxos pela implementação de armazenamento estruturado OLE do Win32.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: Limitações de OLE em fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164829"
---
# <a name="ole-limitations-on-streams"></a><span data-ttu-id="6218d-103">Limitações de OLE em fluxos</span><span class="sxs-lookup"><span data-stu-id="6218d-103">OLE Limitations on Streams</span></span>

<span data-ttu-id="6218d-104">Os desenvolvedores de bancos de dados de instalação precisam estar cientes de duas limitações na manipulação de fluxos pela implementação de armazenamento estruturado OLE do Win32.</span><span class="sxs-lookup"><span data-stu-id="6218d-104">Developers of installation databases need to be aware of two limitations on the handling of streams by the Win32 OLE structured storage implementation.</span></span> <span data-ttu-id="6218d-105">Essas limitações podem afetar as funções do instalador indiretamente por meio de transformações e outros dados que podem ser armazenados no banco de dado como um fluxo.</span><span class="sxs-lookup"><span data-stu-id="6218d-105">These limitations can affect installer functions indirectly through transforms and other data that may be stored in the database as a stream.</span></span>

<span data-ttu-id="6218d-106">Há duas limitações relevantes:</span><span class="sxs-lookup"><span data-stu-id="6218d-106">There are two relevant limitations:</span></span>

-   <span data-ttu-id="6218d-107">Os dados binários são armazenados com um nome de índice criado concatenando o nome da tabela e os valores das chaves primárias do registro usando um delimitador de período.</span><span class="sxs-lookup"><span data-stu-id="6218d-107">Binary data is stored with an index name created by concatenating the table name and the values of the record's primary keys using a period delimiter.</span></span> <span data-ttu-id="6218d-108">O OLE limita os nomes de fluxo a 32 caracteres (31 + terminador nulo).</span><span class="sxs-lookup"><span data-stu-id="6218d-108">OLE limits stream names to 32 characters (31 + null terminator).</span></span> <span data-ttu-id="6218d-109">Windows Installer usa um algoritmo de compactação que pode expandir o limite para 62 caracteres, dependendo do caractere.</span><span class="sxs-lookup"><span data-stu-id="6218d-109">Windows Installer uses a compression algorithm that can expand the limit to 62 characters depending upon the character.</span></span> <span data-ttu-id="6218d-110">Observe que os caracteres de byte duplo contam como 2.</span><span class="sxs-lookup"><span data-stu-id="6218d-110">Note that double-byte characters count as 2.</span></span>
-   <span data-ttu-id="6218d-111">Embora você possa ter vários fluxos abertos ao mesmo tempo, não é possível abrir um fluxo uma segunda vez até que a primeira referência seja fechada.</span><span class="sxs-lookup"><span data-stu-id="6218d-111">Although you can have multiple streams open at one time, you cannot open a stream a second time until the first reference is closed.</span></span> <span data-ttu-id="6218d-112">Isso significa que você não pode selecionar o mesmo fluxo de dados binários a ser aberto em vários registros simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="6218d-112">This means you cannot select the same binary data stream to be open in multiple records simultaneously.</span></span> <span data-ttu-id="6218d-113">Falha nas tentativas de ler os dados binários do segundo registro.</span><span class="sxs-lookup"><span data-stu-id="6218d-113">Attempts to read the binary data from the second record fail.</span></span> <span data-ttu-id="6218d-114">Além disso, você não pode renomear as chaves primárias de um registro enquanto um fluxo de dados binários nesse registro estiver aberto.</span><span class="sxs-lookup"><span data-stu-id="6218d-114">Also you cannot rename the primary keys of a record while a binary data stream in that record is open.</span></span>

 

 



