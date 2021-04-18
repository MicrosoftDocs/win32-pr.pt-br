---
description: O WMI tem vários objetos auxiliares de script que fornecem as conversões exigidas pelos scripts.
ms.assetid: 832660b7-2992-4d1f-af16-7b8f0477b187
ms.tgt_platform: multiple
title: Objetos auxiliares de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 028079e49a2007d99b81f7832c4bce3cb016701d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789398"
---
# <a name="scripting-helper-objects"></a><span data-ttu-id="3ffc6-103">Objetos auxiliares de script</span><span class="sxs-lookup"><span data-stu-id="3ffc6-103">Scripting Helper Objects</span></span>

<span data-ttu-id="3ffc6-104">O WMI tem vários objetos auxiliares de script que fornecem as conversões exigidas pelos scripts.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-104">WMI has several scripting helper objects that supply the conversions required by scripts.</span></span>

<span data-ttu-id="3ffc6-105">Os objetos auxiliares de script WMI incluem:</span><span class="sxs-lookup"><span data-stu-id="3ffc6-105">WMI scripting helper objects include:</span></span>

-   [<span data-ttu-id="3ffc6-106">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="3ffc6-106">**SWbemDateTime**</span></span>](swbemdatetime.md)
-   [<span data-ttu-id="3ffc6-107">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="3ffc6-107">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
-   [<span data-ttu-id="3ffc6-108">**\_SecurityDescriptorHelper Win32**</span><span class="sxs-lookup"><span data-stu-id="3ffc6-108">**Win32\_SecurityDescriptorHelper**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)

<span data-ttu-id="3ffc6-109">Os objetos auxiliares dividem as estruturas de dados compostos para que um script não seja necessário para analisar a estrutura para obter qualquer uma das partes.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-109">The helper objects break down composite data structures so that a script is not required to parse the structure to obtain any of the pieces.</span></span> <span data-ttu-id="3ffc6-110">Por exemplo, a estrutura **DateTime de WMI** não pode ser exibida diretamente e é diferente de outras estruturas de dados DateTime do Windows, como a **\_ Data VT**.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-110">For example, the **WMI DATETIME** structure cannot be displayed directly, and is different from other Windows datetime data structures, such as **VT\_DATE**.</span></span>

## <a name="swbemdatetime"></a><span data-ttu-id="3ffc6-111">SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="3ffc6-111">SWbemDateTime</span></span>

<span data-ttu-id="3ffc6-112">O objeto [**SWbemDateTime**](swbemdatetime.md) fornece propriedades que analisam o dia, o mês, o ano, a hora do dia e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-112">The [**SWbemDateTime**](swbemdatetime.md) object provides properties that parse out the day, month, year, time of day, and so on.</span></span> <span data-ttu-id="3ffc6-113">Ele também fornece métodos de conversão para converter o data e hora de Instrumentação de Gerenciamento do Windows (WMI) de e para os formatos de **\_ Data** e [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) do VT.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-113">It also provides conversion methods to convert the Windows Management Instrumentation (WMI) datetime to and from the **VT\_Date** and [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) formats.</span></span> <span data-ttu-id="3ffc6-114">Para configurações de segurança do Internet Explorer (IE), o objeto **SWbemDateTime** é o único objeto de script WMI que é marcado como seguro para inicialização e seguro para scripts.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-114">For Internet Explorer (IE) security settings, the **SWbemDateTime** object is the only WMI scripting object that is marked safe for initialization and safe for scripting.</span></span> <span data-ttu-id="3ffc6-115">Para obter mais informações e exemplos de conversões de data e hora, consulte [datas e horas](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) e o artigo sobre o TechNet ScriptCenter [é sobre o tempo (Ah, e também sobre datas)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span><span class="sxs-lookup"><span data-stu-id="3ffc6-115">For more information and examples of date and time conversions, see [Dates and Times](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx) and the article on TechNet ScriptCenter [It's About Time (Oh, and About Dates, too)](https://www.microsoft.com/technet/technetmag/issues/2006/07/ScriptingGuy/default.aspx).</span></span>

## <a name="swbemobjectpath"></a><span data-ttu-id="3ffc6-116">SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="3ffc6-116">SWbemObjectPath</span></span>

<span data-ttu-id="3ffc6-117">As propriedades de [**SWbemObjectPath**](swbemobjectpath.md) fornecem o caminho absoluto de um objeto, mas também dividem as partes do caminho do WMI, como servidor, namespace, classe ou caminho relativo.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-117">The properties of [**SWbemObjectPath**](swbemobjectpath.md) supply the absolute path of an object, but also break out the parts of the WMI path, such as server, namespace, class, or relative path.</span></span> <span data-ttu-id="3ffc6-118">O objeto permite que você defina a segurança do caminho, obtenha os valores de chave dos objetos que representam o caminho, determine se um objeto é singleton e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-118">The object allows you to set the security of the path, obtain the key values of the objects representing the path, determine if an object is a singleton, and so on.</span></span> <span data-ttu-id="3ffc6-119">Para obter mais informações sobre como trabalhar com caminhos de objeto WMI, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="3ffc6-119">For more information about working with WMI object paths, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

## <a name="win32_securitydescriptorhelper"></a><span data-ttu-id="3ffc6-120">\_SecurityDescriptorHelper Win32</span><span class="sxs-lookup"><span data-stu-id="3ffc6-120">Win32\_SecurityDescriptorHelper</span></span>

<span data-ttu-id="3ffc6-121">A classe [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) converte o descritor de segurança de um objeto protegível de um formato para outro.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-121">The [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class converts the security descriptor of a securable object from one format to another.</span></span>

<span data-ttu-id="3ffc6-122">Muitos objetos, como impressoras, namespaces WMI, chaves do registro ou aplicativos DCOM, têm descritores de segurança que controlam o acesso ao objeto.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-122">Many objects, such as printers, WMI namespaces, registry keys, or DCOM applications, have security descriptors that control access to the object.</span></span> <span data-ttu-id="3ffc6-123">Você pode usar o WMI para descobrir ou alterar quem tem acesso a esses objetos ao obter ou definir o descritor de segurança associado ao objeto.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-123">You can use WMI to discover or change who has access to these objects by getting or setting the security descriptor associated with the object.</span></span>

<span data-ttu-id="3ffc6-124">No entanto, métodos diferentes podem obter descritores de segurança em uma matriz de bytes binários, no formato SDDL ( [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) ) ou como uma instância do [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span><span class="sxs-lookup"><span data-stu-id="3ffc6-124">However, different methods may obtain security descriptors in a binary byte array, [Security Descriptor Definition Language](/windows/desktop/SecAuthZ/security-descriptor-string-format) (SDDL) format, or as an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span> <span data-ttu-id="3ffc6-125">A forma da matriz de bytes binários de um descritor de segurança não deve ser manipulada, exceto pelos métodos do C++ projetados para [operações de descritor de segurança](/windows/desktop/SecAuthZ/security-descriptor-operations).</span><span class="sxs-lookup"><span data-stu-id="3ffc6-125">The binary byte array form of a security descriptor should not be manipulated except by the C++ methods designed for [Security Descriptor Operations](/windows/desktop/SecAuthZ/security-descriptor-operations).</span></span> <span data-ttu-id="3ffc6-126">Os descritores em SDDL estão em cadeias de caracteres, mas ainda são inconvenientes de manipular.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-126">Descriptors in SDDL are in strings, but are still awkward to manipulate.</span></span> <span data-ttu-id="3ffc6-127">O formato mais fácil de manipular é o **Win32 \_ SecurityDescriptor**, pois ele contém objetos incorporados para Trustee, Ace e Sid.</span><span class="sxs-lookup"><span data-stu-id="3ffc6-127">The easiest format to manipulate is **Win32\_SecurityDescriptor**, because it contains embedded objects for trustee, ACE, and SID.</span></span> <span data-ttu-id="3ffc6-128">Para obter mais informações sobre a estrutura de descritores de segurança no WMI, consulte [objetos do descritor de segurança do WMI](wmi-security-descriptor-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3ffc6-128">For more information about the structure of security descriptors in WMI, see [WMI Security Descriptor Objects](wmi-security-descriptor-objects.md).</span></span> <span data-ttu-id="3ffc6-129">Para obter mais informações sobre como fazer conversões, consulte [alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md).</span><span class="sxs-lookup"><span data-stu-id="3ffc6-129">For more information about how to do conversions, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ffc6-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3ffc6-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ffc6-131">Scripts no WMI</span><span class="sxs-lookup"><span data-stu-id="3ffc6-131">Scripting in WMI</span></span>](/windows/desktop/WmiSdk/creating-a-wmi-script)
</dt> </dl>

 

 
