---
title: Criando controles comuns
description: Este tópico descreve como criar uma janela que pertence a uma classe de janela definida na biblioteca de controle comum, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917788"
---
# <a name="creating-common-controls"></a><span data-ttu-id="f1605-103">Criando controles comuns</span><span class="sxs-lookup"><span data-stu-id="f1605-103">Creating Common Controls</span></span>

<span data-ttu-id="f1605-104">Este tópico descreve como criar uma janela que pertence a uma classe de janela definida na biblioteca de controle comum, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="f1605-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="f1605-105">Os controles mais comuns pertencem a uma classe de janela definida na DLL de controle comum.</span><span class="sxs-lookup"><span data-stu-id="f1605-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="f1605-106">A classe Window e o procedimento de janela correspondente definem as propriedades, a aparência e o comportamento do controle.</span><span class="sxs-lookup"><span data-stu-id="f1605-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="f1605-107">Para garantir que a DLL de controle comum seja carregada, inclua a função [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f1605-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="f1605-108">Você cria um controle comum especificando o nome da classe de janela ao chamar a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou especificando o nome de classe apropriado em um modelo de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="f1605-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="f1605-109">Cada tipo de controle comum tem um conjunto de estilos de controle que você pode usar para variar a aparência e o comportamento do controle.</span><span class="sxs-lookup"><span data-stu-id="f1605-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="f1605-110">A biblioteca de controle comum também inclui um conjunto de estilos de controle que se aplicam a dois ou mais tipos de controles comuns.</span><span class="sxs-lookup"><span data-stu-id="f1605-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="f1605-111">Os estilos de controle comuns são descritos na seção [estilos](common-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="f1605-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f1605-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f1605-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f1605-113">Sobre controles comuns</span><span class="sxs-lookup"><span data-stu-id="f1605-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 