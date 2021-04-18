---
title: Interface IMsTscAdvancedSettings
description: Inclui métodos para recuperar e definir propriedades que habilitam o cache de bitmaps, a compactação e a impressora e o redirecionamento de área de transferência.
ms.assetid: 3385e843-be05-4801-8d59-6395d95686b1
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsTscAdvancedSettings
- Serviços de Área de Trabalho Remota da interface IMsTscAdvancedSettings, descrita
topic_type:
- apiref
api_name:
- IMsTscAdvancedSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad4d55df30c940ecc5a5515f13c05a285507499e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105778810"
---
# <a name="imstscadvancedsettings-interface"></a><span data-ttu-id="62ba8-105">Interface IMsTscAdvancedSettings</span><span class="sxs-lookup"><span data-stu-id="62ba8-105">IMsTscAdvancedSettings interface</span></span>

<span data-ttu-id="62ba8-106">Inclui métodos para recuperar e definir propriedades que habilitam o cache de bitmaps, a compactação e a impressora e o redirecionamento de área de transferência.</span><span class="sxs-lookup"><span data-stu-id="62ba8-106">Includes methods to retrieve and set properties that enable bitmap caching, compression, and printer and clipboard redirection.</span></span> <span data-ttu-id="62ba8-107">Você também pode especificar nomes de DLLs de cliente do canal virtual.</span><span class="sxs-lookup"><span data-stu-id="62ba8-107">You can also specify names of virtual channel client DLLs.</span></span>

<span data-ttu-id="62ba8-108">Você Obtém uma instância dessa interface usando a propriedade [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) .</span><span class="sxs-lookup"><span data-stu-id="62ba8-108">You obtain an instance of this interface by using the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property.</span></span>

## <a name="members"></a><span data-ttu-id="62ba8-109">Membros</span><span class="sxs-lookup"><span data-stu-id="62ba8-109">Members</span></span>

<span data-ttu-id="62ba8-110">A interface **IMsTscAdvancedSettings** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="62ba8-110">The **IMsTscAdvancedSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="62ba8-111">**IMsTscAdvancedSettings** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="62ba8-111">**IMsTscAdvancedSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="62ba8-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62ba8-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62ba8-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="62ba8-113">Properties</span></span>

