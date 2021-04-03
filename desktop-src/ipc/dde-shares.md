---
description: Os compartilhamentos DDE são um recurso de máquina.
ms.assetid: 98d24300-52cc-4f0d-b74f-c58b823ac5f3
title: Compartilhamentos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 012c219897187c9e68b5b9e662b93678b77974c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828625"
---
# <a name="dde-shares"></a><span data-ttu-id="96650-103">Compartilhamentos DDE</span><span class="sxs-lookup"><span data-stu-id="96650-103">DDE Shares</span></span>

<span data-ttu-id="96650-104">\[Não há mais suporte para DDE de rede.</span><span class="sxs-lookup"><span data-stu-id="96650-104">\[Network DDE is no longer supported.</span></span> <span data-ttu-id="96650-105">Nddeapi.dll está presente no Windows Vista, mas todas as chamadas de função retornam NDDE \_ não \_ implementado.\]</span><span class="sxs-lookup"><span data-stu-id="96650-105">Nddeapi.dll is present on Windows Vista, but all function calls return NDDE\_NOT\_IMPLEMENTED.\]</span></span>

<span data-ttu-id="96650-106">Os compartilhamentos DDE são um recurso de máquina.</span><span class="sxs-lookup"><span data-stu-id="96650-106">DDE shares are a machine resource.</span></span> <span data-ttu-id="96650-107">Eles são semelhantes aos compartilhamentos de arquivos porque são usados para controlar o acesso a um recurso.</span><span class="sxs-lookup"><span data-stu-id="96650-107">They are similar to file shares because they are used to control access to a resource.</span></span> <span data-ttu-id="96650-108">Com compartilhamentos de arquivos, o recurso é um arquivo.</span><span class="sxs-lookup"><span data-stu-id="96650-108">With file shares, the resource is a file.</span></span> <span data-ttu-id="96650-109">Com compartilhamentos DDE, o recurso é trocado de dados dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="96650-109">With DDE shares, the resource is dynamically exchanged data.</span></span> <span data-ttu-id="96650-110">O tipo de dados trocado é determinado pelo aplicativo de servidor que fornece os dados e o aplicativo cliente que solicita os dados.</span><span class="sxs-lookup"><span data-stu-id="96650-110">The type of data exchanged is determined by the server application that supplies the data and the client application that requests the data.</span></span>

<span data-ttu-id="96650-111">O servidor chama a função [**NDdeShareAdd**](nddeshareadd.md) para criar o compartilhamento DDE, que é armazenado no DSDM (Gerenciador de banco de dados de compartilhamento DDE).</span><span class="sxs-lookup"><span data-stu-id="96650-111">The server calls the [**NDdeShareAdd**](nddeshareadd.md) function to create the DDE share, which is stored in the DDE share database manager (DSDM).</span></span>

<span data-ttu-id="96650-112">O cliente inicia a conversa DDE conectando-se ao compartilhamento DDE.</span><span class="sxs-lookup"><span data-stu-id="96650-112">The client starts the DDE conversation by connecting to the DDE share.</span></span> <span data-ttu-id="96650-113">O cliente deve chamar a função [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) para inicializar o ddeml e chamar a função [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) para se conectar ao compartilhamento de DDE.</span><span class="sxs-lookup"><span data-stu-id="96650-113">The client must call the [**DdeInitialize**](/windows/win32/api/ddeml/nf-ddeml-ddeinitializea) function to initialize DDEML and call the [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) function to connect to the DDE share.</span></span> <span data-ttu-id="96650-114">Na chamada **DdeConnect** , o cliente especifica o nome do serviço da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="96650-114">In the **DdeConnect** call, the client specifies the service name as follows:</span></span>

<span data-ttu-id="96650-115">\\\\*ComputerName* \\ NDDE $</span><span class="sxs-lookup"><span data-stu-id="96650-115">\\\\*ComputerName*\\NDDE$</span></span>

<span data-ttu-id="96650-116">em que *ComputerName* é o nome do computador que executa o aplicativo de servidor.</span><span class="sxs-lookup"><span data-stu-id="96650-116">where *ComputerName* is the name of the computer running the server application.</span></span> <span data-ttu-id="96650-117">O NDDE $ indica que o tópico fornecido para [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) é o nome do compartilhamento DDE no computador remoto chamado *ComputerName*.</span><span class="sxs-lookup"><span data-stu-id="96650-117">The NDDE$ indicates that the topic provided to [**DdeConnect**](/windows/win32/api/ddeml/nf-ddeml-ddeconnect) is the DDE share name on the remote computer named *ComputerName*.</span></span>

<span data-ttu-id="96650-118">Há três tipos de compartilhamentos DDE: estilo antigo, novo estilo e estático.</span><span class="sxs-lookup"><span data-stu-id="96650-118">There are three types of DDE shares: old style, new style, and static.</span></span> <span data-ttu-id="96650-119">É comum dar suporte apenas ao tipo estático.</span><span class="sxs-lookup"><span data-stu-id="96650-119">It is typical to support only the static type.</span></span> <span data-ttu-id="96650-120">Os nomes de compartilhamentos estáticos usam a seguinte convenção: *ShareName*$.</span><span class="sxs-lookup"><span data-stu-id="96650-120">The names of static shares use the following convention: *ShareName*$.</span></span>

 

 
