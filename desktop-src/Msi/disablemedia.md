---
description: Se essa política do sistema por usuário estiver definida como &\# 0034; 1&\# 0034;, os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis.
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ee50abf36225aa96e52332a53f0b2ab36f058c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930084"
---
# <a name="disablemedia"></a><span data-ttu-id="08a60-103">DisableMedia</span><span class="sxs-lookup"><span data-stu-id="08a60-103">DisableMedia</span></span>

<span data-ttu-id="08a60-104">Se essa [política do sistema](system-policy.md) por usuário for definida como "1", os usuários e administradores que executam uma instalação de manutenção de um produto serão impedidos de usar a caixa de diálogo de procura para procurar fontes de mídia, como CD-ROM, para as fontes de outros produtos instaláveis.</span><span class="sxs-lookup"><span data-stu-id="08a60-104">If this per-user [system policy](system-policy.md) is set to "1", users and administrators running a maintenance installation of one product are prevented from using the Browse Dialog to browse media sources, such as CD-ROM, for the sources of other installable products.</span></span> <span data-ttu-id="08a60-105">Procurar outros produtos é impedido, independentemente de a instalação ser feita com privilégios elevados.</span><span class="sxs-lookup"><span data-stu-id="08a60-105">Browsing for other products is prevented regardless of whether the installation is done with elevated privileges.</span></span> <span data-ttu-id="08a60-106">Ainda é possível que o usuário reinstale o produto da mídia se o usuário tiver uma origem de mídia rotulada corretamente.</span><span class="sxs-lookup"><span data-stu-id="08a60-106">It is still possible for the user to reinstall the product from media if the user has a correctly labeled media source.</span></span>

## <a name="registry-key"></a><span data-ttu-id="08a60-107">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="08a60-107">Registry Key</span></span>

<span data-ttu-id="08a60-108">**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="08a60-108">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="08a60-109">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="08a60-109">Data Type</span></span>

<span data-ttu-id="08a60-110">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="08a60-110">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="08a60-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="08a60-111">Remarks</span></span>

<span data-ttu-id="08a60-112">Observe que a propriedade [**DISABLEMEDIA**](-disablemedia.md) tem um efeito diferente da política de DISABLEMEDIA.</span><span class="sxs-lookup"><span data-stu-id="08a60-112">Note that the [**DISABLEMEDIA**](-disablemedia.md) property has a different effect than the DisableMedia policy.</span></span> <span data-ttu-id="08a60-113">Definir a política do sistema DisableMedia, desabilita apenas a navegação para as fontes de mídia.</span><span class="sxs-lookup"><span data-stu-id="08a60-113">Setting the DisableMedia system policy, only disables browsing to media sources.</span></span> <span data-ttu-id="08a60-114">Definir a propriedade **DISABLEMEDIA** impede que o instalador Registre qualquer fonte de mídia, como um CD-ROM, como uma fonte válida para o produto.</span><span class="sxs-lookup"><span data-stu-id="08a60-114">Setting the **DISABLEMEDIA** property prevents the installer from registering any media source, such as a CD-ROM, as a valid source for the product.</span></span> <span data-ttu-id="08a60-115">No entanto, se a navegação estiver habilitada, um usuário ainda poderá navegar para uma fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="08a60-115">If browsing is enabled however, a user may still browse to a media source.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08a60-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08a60-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a60-117">Resiliência de origem</span><span class="sxs-lookup"><span data-stu-id="08a60-117">Source Resiliency</span></span>](source-resiliency.md)
</dt> </dl>

 

 



