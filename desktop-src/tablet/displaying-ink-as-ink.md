---
description: O comportamento padrão para o controle InkEdit é reconhecer e converter a tinta em texto depois que um tempo limite curto expirar.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Exibindo tinta como tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770590"
---
# <a name="displaying-ink-as-ink"></a><span data-ttu-id="e68cb-103">Exibindo tinta como tinta</span><span class="sxs-lookup"><span data-stu-id="e68cb-103">Displaying Ink as Ink</span></span>

<span data-ttu-id="e68cb-104">O comportamento padrão para o controle [InkEdit](inkedit-control-reference.md) é reconhecer e converter a tinta em texto depois que um tempo limite curto expirar.</span><span class="sxs-lookup"><span data-stu-id="e68cb-104">The default behavior for the [InkEdit](inkedit-control-reference.md) control is to recognize and convert ink into text after a brief timeout has expired.</span></span> <span data-ttu-id="e68cb-105">Como o controle é uma superclasse de [RichEdit](../controls/rich-edit-controls.md), também é possível inserir e exibir tinta dentro do controle.</span><span class="sxs-lookup"><span data-stu-id="e68cb-105">Because the control is a superclass of [RichEdit](../controls/rich-edit-controls.md), it is also possible to embed and display ink within the control.</span></span> <span data-ttu-id="e68cb-106">Cada palavra é inserida no controle como um objeto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="e68cb-106">Each word is inserted into the control as an [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="e68cb-107">O objeto **InkDisp** contém a tinta e suas alternativas de reconhecimento.</span><span class="sxs-lookup"><span data-stu-id="e68cb-107">The **InkDisp** object contains the ink and its recognition alternates.</span></span>

<span data-ttu-id="e68cb-108">Quando inserido, a tinta é dimensionada para o tamanho da fonte atual e outras propriedades de ambiente, como itálico ou negrito, são aplicadas.</span><span class="sxs-lookup"><span data-stu-id="e68cb-108">When inserted, the ink is scaled to the current font size and other ambient properties, such as italics or bold, are applied.</span></span> <span data-ttu-id="e68cb-109">Se o usuário optar por editar o texto de um objeto [**InkDisp**](inkdisp-class.md) , ele deverá primeiro converter a tinta em texto.</span><span class="sxs-lookup"><span data-stu-id="e68cb-109">If the user chooses to edit the text of an [**InkDisp**](inkdisp-class.md) object, he or she must first convert the ink to text.</span></span>

> [!Note]  
> <span data-ttu-id="e68cb-110">Todos os dados alternativos de reconhecimento e tinta são perdidos durante a conversão.</span><span class="sxs-lookup"><span data-stu-id="e68cb-110">All ink and recognition alternate data is lost during the conversion.</span></span>

 

<span data-ttu-id="e68cb-111">Esse recurso está disponível somente em computadores que executam o Microsoft Windows XP Tablet PC Edition, Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="e68cb-111">This feature is available only on computers that run Microsoft Windows XP Tablet PC Edition, Windows Vista, or later.</span></span>

 

 
