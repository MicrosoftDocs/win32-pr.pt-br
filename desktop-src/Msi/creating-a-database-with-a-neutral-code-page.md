---
description: A abordagem recomendada para lidar com páginas de código é criar um banco de dados de base neutro que contenha apenas caracteres que possam ser traduzidos em qualquer página de código.
ms.assetid: 8ded41a6-6e5b-4a39-b783-e2b9f83eaed4
title: Criando um banco de dados com uma página de código neutra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08639b6ab3521f183a2dab46dfd257121b28bae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011164"
---
# <a name="creating-a-database-with-a-neutral-code-page"></a><span data-ttu-id="64ad4-103">Criando um banco de dados com uma página de código neutra</span><span class="sxs-lookup"><span data-stu-id="64ad4-103">Creating a Database with a Neutral Code Page</span></span>

<span data-ttu-id="64ad4-104">A abordagem recomendada para lidar com páginas de código é criar um banco de dados de base neutro que contenha apenas caracteres que possam ser traduzidos em qualquer página de código.</span><span class="sxs-lookup"><span data-stu-id="64ad4-104">The recommended approach for handling code pages is to author a neutral base database that only contains characters that can be translated into any code page.</span></span> <span data-ttu-id="64ad4-105">O banco de dados pode então ser definido para a página de código da localização e as informações de localização podem ser adicionadas conforme descrito em [localizando um pacote de Windows Installer](localizing-a-windows-installer-package.md).</span><span class="sxs-lookup"><span data-stu-id="64ad4-105">The database may then be set to the code page of the localization and the localization information can be added as described in [Localizing a Windows Installer Package](localizing-a-windows-installer-package.md).</span></span>

<span data-ttu-id="64ad4-106">Para criar um banco de dados neutro, evite caracteres estendidos que não pertençam ao conjunto de caracteres ASCII e, portanto, exijam uma página de código especial.</span><span class="sxs-lookup"><span data-stu-id="64ad4-106">To author a neutral database, avoid extended characters that do not belong to the ASCII character set and therefore require a special code page.</span></span> <span data-ttu-id="64ad4-107">Por exemplo, o sinal de direitos autorais, © e o sinal de marca registrada,, não são caracteres ASCII, e exigem uma página de código ANSI especial para exibição adequada.</span><span class="sxs-lookup"><span data-stu-id="64ad4-107">For example, the copyright sign, ©, and the registered trademark sign, , are not ASCII characters, and require a special ANSI code page for proper display.</span></span> <span data-ttu-id="64ad4-108">Em vez disso, use (c) e (r), porque esses caracteres podem ser traduzidos ou transformados para os símbolos para a versão em inglês.</span><span class="sxs-lookup"><span data-stu-id="64ad4-108">Instead use (c) and (r), because these characters can be translated or transformed to the symbols for the English-language version.</span></span> <span data-ttu-id="64ad4-109">Esse banco de dados neutro pode ser localizado definindo sua página de código e adicionando informações de localização por edição de tabela ou Importando arquivos mortos de texto.</span><span class="sxs-lookup"><span data-stu-id="64ad4-109">This neutral database can then be localized by setting its code page and adding localization information by table editing or by importing text archive files.</span></span>

 

 



