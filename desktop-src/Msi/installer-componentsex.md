---
description: Retorna um objeto Recordlist que lista os componentes instalados.
ms.assetid: a91656de-2ebc-45b5-86f8-b13f35c6a762
title: Propriedade Installer. ComponentsEx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentsEx
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1a48261a924280999d2b8329d635d4115de35753
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749793"
---
# <a name="installercomponentsex-property"></a><span data-ttu-id="4f5ac-103">Propriedade Installer. ComponentsEx</span><span class="sxs-lookup"><span data-stu-id="4f5ac-103">Installer.ComponentsEx property</span></span>

<span data-ttu-id="4f5ac-104">Essa propriedade retorna um objeto [**recordlist**](recordlist-object.md) que lista os componentes instalados.</span><span class="sxs-lookup"><span data-stu-id="4f5ac-104">This property returns a [**RecordList**](recordlist-object.md) object that lists installed components.</span></span> <span data-ttu-id="4f5ac-105">Essa propriedade chama [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span><span class="sxs-lookup"><span data-stu-id="4f5ac-105">This property calls [**MsiEnumComponentsEx**](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa).</span></span>

<span data-ttu-id="4f5ac-106">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="4f5ac-106">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="4f5ac-107">Essa propriedade está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="4f5ac-107">This property is available beginning with Windows Installer 5.0.</span></span>

<span data-ttu-id="4f5ac-108">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="4f5ac-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f5ac-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f5ac-109">Syntax</span></span>


```JScript
propVal = Installer.ComponentsEx
```



## <a name="property-value"></a><span data-ttu-id="4f5ac-110">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="4f5ac-110">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="4f5ac-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f5ac-111">Requirements</span></span>



| <span data-ttu-id="4f5ac-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f5ac-112">Requirement</span></span> | <span data-ttu-id="4f5ac-113">Valor</span><span class="sxs-lookup"><span data-stu-id="4f5ac-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f5ac-114">Versão</span><span class="sxs-lookup"><span data-stu-id="4f5ac-114">Version</span></span><br/> | <span data-ttu-id="4f5ac-115">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7</span><span class="sxs-lookup"><span data-stu-id="4f5ac-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7</span></span><br/> |
| <span data-ttu-id="4f5ac-116">DLL</span><span class="sxs-lookup"><span data-stu-id="4f5ac-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f5ac-117"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f5ac-117"><dt>Msi.dll</dt></span></span> </dl>                      |
| <span data-ttu-id="4f5ac-118">IID</span><span class="sxs-lookup"><span data-stu-id="4f5ac-118">IID</span></span><br/>     | <span data-ttu-id="4f5ac-119">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="4f5ac-119">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="4f5ac-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f5ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f5ac-121">**MsiEnumComponentsEx**</span><span class="sxs-lookup"><span data-stu-id="4f5ac-121">**MsiEnumComponentsEx**</span></span>](/windows/desktop/api/Msi/nf-msi-msienumcomponentsexa)
</dt> </dl>

 

 




