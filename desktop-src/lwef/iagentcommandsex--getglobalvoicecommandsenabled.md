---
title: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
description: IAgentCommandsEx GetGlobalVoiceCommandsEnabled
ms.assetid: 9c8fa978-a02b-4dfc-8cf7-e066c5b75122
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea7275bfe28190e06782cb2564dbf4868dd2c096
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104365935"
---
# <a name="iagentcommandsexgetglobalvoicecommandsenabled"></a><span data-ttu-id="85d94-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="85d94-103">IAgentCommandsEx::GetGlobalVoiceCommandsEnabled</span></span>

<span data-ttu-id="85d94-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="85d94-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetGlobalVoiceCommandsEnabled(
   long * pbEnabled  // address of the global voice command setting
);
```

<span data-ttu-id="85d94-105">Recupera se a gramática de voz para comandos globais do agente está habilitada.</span><span class="sxs-lookup"><span data-stu-id="85d94-105">Retrieves whether the voice grammar for Agent's global commands is enabled.</span></span>

-   <span data-ttu-id="85d94-106">Retorna S \_ OK para indicar que a operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="85d94-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="85d94-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span><span class="sxs-lookup"><span data-stu-id="85d94-107"><span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="85d94-108">O endereço que receberá **true** se a gramática de voz para comandos globais do agente estiver habilitada; **false** se estiver desabilitado.</span><span class="sxs-lookup"><span data-stu-id="85d94-108">The address that receives **True** if the voice grammar for Agent's global commands is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="85d94-109">O Microsoft Agent adiciona automaticamente parâmetros de voz (gramática) para abrir e fechar a janela de comandos de voz e para mostrar e ocultar o caractere.</span><span class="sxs-lookup"><span data-stu-id="85d94-109">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="85d94-110">Quando esse método retorna **false**, quaisquer parâmetros de voz para esses comandos, bem como os parâmetros de voz para a [**legenda**](caption-property.md) dos objetos de [**comando**](/windows/desktop/lwef/the-command-object) de outros clientes, não são incluídos na gramática.</span><span class="sxs-lookup"><span data-stu-id="85d94-110">When this method returns **False**, any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other clients' [**Command**](/windows/desktop/lwef/the-command-object) objects are not included in the grammar.</span></span> <span data-ttu-id="85d94-111">Isso permite que você os elimine da gramática ativa atual do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="85d94-111">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="85d94-112">No entanto, essa configuração não reflete a inclusão desses comandos no menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="85d94-112">However, this setting does not reflect the inclusion of these commands in the character's pop-up menu.</span></span>

## <a name="see-also"></a><span data-ttu-id="85d94-113">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="85d94-113">See Also</span></span>

[<span data-ttu-id="85d94-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="85d94-114">**IAgentCommandsEx::SetGlobalVoiceCommandsEnabled**</span></span>](iagentcommandsex--setglobalvoicecommandsenabled.md)


 

 