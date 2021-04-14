---
description: Um aplicativo habilitado para tinta se comunica com o sistema de reconhecimento por meio das APIs da plataforma Tablet PC.
ms.assetid: 0ea6881f-d2d7-4646-9c41-53d1c03ea55b
title: Arquitetura da API de reconhecimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72838b77e11092cacd4adb998c669167940ecad2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565097"
---
# <a name="recognition-api-architecture"></a><span data-ttu-id="476b7-103">Arquitetura da API de reconhecimento</span><span class="sxs-lookup"><span data-stu-id="476b7-103">Recognition API Architecture</span></span>

<span data-ttu-id="476b7-104">Um aplicativo habilitado para tinta se comunica com o sistema de reconhecimento por meio das APIs da plataforma Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="476b7-104">An ink-enabled application communicates with the recognition system through the Tablet PC Platform APIs.</span></span> <span data-ttu-id="476b7-105">Os aplicativos usam o objeto [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) para fazer isso.</span><span class="sxs-lookup"><span data-stu-id="476b7-105">Applications use the [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) object to accomplish this.</span></span> <span data-ttu-id="476b7-106">A plataforma do Tablet PC interage com o reconhecedor usando as interfaces do estilo C documentadas nesta seção.</span><span class="sxs-lookup"><span data-stu-id="476b7-106">The Tablet PC Platform interacts with your recognizer by using the C-style interfaces that are documented in this section.</span></span> <span data-ttu-id="476b7-107">Na ilustração a seguir, a área dentro da linha tracejada mostra o que está documentado nesta seção.</span><span class="sxs-lookup"><span data-stu-id="476b7-107">In the following illustration, the area inside the dashed line shows what is documented in this section.</span></span>

![ilustração de arquitetura de reconhecimento com reconhecedor realçado](images/96ee7367-7b8a-4794-99c1-bcac9daed645.gif)

<span data-ttu-id="476b7-109">Um reconhecedor personalizado deve incluir recapitular. h (instalado por padrão em C: \\ arquivos de programas que \\ o Microsoft Tablet PC Platform SDK \\ inclui).</span><span class="sxs-lookup"><span data-stu-id="476b7-109">A custom recognizer must include Recapis.h (installed by default in C:\\Program Files\\Microsoft Tablet PC Platform SDK\\Include).</span></span> <span data-ttu-id="476b7-110">Exceto quando observado, sua DLL (biblioteca de vínculo dinâmico) deve exportar todas as funções de API, mesmo que você opte por ter algumas delas retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="476b7-110">Except where noted, your dynamic-link library (DLL) must export all of the API functions, even if you choose to have some of them return E\_NOTIMPL.</span></span>

<span data-ttu-id="476b7-111">Sob nenhuma circunstância o reconhecedor será chamado diretamente por um aplicativo habilitado para tinta.</span><span class="sxs-lookup"><span data-stu-id="476b7-111">Under no circumstances will your recognizer be called directly by an ink-enabled application.</span></span> <span data-ttu-id="476b7-112">Em vez disso, os aplicativos chamarão as APIs de automação ou as APIs gerenciadas para obter os resultados do reconhecedor.</span><span class="sxs-lookup"><span data-stu-id="476b7-112">Instead, applications will call either the Automation APIs or the Managed APIs to get results from your recognizer.</span></span>

 

 



