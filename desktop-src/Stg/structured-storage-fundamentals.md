---
title: Conceitos básicos de armazenamento estruturado
description: O armazenamento estruturado fornece o equivalente a um sistema de arquivos completo para armazenar objetos.
ms.assetid: 7e2d6211-2ea0-4cad-9388-c789b12446ab
keywords:
- Strctd de armazenamento estruturado STG, conceitos básicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d93b74afd620edca5b6beaa43bde6fff43d7263
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823829"
---
# <a name="structured-storage-fundamentals"></a><span data-ttu-id="133b7-104">Conceitos básicos de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="133b7-104">Structured Storage Fundamentals</span></span>

<span data-ttu-id="133b7-105">O armazenamento estruturado fornece o equivalente a um sistema de arquivos completo para armazenar objetos por meio dos elementos listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="133b7-105">Structured Storage provides the equivalent of a complete file system for storing objects through the elements listed in the following table.</span></span>



| <span data-ttu-id="133b7-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="133b7-106">Element</span></span>                                                                  | <span data-ttu-id="133b7-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="133b7-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="133b7-108">Interfaces de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="133b7-108">Structured Storage Interfaces</span></span>](structured-storage-interfaces.md)       | <span data-ttu-id="133b7-109">As interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)e [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) , juntamente com um conjunto de interfaces relacionadas —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)e [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="133b7-109">The [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage), [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream), [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes), and [**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage) interfaces, along with a set of related interfaces —[**IPersistStorage**](/windows/win32/api/objidl/nn-objidl-ipersiststorage), [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile), and [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> |
| [<span data-ttu-id="133b7-110">Funções de API de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="133b7-110">Structured Storage API Functions</span></span>](structured-storage-api-functions.md) | <span data-ttu-id="133b7-111">APIs auxiliares que facilitam uma implementação de armazenamento estruturado, bem como um segundo conjunto de APIs para arquivos compostos; Essa é a implementação COM das interfaces de armazenamento estruturado.</span><span class="sxs-lookup"><span data-stu-id="133b7-111">Helper APIs that facilitate an implementation of structured storage, as well as a second set of APIs for compound files; that is the COM implementation of the structured storage interfaces.</span></span> <span data-ttu-id="133b7-112">COM também fornece um conjunto de estruturas de suporte e valores de enumeração usados para organizar parâmetros para métodos de interface e APIs.</span><span class="sxs-lookup"><span data-stu-id="133b7-112">COM also provides a set of supporting structures and enumeration values used to organize parameters for interface methods and APIs.</span></span>                              |
| [<span data-ttu-id="133b7-113">Modos de acesso de armazenamento estruturado</span><span class="sxs-lookup"><span data-stu-id="133b7-113">Structured Storage Access Modes</span></span>](structured-storage-access-modes.md)   | <span data-ttu-id="133b7-114">Um conjunto de modos de acesso para controlar o acesso a arquivos compostos.</span><span class="sxs-lookup"><span data-stu-id="133b7-114">A set of access modes for regulating access to compound files.</span></span>                                                                                                                                                                                                                                                                                                 |



 

 

 