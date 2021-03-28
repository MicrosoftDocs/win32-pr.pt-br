---
description: Ilustra a invocação de um comando DDE usando um verbo do Shell.
ms.assetid: 65DDD992-5E96-447E-9151-2CCA740822A1
title: Como associar verbos a comandos DDE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7174a22c993d93c347c8a0368fa7d1798362070f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967914"
---
# <a name="how-to-associate-verbs-with-dde-commands"></a><span data-ttu-id="3f11c-103">Como associar verbos a comandos DDE</span><span class="sxs-lookup"><span data-stu-id="3f11c-103">How to Associate Verbs with DDE Commands</span></span>

<span data-ttu-id="3f11c-104">Invocar um verbo normalmente inicia o aplicativo que é especificado pela subchave de comando do verbo.</span><span class="sxs-lookup"><span data-stu-id="3f11c-104">Invoking a verb ordinarily launches the application that is specified by the verb's command subkey.</span></span> <span data-ttu-id="3f11c-105">No entanto, se seu aplicativo der suporte a troca dinâmica de dados (DDE), você poderá fazer com que o Shell inicie uma conversa DDE.</span><span class="sxs-lookup"><span data-stu-id="3f11c-105">However, if your application supports Dynamic Data Exchange (DDE), you can instead have the Shell initiate a DDE conversation.</span></span>

<span data-ttu-id="3f11c-106">Para especificar que a invocação de um verbo deve iniciar uma conversa DDE, siga estas etapas.</span><span class="sxs-lookup"><span data-stu-id="3f11c-106">To specify that invoking a verb should initiate a DDE conversation, follow these steps.</span></span>

## <a name="instructions"></a><span data-ttu-id="3f11c-107">Instruções</span><span class="sxs-lookup"><span data-stu-id="3f11c-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="3f11c-108">Etapa 1:</span><span class="sxs-lookup"><span data-stu-id="3f11c-108">Step 1:</span></span>

<span data-ttu-id="3f11c-109">Adicione uma subchave **ddeexec** à chave do verbo.</span><span class="sxs-lookup"><span data-stu-id="3f11c-109">Add a **ddeexec** subkey to the verb's key.</span></span>

### <a name="step-2"></a><span data-ttu-id="3f11c-110">Etapa 2:</span><span class="sxs-lookup"><span data-stu-id="3f11c-110">Step 2:</span></span>

<span data-ttu-id="3f11c-111">Defina o valor padrão de **ddeexec** para a cadeia de caracteres de comando DDE.</span><span class="sxs-lookup"><span data-stu-id="3f11c-111">Set the default value of **ddeexec** to the DDE command string.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f11c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f11c-112">Remarks</span></span>

<span data-ttu-id="3f11c-113">A chave **ddeexec** tem três subchaves opcionais que fornecem algum controle sobre o processo DDE:</span><span class="sxs-lookup"><span data-stu-id="3f11c-113">The **ddeexec** key has three optional subkeys that provide some control over the DDE process:</span></span>

-   <span data-ttu-id="3f11c-114">**aplicativo**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-114">**application**.</span></span> <span data-ttu-id="3f11c-115">Defina o valor padrão dessa subchave como o nome do aplicativo a ser usado para estabelecer a conversa DDE.</span><span class="sxs-lookup"><span data-stu-id="3f11c-115">Set the default value of this subkey to the application name to be used to establish the DDE conversation.</span></span> <span data-ttu-id="3f11c-116">Se não houver nenhuma subchave de **aplicativo** , o valor padrão da subchave de **comando** do verbo será usado como o nome do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3f11c-116">If there is no **application** subkey, the default value of the verb's **command** subkey is used as the application name.</span></span>
-   <span data-ttu-id="3f11c-117">**tópico**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-117">**topic**.</span></span> <span data-ttu-id="3f11c-118">Defina o valor padrão dessa subchave como o nome do tópico da conversa DDE.</span><span class="sxs-lookup"><span data-stu-id="3f11c-118">Set the default value of this subkey to the topic name of the DDE conversation.</span></span> <span data-ttu-id="3f11c-119">Se não houver subchave de **tópico** , o sistema será usado como o nome do tópico.</span><span class="sxs-lookup"><span data-stu-id="3f11c-119">If there is no **topic** subkey, System is used as the topic name.</span></span>
-   <span data-ttu-id="3f11c-120">**ifexec**.</span><span class="sxs-lookup"><span data-stu-id="3f11c-120">**ifexec**.</span></span> <span data-ttu-id="3f11c-121">Defina o valor padrão dessa subchave como o comando DDE a ser usado se a conversa DDE não puder ser iniciada.</span><span class="sxs-lookup"><span data-stu-id="3f11c-121">Set the default value of this subkey to the DDE command to be used if DDE conversation cannot be initiated.</span></span> <span data-ttu-id="3f11c-122">Quando a inicialização falha, o aplicativo especificado pelo valor padrão da subchave de **comando** do verbo é iniciado.</span><span class="sxs-lookup"><span data-stu-id="3f11c-122">When initiation fails, the application that is specified by the default value of the verb's **command** subkey is launched.</span></span> <span data-ttu-id="3f11c-123">Se existir uma chave **ifexec** , seu valor padrão será usado como o comando DDE.</span><span class="sxs-lookup"><span data-stu-id="3f11c-123">If an **ifexec** key exists, its default value will then be used as the DDE command.</span></span> <span data-ttu-id="3f11c-124">Se não houver nenhuma subchave **ifexec** , o valor padrão da chave **ddeexec** será usado novamente como o comando DDE.</span><span class="sxs-lookup"><span data-stu-id="3f11c-124">If there is no **ifexec** subkey, the default value of the **ddeexec** key will be used again as the DDE command.</span></span>

<span data-ttu-id="3f11c-125">O exemplo a seguir especifica que invocar o verbo Open para myprogram. 1 inicia uma conversa DDE com um comando DDE aberto ("%1") e um nome de aplicativo de myprogram.</span><span class="sxs-lookup"><span data-stu-id="3f11c-125">The following example specifies that invoking the open verb for MyProgram.1 initiates a DDE conversation with a DDE command of Open("%1") and an application name of MyProgram.</span></span>

```
HKEY_CLASSES_ROOT
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = doit
         open
            command
               (Default) = C:\MyDir\MyProgram.exe "%1"
            ddeexec
               (Default) = Open("%1")
               application
                  (Default) = MyProgram
```

 

 



