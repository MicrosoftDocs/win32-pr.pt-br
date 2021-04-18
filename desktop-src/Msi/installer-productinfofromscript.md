---
description: A propriedade ProductInfoFromScript do objeto do instalador retorna o valor do atributo especificado que é armazenado em um script de anúncio.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Instalador::P Propriedade roductInfoFromScript
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752640"
---
# <a name="installerproductinfofromscript-property"></a><span data-ttu-id="7b1be-103">Instalador::P Propriedade roductInfoFromScript</span><span class="sxs-lookup"><span data-stu-id="7b1be-103">Installer::ProductInfoFromScript property</span></span>

<span data-ttu-id="7b1be-104">A propriedade **ProductInfoFromScript** do objeto do [**instalador**](installer-object.md) retorna o valor do atributo especificado que é armazenado em um script de anúncio.</span><span class="sxs-lookup"><span data-stu-id="7b1be-104">The **ProductInfoFromScript** property of the [**Installer**](installer-object.md) object returns the value of the specified attribute that is stored in an advertise script.</span></span>

<span data-ttu-id="7b1be-105">Essa propriedade é somente gravação.</span><span class="sxs-lookup"><span data-stu-id="7b1be-105">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b1be-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b1be-106">Syntax</span></span>


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a><span data-ttu-id="7b1be-107">Valor da propriedade</span><span class="sxs-lookup"><span data-stu-id="7b1be-107">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="7b1be-108">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="7b1be-108">Error codes</span></span>

<span data-ttu-id="7b1be-109">Uma cadeia de caracteres ou um valor inteiro, dependendo do atributo solicitado.</span><span class="sxs-lookup"><span data-stu-id="7b1be-109">A string or integer value depending upon requested attribute.</span></span>

## <a name="remarks"></a><span data-ttu-id="7b1be-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7b1be-110">Remarks</span></span>

<span data-ttu-id="7b1be-111">A propriedade **ProductInfoFromScript** usa a função [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .</span><span class="sxs-lookup"><span data-stu-id="7b1be-111">The **ProductInfoFromScript** property uses the [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) function.</span></span>

## <a name="examples"></a><span data-ttu-id="7b1be-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7b1be-112">Examples</span></span>

<span data-ttu-id="7b1be-113">O exemplo de script a seguir demonstra o uso da propriedade **ProductInfoFromScript** .</span><span class="sxs-lookup"><span data-stu-id="7b1be-113">The following sample script demonstrates the use of the **ProductInfoFromScript** property .</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a><span data-ttu-id="7b1be-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7b1be-114">Requirements</span></span>



| <span data-ttu-id="7b1be-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b1be-115">Requirement</span></span> | <span data-ttu-id="7b1be-116">Valor</span><span class="sxs-lookup"><span data-stu-id="7b1be-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b1be-117">Versão</span><span class="sxs-lookup"><span data-stu-id="7b1be-117">Version</span></span><br/> | <span data-ttu-id="7b1be-118">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7b1be-118">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7b1be-119">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7b1be-119">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7b1be-120">Windows Installer 4,5 no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="7b1be-120">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="7b1be-121">DLL</span><span class="sxs-lookup"><span data-stu-id="7b1be-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="7b1be-122"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b1be-122"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="7b1be-123">IID</span><span class="sxs-lookup"><span data-stu-id="7b1be-123">IID</span></span><br/>     | <span data-ttu-id="7b1be-124">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="7b1be-124">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="7b1be-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="7b1be-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b1be-126">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="7b1be-126">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="7b1be-127">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="7b1be-127">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




