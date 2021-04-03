---
title: Propriedade DefaultCommand
description: Propriedade DefaultCommand
ms.assetid: ba4d51fc-7178-4dbb-9ae5-f1991f40aad6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d57d937cec575f0fdd99cc1f14511b9c88f9235
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104007473"
---
# <a name="defaultcommand-property"></a><span data-ttu-id="df033-103">Propriedade DefaultCommand</span><span class="sxs-lookup"><span data-stu-id="df033-103">DefaultCommand Property</span></span>

<span data-ttu-id="df033-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="df033-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="df033-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="df033-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="df033-106">Retorna ou define o comando padrão do objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="df033-106">Returns or sets the default command of the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object.</span></span>

</dd> <dt>

<span data-ttu-id="df033-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="df033-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="df033-108">*Agent. \* \* \* caracteres* \*  **("***Characterid***"). Commands. DefaultCommand** \[  =  *String*\]</span><span class="sxs-lookup"><span data-stu-id="df033-108">*agent.\*\*\*Characters*\* **("***CharacterID***").Commands.DefaultCommand** \[ = *string*\]</span></span>



| <span data-ttu-id="df033-109">Parte</span><span class="sxs-lookup"><span data-stu-id="df033-109">Part</span></span>     | <span data-ttu-id="df033-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="df033-110">Description</span></span>                                                                         |
|----------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df033-111">*cadeia de caracteres*</span><span class="sxs-lookup"><span data-stu-id="df033-111">*string*</span></span> | <span data-ttu-id="df033-112">Um valor de cadeia de caracteres que identifica o nome (ID) do [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="df033-112">A string value identifying the name (ID) of the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df033-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="df033-113">Remarks</span></span>

<span data-ttu-id="df033-114">Essa propriedade permite que você defina um [**comando**](/windows/desktop/lwef/the-command-object) em sua coleção de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) como o comando padrão, renderizando-o em negrito.</span><span class="sxs-lookup"><span data-stu-id="df033-114">This property enables you to set a [**Command**](/windows/desktop/lwef/the-command-object) in your [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection as the default command, rendering it bold.</span></span> <span data-ttu-id="df033-115">Isso não altera de fato o tratamento de comandos nem eventos de clique duplo.</span><span class="sxs-lookup"><span data-stu-id="df033-115">This does not actually change command handling or double-click events.</span></span>

<span data-ttu-id="df033-116">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="df033-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

 

 