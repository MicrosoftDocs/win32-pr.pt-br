---
description: A propriedade SourceDir é o diretório raiz que contém o arquivo de gabinete de origem ou a árvore do arquivo de origem do pacote de instalação. Esse valor é usado para a resolução de diretório.
ms.assetid: 900b26e8-80dd-4e70-8d79-37f09a0c6e86
title: Propriedade SourceDir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a366e4afecdd16722a06ecfbec08552baab8f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759374"
---
# <a name="sourcedir-property"></a><span data-ttu-id="ff512-104">Propriedade SourceDir</span><span class="sxs-lookup"><span data-stu-id="ff512-104">SourceDir property</span></span>

<span data-ttu-id="ff512-105">A propriedade **SourceDir** é o diretório raiz que contém o arquivo de gabinete de origem ou a árvore do arquivo de origem do pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="ff512-105">The **SourceDir** property is the root directory that contains the source cabinet file or the source file tree of the installation package.</span></span> <span data-ttu-id="ff512-106">Esse valor é usado para a resolução de diretório.</span><span class="sxs-lookup"><span data-stu-id="ff512-106">This value is used for directory resolution.</span></span>

## <a name="default-value"></a><span data-ttu-id="ff512-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="ff512-107">Default Value</span></span>

<span data-ttu-id="ff512-108">O diretório que contém o pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="ff512-108">The directory that contains the installation package.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff512-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff512-109">Remarks</span></span>

<span data-ttu-id="ff512-110">A [ação de resolução](resolvesource-action.md) deve ser chamada antes de usar a **Propriedade SourceDir** em qualquer expressão ou tentar recuperar o valor de **SourceDir** com [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span><span class="sxs-lookup"><span data-stu-id="ff512-110">The [ResolveSource action](resolvesource-action.md) must be called before using the **SourceDir** property in any expression or attempting to retrieve the value of **SourceDir** with [**MsiGetProperty**](/windows/desktop/api/Msiquery/nf-msiquery-msigetpropertya).</span></span> <span data-ttu-id="ff512-111">A ação de resolução não deve ser executada enquanto a origem não estiver disponível, como ao desinstalar um aplicativo, pois isso pode causar um aviso indesejado para a mídia de origem.</span><span class="sxs-lookup"><span data-stu-id="ff512-111">The ResolveSource action should not be run while the source is unavailable, such as when uninstalling an application, because this can cause an unintended prompt for the source media.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff512-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ff512-112">Requirements</span></span>



| <span data-ttu-id="ff512-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ff512-113">Requirement</span></span> | <span data-ttu-id="ff512-114">Valor</span><span class="sxs-lookup"><span data-stu-id="ff512-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff512-115">Versão</span><span class="sxs-lookup"><span data-stu-id="ff512-115">Version</span></span><br/> | <span data-ttu-id="ff512-116">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ff512-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ff512-117">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ff512-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ff512-118">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ff512-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ff512-119">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="ff512-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff512-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ff512-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff512-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ff512-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




