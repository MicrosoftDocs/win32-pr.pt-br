---
description: A propriedade ProductElevated do objeto do instalador retornará true se o produto for gerenciado ou false se o produto não for gerenciado.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Instalador::P Propriedade roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751852"
---
# <a name="installerproductelevated-property"></a><span data-ttu-id="496cf-103">Instalador::P Propriedade roductElevated</span><span class="sxs-lookup"><span data-stu-id="496cf-103">Installer::ProductElevated property</span></span>

<span data-ttu-id="496cf-104">A propriedade **ProductElevated** do objeto do [**instalador**](installer-object.md) retornará true se o produto for gerenciado ou false se o produto não for gerenciado.</span><span class="sxs-lookup"><span data-stu-id="496cf-104">The **ProductElevated** property of the [**Installer**](installer-object.md) object returns True if the product is managed or False if the product is not managed.</span></span>

<span data-ttu-id="496cf-105">Esta propriedade é somente para leitura.</span><span class="sxs-lookup"><span data-stu-id="496cf-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="496cf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="496cf-106">Syntax</span></span>


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a><span data-ttu-id="496cf-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="496cf-107">Property value</span></span>

<span data-ttu-id="496cf-108">O GUID do código completo do produto.</span><span class="sxs-lookup"><span data-stu-id="496cf-108">The full product code GUID of the product.</span></span> <span data-ttu-id="496cf-109">Este parâmetro é necessário.</span><span class="sxs-lookup"><span data-stu-id="496cf-109">This parameter is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="496cf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="496cf-110">Remarks</span></span>

<span data-ttu-id="496cf-111">A propriedade **ProductElevated** usa a função [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) .</span><span class="sxs-lookup"><span data-stu-id="496cf-111">The **ProductElevated** property uses the [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) function.</span></span> <span data-ttu-id="496cf-112">O retorno da propriedade não leva em conta a política [AlwaysInstallElevated](alwaysinstallelevated.md) .</span><span class="sxs-lookup"><span data-stu-id="496cf-112">The return of the property does not take into account the [AlwaysInstallElevated](alwaysinstallelevated.md) policy.</span></span>

## <a name="examples"></a><span data-ttu-id="496cf-113">Exemplos</span><span class="sxs-lookup"><span data-stu-id="496cf-113">Examples</span></span>

<span data-ttu-id="496cf-114">O exemplo de script a seguir demonstra o uso da propriedade **ProductElevated** .</span><span class="sxs-lookup"><span data-stu-id="496cf-114">The following sample script demonstrates the use of the **ProductElevated** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a><span data-ttu-id="496cf-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="496cf-115">Requirements</span></span>



| <span data-ttu-id="496cf-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="496cf-116">Requirement</span></span> | <span data-ttu-id="496cf-117">Valor</span><span class="sxs-lookup"><span data-stu-id="496cf-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="496cf-118">Versão</span><span class="sxs-lookup"><span data-stu-id="496cf-118">Version</span></span><br/> | <span data-ttu-id="496cf-119">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="496cf-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="496cf-120">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="496cf-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="496cf-121">Windows Installer 4,5 no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="496cf-121">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="496cf-122">DLL</span><span class="sxs-lookup"><span data-stu-id="496cf-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="496cf-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="496cf-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="496cf-124">IID</span><span class="sxs-lookup"><span data-stu-id="496cf-124">IID</span></span><br/>     | <span data-ttu-id="496cf-125">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="496cf-125">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="496cf-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="496cf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="496cf-127">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="496cf-127">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="496cf-128">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="496cf-128">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




