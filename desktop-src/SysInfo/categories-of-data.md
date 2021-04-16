---
description: 'Antes de colocar dados no registro, um aplicativo deve dividir os dados em duas categorias: dados específicos do computador e dados específicos do usuário.'
ms.assetid: 470d00c1-5975-4a58-9a78-fbed7326a60c
title: Categorias de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 009a3c89d23f713bb2ed08a7f7c53790e08055db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753696"
---
# <a name="categories-of-data"></a><span data-ttu-id="2234a-103">Categorias de dados</span><span class="sxs-lookup"><span data-stu-id="2234a-103">Categories of Data</span></span>

<span data-ttu-id="2234a-104">Antes de colocar dados no registro, um aplicativo deve dividir os dados em duas categorias: dados específicos do computador e dados específicos do usuário.</span><span class="sxs-lookup"><span data-stu-id="2234a-104">Before putting data into the registry, an application should divide the data into two categories: computer-specific data and user-specific data.</span></span> <span data-ttu-id="2234a-105">Fazendo essa distinção, um aplicativo pode dar suporte a vários usuários e, ainda assim, localizar dados específicos do usuário em uma rede e usá-los em locais diferentes, permitindo dados de perfil de usuário independentes de local.</span><span class="sxs-lookup"><span data-stu-id="2234a-105">By making this distinction, an application can support multiple users, and yet locate user-specific data over a network and use that data in different locations, allowing location-independent user profile data.</span></span> <span data-ttu-id="2234a-106">(Um perfil de usuário é um conjunto de dados de configuração salvos para cada usuário.)</span><span class="sxs-lookup"><span data-stu-id="2234a-106">(A user profile is a set of configuration data saved for every user.)</span></span>

<span data-ttu-id="2234a-107">Quando o aplicativo é instalado, ele deve registrar os dados específicos do computador na chave **do \_ \_ computador local hKey** .</span><span class="sxs-lookup"><span data-stu-id="2234a-107">When the application is installed, it should record the computer-specific data under the **HKEY\_LOCAL\_MACHINE** key.</span></span> <span data-ttu-id="2234a-108">Em particular, ele deve criar chaves para o nome da empresa, o nome do produto e o número de versão, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="2234a-108">In particular, it should create keys for the company name, product name, and version number, as shown in the following example:</span></span>

<span data-ttu-id="2234a-109">**HKEY \_ O \_ \\ software \\ da máquina local**_MyCompany \\ MyProduct \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="2234a-109">**HKEY\_LOCAL\_MACHINE\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

<span data-ttu-id="2234a-110">Se o aplicativo oferecer suporte a COM, ele deverá registrar esses dados em **HKEY \_ local \_ Machine \\ software \\ classes**.</span><span class="sxs-lookup"><span data-stu-id="2234a-110">If the application supports COM, it should record that data under **HKEY\_LOCAL\_MACHINE\\Software\\Classes**.</span></span>

<span data-ttu-id="2234a-111">Um aplicativo deve registrar dados específicos do usuário sob a chave de **\_ \_ usuário atual hKey** , conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="2234a-111">An application should record user-specific data under the **HKEY\_CURRENT\_USER** key, as shown in the following example:</span></span>

<span data-ttu-id="2234a-112">**HKEY \_ \_ \\ Software \\ do usuário atual**_MyCompany \\ MyProduct \\ 1,0_</span><span class="sxs-lookup"><span data-stu-id="2234a-112">**HKEY\_CURRENT\_USER\\Software\\**_MyCompany\\MyProduct\\1.0_</span></span>

 

 