<span data-ttu-id="62ba8-114">A interface **IMsTscAdvancedSettings** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="62ba8-114">The **IMsTscAdvancedSettings** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="62ba8-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="62ba8-115">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="62ba8-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="62ba8-116">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="62ba8-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="62ba8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="62ba8-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-118"><a href="imstscadvancedsettings-allowbackgroundinput.md"><strong>allowBackgroundInput</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-119">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-119">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-120">Especifica se o modo de entrada em segundo plano está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62ba8-120">Specifies whether background input mode is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="62ba8-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-121"><a href="imstscadvancedsettings-bitmapperistence.md"><strong>BitmapPeristence</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-122">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-122">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-123">Especifica se o cache de bitmaps está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62ba8-123">Specifies whether bitmap caching is enabled.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="62ba8-124">O erro ortográfico no nome da propriedade está na versão liberada do controle.</span><span class="sxs-lookup"><span data-stu-id="62ba8-124">The spelling error in the name of the property is in the released version of the control.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="62ba8-125"><a href="imstscadvancedsettings-compress.md"><strong>Compactar</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-125"><a href="imstscadvancedsettings-compress.md"><strong>Compress</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-126">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-127">Especifica se a compactação está habilitada.</span><span class="sxs-lookup"><span data-stu-id="62ba8-127">Specifies whether compression is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="62ba8-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-128"><a href="imstscadvancedsettings-containerhandledfullscreen.md"><strong>ContainerHandledFullScreen</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-130">Especifica se o modo de tela inteira manipulado por contêiner está habilitado.</span><span class="sxs-lookup"><span data-stu-id="62ba8-130">Specifies whether the container-handled full-screen mode is enabled.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="62ba8-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-131"><a href="imstscadvancedsettings-disablerdpdr.md"><strong>DisableRdpdr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-133">Especifica se a impressora e o redirecionamento de área de transferência estão habilitados.</span><span class="sxs-lookup"><span data-stu-id="62ba8-133">Specifies whether printer and clipboard redirection is enabled.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="62ba8-134"><a href="imstscadvancedsettings-iconfile.md"><strong>Ícone</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-134"><a href="imstscadvancedsettings-iconfile.md"><strong>IconFile</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-135">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-135">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-136">Especifica o nome do arquivo que contém os dados de ícone que serão acessados ao exibir o cliente no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="62ba8-136">Specifies the name of the file containing icon data that will be accessed when displaying the client in full-screen mode.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="62ba8-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-137"><a href="imstscadvancedsettings-iconindex.md"><strong>IconIndex</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-138">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-138">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-139">Especifica o índice do ícone dentro do arquivo de ícone atual.</span><span class="sxs-lookup"><span data-stu-id="62ba8-139">Specifies the index of the icon within the current icon file.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="62ba8-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-140"><a href="imstscadvancedsettings-keyboardlayoutstr.md"><strong>KeyBoardLayoutStr</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-141">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-141">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-142">Especifica o nome do identificador de localidade de entrada ativo (anteriormente chamado de layout de teclado) a ser usado para a conexão.</span><span class="sxs-lookup"><span data-stu-id="62ba8-142">Specifies the name of the active input locale identifier (formerly called the keyboard layout) to use for the connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="62ba8-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span><span class="sxs-lookup"><span data-stu-id="62ba8-143"><a href="imstscadvancedsettings-plugindlls.md"><strong>PluginDlls</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-144">Somente gravação</span><span class="sxs-lookup"><span data-stu-id="62ba8-144">Write-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="62ba8-145">Especifica os nomes das DLLs de cliente do canal virtual a serem carregadas.</span><span class="sxs-lookup"><span data-stu-id="62ba8-145">Specifies the names of virtual channel client DLLs to be loaded.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="62ba8-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="62ba8-146">Remarks</span></span>

<span data-ttu-id="62ba8-147">Essa interface foi estendida pelas seguintes interfaces, com cada nova interface herdando todos os métodos e propriedades das interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="62ba8-147">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="62ba8-148">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="62ba8-148">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
-   [<span data-ttu-id="62ba8-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="62ba8-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
-   [<span data-ttu-id="62ba8-150">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="62ba8-150">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
-   [<span data-ttu-id="62ba8-151">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="62ba8-151">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="62ba8-152">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="62ba8-152">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="62ba8-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="62ba8-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="62ba8-154">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="62ba8-154">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="62ba8-155">Para obter mais informações sobre Conexão Web de Área de Trabalho Remota, consulte [Requirements for conexão Web de área de trabalho remota](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="62ba8-155">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62ba8-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62ba8-156">Requirements</span></span>



| <span data-ttu-id="62ba8-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="62ba8-157">Requirement</span></span> | <span data-ttu-id="62ba8-158">Valor</span><span class="sxs-lookup"><span data-stu-id="62ba8-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="62ba8-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62ba8-159">Minimum supported client</span></span><br/> | <span data-ttu-id="62ba8-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62ba8-160">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="62ba8-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="62ba8-161">Minimum supported server</span></span><br/> | <span data-ttu-id="62ba8-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62ba8-162">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="62ba8-163">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="62ba8-163">Type library</span></span><br/>             | <dl> <span data-ttu-id="62ba8-164"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ba8-164"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="62ba8-165">DLL</span><span class="sxs-lookup"><span data-stu-id="62ba8-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62ba8-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62ba8-166"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="62ba8-167">IID</span><span class="sxs-lookup"><span data-stu-id="62ba8-167">IID</span></span><br/>                      | <span data-ttu-id="62ba8-168">IID \_ IMsTscAdvancedSettings é definido como 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span><span class="sxs-lookup"><span data-stu-id="62ba8-168">IID\_IMsTscAdvancedSettings is defined as 809945cc-4b3b-4a92-a6b0-dbf9b5f2ef2d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62ba8-169">Confira também</span><span class="sxs-lookup"><span data-stu-id="62ba8-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62ba8-170">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="62ba8-170">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="62ba8-171">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="62ba8-171">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

