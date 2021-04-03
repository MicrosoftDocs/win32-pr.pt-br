---
title: Novo recurso de histórico de arquivo
description: Novo recurso de histórico de arquivo
ms.assetid: B1EE4638-5591-483B-AA09-600E242ED50B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a70aad84f4d052d6a872c7b0cfc979d0fa05cb84
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/01/2020
ms.locfileid: "104084958"
---
# <a name="new-file-history-feature"></a><span data-ttu-id="ca60e-103">Novo recurso de histórico de arquivo</span><span class="sxs-lookup"><span data-stu-id="ca60e-103">New File History feature</span></span>

## <a name="platform"></a><span data-ttu-id="ca60e-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="ca60e-104">Platform</span></span>

<span data-ttu-id="ca60e-105">**Clientes** – Windows 8</span><span class="sxs-lookup"><span data-stu-id="ca60e-105">**Clients** – Windows 8</span></span> 


## <a name="description"></a><span data-ttu-id="ca60e-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca60e-106">Description</span></span>

<span data-ttu-id="ca60e-107">O novo recurso de histórico de arquivo substitui a função de backup e restauração existente e oferece proteção para arquivos de usuário armazenados em bibliotecas de usuário.</span><span class="sxs-lookup"><span data-stu-id="ca60e-107">The new File History feature replaces the existing Backup and Restore function, and offers protection for user files stored in user libraries.</span></span> <span data-ttu-id="ca60e-108">É fornecido um conjunto de APIs que permite aos desenvolvedores habilitar programaticamente o histórico de arquivos e selecionar um destino de armazenamento específico.</span><span class="sxs-lookup"><span data-stu-id="ca60e-108">A set of APIs is provided that allows developers to programmatically enable File History and select a specific storage target.</span></span> <span data-ttu-id="ca60e-109">A documentação para essas APIs está disponível no MSDN.</span><span class="sxs-lookup"><span data-stu-id="ca60e-109">Documentation for these APIs is available on MSDN.</span></span>

<span data-ttu-id="ca60e-110">Ele pode afetar os fluxos de trabalho relacionados à proteção e à documentação dos dados que dependem do recurso de backup e restauração do Windows.</span><span class="sxs-lookup"><span data-stu-id="ca60e-110">It may affect workflows related to data protection and documentation that depend on the Windows Backup and Restore feature.</span></span>

<span data-ttu-id="ca60e-111">Não recomendamos o uso de ambos os recursos ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="ca60e-111">We do not recommend using both features at the same time.</span></span> <span data-ttu-id="ca60e-112">O histórico de arquivos verifica se um agendamento de backup existe e se está ativo e se encontra um, ele não permitirá que os usuários o ativem.</span><span class="sxs-lookup"><span data-stu-id="ca60e-112">File History checks if a Backup schedule exists and is active and if it finds one, it will not let users to turn it on.</span></span> <span data-ttu-id="ca60e-113">Nesse caso, os usuários que desejarem usar o histórico de arquivos precisarão excluir o agendamento de backup do Windows.</span><span class="sxs-lookup"><span data-stu-id="ca60e-113">In this case, users who want to use File History will have to delete the Windows Backup schedule.</span></span>

## <a name="manifestation"></a><span data-ttu-id="ca60e-114">Manifestação</span><span class="sxs-lookup"><span data-stu-id="ca60e-114">Manifestation</span></span>

<span data-ttu-id="ca60e-115">Os fluxos de trabalho podem ser interrompidos e a documentação do método anterior para acessar o recurso de backup e restauração do Windows precisará ser atualizada para refletir essas alterações.</span><span class="sxs-lookup"><span data-stu-id="ca60e-115">Workflows may be interrupted and documentation for the previous method for accessing the Windows Backup and Restore feature will need to be updated to reflect these changes.</span></span>

## <a name="solution"></a><span data-ttu-id="ca60e-116">Solução</span><span class="sxs-lookup"><span data-stu-id="ca60e-116">Solution</span></span>

<span data-ttu-id="ca60e-117">Revisar aplicativos que contêm fluxos de trabalho que são afetados negativamente pelo novo recurso de histórico de arquivo para remover conflitos e incorporar o novo conjunto de APIs.</span><span class="sxs-lookup"><span data-stu-id="ca60e-117">Revise apps that contain workflows that are adversely impacted by the new File History feature to remove any conflicts and incorporate the new set of APIs.</span></span>

## <a name="tests"></a><span data-ttu-id="ca60e-118">Testes</span><span class="sxs-lookup"><span data-stu-id="ca60e-118">Tests</span></span>

<span data-ttu-id="ca60e-119">A API permite que os desenvolvedores determinem se o histórico de arquivos está ativado.</span><span class="sxs-lookup"><span data-stu-id="ca60e-119">The API allows developers to determine if File History is turned on.</span></span>

 

 




