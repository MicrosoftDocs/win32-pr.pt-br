---
description: O método CreateAdvertiseScript do objeto do instalador gera um script de anúncio.
ms.assetid: 32a331e5-d291-49cd-ab0e-7d0e4d72a95b
title: 'Método Installer:: CreateAdvertiseScript'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateAdvertiseScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9ec4b18eee376e7bde4824a497ea14b503045f43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748982"
---
# <a name="installercreateadvertisescript-method"></a><span data-ttu-id="0e57a-103">Método Installer:: CreateAdvertiseScript</span><span class="sxs-lookup"><span data-stu-id="0e57a-103">Installer::CreateAdvertiseScript method</span></span>

<span data-ttu-id="0e57a-104">O método **CreateAdvertiseScript** do objeto do [**instalador**](installer-object.md) gera um script de anúncio.</span><span class="sxs-lookup"><span data-stu-id="0e57a-104">The **CreateAdvertiseScript** method of the [**Installer**](installer-object.md) object generates an advertise script.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e57a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0e57a-105">Syntax</span></span>


```JScript
.CreateAdvertiseScript(
  packagePath,
  scriptFilePath,
  transforms,
  language,
  platform,
  options
)
```



## <a name="parameters"></a><span data-ttu-id="0e57a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e57a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e57a-107">*packagePath*</span><span class="sxs-lookup"><span data-stu-id="0e57a-107">*packagePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0e57a-108">O caminho completo para o pacote de Windows Installer (. msi) a ser anunciado.</span><span class="sxs-lookup"><span data-stu-id="0e57a-108">The full path to the Windows Installer package (.msi) to be advertised.</span></span>

</dd> <dt>

<span data-ttu-id="0e57a-109">*scriptFilePath*</span><span class="sxs-lookup"><span data-stu-id="0e57a-109">*scriptFilePath*</span></span> 
</dt> <dd>

<span data-ttu-id="0e57a-110">O caminho completo para o arquivo de script a ser criado com as informações anunciadas.</span><span class="sxs-lookup"><span data-stu-id="0e57a-110">The full path to the script file to be created with the advertised information.</span></span>

</dd> <dt>

<span data-ttu-id="0e57a-111">*transformações*</span><span class="sxs-lookup"><span data-stu-id="0e57a-111">*transforms*</span></span> 
</dt> <dd>

<span data-ttu-id="0e57a-112">A lista de transformações a ser aplicada ao produto.</span><span class="sxs-lookup"><span data-stu-id="0e57a-112">The list of transforms to apply to the product.</span></span> <span data-ttu-id="0e57a-113">As transformações na lista são delimitadas por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="0e57a-113">Transforms in the list are delimited by semicolons.</span></span> <span data-ttu-id="0e57a-114">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0e57a-114">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="0e57a-115">*linguagem*</span><span class="sxs-lookup"><span data-stu-id="0e57a-115">*language*</span></span> 
</dt> <dd>

<span data-ttu-id="0e57a-116">O idioma do pacote de instalação a ser usado.</span><span class="sxs-lookup"><span data-stu-id="0e57a-116">The language of the installation package to use.</span></span> <span data-ttu-id="0e57a-117">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0e57a-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="0e57a-118">*platform*</span><span class="sxs-lookup"><span data-stu-id="0e57a-118">*platform*</span></span> 
</dt> <dd>

<span data-ttu-id="0e57a-119">Esse parâmetro especifica para qual plataforma o instalador deve criar o script.</span><span class="sxs-lookup"><span data-stu-id="0e57a-119">This parameter specifies for which platform the installer should create the script.</span></span> <span data-ttu-id="0e57a-120">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e57a-120">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="0e57a-121">Valor</span><span class="sxs-lookup"><span data-stu-id="0e57a-121">Value</span></span>                                                                                                                                                                                                                                                                                                       | <span data-ttu-id="0e57a-122">Significado</span><span class="sxs-lookup"><span data-stu-id="0e57a-122">Meaning</span></span>                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="msiAdvertiseCurrentPlatform"></span><span id="msiadvertisecurrentplatform"></span><span id="MSIADVERTISECURRENTPLATFORM"></span><dl> <span data-ttu-id="0e57a-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-123"><dt>**msiAdvertiseCurrentPlatform**</dt> <dt>0</dt></span></span> </dl> | <span data-ttu-id="0e57a-124">Cria um script para a plataforma atual.</span><span class="sxs-lookup"><span data-stu-id="0e57a-124">Creates a script for the current platform.</span></span><br/>  |
| <span id="msiAdvertiseX86Platform"></span><span id="msiadvertisex86platform"></span><span id="MSIADVERTISEX86PLATFORM"></span><dl> <span data-ttu-id="0e57a-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-125"><dt>**msiAdvertiseX86Platform**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="0e57a-126">Cria um script para a plataforma x86.</span><span class="sxs-lookup"><span data-stu-id="0e57a-126">Creates a script for the x86 platform.</span></span><br/>      |
| <span id="msiAdvertiseIA64Platform"></span><span id="msiadvertiseia64platform"></span><span id="MSIADVERTISEIA64PLATFORM"></span><dl> <span data-ttu-id="0e57a-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-127"><dt>**msiAdvertiseIA64Platform**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="0e57a-128">Cria um script para sistemas baseados em Itanium.</span><span class="sxs-lookup"><span data-stu-id="0e57a-128">Creates a script for Itanium-based systems.</span></span><br/> |
| <span id="msiAdvertiseX64Platform"></span><span id="msiadvertisex64platform"></span><span id="MSIADVERTISEX64PLATFORM"></span><dl> <span data-ttu-id="0e57a-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-129"><dt>**msiAdvertiseX64Platform**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="0e57a-130">Cria um script para a plataforma x64.</span><span class="sxs-lookup"><span data-stu-id="0e57a-130">Creates a script for the x64 platform.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="0e57a-131">*options*</span><span class="sxs-lookup"><span data-stu-id="0e57a-131">*options*</span></span> 
</dt> <dd>

