---
description: Você pode criar um objeto para WMI em Visual Basic Scripting Edition (VBScript) conectando-se ao WMI e chamando CreateObject. A tabela a seguir lista os métodos na API de script para WMI que dão suporte à criação de objetos.
ms.assetid: 3acbce31-6d56-4a7a-af03-fa37b2b868be
ms.tgt_platform: multiple
title: Criando um objeto usando o VBScript
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6bfbb4753f19f8ed6f7a61d94ab1d9f03b57e091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104461218"
---
# <a name="creating-an-object-using-vbscript"></a><span data-ttu-id="8c99a-104">Criando um objeto usando o VBScript</span><span class="sxs-lookup"><span data-stu-id="8c99a-104">Creating an Object Using VBScript</span></span>

<span data-ttu-id="8c99a-105">Você pode criar um objeto para WMI em Visual Basic Scripting Edition (VBScript) conectando-se ao WMI e chamando [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8c99a-105">You can create an object for WMI in Visual Basic Scripting Edition (VBScript) by connecting to WMI and then calling [CreateObject](/previous-versions//xzysf6hc(v=vs.85)).</span></span> <span data-ttu-id="8c99a-106">A tabela a seguir lista os métodos na API de script para WMI que dão suporte à criação de objetos.</span><span class="sxs-lookup"><span data-stu-id="8c99a-106">The following table lists the methods in the Scripting API for WMI that support object creation.</span></span>



| <span data-ttu-id="8c99a-107">Interface</span><span class="sxs-lookup"><span data-stu-id="8c99a-107">Interface</span></span>                                        | <span data-ttu-id="8c99a-108">ProgID</span><span class="sxs-lookup"><span data-stu-id="8c99a-108">ProgID</span></span>                             |
|--------------------------------------------------|------------------------------------|
| [<span data-ttu-id="8c99a-109">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="8c99a-109">**SWbemDateTime**</span></span>](swbemdatetime.md)           | <span data-ttu-id="8c99a-110">"WbemScripting. SwbemDateTime"</span><span class="sxs-lookup"><span data-stu-id="8c99a-110">"WbemScripting.SwbemDateTime"</span></span>      |
| [<span data-ttu-id="8c99a-111">**SWbemLocator**</span><span class="sxs-lookup"><span data-stu-id="8c99a-111">**SWbemLocator**</span></span>](swbemlocator.md)             | <span data-ttu-id="8c99a-112">"WbemScripting. SWbemLocator"</span><span class="sxs-lookup"><span data-stu-id="8c99a-112">"WbemScripting.SWbemLocator"</span></span>       |
| [<span data-ttu-id="8c99a-113">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="8c99a-113">**SWbemLastError**</span></span>](swbemlasterror.md)         | <span data-ttu-id="8c99a-114">"WbemScripting. SWbem. LastError"</span><span class="sxs-lookup"><span data-stu-id="8c99a-114">"WbemScripting.SWbem.LastError"</span></span>    |
| [<span data-ttu-id="8c99a-115">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="8c99a-115">**SWbemObjectPath**</span></span>](swbemobjectpath.md)       | <span data-ttu-id="8c99a-116">"WbemScripting.SWbemObjectPath"</span><span class="sxs-lookup"><span data-stu-id="8c99a-116">"WbemScripting.SWbemObjectPath"</span></span>    |
| [<span data-ttu-id="8c99a-117">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="8c99a-117">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md) | <span data-ttu-id="8c99a-118">"WbemScripting.SWbemNamedValueSet"</span><span class="sxs-lookup"><span data-stu-id="8c99a-118">"WbemScripting.SWbemNamedValueSet"</span></span> |
| [<span data-ttu-id="8c99a-119">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="8c99a-119">**SWbemRefresher**</span></span>](swbemrefresher.md)         | <span data-ttu-id="8c99a-120">"WbemScripting.SWbemRefresher"</span><span class="sxs-lookup"><span data-stu-id="8c99a-120">"WbemScripting.SWbemRefresher"</span></span>     |
| [<span data-ttu-id="8c99a-121">**SWbemSink**</span><span class="sxs-lookup"><span data-stu-id="8c99a-121">**SWbemSink**</span></span>](swbemsink.md)                   | <span data-ttu-id="8c99a-122">"WbemScripting. SWbemSink"</span><span class="sxs-lookup"><span data-stu-id="8c99a-122">"WbemScripting.SWbemSink"</span></span>          |



 

<span data-ttu-id="8c99a-123">O procedimento a seguir descreve como criar um objeto WMI usando o VBScript.</span><span class="sxs-lookup"><span data-stu-id="8c99a-123">The following procedure describes how to create a WMI object using VBScript.</span></span>

<span data-ttu-id="8c99a-124">**Para criar um objeto WMI usando o VBScript**</span><span class="sxs-lookup"><span data-stu-id="8c99a-124">**To create a WMI object using VBScript**</span></span>

1.  <span data-ttu-id="8c99a-125">Conecte-se ao WMI usando um moniker ou um objeto [**SWbemLocator**](swbemlocator.md) .</span><span class="sxs-lookup"><span data-stu-id="8c99a-125">Connect to WMI using either a moniker or an [**SWbemLocator**](swbemlocator.md) object.</span></span>

    <span data-ttu-id="8c99a-126">Para obter mais informações, consulte [criando um script WMI](creating-a-wmi-script.md).</span><span class="sxs-lookup"><span data-stu-id="8c99a-126">For more information, see [Creating a WMI Script](creating-a-wmi-script.md).</span></span>

2.  <span data-ttu-id="8c99a-127">Faça uma chamada para o método [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) do VBScript.</span><span class="sxs-lookup"><span data-stu-id="8c99a-127">Make a call to the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method.</span></span>

    <span data-ttu-id="8c99a-128">O exemplo de código a seguir mostra como criar um objeto.</span><span class="sxs-lookup"><span data-stu-id="8c99a-128">The following code example shows how to create an object.</span></span>

    ```VB
    Set locator = CreateObject("WbemScripting.SWbemLocator")
    ```

    

    <span data-ttu-id="8c99a-129">Se você usar um moniker na etapa 1, não precisará chamar [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) novamente.</span><span class="sxs-lookup"><span data-stu-id="8c99a-129">If you use a moniker in Step 1, you do not need to call [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) again.</span></span>

 

 
