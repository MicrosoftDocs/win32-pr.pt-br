---
description: Retorna um objeto Recordlist que fornece o caminho completo de um componente instalado especificado.
ms.assetid: 0f4f9d21-f1cc-44fd-a22f-1b6f055fef9e
title: Propriedade Installer. ComponentPathEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPathEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b7bf98dd8e7a81a0dd261f22a565bec8298a86a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747547"
---
# <a name="installercomponentpathex-property"></a><span data-ttu-id="eb052-103">Propriedade Installer. ComponentPathEx</span><span class="sxs-lookup"><span data-stu-id="eb052-103">Installer.ComponentPathEx property</span></span>

<span data-ttu-id="eb052-104">Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que fornece o caminho completo de um componente instalado especificado.</span><span class="sxs-lookup"><span data-stu-id="eb052-104">This property returns a [**RecordList**](recordlist-object.md) object that gives the full path of a specified installed component.</span></span> <span data-ttu-id="eb052-105">Essa propriedade chama [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span><span class="sxs-lookup"><span data-stu-id="eb052-105">This property calls [**MsiGetComponentPathEx**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa).</span></span>

<span data-ttu-id="eb052-106">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="eb052-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="eb052-107">Essa propriedade está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="eb052-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="eb052-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="eb052-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb052-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb052-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentPathEx
```



## <a name="property-value"></a><span data-ttu-id="eb052-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="eb052-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="eb052-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb052-111">Requirements</span></span>



| <span data-ttu-id="eb052-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb052-112">Requirement</span></span> | <span data-ttu-id="eb052-113">Valor</span><span class="sxs-lookup"><span data-stu-id="eb052-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb052-114">Versão</span><span class="sxs-lookup"><span data-stu-id="eb052-114">Version</span></span><br/> | <span data-ttu-id="eb052-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="eb052-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="eb052-116">DLL</span><span class="sxs-lookup"><span data-stu-id="eb052-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="eb052-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb052-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="eb052-118">IID</span><span class="sxs-lookup"><span data-stu-id="eb052-118">IID</span></span><br/>     | <span data-ttu-id="eb052-119">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="eb052-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="eb052-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb052-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb052-121">**MsiGetComponentPathEx**</span><span class="sxs-lookup"><span data-stu-id="eb052-121">**MsiGetComponentPathEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msigetcomponentpathexa)
</dt> </dl>

 

 




