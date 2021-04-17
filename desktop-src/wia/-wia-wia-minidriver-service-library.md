---
description: Para simplificar a implementação do driver o máximo possível, o WIA (aquisição de imagem do Windows) fornece uma biblioteca de serviço minidriver que executa muitas das tarefas administrativas exigidas pela arquitetura WIA.
ms.assetid: 074a53a3-20b0-4b25-991d-5d48f75c5d75
title: Biblioteca de serviço minidriver WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45856fb795810e4e447a226f1b92a28698f08cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813297"
---
# <a name="wia-minidriver-service-library"></a><span data-ttu-id="feeb6-103">Biblioteca de serviço minidriver WIA</span><span class="sxs-lookup"><span data-stu-id="feeb6-103">WIA Minidriver Service Library</span></span>

<span data-ttu-id="feeb6-104">Para simplificar a implementação do driver o máximo possível, o WIA (aquisição de imagem do Windows) fornece uma biblioteca de serviço minidriver que executa muitas das tarefas administrativas exigidas pela arquitetura WIA.</span><span class="sxs-lookup"><span data-stu-id="feeb6-104">To simplify driver implementation as much as possible, Windows Image Acquisition (WIA) provides a Minidriver Service Library that performs many of the administrative tasks required by the WIA architecture.</span></span> <span data-ttu-id="feeb6-105">A biblioteca de serviços fornece funções auxiliares para manter a árvore do dispositivo de objetos da [interface IWiaDrvItem](https://msdn.microsoft.com/library/ms793976.aspx) .</span><span class="sxs-lookup"><span data-stu-id="feeb6-105">The service library provides helper functions to maintain the device's tree of [IWiaDrvItem Interface](https://msdn.microsoft.com/library/ms793976.aspx) objects.</span></span>

<span data-ttu-id="feeb6-106">As funções básicas da biblioteca de serviços executam funções auxiliares que a maioria dos drivers de dispositivo precisariam implementar.</span><span class="sxs-lookup"><span data-stu-id="feeb6-106">The basic service library functions perform helper functions that most device drivers would otherwise need to implement.</span></span> <span data-ttu-id="feeb6-107">Essas funções lêem e gravam Propriedades.</span><span class="sxs-lookup"><span data-stu-id="feeb6-107">These functions read and write properties.</span></span> <span data-ttu-id="feeb6-108">Eles também criam objetos de item de driver e copiam Propriedades de informações de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="feeb6-108">They also create driver item objects and copy device information properties.</span></span>

 

 



