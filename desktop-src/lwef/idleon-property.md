---
title: Propriedade idleize
description: Propriedade idleize
ms.assetid: ba436dec-c7b4-42e8-99d6-c6ff93afd73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e7fcec4bd6e163baab7722e4d893146819408a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291738"
---
# <a name="idleon-property"></a><span data-ttu-id="6da37-103">Propriedade idleize</span><span class="sxs-lookup"><span data-stu-id="6da37-103">IdleOn Property</span></span>

<span data-ttu-id="6da37-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6da37-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6da37-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="6da37-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="6da37-106">Retorna ou define um valor booliano que determina se o servidor gerencia as animações de estado **deixar** do caractere especificado.</span><span class="sxs-lookup"><span data-stu-id="6da37-106">Returns or sets a Boolean value that determines whether the server manages the specified character's **Idling** state animations.</span></span>

</dd> <dt>

<span data-ttu-id="6da37-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="6da37-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6da37-108">\*agente do ***. Caracteres ("*** characterid \* \* *").* \*  \[  =  *Booliano* de ociosidade\]</span><span class="sxs-lookup"><span data-stu-id="6da37-108">*agent ***.Characters ("*** CharacterID\*\*\*").IdleOn*\* \[ = *boolean*\]</span></span>

</dd> </dl> 

| <span data-ttu-id="6da37-109">Parte</span><span class="sxs-lookup"><span data-stu-id="6da37-109">Part</span></span>      | <span data-ttu-id="6da37-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6da37-110">Description</span></span>                                                                                                                                                                                                             |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6da37-111">*booleano*</span><span class="sxs-lookup"><span data-stu-id="6da37-111">*boolean*</span></span> | <span data-ttu-id="6da37-112">Uma expressão booliana que especifica se o servidor gerencia o modo ocioso.</span><span class="sxs-lookup"><span data-stu-id="6da37-112">A Boolean expression specifying whether the server manages idle mode.</span></span> <span data-ttu-id="6da37-113">**True** (padrão) a manipulação de servidor do estado ocioso está habilitada.</span><span class="sxs-lookup"><span data-stu-id="6da37-113">**True** (Default) Server handling of the idle state is enabled.</span></span> <br/> <span data-ttu-id="6da37-114">**Falso** A manipulação de servidor do estado ocioso está desabilitada.</span><span class="sxs-lookup"><span data-stu-id="6da37-114">**False** Server handling of the idle state is disabled.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="6da37-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6da37-115">Remarks</span></span>

<span data-ttu-id="6da37-116">O servidor define automaticamente um tempo limite após a última animação executada para um caractere.</span><span class="sxs-lookup"><span data-stu-id="6da37-116">The server automatically sets a time-out after the last animation played for a character.</span></span> <span data-ttu-id="6da37-117">Quando o intervalo desse temporizador for concluído, o servidor começará o estado **deixar** de um caractere, jogando suas animações **deixar** associadas em intervalos regulares.</span><span class="sxs-lookup"><span data-stu-id="6da37-117">When this timer's interval is complete, the server begins the **Idling** state for a character, playing its associated **Idling** animations at regular intervals.</span></span> <span data-ttu-id="6da37-118">Se você quiser desabilitar o servidor de reproduzir automaticamente as animações de estado **deixar** , defina a propriedade como **false** e reproduza uma animação ou chame o método [**Stop**](stop-method.md) .</span><span class="sxs-lookup"><span data-stu-id="6da37-118">If you want to disable the server from automatically playing the **Idling** state animations, set the property to **False** and play an animation or call the [**Stop**](stop-method.md) method.</span></span> <span data-ttu-id="6da37-119">A definição desse valor não afeta o estado de animação atual do caractere.</span><span class="sxs-lookup"><span data-stu-id="6da37-119">Setting this value does not affect the current animation state of the character.</span></span>

<span data-ttu-id="6da37-120">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="6da37-120">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 





