---
title: Arquitetura do manipulador
description: Arquitetura do manipulador
ms.assetid: 93839b82-09cb-41af-ac0e-a8e9448bf04b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2b02d0184d364ce438dc28f8219beea01c4868
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005620"
---
# <a name="handler-architecture"></a><span data-ttu-id="4b777-103">Arquitetura do manipulador</span><span class="sxs-lookup"><span data-stu-id="4b777-103">Handler Architecture</span></span>

<span data-ttu-id="4b777-104">A função interna de um manipulador de arquivo ou fluxo é definida pelo próprio manipulador.</span><span class="sxs-lookup"><span data-stu-id="4b777-104">The internal function of a file or stream handler is defined by the handler itself.</span></span> <span data-ttu-id="4b777-105">Para um aplicativo, um manipulador de arquivos normalmente aparece como um módulo para ler e gravar arquivos AVI.</span><span class="sxs-lookup"><span data-stu-id="4b777-105">To an application, a file handler typically appears as a module to read and write AVI files.</span></span> <span data-ttu-id="4b777-106">Da mesma forma, um manipulador de fluxo aparece como um módulo para ler e gravar um tipo específico de fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="4b777-106">Similarly, a stream handler appears as a module to read and write a specific type of data stream.</span></span> <span data-ttu-id="4b777-107">A interface de fluxo consistente torna a origem e o destino do fluxo não importantes para o aplicativo que usa o manipulador.</span><span class="sxs-lookup"><span data-stu-id="4b777-107">The consistent stream interface makes the source and destination of the stream unimportant to the application that uses the handler.</span></span>

<span data-ttu-id="4b777-108">Um manipulador de arquivos fornece acesso a uma fonte de dados que consiste em um ou mais fluxos de dados.</span><span class="sxs-lookup"><span data-stu-id="4b777-108">A file handler provides access to a data source consisting of one or more data streams.</span></span> <span data-ttu-id="4b777-109">Os manipuladores de arquivos normalmente fornecem acesso a arquivos de disco que contêm um ou mais fluxos de dados, e as funções internas do manipulador de arquivos lêem e gravam os dados de multimídia.</span><span class="sxs-lookup"><span data-stu-id="4b777-109">File handlers typically provide access to disk files containing one or more data streams, and the internal functions of the file handler read and write the multimedia data.</span></span> <span data-ttu-id="4b777-110">No entanto, os manipuladores de arquivos podem trabalhar com qualquer fonte de dados, como um canal de transmissão digital contendo vários fluxos de dados intermisturados.</span><span class="sxs-lookup"><span data-stu-id="4b777-110">However, file handlers can work with any data source, such as a digital transmission channel containing several intermingled data streams.</span></span>

<span data-ttu-id="4b777-111">Por outro lado, um manipulador de fluxo processa um tipo de dados e aparece como um fluxo de dados para um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4b777-111">In contrast, a stream handler processes one type of data and appears as a data stream to an application.</span></span> <span data-ttu-id="4b777-112">Um manipulador de fluxo pode fornecer dados que ele fabrica, ou pode recuperar dados de um arquivo ou de uma fonte externa.</span><span class="sxs-lookup"><span data-stu-id="4b777-112">A stream handler can provide data that it manufactures, or it can retrieve data from a file or an external source.</span></span> <span data-ttu-id="4b777-113">Ele fornece seus dados em um formato que seu aplicativo pode usar.</span><span class="sxs-lookup"><span data-stu-id="4b777-113">It supplies its data in a format that your application can use.</span></span>

 

 




