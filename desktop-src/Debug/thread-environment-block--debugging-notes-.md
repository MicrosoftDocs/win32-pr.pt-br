---
description: Bloco de ambiente de thread (observações de depuração)
ms.assetid: 5040CB82-D32F-4C44-8C03-30238D5B897A
title: Bloco de ambiente de thread (observações de depuração)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d66b04b522bed8bdf7f5a5571c300019e4537b5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826401"
---
# <a name="thread-environment-block-debugging-notes"></a><span data-ttu-id="85e0c-103">Bloco de ambiente de thread (observações de depuração)</span><span class="sxs-lookup"><span data-stu-id="85e0c-103">Thread Environment Block (Debugging Notes)</span></span>

<span data-ttu-id="85e0c-104">O bloco de ambiente de thread ([**estrutura TEB**](/windows/win32/api/winternl/ns-winternl-teb)) contém informações de contexto para um thread.</span><span class="sxs-lookup"><span data-stu-id="85e0c-104">The Thread Environment Block ([**TEB structure**](/windows/win32/api/winternl/ns-winternl-teb)) holds context information for a thread.</span></span>

<span data-ttu-id="85e0c-105">Nas versões a seguir do Windows, o deslocamento do endereço TEB de 32 bits dentro do TEB de 64 bits é 0.</span><span class="sxs-lookup"><span data-stu-id="85e0c-105">In the following versions of Windows, the offset of the 32-bit TEB address within the 64-bit TEB is 0.</span></span> <span data-ttu-id="85e0c-106">Isso pode ser usado para acessar diretamente o TEB de 32 bits de um thread do WOW64.</span><span class="sxs-lookup"><span data-stu-id="85e0c-106">This can be used to directly access the 32-bit TEB of a WOW64 thread.</span></span> <span data-ttu-id="85e0c-107">Isso pode ser alterado em versões posteriores do Windows</span><span class="sxs-lookup"><span data-stu-id="85e0c-107">This might change in later versions of Windows</span></span>



|               |                        |
|---------------|------------------------|
| <span data-ttu-id="85e0c-108">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="85e0c-108">Windows Vista</span></span> | <span data-ttu-id="85e0c-109">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="85e0c-109">Windows Server 2008</span></span>    |
| <span data-ttu-id="85e0c-110">Windows 7</span><span class="sxs-lookup"><span data-stu-id="85e0c-110">Windows 7</span></span>     | <span data-ttu-id="85e0c-111">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="85e0c-111">Windows Server 2008 R2</span></span> |
| <span data-ttu-id="85e0c-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="85e0c-112">Windows 8</span></span>     | <span data-ttu-id="85e0c-113">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="85e0c-113">Windows Server 2012</span></span>    |
| <span data-ttu-id="85e0c-114">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="85e0c-114">Windows 8.1</span></span>   | <span data-ttu-id="85e0c-115">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="85e0c-115">Windows Server 2012 R2</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="85e0c-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85e0c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e0c-117">Estruturas de depuração</span><span class="sxs-lookup"><span data-stu-id="85e0c-117">Debugging Structures</span></span>](debugging-structures.md)
</dt> <dt>

[<span data-ttu-id="85e0c-118">**Contexto do WOW64 \_**</span><span class="sxs-lookup"><span data-stu-id="85e0c-118">**WOW64\_CONTEXT**</span></span>](/windows/desktop/api/WinNT/ns-winnt-wow64_context)
</dt> </dl>

 

 
