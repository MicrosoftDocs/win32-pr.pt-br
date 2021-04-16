---
description: Quando você define um nível de autenticação para um aplicativo, determina qual grau de autenticação é executado quando os clientes chamam o aplicativo.
ms.assetid: a59935de-6b8f-4c0a-8479-e30bc0509698
title: Definindo um nível de autenticação para um aplicativo de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83450b3f8d1939d08cc3d16a21f438c8da6f8fc1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105761075"
---
# <a name="setting-an-authentication-level-for-a-server-application"></a><span data-ttu-id="9e112-103">Definindo um nível de autenticação para um aplicativo de servidor</span><span class="sxs-lookup"><span data-stu-id="9e112-103">Setting an Authentication Level for a Server Application</span></span>

<span data-ttu-id="9e112-104">Quando você define um nível de autenticação para um aplicativo, determina qual grau de autenticação é executado quando os clientes chamam o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="9e112-104">When you set an authentication level for an application, you determine what degree of authentication is performed when clients call into the application.</span></span> <span data-ttu-id="9e112-105">Níveis de autenticação mais altos fornecem maior segurança e integridade dos dados, embora geralmente com alguma degradação do desempenho.</span><span class="sxs-lookup"><span data-stu-id="9e112-105">Higher authentication levels provide greater security and data integrity, although usually with some performance degradation.</span></span> <span data-ttu-id="9e112-106">Para obter mais informações, consulte [autenticação de cliente](client-authentication.md).</span><span class="sxs-lookup"><span data-stu-id="9e112-106">For more information, see [Client Authentication](client-authentication.md).</span></span>

<span data-ttu-id="9e112-107">**Para selecionar um nível de autenticação para um aplicativo de servidor**</span><span class="sxs-lookup"><span data-stu-id="9e112-107">**To select an authentication level for a server application**</span></span>

1.  <span data-ttu-id="9e112-108">Clique com o botão direito do mouse no aplicativo COM+ para o qual você está definindo autenticação e clique em **Propriedades**.</span><span class="sxs-lookup"><span data-stu-id="9e112-108">Right-click the COM+ application for which you are setting authentication, and then click **Properties**.</span></span>

2.  <span data-ttu-id="9e112-109">Na caixa de diálogo Propriedades do aplicativo, clique na guia **segurança** .</span><span class="sxs-lookup"><span data-stu-id="9e112-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="9e112-110">Na caixa **nível de autenticação para chamadas** , selecione o nível apropriado.</span><span class="sxs-lookup"><span data-stu-id="9e112-110">In the **Authentication level for calls** box, select the appropriate level.</span></span> <span data-ttu-id="9e112-111">Os níveis são os seguintes, ordenados da mais baixa para a mais alta segurança:</span><span class="sxs-lookup"><span data-stu-id="9e112-111">The levels are as follows, ordered from lowest to highest security:</span></span>

    -   <span data-ttu-id="9e112-112">**None**.</span><span class="sxs-lookup"><span data-stu-id="9e112-112">**None**.</span></span> <span data-ttu-id="9e112-113">Nenhuma autenticação ocorre.</span><span class="sxs-lookup"><span data-stu-id="9e112-113">No authentication occurs.</span></span>
    -   <span data-ttu-id="9e112-114">**Conecte-se**.</span><span class="sxs-lookup"><span data-stu-id="9e112-114">**Connect**.</span></span> <span data-ttu-id="9e112-115">Autentica as credenciais somente quando a conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="9e112-115">Authenticates credentials only when the connection is made.</span></span>
    -   <span data-ttu-id="9e112-116">**Chame**.</span><span class="sxs-lookup"><span data-stu-id="9e112-116">**Call**.</span></span> <span data-ttu-id="9e112-117">Autentica as credenciais no início de cada chamada.</span><span class="sxs-lookup"><span data-stu-id="9e112-117">Authenticates credentials at the beginning of every call.</span></span>
    -   <span data-ttu-id="9e112-118">**Pacote**.</span><span class="sxs-lookup"><span data-stu-id="9e112-118">**Packet**.</span></span> <span data-ttu-id="9e112-119">Autentica as credenciais e verifica se todos os dados de chamada foram recebidos.</span><span class="sxs-lookup"><span data-stu-id="9e112-119">Authenticates credentials and verifies that all call data is received.</span></span> <span data-ttu-id="9e112-120">Essa é a configuração padrão para aplicativos de servidor COM+.</span><span class="sxs-lookup"><span data-stu-id="9e112-120">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="9e112-121">**Integridade do pacote**.</span><span class="sxs-lookup"><span data-stu-id="9e112-121">**Packet Integrity**.</span></span> <span data-ttu-id="9e112-122">Autentica as credenciais e verifica se nenhum dado de chamada foi modificado em trânsito.</span><span class="sxs-lookup"><span data-stu-id="9e112-122">Authenticates credentials and verifies that no call data has been modified in transit.</span></span>
    -   <span data-ttu-id="9e112-123">**Privacidade do pacote**.</span><span class="sxs-lookup"><span data-stu-id="9e112-123">**Packet Privacy**.</span></span> <span data-ttu-id="9e112-124">Autentica as credenciais e criptografa o pacote, incluindo os dados, a identidade e a assinatura do remetente.</span><span class="sxs-lookup"><span data-stu-id="9e112-124">Authenticates credentials and encrypts the packet, including the data and the sender's identity and signature.</span></span>

4.  <span data-ttu-id="9e112-125">Clique em **OK**.</span><span class="sxs-lookup"><span data-stu-id="9e112-125">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e112-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e112-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e112-127">Habilitando a autenticação para um aplicativo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="9e112-127">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> </dl>

 

 



