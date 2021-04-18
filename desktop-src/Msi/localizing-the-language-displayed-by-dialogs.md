---
description: O serviço de Windows Installer usa o idioma do usuário atual em todas as caixas de diálogo até que um pacote de Windows Installer seja aberto.
ms.assetid: c9902990-7a26-48fd-96ac-4d5a749e34be
title: Localizando o idioma exibido por caixas de diálogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042b2b7f9ac256ebad265b75a8756fc422403e37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778564"
---
# <a name="localizing-the-language-displayed-by-dialogs"></a><span data-ttu-id="b1b6c-103">Localizando o idioma exibido por caixas de diálogo</span><span class="sxs-lookup"><span data-stu-id="b1b6c-103">Localizing the Language Displayed by Dialogs</span></span>

<span data-ttu-id="b1b6c-104">O serviço de Windows Installer usa o idioma do usuário atual em todas as caixas de diálogo até que um pacote de Windows Installer seja aberto.</span><span class="sxs-lookup"><span data-stu-id="b1b6c-104">The Windows Installer service uses the current user's language in all dialogs until a Windows Installer package is opened.</span></span> <span data-ttu-id="b1b6c-105">O Windows Installer determina isso usando **GetUserDefaultUILanguage**.</span><span class="sxs-lookup"><span data-stu-id="b1b6c-105">The Windows Installer determines this by using **GetUserDefaultUILanguage**.</span></span> <span data-ttu-id="b1b6c-106">Quando um pacote de Windows Installer é aberto, o instalador exibe caixas de diálogo usando o idioma do pacote conforme especificado pela propriedade de [**Resumo do modelo**](template-summary.md) .</span><span class="sxs-lookup"><span data-stu-id="b1b6c-106">When a Windows Installer package is opened, the installer displays dialogs using the package's language as specified by the [**Template Summary**](template-summary.md) Property.</span></span>

<span data-ttu-id="b1b6c-107">Para obter mais informações sobre como localizar o idioma de um pacote de Windows Installer, consulte também [um exemplo de localização](a-localization-example.md).</span><span class="sxs-lookup"><span data-stu-id="b1b6c-107">For more information about localizing the language of a Windows Installer package, see also [A Localization Example](a-localization-example.md).</span></span>

 

 



