---
title: Propriedade HelpFile
description: Propriedade HelpFile
ms.assetid: 18a5fd9b-4ca7-4701-9993-1e0c55f6e232
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d5307abfba0f884261f5b4a21131a75cf87224
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636042"
---
# <a name="helpfile-property"></a><span data-ttu-id="0a12f-103">Propriedade HelpFile</span><span class="sxs-lookup"><span data-stu-id="0a12f-103">HelpFile Property</span></span>

<span data-ttu-id="0a12f-104">\[O Microsoft Agent foi preterido a partir do Windows 7 e pode não estar disponível nas versões subsequentes do Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0a12f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0a12f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Ndescrição**</span><span class="sxs-lookup"><span data-stu-id="0a12f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0a12f-106">Retorna ou define o caminho e o nome do arquivo de uma ajuda sensível ao contexto do Microsoft Windows fornecida pelo aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0a12f-106">Returns or sets the path and filename for a Microsoft Windows context-sensitive Help file supplied by the client application.</span></span>

</dd> <dt>

<span data-ttu-id="0a12f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxe**</span><span class="sxs-lookup"><span data-stu-id="0a12f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0a12f-108">\*agente do. ***Caracteres ("*** characterid \* \* *").* \*  \[  =  *Nome de arquivo* do ArquivoDeAjuda\]</span><span class="sxs-lookup"><span data-stu-id="0a12f-108">*agent.\*\*\*Characters("*\*\* CharacterID\***").Helpfile** \[ = *Filename*\]</span></span>



| <span data-ttu-id="0a12f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0a12f-109">Part</span></span>       | <span data-ttu-id="0a12f-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a12f-110">Description</span></span>                                                                    |
|------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="0a12f-111">*Filename*</span><span class="sxs-lookup"><span data-stu-id="0a12f-111">*Filename*</span></span> | <span data-ttu-id="0a12f-112">Uma expressão de cadeia de caracteres especificando o caminho e o nome do arquivo de ajuda do Windows.</span><span class="sxs-lookup"><span data-stu-id="0a12f-112">A string expression specifying the path and filename of the Windows Help file.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a12f-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0a12f-113">Remarks</span></span>

<span data-ttu-id="0a12f-114">Se você tiver criado um arquivo de ajuda do Windows para seu aplicativo e definir a propriedade **HelpFile** do caractere, o Agent chamará automaticamente a ajuda quando [**HelpModeOn**](helpmodeon-property.md) for definido como **true** e o usuário clicar no caractere ou selecionar um comando no menu pop-up.</span><span class="sxs-lookup"><span data-stu-id="0a12f-114">If you've created a Windows Help file for your application and set the character's **HelpFile** property, Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user clicks the character or selects a command from its pop-up menu.</span></span> <span data-ttu-id="0a12f-115">Se você especificou um número de contexto na propriedade [**HelpContextId**](helpcontextid-property.md) do comando selecionado, a ajuda exibirá um tópico correspondente ao contexto de ajuda atual; caso contrário, ele exibirá "nenhum tópico da ajuda associado a este item".</span><span class="sxs-lookup"><span data-stu-id="0a12f-115">If you specified a context number in the [**HelpContextID**](helpcontextid-property.md) property of the selected command, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="0a12f-116">Essa propriedade aplica-se somente ao uso do caractere do aplicativo cliente; a configuração não afeta outros clientes do caractere ou outros caracteres do seu aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="0a12f-116">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

## <a name="see-also"></a><span data-ttu-id="0a12f-117">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0a12f-117">See Also</span></span>

<span data-ttu-id="0a12f-118">[**Propriedade HelpModeOn**](helpmodeon-property.md), [ **propriedade HelpContextID**](helpcontextid-property.md)</span><span class="sxs-lookup"><span data-stu-id="0a12f-118">[**HelpModeOn property**](helpmodeon-property.md), [**HelpContextID property**](helpcontextid-property.md)</span></span>


 

 




