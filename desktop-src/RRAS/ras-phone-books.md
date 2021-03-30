---
title: Manuais de telefones RAS
description: Os catálogos telefônicos fornecem uma maneira padrão de coletar e especificar as informações que o Gerenciador de conexões de acesso remoto precisa para estabelecer uma conexão remota.
ms.assetid: db6d076c-c683-4e27-ace1-d2c0cd0931f6
keywords:
- Catálogos telefônicos, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bbdfe7d2293f87e01fe33f3a078f861a35a732d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005617"
---
# <a name="ras-phone-books"></a><span data-ttu-id="15829-104">Manuais de telefones RAS</span><span class="sxs-lookup"><span data-stu-id="15829-104">RAS Phone Books</span></span>

<span data-ttu-id="15829-105">Os catálogos telefônicos fornecem uma maneira padrão de coletar e especificar as informações que o Gerenciador de conexões de acesso remoto precisa para estabelecer uma conexão remota.</span><span class="sxs-lookup"><span data-stu-id="15829-105">Phone books provide a standard way to collect and specify the information that the Remote Access Connection Manager needs to establish a remote connection.</span></span> <span data-ttu-id="15829-106">Os catálogos telefônicos associam nomes de entrada com informações como números de telefone, portas COM e configurações de modem.</span><span class="sxs-lookup"><span data-stu-id="15829-106">Phone books associate entry names with information such as phone numbers, COM ports, and modem settings.</span></span> <span data-ttu-id="15829-107">Cada entrada do catálogo telefônico contém as informações necessárias para estabelecer uma conexão RAS.</span><span class="sxs-lookup"><span data-stu-id="15829-107">Each phone-book entry contains the information needed to establish a RAS connection.</span></span>

<span data-ttu-id="15829-108">Os catálogos telefônicos são armazenados em arquivos de catálogo telefônico, que são arquivos de texto que contêm os nomes de entrada e as informações associadas.</span><span class="sxs-lookup"><span data-stu-id="15829-108">Phone books are stored in phone-book files, which are text files that contain the entry names and associated information.</span></span> <span data-ttu-id="15829-109">O RAS cria um arquivo de catálogo telefônico chamado RASPHONE. PBK.</span><span class="sxs-lookup"><span data-stu-id="15829-109">RAS creates a phone-book file called RASPHONE.PBK.</span></span> <span data-ttu-id="15829-110">O usuário pode usar a caixa de diálogo **rede dial-up** principal para criar arquivos de catálogo telefônico pessoal.</span><span class="sxs-lookup"><span data-stu-id="15829-110">The user can use the main **Dial-Up Networking** dialog box to create personal phone-book files.</span></span> <span data-ttu-id="15829-111">Atualmente, a API RAS não oferece suporte para a criação de um arquivo de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="15829-111">The RAS API does not currently provide support for creating a phone-book file.</span></span> <span data-ttu-id="15829-112">Algumas funções de RAS, como a função [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) , têm um parâmetro que especifica um arquivo de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="15829-112">Some RAS functions, such as the [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) function, have a parameter that specifies a phone-book file.</span></span> <span data-ttu-id="15829-113">Se o chamador não especificar um arquivo de catálogo telefônico, a função usará o arquivo de catálogo telefônico padrão, que é aquele selecionado pelo usuário na folha de propriedades **preferências do usuário** da caixa de diálogo **rede dial-up** .</span><span class="sxs-lookup"><span data-stu-id="15829-113">If the caller does not specify a phone-book file, the function uses the default phone-book file, which is the one selected by the user in the **User Preferences** property sheet of the **Dial-Up Networking** dialog box.</span></span>

<span data-ttu-id="15829-114">O Windows NT 4,0 fornece as funções [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) e [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) que exibem a interface do usuário RAS interna que permite que os usuários trabalhem com catálogos telefônicos e entradas de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="15829-114">Windows NT 4.0 provides the [**RasPhonebookDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga) and [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) functions that display the built-in RAS user interface that enable users to work with phone books and phone-book entries.</span></span>

<span data-ttu-id="15829-115">**Windows 95:** A rede dial-up armazena entradas de catálogo telefônico no registro em vez de em um arquivo de catálogo telefônico.</span><span class="sxs-lookup"><span data-stu-id="15829-115">**Windows 95:** Dial-up networking stores phone-book entries in the registry rather than in a phone-book file.</span></span> <span data-ttu-id="15829-116">O Windows 95 não oferece suporte a arquivos de catálogo telefônico pessoais ou funções que exibem as caixas de diálogo internas de RAS.</span><span class="sxs-lookup"><span data-stu-id="15829-116">Windows 95 does not support personal phone-book files or functions that display the built-in RAS dialog boxes.</span></span>

 

 




