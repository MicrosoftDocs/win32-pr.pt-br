---
description: A propriedade MsiHiddenProperties pode ser usada para impedir que o instalador exiba senhas ou outras informações confidenciais no arquivo de log.
ms.assetid: 7d5eb9cf-04a5-41bd-9ca9-f30af45ab0a5
title: Propriedade MsiHiddenProperties
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6124f7002edd8ab7d3d5e6691b7b0a322b93c285
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766868"
---
# <a name="msihiddenproperties-property"></a><span data-ttu-id="c3476-103">Propriedade MsiHiddenProperties</span><span class="sxs-lookup"><span data-stu-id="c3476-103">MsiHiddenProperties property</span></span>

<span data-ttu-id="c3476-104">A propriedade **MsiHiddenProperties** pode ser usada para impedir que o instalador exiba senhas ou outras informações confidenciais no arquivo de log.</span><span class="sxs-lookup"><span data-stu-id="c3476-104">The **MsiHiddenProperties** property may be used to prevent the installer from displaying passwords or other confidential information in the log file.</span></span> <span data-ttu-id="c3476-105">Para impedir que uma propriedade seja gravada no arquivo de log, defina o valor da propriedade **MsiHiddenProperties** como o nome da propriedade que você deseja ocultar.</span><span class="sxs-lookup"><span data-stu-id="c3476-105">To prevent a property from being written into the log file, set the value of the **MsiHiddenProperties** property to the name of the property you wish to hide.</span></span> <span data-ttu-id="c3476-106">Você pode ocultar várias propriedades especificando uma cadeia de caracteres de nomes de propriedade delimitada por ponto-e-vírgula (;).</span><span class="sxs-lookup"><span data-stu-id="c3476-106">You can hide multiple properties by specifying a string of property names delimited by semicolons (;).</span></span>

> [!Note]  
> <span data-ttu-id="c3476-107">Quando a política de [depuração](debug.md) for definida com um valor de 7, o instalador gravará as informações inseridas em uma linha de comando no log.</span><span class="sxs-lookup"><span data-stu-id="c3476-107">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="c3476-108">Isso torna as propriedades públicas inseridas em uma linha de comando visíveis, mesmo que a propriedade seja incluída na propriedade **MsiHiddenProperties** .</span><span class="sxs-lookup"><span data-stu-id="c3476-108">This makes public properties entered on a command line visible even if the property is included in the **MsiHiddenProperties** property.</span></span> <span data-ttu-id="c3476-109">Isso pode tornar as informações confidenciais inseridas em uma linha de comando visíveis no log.</span><span class="sxs-lookup"><span data-stu-id="c3476-109">This can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="c3476-110">Para obter mais informações, consulte [impedindo que informações confidenciais sejam gravadas no arquivo de log](preventing-confidential-information-from-being-written-into-the-log-file.md).</span><span class="sxs-lookup"><span data-stu-id="c3476-110">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c3476-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3476-111">Requirements</span></span>



| <span data-ttu-id="c3476-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3476-112">Requirement</span></span> | <span data-ttu-id="c3476-113">Valor</span><span class="sxs-lookup"><span data-stu-id="c3476-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3476-114">Versão</span><span class="sxs-lookup"><span data-stu-id="c3476-114">Version</span></span><br/> | <span data-ttu-id="c3476-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3476-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c3476-116">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3476-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c3476-117">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3476-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c3476-118">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="c3476-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3476-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3476-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3476-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c3476-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




