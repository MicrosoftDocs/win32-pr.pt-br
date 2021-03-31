---
title: Árvores de domínio
description: Uma árvore de domínio é composta por vários domínios que compartilham um esquema e uma configuração comuns, formando um namespace contíguo.
ms.assetid: 3deb4053-3124-4180-8ab0-35fff689a37e
ms.tgt_platform: multiple
keywords:
- Active Directory de árvore de domínio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21d2b36968615fd4e92912fdd94246ef8dda0c1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159332"
---
# <a name="domain-trees"></a><span data-ttu-id="23492-104">Árvores de domínio</span><span class="sxs-lookup"><span data-stu-id="23492-104">Domain Trees</span></span>

<span data-ttu-id="23492-105">Uma *árvore de domínio* é composta por vários domínios que compartilham um esquema e uma configuração comuns, formando um namespace contíguo.</span><span class="sxs-lookup"><span data-stu-id="23492-105">A *domain tree* is made up of several domains that share a common schema and configuration, forming a contiguous namespace.</span></span> <span data-ttu-id="23492-106">Os domínios em uma árvore também são vinculados por relações de confiança.</span><span class="sxs-lookup"><span data-stu-id="23492-106">Domains in a tree are also linked together by trust relationships.</span></span> <span data-ttu-id="23492-107">Active Directory é um conjunto de uma ou mais árvores.</span><span class="sxs-lookup"><span data-stu-id="23492-107">Active Directory is a set of one or more trees.</span></span>

<span data-ttu-id="23492-108">As árvores podem ser exibidas de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="23492-108">Trees can be viewed two ways.</span></span> <span data-ttu-id="23492-109">Uma exibição é a relação de confiança entre domínios.</span><span class="sxs-lookup"><span data-stu-id="23492-109">One view is the trust relationships between domains.</span></span> <span data-ttu-id="23492-110">A outra exibição é o namespace da árvore de domínio.</span><span class="sxs-lookup"><span data-stu-id="23492-110">The other view is the namespace of the domain tree.</span></span>

## <a name="viewing-trust-relationships"></a><span data-ttu-id="23492-111">Exibindo relações de confiança</span><span class="sxs-lookup"><span data-stu-id="23492-111">Viewing Trust Relationships</span></span>

<span data-ttu-id="23492-112">Você pode desenhar um diagrama de uma árvore de domínio com base nos domínios individuais e na relação de confiança existente.</span><span class="sxs-lookup"><span data-stu-id="23492-112">You can draw a diagram of a domain tree based on the individual domains and the existing trust relationship.</span></span>

<span data-ttu-id="23492-113">O Windows 2000 estabelece relações de confiança entre domínios com base no protocolo de segurança Kerberos.</span><span class="sxs-lookup"><span data-stu-id="23492-113">Windows 2000 establishes trust relationships between domains based on the Kerberos security protocol.</span></span> <span data-ttu-id="23492-114">A confiança Kerberos é transitiva e hierárquica – se o domínio A confiar no domínio B e o domínio B confiar no domínio C, o domínio A confiará no domínio C.</span><span class="sxs-lookup"><span data-stu-id="23492-114">Kerberos trust is transitive and hierarchical—if domain A trusts domain B, and domain B trusts domain C, then domain A trusts domain C.</span></span>

![relação de confiança da árvore de domínio](images/domain-trust.png)

## <a name="viewing-the-namespace"></a><span data-ttu-id="23492-116">Exibindo o namespace</span><span class="sxs-lookup"><span data-stu-id="23492-116">Viewing the Namespace</span></span>

<span data-ttu-id="23492-117">Você também pode desenhar um diagrama de uma árvore de domínio com base no namespace.</span><span class="sxs-lookup"><span data-stu-id="23492-117">You can also draw a diagram of a domain tree based on the namespace.</span></span> <span data-ttu-id="23492-118">Você pode determinar o nome distinto de um objeto seguindo o caminho para cima na hierarquia do namespace da árvore de domínio.</span><span class="sxs-lookup"><span data-stu-id="23492-118">You can determine an object's distinguished name by following the path up the hierarchy of the domain tree namespace.</span></span> <span data-ttu-id="23492-119">Essa exibição é útil para agrupar objetos em uma hierarquia lógica.</span><span class="sxs-lookup"><span data-stu-id="23492-119">This view is useful for grouping objects into a logical hierarchy.</span></span> <span data-ttu-id="23492-120">A principal vantagem de um namespace contíguo é que uma pesquisa profunda da raiz do namespace pesquisa toda a hierarquia.</span><span class="sxs-lookup"><span data-stu-id="23492-120">The chief advantage of a contiguous namespace is that a deep search from the root of the namespace searches the entire hierarchy.</span></span>

![árvore de domínio de namespace](images/namespace.png)

 

 