<span data-ttu-id="0e57a-132">Opções de anúncio.</span><span class="sxs-lookup"><span data-stu-id="0e57a-132">Advertisement options.</span></span> <span data-ttu-id="0e57a-133">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0e57a-133">This parameter is optional.</span></span> <span data-ttu-id="0e57a-134">Esse parâmetro pode usar um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="0e57a-134">This parameter can be one of the following values.</span></span> <span data-ttu-id="0e57a-135">Esse parâmetro é opcional.</span><span class="sxs-lookup"><span data-stu-id="0e57a-135">This parameter is optional.</span></span>



| <span data-ttu-id="0e57a-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0e57a-136">Value</span></span>                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="0e57a-137">Significado</span><span class="sxs-lookup"><span data-stu-id="0e57a-137">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <span data-ttu-id="0e57a-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-138"><dt>**msiAdvertiseDefault**</dt> <dt>0</dt></span></span> </dl>                             | <span data-ttu-id="0e57a-139">Anúncio padrão</span><span class="sxs-lookup"><span data-stu-id="0e57a-139">Standard advertisement</span></span><br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <span data-ttu-id="0e57a-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-140"><dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="0e57a-141">Anuncia uma nova instância do produto.</span><span class="sxs-lookup"><span data-stu-id="0e57a-141">Advertises a new instance of the product.</span></span> <span data-ttu-id="0e57a-142">Requer que a primeira transformação na lista de transformação do parâmetro *transformações* seja a transformação de instância que altera o código do produto.</span><span class="sxs-lookup"><span data-stu-id="0e57a-142">Requires that the first transform in the transform list of the *transforms* parameter be the instance transform that changes the product code.</span></span> <span data-ttu-id="0e57a-143">Para obter mais informações, consulte [Instalando várias instâncias de produtos e patches](installing-multiple-instances-of-products-and-patches.md).</span><span class="sxs-lookup"><span data-stu-id="0e57a-143">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md).</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e57a-144">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0e57a-144">Return value</span></span>

<span data-ttu-id="0e57a-145">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="0e57a-145">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e57a-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e57a-146">Remarks</span></span>

<span data-ttu-id="0e57a-147">O método [**AdvertiseProduct**](installer-advertiseproduct.md) usa a função [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .</span><span class="sxs-lookup"><span data-stu-id="0e57a-147">The [**AdvertiseProduct**](installer-advertiseproduct.md) method uses the [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) function.</span></span>

## <a name="examples"></a><span data-ttu-id="0e57a-148">Exemplos</span><span class="sxs-lookup"><span data-stu-id="0e57a-148">Examples</span></span>

<span data-ttu-id="0e57a-149">O exemplo a seguir demonstra o uso do método **CreateAdvertiseScript** .</span><span class="sxs-lookup"><span data-stu-id="0e57a-149">The following example demonstrates the use of the **CreateAdvertiseScript** method.</span></span>


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Create an advertise script for Orca
'

Installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scripts\orca.aas"
```



## <a name="requirements"></a><span data-ttu-id="0e57a-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e57a-150">Requirements</span></span>



| <span data-ttu-id="0e57a-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e57a-151">Requirement</span></span> | <span data-ttu-id="0e57a-152">Valor</span><span class="sxs-lookup"><span data-stu-id="0e57a-152">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e57a-153">Versão</span><span class="sxs-lookup"><span data-stu-id="0e57a-153">Version</span></span><br/> | <span data-ttu-id="0e57a-154">Windows Installer 5,0 no Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e57a-154">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0e57a-155">Windows Installer 4,0 ou Windows Installer 4,5 no Windows Server 2008 ou no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e57a-155">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0e57a-156">Windows Installer 4,5 no Windows Server 2003 e no Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e57a-156">Windows Installer 4.5 on Windows Server 2003 and Windows XP</span></span><br/> |
| <span data-ttu-id="0e57a-157">DLL</span><span class="sxs-lookup"><span data-stu-id="0e57a-157">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e57a-158"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e57a-158"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                           |
| <span data-ttu-id="0e57a-159">IID</span><span class="sxs-lookup"><span data-stu-id="0e57a-159">IID</span></span><br/>     | <span data-ttu-id="0e57a-160">IID \_ IInstaller é definido como 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0e57a-160">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                |



## <a name="see-also"></a><span data-ttu-id="0e57a-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e57a-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e57a-162">**Instalador**</span><span class="sxs-lookup"><span data-stu-id="0e57a-162">**Installer**</span></span>](installer-object.md)
</dt> <dt>

[<span data-ttu-id="0e57a-163">Sem suporte no Windows Installer 3,1 e versões anteriores</span><span class="sxs-lookup"><span data-stu-id="0e57a-163">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




