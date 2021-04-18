---
title: Configuração do registro de aquisição silenciosa
description: Configuração do registro de aquisição silenciosa
ms.assetid: 50e0b27e-ddf8-441f-adcd-d88d36f3edaf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a00bbb6d930cb137ed12ffbcb05af31cee3c99c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781446"
---
# <a name="silent-acquisition-registry-setting"></a><span data-ttu-id="c7bb8-103">Configuração do registro de aquisição silenciosa</span><span class="sxs-lookup"><span data-stu-id="c7bb8-103">Silent Acquisition Registry Setting</span></span>

<span data-ttu-id="c7bb8-104">O Microsoft Windows Media Player usa o seguinte valor de registro para determinar se a aquisição silenciosa deve ser habilitada, um estado no qual o Player baixa direitos de uso automaticamente quando o usuário toca ou sincroniza o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="c7bb8-104">Microsoft Windows Media Player uses the following registry value to determine whether to enable silent acquisition, a state in which the player downloads usage rights automatically when the user plays or syncs protected content.</span></span>

<span data-ttu-id="c7bb8-105">**HKEY \_ SOFTWARE do \_ computador local** \\  \\ **preferências do Microsoft** \\ **MediaPlayer** \\  \\ **SilentAcquisition**</span><span class="sxs-lookup"><span data-stu-id="c7bb8-105">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**MediaPlayer**\\**Preferences**\\**SilentAcquisition**</span></span>

<span data-ttu-id="c7bb8-106">O valor de SilentAcquisition tem o seguinte formato:</span><span class="sxs-lookup"><span data-stu-id="c7bb8-106">The SilentAcquisition value has the following form:</span></span>



| <span data-ttu-id="c7bb8-107">Nome</span><span class="sxs-lookup"><span data-stu-id="c7bb8-107">Name</span></span>              | <span data-ttu-id="c7bb8-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="c7bb8-108">Type</span></span>           | <span data-ttu-id="c7bb8-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c7bb8-109">Description</span></span>                                                                                                       |
|-------------------|----------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7bb8-110">SilentAcquisition</span><span class="sxs-lookup"><span data-stu-id="c7bb8-110">SilentAcquisition</span></span> | <span data-ttu-id="c7bb8-111">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="c7bb8-111">**REG\_DWORD**</span></span> | <span data-ttu-id="c7bb8-112">Defina esse valor como 1 para habilitar a aquisição silenciosa ou defina-a como 0 para desabilitar a aquisição silenciosa.</span><span class="sxs-lookup"><span data-stu-id="c7bb8-112">Set this value to 1 to enable silent acquisition, or set it to 0 to disable silent acquisition.</span></span> <span data-ttu-id="c7bb8-113">O padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="c7bb8-113">The default is 1.</span></span> |



 

<span data-ttu-id="c7bb8-114">Para especificar um valor, o usuário pode iniciar o Windows Media Player, abrir a caixa de diálogo **Opções** , clicar na guia **privacidade** e, em seguida, marcar ou desmarcar a caixa de seleção **baixar direitos de uso automaticamente quando eu reproduzir ou sincronizar um arquivo** .</span><span class="sxs-lookup"><span data-stu-id="c7bb8-114">To specify a value, the user can start Windows Media Player, open the **Options** dialog box, click the **Privacy** tab, and then select or clear the **Download usage rights automatically when I play or sync a file** check box.</span></span> <span data-ttu-id="c7bb8-115">Marcar essa caixa de seleção define SilentAcquisition como 1; desmarcar a caixa de seleção o define como 0.</span><span class="sxs-lookup"><span data-stu-id="c7bb8-115">Selecting this check box sets SilentAcquisition to 1; clearing the check box sets it to 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7bb8-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7bb8-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7bb8-117">**Configurações do registro**</span><span class="sxs-lookup"><span data-stu-id="c7bb8-117">**Registry Settings**</span></span>](registry-settings.md)
</dt> </dl>

 

 




