---
description: 'Há dois tipos distintos de aplicativos de rede de soquete: servidor e cliente.'
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: Sobre servidores e clientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763521"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="b8986-103">Sobre servidores e clientes</span><span class="sxs-lookup"><span data-stu-id="b8986-103">About Servers and Clients</span></span>

<span data-ttu-id="b8986-104">Há dois tipos distintos de aplicativos de rede de soquete: servidor e cliente.</span><span class="sxs-lookup"><span data-stu-id="b8986-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="b8986-105">Servidores e clientes têm comportamentos diferentes; Portanto, o processo de criá-los é diferente.</span><span class="sxs-lookup"><span data-stu-id="b8986-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="b8986-106">O que vem a seguir é o modelo geral para criar um cliente e servidor TCP/IP de streaming.</span><span class="sxs-lookup"><span data-stu-id="b8986-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="b8986-107">Servidor</span><span class="sxs-lookup"><span data-stu-id="b8986-107">Server</span></span>

1.  <span data-ttu-id="b8986-108">Inicialize o Winsock.</span><span class="sxs-lookup"><span data-stu-id="b8986-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="b8986-109">Crie um soquete.</span><span class="sxs-lookup"><span data-stu-id="b8986-109">Create a socket.</span></span>
3.  <span data-ttu-id="b8986-110">Associe o soquete.</span><span class="sxs-lookup"><span data-stu-id="b8986-110">Bind the socket.</span></span>
4.  <span data-ttu-id="b8986-111">Ouça o soquete de um cliente.</span><span class="sxs-lookup"><span data-stu-id="b8986-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="b8986-112">Aceitar uma conexão de um cliente.</span><span class="sxs-lookup"><span data-stu-id="b8986-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="b8986-113">Receber e enviar dados.</span><span class="sxs-lookup"><span data-stu-id="b8986-113">Receive and send data.</span></span>
7.  <span data-ttu-id="b8986-114">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="b8986-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="b8986-115">Cliente</span><span class="sxs-lookup"><span data-stu-id="b8986-115">Client</span></span>

1.  <span data-ttu-id="b8986-116">Inicialize o Winsock.</span><span class="sxs-lookup"><span data-stu-id="b8986-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="b8986-117">Crie um soquete.</span><span class="sxs-lookup"><span data-stu-id="b8986-117">Create a socket.</span></span>
3.  <span data-ttu-id="b8986-118">Conecte-se ao servidor.</span><span class="sxs-lookup"><span data-stu-id="b8986-118">Connect to the server.</span></span>
4.  <span data-ttu-id="b8986-119">Enviar e receber dados.</span><span class="sxs-lookup"><span data-stu-id="b8986-119">Send and receive data.</span></span>
5.  <span data-ttu-id="b8986-120">Desconectar.</span><span class="sxs-lookup"><span data-stu-id="b8986-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="b8986-121">Algumas das etapas são as mesmas para um cliente e um servidor.</span><span class="sxs-lookup"><span data-stu-id="b8986-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="b8986-122">Essas etapas são implementadas quase exatamente da mesma forma.</span><span class="sxs-lookup"><span data-stu-id="b8986-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="b8986-123">Algumas das etapas neste guia serão específicas para o tipo de aplicativo que está sendo criado.</span><span class="sxs-lookup"><span data-stu-id="b8986-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="b8986-124">Primeira etapa: [criando um aplicativo Winsock básico](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="b8986-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b8986-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8986-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8986-126">Introdução com o Winsock</span><span class="sxs-lookup"><span data-stu-id="b8986-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



