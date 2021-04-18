---
description: 'Se o pacote de instalação enviado com um aplicativo não estiver na raiz do CD-ROM que os clientes recebem, a propriedade MEDIAPACKAGEPATH deverá ser definida na linha de comando para o caminho relativo do aplicativo no CD-ROM. Por exemplo, se o caminho para o pacote na mídia for E: \\ MYPATH \\My.msi, use MEDIAPACKAGEPATH =&\# 0034; \\ MYPATH \\ & \# 0034;. Os administradores podem criar CD-ROMs de um ponto de instalação administrativa. Se o local da raiz da instalação for alterado nos novos CD-ROMs, a propriedade MEDIAPACKAGEPATH deverá ser definida como o novo caminho a ser instalado dessa mídia. Uma fonte com um local no CD-ROM diferente do que está especificado no pacote é inutilizável. No entanto, não é necessário usar essa propriedade ao criar um ponto de instalação administrativa da mídia de envio.'
ms.assetid: 18b3b19d-28e9-4311-9cc9-3e4224b4ddfe
title: Propriedade MEDIAPACKAGEPATH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91cd35cca81d8f77d16c1766b71443107af9be0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757388"
---
# <a name="mediapackagepath-property"></a><span data-ttu-id="3a618-106">Propriedade MEDIAPACKAGEPATH</span><span class="sxs-lookup"><span data-stu-id="3a618-106">MEDIAPACKAGEPATH property</span></span>

<span data-ttu-id="3a618-107">Se o pacote de instalação enviado com um aplicativo não estiver na raiz do CD-ROM que os clientes recebem, a propriedade **MEDIAPACKAGEPATH** deverá ser definida na linha de comando para o caminho relativo do aplicativo no CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="3a618-107">If the installation package shipping with an application is not at the root of the CD-ROM that customers receive, the **MEDIAPACKAGEPATH** property must be set on the command line to the relative path of the application on the CD-ROM.</span></span>

<span data-ttu-id="3a618-108">Por exemplo, se o caminho para o pacote na mídia for E: \\ MYPATH \\My.msi, então use MEDIAPACKAGEPATH = " \\ MYPATH \\ ".</span><span class="sxs-lookup"><span data-stu-id="3a618-108">For example, if the path to the package on the media is E:\\MyPath\\My.msi, then use MEDIAPACKAGEPATH="\\MyPath\\".</span></span>

<span data-ttu-id="3a618-109">Os administradores podem criar CD-ROMs de um ponto de instalação administrativa.</span><span class="sxs-lookup"><span data-stu-id="3a618-109">Administrators may create CD-ROMs from an administrative installation point.</span></span> <span data-ttu-id="3a618-110">Se o local da raiz da instalação for alterado nos novos CD-ROMs, a propriedade **MEDIAPACKAGEPATH** deverá ser definida como o novo caminho a ser instalado dessa mídia.</span><span class="sxs-lookup"><span data-stu-id="3a618-110">If the location of the root of the installation is changed on the new CD-ROMs, the **MEDIAPACKAGEPATH** property must be set to the new path to install from this media.</span></span> <span data-ttu-id="3a618-111">Uma fonte com um local no CD-ROM diferente do que está especificado no pacote é inutilizável.</span><span class="sxs-lookup"><span data-stu-id="3a618-111">A source with a location on the CD-ROM different than what is specified in the package is unusable.</span></span> <span data-ttu-id="3a618-112">No entanto, não é necessário usar essa propriedade ao criar um ponto de instalação administrativa da mídia de envio.</span><span class="sxs-lookup"><span data-stu-id="3a618-112">It is not necessary, however, to use this property when creating an administrative installation point from shipping media.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a618-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a618-113">Requirements</span></span>



| <span data-ttu-id="3a618-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a618-114">Requirement</span></span> | <span data-ttu-id="3a618-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3a618-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a618-116">Versão</span><span class="sxs-lookup"><span data-stu-id="3a618-116">Version</span></span><br/> | <span data-ttu-id="3a618-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3a618-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3a618-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3a618-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3a618-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3a618-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3a618-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="3a618-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3a618-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a618-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a618-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3a618-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




