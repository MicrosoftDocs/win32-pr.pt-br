---
title: Sobre os joysticks
description: Sobre os joysticks
ms.assetid: 0cfff45b-48d4-4e0c-addf-e131d3a31187
keywords:
- Multimídia do Windows, joysticks
- multimídia, joysticks
- entrada de multimídia, joysticks
- joysticks, sobre
- joysticks, movimento de dois eixos
- joysticks, movimentação de três eixos
- joysticks, botões
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21a5b2c890e64e397887d89eb5d632b6c4b63689
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005182"
---
# <a name="about-joysticks"></a><span data-ttu-id="c58e2-110">Sobre os joysticks</span><span class="sxs-lookup"><span data-stu-id="c58e2-110">About Joysticks</span></span>

<span data-ttu-id="c58e2-111">O joystick é um dispositivo de entrada auxiliar para aplicativos que fornecem alternativas ao uso do teclado e do mouse.</span><span class="sxs-lookup"><span data-stu-id="c58e2-111">The joystick is an ancillary input device for applications that provide alternatives to using the keyboard and mouse.</span></span> <span data-ttu-id="c58e2-112">O joystick fornece informações posicionais em um sistema de coordenadas que tem valores máximos e mínimos absolutos em cada eixo de movimento.</span><span class="sxs-lookup"><span data-stu-id="c58e2-112">The joystick provides positional information within a coordinate system that has absolute maximum and minimum values in each axis of movement.</span></span>

<span data-ttu-id="c58e2-113">Os serviços de joystick são carregados quando o sistema operacional é iniciado.</span><span class="sxs-lookup"><span data-stu-id="c58e2-113">Joystick services are loaded when the operating system is started.</span></span> <span data-ttu-id="c58e2-114">Os serviços de joystick podem monitorar simultaneamente dois joysticks, cada um com movimento de dois ou três eixos.</span><span class="sxs-lookup"><span data-stu-id="c58e2-114">The joystick services can simultaneously monitor two joysticks, each with two- or three-axis movement.</span></span> <span data-ttu-id="c58e2-115">Cada joystick pode ter até quatro botões.</span><span class="sxs-lookup"><span data-stu-id="c58e2-115">Each joystick can have up to four buttons.</span></span> <span data-ttu-id="c58e2-116">Você pode usar as funções do joystick para determinar os recursos dos joysticks e do driver do joystick.</span><span class="sxs-lookup"><span data-stu-id="c58e2-116">You can use the joystick functions to determine the capabilities of the joysticks and joystick driver.</span></span> <span data-ttu-id="c58e2-117">Além disso, você pode processar as informações posicionais e de botão de um joystick consultando o joystick diretamente ou capturando o joystick e processando as mensagens dele.</span><span class="sxs-lookup"><span data-stu-id="c58e2-117">Also, you can process a joystick's positional and button information by querying the joystick directly or by capturing the joystick and processing messages from it.</span></span> <span data-ttu-id="c58e2-118">O último método é mais simples porque seu aplicativo não precisa consultar o joystick manualmente ou controlar o tempo para gerar consultas em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="c58e2-118">The latter method is simpler because your application does not have to manually query the joystick or track the time to generate queries at regular intervals.</span></span>

 

 




