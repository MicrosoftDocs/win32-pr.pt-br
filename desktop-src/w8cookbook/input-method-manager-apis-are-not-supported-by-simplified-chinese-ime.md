---
title: As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado
description: As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado
ms.assetid: 829E1920-8A5C-4DBB-A844-72DA75D58B92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d01d79d569ee7c72508bc217b68bcdf784f0d61
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084674"
---
# <a name="input-method-manager-apis-are-not-supported-by-simplified-chinese-ime"></a><span data-ttu-id="22747-103">As APIs do Gerenciador de métodos de entrada não são suportadas pelo IME do chinês simplificado</span><span class="sxs-lookup"><span data-stu-id="22747-103">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>

## <a name="platforms"></a><span data-ttu-id="22747-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="22747-104">Platforms</span></span>

<dl> <span data-ttu-id="22747-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="22747-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="22747-106">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="22747-106">Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="22747-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="22747-107">Description</span></span>

<span data-ttu-id="22747-108">As seguintes APIs do Gerenciador de métodos de entrada não são suportadas por IMEs do chinês simplificado no Windows 8.1:</span><span class="sxs-lookup"><span data-stu-id="22747-108">The following input method manager APIs are not supported by Simplified Chinese IMEs in Windows 8.1:</span></span>

-   <span data-ttu-id="22747-109">Interface IFECommon</span><span class="sxs-lookup"><span data-stu-id="22747-109">IFECommon interface</span></span>
-   <span data-ttu-id="22747-110">Interface IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="22747-110">IFEDictionary interface</span></span>
-   <span data-ttu-id="22747-111">Interface IFELanguage</span><span class="sxs-lookup"><span data-stu-id="22747-111">IFELanguage interface</span></span>
-   <span data-ttu-id="22747-112">Interface IImePad</span><span class="sxs-lookup"><span data-stu-id="22747-112">IImePad interface</span></span>
-   <span data-ttu-id="22747-113">Interface IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="22747-113">IImePadApplet interface</span></span>
-   <span data-ttu-id="22747-114">Interface IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="22747-114">IImeSpecifyApplets interface</span></span>

## <a name="manifestations"></a><span data-ttu-id="22747-115">Manifestações</span><span class="sxs-lookup"><span data-stu-id="22747-115">Manifestations</span></span>

<span data-ttu-id="22747-116">As funções que usam essas APIs não funcionam com o IME do chinês simplificado.</span><span class="sxs-lookup"><span data-stu-id="22747-116">The functions that use those APIs don’t work with Simplified Chinese IME.</span></span>

## <a name="solution"></a><span data-ttu-id="22747-117">Solução</span><span class="sxs-lookup"><span data-stu-id="22747-117">Solution</span></span>

<span data-ttu-id="22747-118">Os aplicativos devem ser projetados para que os usuários possam concluir a tarefa desejada sem usar a API especificada.</span><span class="sxs-lookup"><span data-stu-id="22747-118">Applications must be designed so that users can complete the desired task without using the specified API.</span></span>

## <a name="resources"></a><span data-ttu-id="22747-119">Recursos</span><span class="sxs-lookup"><span data-stu-id="22747-119">Resources</span></span>

-   [<span data-ttu-id="22747-120">Interfaces do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="22747-120">Input Method Manager Interfaces</span></span>](../intl/input-method-manager-interfaces.md)
-   [<span data-ttu-id="22747-121">IFECommon</span><span class="sxs-lookup"><span data-stu-id="22747-121">IFECommon</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="22747-122">Interface IFECommon</span><span class="sxs-lookup"><span data-stu-id="22747-122">IFECommon interface</span></span>](/windows/win32/api/msime/nn-msime-ifecommon)
-   [<span data-ttu-id="22747-123">Interface IFEDictionary</span><span class="sxs-lookup"><span data-stu-id="22747-123">IFEDictionary interface</span></span>](/windows/win32/api/msime/nn-msime-ifedictionary)
-   [<span data-ttu-id="22747-124">IFELanguage</span><span class="sxs-lookup"><span data-stu-id="22747-124">IFELanguage</span></span>](/windows/win32/api/msime/nn-msime-ifelanguage)
-   [<span data-ttu-id="22747-125">IImePad</span><span class="sxs-lookup"><span data-stu-id="22747-125">IImePad</span></span>](/windows/win32/api/imepad/nn-imepad-iimepad)
-   [<span data-ttu-id="22747-126">IImePadApplet</span><span class="sxs-lookup"><span data-stu-id="22747-126">IImePadApplet</span></span>](/windows/win32/api/imepad/nn-imepad-iimepadapplet)
-   [<span data-ttu-id="22747-127">IimePlugInDictDictionaryList</span><span class="sxs-lookup"><span data-stu-id="22747-127">IimePlugInDictDictionaryList</span></span>](/windows/win32/api/msimeapi/nn-msimeapi-iimeplugindictdictionarylist)
-   [<span data-ttu-id="22747-128">IImeSpecifyApplets</span><span class="sxs-lookup"><span data-stu-id="22747-128">IImeSpecifyApplets</span></span>](/windows/win32/api/imepad/nn-imepad-iimespecifyapplets)

 

 