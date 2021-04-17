---
description: Definir a propriedade SHORTFILENAMES faz com que nomes de arquivo curtos sejam usados para os nomes dos arquivos de destino, em vez de nomes de arquivo longos. Ele não afeta os nomes de arquivo que o instalador procura na origem.
ms.assetid: b330f9c3-3297-45cf-915c-5fbb291b8afb
title: Propriedade SHORTFILENAMES
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e347e5ec400a1593858f0cac558f33528e25396e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752837"
---
# <a name="shortfilenames-property"></a><span data-ttu-id="e2f63-104">Propriedade SHORTFILENAMES</span><span class="sxs-lookup"><span data-stu-id="e2f63-104">SHORTFILENAMES property</span></span>

<span data-ttu-id="e2f63-105">Definir a propriedade **SHORTFILENAMES** faz com que nomes de arquivo curtos sejam usados para os nomes dos arquivos de destino, em vez de nomes de arquivo longos.</span><span class="sxs-lookup"><span data-stu-id="e2f63-105">Setting the **SHORTFILENAMES** property causes short file names to be used for the names of target files, rather than long file names.</span></span> <span data-ttu-id="e2f63-106">Ele não afeta os nomes de arquivo que o instalador procura na origem.</span><span class="sxs-lookup"><span data-stu-id="e2f63-106">It does not affect the file names the installer looks for at the source.</span></span>

## <a name="default-value"></a><span data-ttu-id="e2f63-107">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="e2f63-107">Default Value</span></span>

<span data-ttu-id="e2f63-108">Nomes longos são usados pelo instalador se a propriedade **SHORTFILENAMES** não estiver definida e o volume de destino der suporte a nomes longos.</span><span class="sxs-lookup"><span data-stu-id="e2f63-108">Long names are used by the installer if the **SHORTFILENAMES** property is not set and the target volume supports long names.</span></span> <span data-ttu-id="e2f63-109">Nomes curtos são usados pelo instalador se o volume de destino não oferecer suporte a nomes longos.</span><span class="sxs-lookup"><span data-stu-id="e2f63-109">Short names are used by the installer if the target volume does not support long names.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f63-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2f63-110">Remarks</span></span>

<span data-ttu-id="e2f63-111">Quando a propriedade **SHORTFILENAMES** é definida, o instalador cria pastas e instala arquivos usando nomes de arquivo curtos a partir de qualquer par pequeno de \| pares listados na tabela de [arquivos](file-table.md) ou no [diretório](directory-table.md).</span><span class="sxs-lookup"><span data-stu-id="e2f63-111">When the **SHORTFILENAMES** property is set, the installer creates folders and installs files using short file names from any short\|long pairs listed in the [File table](file-table.md) or [Directory table](directory-table.md).</span></span>

<span data-ttu-id="e2f63-112">Os aplicativos podem usar a função [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) para recuperar a forma de caminho curto de um caminho de arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e2f63-112">Applications can use the [**GetShortPathName**](/windows/win32/api/fileapi/nf-fileapi-getshortpathnamew) function to retrieve the short path form of a specified file path.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f63-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2f63-113">Requirements</span></span>



| <span data-ttu-id="e2f63-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2f63-114">Requirement</span></span> | <span data-ttu-id="e2f63-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e2f63-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f63-116">Versão</span><span class="sxs-lookup"><span data-stu-id="e2f63-116">Version</span></span><br/> | <span data-ttu-id="e2f63-117">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e2f63-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e2f63-118">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e2f63-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e2f63-119">Windows Installer no Windows Server 2003 ou no Windows XP.</span><span class="sxs-lookup"><span data-stu-id="e2f63-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e2f63-120">Consulte os [requisitos de Run-Time Windows Installer](windows-installer-portal.md) para obter informações sobre a Service Pack mínima do Windows exigida por uma versão Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e2f63-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e2f63-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2f63-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f63-122">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e2f63-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 
