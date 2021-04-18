---
description: A interface de controle de luz inleve é uma interface de IOCTL padronizada para controlar o brilho da luz de LCD de cristal líquido.
ms.assetid: edf2b7ed-2676-483a-80ba-f148951e0e58
title: Interface de controle de luz Invista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ecbcc3d635d120c1049f8ec586d7296a953dfac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756875"
---
# <a name="backlight-control-interface"></a><span data-ttu-id="38d44-103">Interface de controle de luz Invista</span><span class="sxs-lookup"><span data-stu-id="38d44-103">Backlight Control Interface</span></span>

<span data-ttu-id="38d44-104">A interface de controle de luz inleve é uma interface de IOCTL padronizada para controlar o brilho da luz de LCD de cristal líquido.</span><span class="sxs-lookup"><span data-stu-id="38d44-104">The backlight control interface is a standardized IOCTL interface for controlling the brightness of the LCD backlight.</span></span>

<span data-ttu-id="38d44-105">Aplicativos que exigem controle programático do brilho de tela de luz ou fornecem controles para que o usuário faça isso deve usar essa interface em vez de uma interface proprietária; caso contrário, o sistema não poderá consultar o brilho do hardware atual e poderá se tornar não sincronizado.</span><span class="sxs-lookup"><span data-stu-id="38d44-105">Applications that require programmatic control of the backlight brightness or provide controls for the user to do so should use this interface rather than a proprietary interface; otherwise, the system cannot query the current hardware brightness and may become unsynchronized.</span></span>

<span data-ttu-id="38d44-106">A primeira etapa é consultar o dispositivo para o brilho com suporte usando o código de controle de [**\_ \_ \_ \_ brilho com suporte da consulta de vídeo do IOCTL**](ioctl-video-query-supported-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="38d44-106">The first step is to query the device for the supported brightness using the [**IOCTL\_VIDEO\_QUERY\_SUPPORTED\_BRIGHTNESS**](ioctl-video-query-supported-brightness.md) control code.</span></span> <span data-ttu-id="38d44-107">Esta operação retorna um buffer que especifica os níveis de brilho disponíveis.</span><span class="sxs-lookup"><span data-stu-id="38d44-107">This operation returns a buffer that specifies the available brightness levels.</span></span> <span data-ttu-id="38d44-108">Em seguida, você pode consultar o dispositivo para obter o brilho de vídeo atual usando a consulta de vídeo do IOCTL exibir código de controle de [**\_ \_ \_ \_ brilho**](ioctl-video-query-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="38d44-108">Next, you can query the device for the current display brightness using the [**IOCTL\_VIDEO\_QUERY\_DISPLAY\_BRIGHTNESS**](ioctl-video-query-display-brightness.md) control code.</span></span> <span data-ttu-id="38d44-109">Essa operação retorna as configurações atuais para o brilho atual (AC) alternado, o brilho do corrente direto (DC) e o estado de energia.</span><span class="sxs-lookup"><span data-stu-id="38d44-109">This operation returns the current settings for alternating current (AC) brightness, direct current (DC) brightness, and the power state.</span></span>

<span data-ttu-id="38d44-110">Para alterar o brilho da tela, use o [**conjunto de vídeo do IOCTL exibir código de controle de \_ \_ \_ \_ brilho**](ioctl-video-set-display-brightness.md) .</span><span class="sxs-lookup"><span data-stu-id="38d44-110">To change the display brightness, use the [**IOCTL\_VIDEO\_SET\_DISPLAY\_BRIGHTNESS**](ioctl-video-set-display-brightness.md) control code.</span></span> <span data-ttu-id="38d44-111">Você pode definir o brilho de AC, o brilho do DC ou ambos.</span><span class="sxs-lookup"><span data-stu-id="38d44-111">You can set the AC brightness, the DC brightness, or both.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38d44-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="38d44-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38d44-113">Sobre o gerenciamento de energia</span><span class="sxs-lookup"><span data-stu-id="38d44-113">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



