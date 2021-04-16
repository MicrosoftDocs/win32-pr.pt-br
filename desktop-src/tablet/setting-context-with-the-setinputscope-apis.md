---
description: A técnica de programação recomendada para configurar contextos em um aplicativo que não está habilitado para tinta é usar as funções SetInputScope para associar o contexto aos campos no aplicativo.
ms.assetid: 95b93804-8079-4b97-b1b0-dfc0138c94e8
title: Configurando o contexto com as APIs SetInputScope
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74c1b507b1719bea8c04288dca9214ad5675f8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787013"
---
# <a name="setting-context-with-the-setinputscope-apis"></a><span data-ttu-id="7459f-103">Configurando o contexto com as APIs SetInputScope</span><span class="sxs-lookup"><span data-stu-id="7459f-103">Setting Context with the SetInputScope APIs</span></span>

<span data-ttu-id="7459f-104">A técnica de programação recomendada para configurar contextos em um aplicativo que não está habilitado para tinta é usar as funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) para associar o contexto aos campos no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7459f-104">The recommended programmatic technique for setting contexts in an application that is not ink enabled is to use the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions to associate context with the fields in the application.</span></span>

<span data-ttu-id="7459f-105">O Microsoft Windows XP Tablet PC Edition Development Kit 1,7 foi a primeira versão do Microsoft Windows a oferecer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="7459f-105">The Microsoft Windows XP Tablet PC Edition Development Kit 1.7 was the first version of Microsoft Windows to offer [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span> <span data-ttu-id="7459f-106">O Windows Vista também fornece suporte para essas funções.</span><span class="sxs-lookup"><span data-stu-id="7459f-106">Windows Vista also provides support for these functions.</span></span> <span data-ttu-id="7459f-107">As definições de **SetInputScope** são declaradas em InputScope. idl e InputScope. h.</span><span class="sxs-lookup"><span data-stu-id="7459f-107">The **SetInputScope** definitions are declared in InputScope.idl and InputScope.h.</span></span> <span data-ttu-id="7459f-108">Para obter mais detalhes, consulte [estrutura de serviços de texto](../tsf/text-services-framework.md).</span><span class="sxs-lookup"><span data-stu-id="7459f-108">For more details, see [Text Services Framework](../tsf/text-services-framework.md).</span></span>

<span data-ttu-id="7459f-109">As funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) são a maneira recomendada de definir o contexto para controles e aplicativos que não são habilitados para tinta.</span><span class="sxs-lookup"><span data-stu-id="7459f-109">The [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions are the recommended way to set context for controls and applications that are not ink enabled.</span></span>

## <a name="common-input-scopes"></a><span data-ttu-id="7459f-110">Escopos de entrada comuns</span><span class="sxs-lookup"><span data-stu-id="7459f-110">Common Input Scopes</span></span>

<span data-ttu-id="7459f-111">Usando as funções [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) e o conjunto definido de escopos de entrada comuns descritos na enumeração [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) , você pode melhorar a precisão de reconhecimento dos reconhecedores de manuscrito da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7459f-111">Using the [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope) functions and the defined set of common input scopes described in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration, you can improve the recognition accuracy of the Microsoft handwriting recognizers.</span></span>

> [!Note]  
> <span data-ttu-id="7459f-112">Os reconhecedores para inglês (Estados Unidos), inglês (Reino Unido), alemão, francês, italiano, espanhol, holandês e Português atualmente dão suporte ao uso de escopos de entrada comuns com [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span><span class="sxs-lookup"><span data-stu-id="7459f-112">The recognizers for English (United States), English (United Kingdom), German, French, Italian, Spanish, Dutch, and Portuguese currently support using the common input scopes with [**SetInputScope**](/windows/win32/api/inputscope/nf-inputscope-setinputscope).</span></span>

 

 

 
