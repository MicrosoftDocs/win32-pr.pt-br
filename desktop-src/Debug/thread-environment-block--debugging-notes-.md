---
description: Bloco de ambiente de thread (observações de depuração)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloco de ambiente de thread (observações de depuração)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e9397c2d442b09b308c4886c2672e3be58b661c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550581"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="83c75-103">Bloco de ambiente de thread (observações de depuração)</span><span class="sxs-lookup"><span data-stu-id="83c75-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="83c75-104">O bloco de ambiente de thread ([**estrutura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contém informações de contexto para um thread.</span><span class="sxs-lookup"><span data-stu-id="83c75-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="83c75-105">Nas versões a seguir do Windows, o deslocamento do endereço TEB de 32 bits dentro do TEB de 64 bits é 0.</span><span class="sxs-lookup"><span data-stu-id="83c75-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="83c75-106">Isso pode ser usado para acessar diretamente o TEB de 32 bits de um thread do WOW64.</span><span class="sxs-lookup"><span data-stu-id="83c75-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="83c75-107">Isso pode ser alterado em versões posteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="83c75-107">This might change in later versions of Windows</span></span>



|  <span data-ttu-id="83c75-108">Plataforma</span><span class="sxs-lookup"><span data-stu-id="83c75-108">Platform</span></span>     | <span data-ttu-id="83c75-109">Versão</span><span class="sxs-lookup"><span data-stu-id="83c75-109">Version</span></span>                |
|---------------|------------------------|
| <span data-ttu-id="83c75-110">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="83c75-110">Windows Vista</span></span> | <span data-ttu-id="83c75-111">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83c75-111">Windows Server 2008</span></span>    |
| <span data-ttu-id="83c75-112">Windows 7</span><span class="sxs-lookup"><span data-stu-id="83c75-112">Windows 7</span></span>     | <span data-ttu-id="83c75-113">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="83c75-113">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="83c75-114">Windows 8</span><span class="sxs-lookup"><span data-stu-id="83c75-114">Windows 8</span></span>     | <span data-ttu-id="83c75-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="83c75-115">Windows Server 2012</span></span>    |
| <span data-ttu-id="83c75-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="83c75-116">Windows 8.1</span></span>   | <span data-ttu-id="83c75-117">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="83c75-117">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="83c75-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="83c75-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83c75-119">Estruturas de depuração</span><span class="sxs-lookup"><span data-stu-id="83c75-119">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="83c75-120">**Contexto do WOW64 \_**</span><span class="sxs-lookup"><span data-stu-id="83c75-120">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
