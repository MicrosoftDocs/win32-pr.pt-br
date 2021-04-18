---
description: O método AdvertiseProduct do objeto do instalador anuncia um pacote de instalação.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Método Installer:: AdvertiseProduct'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751855"
---
# <a name="installeradvertiseproduct-method"></a><span data-ttu-id="055d0-103">Método Installer:: AdvertiseProduct</span><span class="sxs-lookup"><span data-stu-id="055d0-103">Installer::AdvertiseProduct method</span></span>

<span data-ttu-id="055d0-104">O método **AdvertiseProduct** do objeto do [**instalador**](installer-object.md) anuncia um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="055d0-104">The **AdvertiseProduct** method of the [**Installer**](installer-object.md) object advertises an installation package.</span></span>

## <a name="syntax"></a><span data-ttu-id="055d0-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="055d0-105">Syntax</span></span>


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="055d0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="055d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="055d0-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="055d0-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="055d0-108">O caminho completo para o pacote de Windows Installer (. msi) a ser anunciado.</span><span class="sxs-lookup"><span data-stu-id="055d0-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="055d0-109">*contexto*</span><span class="sxs-lookup"><span data-stu-id="055d0-109">*context*</span></span> 
</dt> <dd>

<span data-ttu-id="055d0-110">O contexto do anúncio.</span><span class="sxs-lookup"><span data-stu-id="055d0-110">The context of the advertisement.</span></span> <span data-ttu-id="055d0-111">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="055d0-111">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="055d0-112">Valor</span><span class="sxs-lookup"><span data-stu-id="055d0-112">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="055d0-113">Significado</span><span class="sxs-lookup"><span data-stu-id="055d0-113">Meaning</span></span>                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <span data-ttu-id="055d0-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="055d0-114"><dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="055d0-115">Anuncia o aplicativo para uma [instalação no contexto de instalações](installation-context.md)por máquina.</span><span class="sxs-lookup"><span data-stu-id="055d0-115">Advertises the application for an instalation in the per-machine [installation context](installation-context.md).</span></span> <span data-ttu-id="055d0-116">Isso torna o pacote disponível para instalação por todos os usuários do computador.</span><span class="sxs-lookup"><span data-stu-id="055d0-116">This makes the package available for installation by all users of the computer.</span></span><br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <span data-ttu-id="055d0-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="055d0-117"><dt>**msiAdvertiseProductUser**</dt> <dt>1</dt></span></span> </dl>             | <span data-ttu-id="055d0-118">Anuncia o aplicativo para uma instalação no [contexto de instalação](installation-context.md)por usuário.</span><span class="sxs-lookup"><span data-stu-id="055d0-118">Advertises the application for an installation in the per-user [installation context](installation-context.md).</span></span><br/>                                                                                   |



 

</dd> <dt>

<span data-ttu-id="055d0-119">*transformações*</span><span class="sxs-lookup"><span data-stu-id="055d0-119">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="055d0-120">A lista de transformações a ser aplicada ao produto.</span><span class="sxs-lookup"><span data-stu-id="055d0-120">The list of transforms to apply to the product.</span></span> <span data-ttu-id="055d0-121">As transformações na lista são delimitadas por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="055d0-121">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="055d0-122">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="055d0-122">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="055d0-123">*linguagem*</span><span class="sxs-lookup"><span data-stu-id="055d0-123">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="055d0-124">O idioma do pacote de instalação a ser usado.</span><span class="sxs-lookup"><span data-stu-id="055d0-124">The language of the installation package to use.</span></span> <span data-ttu-id="055d0-125">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="055d0-125">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="055d0-126">*options*</span><span class="sxs-lookup"><span data-stu-id="055d0-126">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="055d0-127">As opções de anúncio.</span><span class="sxs-lookup"><span data-stu-id="055d0-127">The advertisement options.</span></span> <span data-ttu-id="055d0-128">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="055d0-128">This parameter is optional.</span></span> <span data-ttu-id="055d0-129">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="055d0-129">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="055d0-130">Valor</span><span class="sxs-lookup"><span data-stu-id="055d0-130">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="055d0-131">Significado</span><span class="sxs-lookup"><span data-stu-id="055d0-131">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="055d0-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="055d0-132"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="055d0-133">Anúncio padrão</span><span class="sxs-lookup"><span data-stu-id="055d0-133">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="055d0-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="055d0-134"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="055d0-135">Anuncia uma nova instância do produto.</span><span class="sxs-lookup"><span data-stu-id="055d0-135">Advertises a new instance of the product.</span></span> <span data-ttu-id="055d0-136">Requer que a primeira transformação na lista de transformação do parâmetro *transformações* seja a transformação de instância que altera o código do produto.</span><span class="sxs-lookup"><span data-stu-id="055d0-136">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="055d0-137">Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="055d0-137">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="055d0-138">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="055d0-138">Return value</span></span>

<span data-ttu-id="055d0-139">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="055d0-139">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="055d0-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="055d0-140">Remarks</span></span>

<span data-ttu-id="055d0-141">O método **AdvertiseProduct** usa a função [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="055d0-141">The **AdvertiseProduct** method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="055d0-142">Exemplos</span><span class="sxs-lookup"><span data-stu-id="055d0-142">Examples</span></span>

<span data-ttu-id="055d0-143">O exemplo a seguir demonstra o uso do método **AdvertiseProduct** .</span><span class="sxs-lookup"><span data-stu-id="055d0-143">The following example demonstrates the use of the **AdvertiseProduct** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
```



## <a name="requirements"></a><span data-ttu-id="055d0-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="055d0-144">Requirements</span></span>



| <span data-ttu-id="055d0-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="055d0-145">Requirement</span></span> | <span data-ttu-id="055d0-146">Valor</span><span class="sxs-lookup"><span data-stu-id="055d0-146">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="055d0-147">Versão</span><span class="sxs-lookup"><span data-stu-id="055d0-147">Version</span></span><br/> | <span data-ttu-id="055d0-148">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="055d0-148">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="055d0-149">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="055d0-149">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="055d0-150">Windows Installer 4,5 no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="055d0-150">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="055d0-151">DLL</span><span class="sxs-lookup"><span data-stu-id="055d0-151">DLL</span></span><br/>     | <dl> <span data-ttu-id="055d0-152"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="055d0-152"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="055d0-153">IID</span><span class="sxs-lookup"><span data-stu-id="055d0-153">IID</span></span><br/>     | <span data-ttu-id="055d0-154">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="055d0-154">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="055d0-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="055d0-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="055d0-156">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="055d0-156">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="055d0-157">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="055d0-157">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




