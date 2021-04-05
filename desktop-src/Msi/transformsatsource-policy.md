---
description: Se essa política do sistema por usuário estiver definida como &\# 0034; 1&\# 0034;; o instalador pesquisará arquivos de transformação na raiz de qualquer fonte de rede na lista de origem do produto. Por padrão, as transformações são armazenadas na pasta de dados do aplicativo do perfil de um usuário.
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: Política de TransformsAtSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089850"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="68e14-104">Política de TransformsAtSource</span><span class="sxs-lookup"><span data-stu-id="68e14-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="68e14-105">Se essa [política do sistema](system-policy.md) por usuário estiver definida como "1"; o instalador pesquisa arquivos de transformação na raiz de qualquer fonte de rede na lista de origem do produto.</span><span class="sxs-lookup"><span data-stu-id="68e14-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="68e14-106">Por padrão, as transformações são armazenadas na pasta de dados do aplicativo do perfil de um usuário.</span><span class="sxs-lookup"><span data-stu-id="68e14-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="68e14-107">Windows Installer interpreta a política TransformsAtSource para ser a mesma que a [política TransformsSecure](transformssecure-policy.md).</span><span class="sxs-lookup"><span data-stu-id="68e14-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="68e14-108">Chave do Registro</span><span class="sxs-lookup"><span data-stu-id="68e14-108">Registry Key</span></span>

<span data-ttu-id="68e14-109">**HKEY \_ \_** Políticas de software de usuário atuais \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="68e14-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="68e14-110">Tipo de Dados</span><span class="sxs-lookup"><span data-stu-id="68e14-110">Data Type</span></span>

<span data-ttu-id="68e14-111">**REG \_ sz**</span><span class="sxs-lookup"><span data-stu-id="68e14-111">**REG\_SZ**</span></span>

 

 



