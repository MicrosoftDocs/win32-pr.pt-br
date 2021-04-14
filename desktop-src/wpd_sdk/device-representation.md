---
description: Representação do dispositivo
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: Representação do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461064"
---
# <a name="device-representation"></a><span data-ttu-id="02e8e-103">Representação do dispositivo</span><span class="sxs-lookup"><span data-stu-id="02e8e-103">Device Representation</span></span>

<span data-ttu-id="02e8e-104">Os dispositivos têm dois comportamentos principais que são abordados pela arquitetura de dispositivos portáteis do Windows (WPD):</span><span class="sxs-lookup"><span data-stu-id="02e8e-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="02e8e-105">Acessando e armazenando conteúdo.</span><span class="sxs-lookup"><span data-stu-id="02e8e-105">Accessing and storing content.</span></span> <span data-ttu-id="02e8e-106">Por exemplo, os aplicativos devem ser capazes de adicionar arquivos de música a um player portátil de música.</span><span class="sxs-lookup"><span data-stu-id="02e8e-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="02e8e-107">Programando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02e8e-107">Programming the device.</span></span> <span data-ttu-id="02e8e-108">Isso inclui operações simples, como alteração de configurações e preparação do dispositivo para captura de dados, ou operações mais complexas, como carregar o firmware.</span><span class="sxs-lookup"><span data-stu-id="02e8e-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="02e8e-109">Os exemplos incluem a emissão de um comando "pegar imagem" para uma câmera digital ainda.</span><span class="sxs-lookup"><span data-stu-id="02e8e-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="02e8e-110">Em WPD, esses comportamentos são descritos pela representação do dispositivo como uma hierarquia de objetos.</span><span class="sxs-lookup"><span data-stu-id="02e8e-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="02e8e-111">A ilustração a seguir mostra uma representação de objeto WPD para um dispositivo de várias funções, que nesse caso é um telefone celular.</span><span class="sxs-lookup"><span data-stu-id="02e8e-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![ilustração mostrando a hierarquia de objetos para um telefone celular](images/wpd-overview-figure3.gif)

<span data-ttu-id="02e8e-113">Essa hierarquia ilustra a funcionalidade e o conteúdo a seguir.</span><span class="sxs-lookup"><span data-stu-id="02e8e-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="02e8e-114">Função</span><span class="sxs-lookup"><span data-stu-id="02e8e-114">Functionality:</span></span>

-   <span data-ttu-id="02e8e-115">Objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="02e8e-115">Storage object.</span></span> <span data-ttu-id="02e8e-116">Este dispositivo tem armazenamento de dados.</span><span class="sxs-lookup"><span data-stu-id="02e8e-116">This device has data storage.</span></span>
-   <span data-ttu-id="02e8e-117">Serviço de contatos.</span><span class="sxs-lookup"><span data-stu-id="02e8e-117">Contacts Service.</span></span> <span data-ttu-id="02e8e-118">Esse serviço é um objeto funcional que pode ser usado para sincronizar e armazenar contatos no telefone.</span><span class="sxs-lookup"><span data-stu-id="02e8e-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="02e8e-119">Serviço SMS.</span><span class="sxs-lookup"><span data-stu-id="02e8e-119">SMS Service.</span></span> <span data-ttu-id="02e8e-120">Esse serviço é um objeto funcional que pode ser usado para enviar, receber e armazenar mensagens SMS.</span><span class="sxs-lookup"><span data-stu-id="02e8e-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="02e8e-121">Conteúdo:</span><span class="sxs-lookup"><span data-stu-id="02e8e-121">Contents:</span></span>

-   <span data-ttu-id="02e8e-122">Objetos de mídia.</span><span class="sxs-lookup"><span data-stu-id="02e8e-122">Media objects.</span></span> <span data-ttu-id="02e8e-123">Este dispositivo armazena imagens, música e arquivos de vídeo em pastas no objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="02e8e-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="02e8e-124">Embora os arquivos mostrados na ilustração sejam armazenados em uma pasta, um dispositivo pode subdividir o conteúdo em pastas organizadas pelo tipo de mídia armazenada; por exemplo, pastas de imagens, pastas de música e pastas de vídeo.</span><span class="sxs-lookup"><span data-stu-id="02e8e-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="02e8e-125">Objetos de contato.</span><span class="sxs-lookup"><span data-stu-id="02e8e-125">Contact objects.</span></span> <span data-ttu-id="02e8e-126">Este dispositivo armazena informações de contato (como nome, número de telefone e endereço) como filhos do serviço de contatos</span><span class="sxs-lookup"><span data-stu-id="02e8e-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="02e8e-127">Objetos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="02e8e-127">Message objects.</span></span> <span data-ttu-id="02e8e-128">Esse dispositivo armazena mensagens SMS como filhos do serviço SMS.</span><span class="sxs-lookup"><span data-stu-id="02e8e-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02e8e-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02e8e-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02e8e-130">**Visão geral do aplicativo**</span><span class="sxs-lookup"><span data-stu-id="02e8e-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



