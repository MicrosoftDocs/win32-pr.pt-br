---
description: Esta seção descreve as interfaces do IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Interfaces do Gerenciador de métodos de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759661"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="ce2ba-103">Interfaces do Gerenciador de métodos de entrada</span><span class="sxs-lookup"><span data-stu-id="ce2ba-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="ce2ba-104">Esta seção descreve as interfaces do IMM.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="ce2ba-105">Interface</span><span class="sxs-lookup"><span data-stu-id="ce2ba-105">Interface</span></span>                                                            | <span data-ttu-id="ce2ba-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce2ba-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce2ba-107">**IFECommon**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="ce2ba-108">Fornece serviços relacionados ao IME que são comuns para diferentes idiomas.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="ce2ba-109">**IFEDictionary**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="ce2ba-110">Permite que os clientes acessem um dicionário de usuário do Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="ce2ba-111">**IFELanguage**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="ce2ba-112">Fornece serviços de processamento de idioma usando o Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="ce2ba-113">**IImePad**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="ce2ba-114">Insere texto em aplicativos do IMEPadApplets que implementam a interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="ce2ba-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="ce2ba-115">**IImePadApplet**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="ce2ba-116">Insere cadeias de caracteres em aplicativos por meio da interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .</span><span class="sxs-lookup"><span data-stu-id="ce2ba-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="ce2ba-117">**IImePlugInDictDictionaryList**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="ce2ba-118">Fornece acesso à lista de dicionários de plug-ins do IME.</span><span class="sxs-lookup"><span data-stu-id="ce2ba-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="ce2ba-119">**IImeSpecifyApplets**</span><span class="sxs-lookup"><span data-stu-id="ce2ba-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="ce2ba-120">Especifica os métodos chamados do objeto de interface [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) para emular a interface [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="ce2ba-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 



