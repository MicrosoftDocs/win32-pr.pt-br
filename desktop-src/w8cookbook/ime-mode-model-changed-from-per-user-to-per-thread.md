---
title: Alterações do modelo do modo IME
description: O modelo de modo IME mudou de por usuário para por thread
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294400"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="12f40-103">O modelo de modo IME mudou de por usuário para por thread</span><span class="sxs-lookup"><span data-stu-id="12f40-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="12f40-104">Plataformas</span><span class="sxs-lookup"><span data-stu-id="12f40-104">Platforms</span></span>

<dl> <span data-ttu-id="12f40-105">Clientes-Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="12f40-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="12f40-106">Servidores-Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="12f40-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="12f40-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="12f40-107">Description</span></span>

<span data-ttu-id="12f40-108">No Windows 8, o modo de conversão IME e o modo de frase IME foram baseados no contexto do usuário e a alteração do modo de um aplicativo afetou todos os outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="12f40-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="12f40-109">Esse comportamento pode ser desabilitado usando a configuração "Deixe-me definir um método de entrada diferente para cada janela de aplicativo" na seção Configurações avançadas do painel de controle de idioma.</span><span class="sxs-lookup"><span data-stu-id="12f40-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="12f40-110">Para melhorar a compatibilidade, em Windows 8.1 os modos são armazenados em um contexto de entrada, independentemente de como o controle "Deixe-me definir um método de entrada diferente para cada janela do aplicativo" está definido.</span><span class="sxs-lookup"><span data-stu-id="12f40-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="12f40-111">No Windows 8.1, a configuração "Deixe-me definir um método de entrada diferente para cada janela de aplicativo" afeta apenas a seleção do próprio método de entrada.</span><span class="sxs-lookup"><span data-stu-id="12f40-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="12f40-112">Na inicialização do aplicativo, o modo IME é definido com os seguintes padrões:</span><span class="sxs-lookup"><span data-stu-id="12f40-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="12f40-113">Painel de entrada de software</span><span class="sxs-lookup"><span data-stu-id="12f40-113">Software input panel</span></span> | <span data-ttu-id="12f40-114">Teclado de hardware</span><span class="sxs-lookup"><span data-stu-id="12f40-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="12f40-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="12f40-115">KOR, JPN</span></span> | <span data-ttu-id="12f40-116">Ativado</span><span class="sxs-lookup"><span data-stu-id="12f40-116">On</span></span>                   | <span data-ttu-id="12f40-117">Desativado</span><span class="sxs-lookup"><span data-stu-id="12f40-117">Off</span></span>               |
| <span data-ttu-id="12f40-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="12f40-118">CHS,CHT</span></span>  | <span data-ttu-id="12f40-119">Ativado</span><span class="sxs-lookup"><span data-stu-id="12f40-119">On</span></span>                   | <span data-ttu-id="12f40-120">Ativado</span><span class="sxs-lookup"><span data-stu-id="12f40-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="12f40-121">Manifestações</span><span class="sxs-lookup"><span data-stu-id="12f40-121">Manifestations</span></span>

<span data-ttu-id="12f40-122">Quando um usuário altera o modo IME em um aplicativo, a alteração não afeta outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="12f40-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="12f40-123">Recursos</span><span class="sxs-lookup"><span data-stu-id="12f40-123">Resources</span></span>

-   [<span data-ttu-id="12f40-124">Valores do modo de conversão do IME</span><span class="sxs-lookup"><span data-stu-id="12f40-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="12f40-125">Valores do modo de frase do IME</span><span class="sxs-lookup"><span data-stu-id="12f40-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 