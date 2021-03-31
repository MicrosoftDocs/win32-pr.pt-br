---
title: Propriedade GlobalVoiceCommandsEnabled
description: Propriedade GlobalVoiceCommandsEnabled
ms.assetid: d4f74019-fa33-41fc-abe7-01791ff188f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f523171187c9956a7741afc0fabcc7ec794071
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103917314"
---
# <a name="globalvoicecommandsenabled-property"></a><span data-ttu-id="c3a73-103">Propriedade GlobalVoiceCommandsEnabled</span><span class="sxs-lookup"><span data-stu-id="c3a73-103">GlobalVoiceCommandsEnabled Property</span></span>

<span data-ttu-id="c3a73-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c3a73-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="c3a73-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="c3a73-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="c3a73-106">Retorna ou define se a voz está habilitada para os comandos globais do agente.</span><span class="sxs-lookup"><span data-stu-id="c3a73-106">Returns or sets whether voice is enabled for Agent's global commands.</span></span>

</dd> <dt>

<span data-ttu-id="c3a73-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="c3a73-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="c3a73-108">*Agente. ***Caracteres ("*** characterid \* \* *"). Commands. GlobalVoiceCommandsEnabled**</span><span class="sxs-lookup"><span data-stu-id="c3a73-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Commands.GlobalVoiceCommandsEnabled**</span></span>

<span data-ttu-id="c3a73-109">\[ = *Boolean*\]</span><span class="sxs-lookup"><span data-stu-id="c3a73-109">\[ = *boolean*\]</span></span>



| <span data-ttu-id="c3a73-110">Parte</span><span class="sxs-lookup"><span data-stu-id="c3a73-110">Part</span></span>      | <span data-ttu-id="c3a73-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="c3a73-111">Description</span></span>                                                                                                                                                                                                            |
|-----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3a73-112">*booleano*</span><span class="sxs-lookup"><span data-stu-id="c3a73-112">*boolean*</span></span> | <span data-ttu-id="c3a73-113">Uma expressão booliana que indica se os parâmetros de voz para comandos globais do agente estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="c3a73-113">A Boolean expression that indicates whether voice parameters for Agent's global commands are enabled.</span></span> <span data-ttu-id="c3a73-114">Os parâmetros de voz **verdadeiros** (padrão) estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="c3a73-114">**True** (Default) Voice parameters are enabled.</span></span> <br/> <span data-ttu-id="c3a73-115">**Falso** Os parâmetros de voz estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="c3a73-115">**False** Voice parameters are disabled.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c3a73-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3a73-116">Remarks</span></span>

<span data-ttu-id="c3a73-117">O Microsoft Agent adiciona automaticamente parâmetros de voz (gramática) para abrir e fechar a janela de comandos de voz e para mostrar e ocultar o caractere.</span><span class="sxs-lookup"><span data-stu-id="c3a73-117">Microsoft Agent automatically adds voice parameters (grammar) for opening and closing the Voice Commands Window and for showing and hiding the character.</span></span> <span data-ttu-id="c3a73-118">Se você definir **GlobalVoiceCommandsEnabled** como **false**, o Agent desabilitará quaisquer parâmetros de voz para esses comandos, bem como os parâmetros de voz para a [**legenda**](caption-property.md) dos objetos de outros [**comandos**](/windows/desktop/lwef/the-commands-collection-object) do cliente.</span><span class="sxs-lookup"><span data-stu-id="c3a73-118">If you set **GlobalVoiceCommandsEnabled** to **False**, Agent disables any voice parameters for these commands as well as the voice parameters for the [**Caption**](caption-property.md) of other client's [**Commands**](/windows/desktop/lwef/the-commands-collection-object) objects.</span></span> <span data-ttu-id="c3a73-119">Isso permite que você os elimine da gramática ativa atual do seu cliente.</span><span class="sxs-lookup"><span data-stu-id="c3a73-119">This enables you to eliminate these from your client's current active grammar.</span></span> <span data-ttu-id="c3a73-120">No entanto, como isso potencialmente bloqueia o acesso de voz a outros clientes, redefina essa propriedade como **true** depois de processar a entrada de voz do usuário.</span><span class="sxs-lookup"><span data-stu-id="c3a73-120">However, because this potentially blocks voice access to other clients, reset this property to **True** after processing the user's voice input.</span></span>

<span data-ttu-id="c3a73-121">Desabilitar a propriedade não afeta o menu pop-up do caractere.</span><span class="sxs-lookup"><span data-stu-id="c3a73-121">Disabling the property does not affect the character's pop-up menu.</span></span> <span data-ttu-id="c3a73-122">Os comandos globais adicionados pelo servidor ainda serão exibidos.</span><span class="sxs-lookup"><span data-stu-id="c3a73-122">The global commands added by the server will still appear.</span></span> <span data-ttu-id="c3a73-123">Você não pode removê-los do menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="c3a73-123">You cannot remove them from the pop-up menu.</span></span>

 

