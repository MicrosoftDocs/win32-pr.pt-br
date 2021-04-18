---
Description: As constantes KNOWNFOLDERID representam GUIDs que identificam as pastas padrão registradas com o sistema como pastas conhecidas.
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: KNOWNFOLDERID (KnownFolders. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104968768"
---
# <a name="knownfolderid"></a><span data-ttu-id="dfa36-103">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="dfa36-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="dfa36-104">As constantes **KNOWNFOLDERID** representam GUIDs que identificam as pastas padrão registradas com o sistema como [pastas conhecidas](known-folders.md).</span><span class="sxs-lookup"><span data-stu-id="dfa36-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="dfa36-105">Essas pastas são instaladas com o Windows Vista e sistemas operacionais posteriores, e um computador terá apenas pastas apropriadas para ele instalado.</span><span class="sxs-lookup"><span data-stu-id="dfa36-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="dfa36-106">Para obter descrições dessas pastas, consulte [**CSIDL**](csidl.md).</span><span class="sxs-lookup"><span data-stu-id="dfa36-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="dfa36-107">Exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="dfa36-108">Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) no github.</span><span class="sxs-lookup"><span data-stu-id="dfa36-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="dfa36-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="dfa36-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="dfa36-110">Constante</span><span class="sxs-lookup"><span data-stu-id="dfa36-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="dfa36-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="dfa36-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="dfa36-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-113">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-113">GUID</span></span></td>
<td><span data-ttu-id="dfa36-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="dfa36-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-115">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-115">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-116">Imagens da conta</span><span class="sxs-lookup"><span data-stu-id="dfa36-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-117">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-117">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-118">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-119">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-119">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-120">%APPDATA%\Microsoft\Windows\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="dfa36-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-121">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-122">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-123">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-124">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-125">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-126">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="dfa36-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-128">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-128">GUID</span></span></td>
<td><span data-ttu-id="dfa36-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="dfa36-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-130">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-130">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-131">Obter programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-132">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-132">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-133">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-134">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-134">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-135">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-136">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-138">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-139">Adicionar novos programas (encontrados no item <strong>Adicionar ou remover programas</strong> no painel de controle)</span><span class="sxs-lookup"><span data-stu-id="dfa36-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-140">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-141">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="dfa36-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-143">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-143">GUID</span></span></td>
<td><span data-ttu-id="dfa36-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span><span class="sxs-lookup"><span data-stu-id="dfa36-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-145">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-145">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-146">Ferramentas Administrativas</span><span class="sxs-lookup"><span data-stu-id="dfa36-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-147">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-147">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-148">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-149">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-149">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-150">Ferramentas do%APPDATA%\Microsoft\Windows\Start Iniciar\programas\ferramentas</span><span class="sxs-lookup"><span data-stu-id="dfa36-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-151">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="dfa36-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-153">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-154">Ferramentas Administrativas</span><span class="sxs-lookup"><span data-stu-id="dfa36-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-155">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-156">Ferramentas do%USERPROFILE%\Start Iniciar\programas\ferramentas</span><span class="sxs-lookup"><span data-stu-id="dfa36-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="dfa36-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-158">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-158">GUID</span></span></td>
<td><span data-ttu-id="dfa36-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="dfa36-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-160">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-160">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-161">AppDataDesktop</span><span class="sxs-lookup"><span data-stu-id="dfa36-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-162">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-162">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-163">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-164">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-164">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-165">%LOCALAPPDATA%\Desktop</span><span class="sxs-lookup"><span data-stu-id="dfa36-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-166">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-167">Nenhum, valor introduzido no Windows 10, versão 1709</span><span class="sxs-lookup"><span data-stu-id="dfa36-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-168">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-169">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-170">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-171">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dfa36-172">Esta FOLDERid é usada internamente por aplicativos .NET para habilitar a funcionalidade do aplicativo de plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="dfa36-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="dfa36-173">Ele não se destina a ser usado diretamente de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dfa36-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="dfa36-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-175">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-175">GUID</span></span></td>
<td><span data-ttu-id="dfa36-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span><span class="sxs-lookup"><span data-stu-id="dfa36-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-177">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-177">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-178">AppDataDocuments</span><span class="sxs-lookup"><span data-stu-id="dfa36-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-179">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-179">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-180">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-181">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-181">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-182">%LOCALAPPDATA%\Documents</span><span class="sxs-lookup"><span data-stu-id="dfa36-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-183">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-184">Nenhum, valor introduzido no Windows 10, versão 1709</span><span class="sxs-lookup"><span data-stu-id="dfa36-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-185">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-186">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-187">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-188">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dfa36-189">Esta FOLDERid é usada internamente por aplicativos .NET para habilitar a funcionalidade do aplicativo de plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="dfa36-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="dfa36-190">Ele não se destina a ser usado diretamente de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dfa36-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="dfa36-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-192">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-192">GUID</span></span></td>
<td><span data-ttu-id="dfa36-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span><span class="sxs-lookup"><span data-stu-id="dfa36-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-194">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-194">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-195">AppDataFavorites</span><span class="sxs-lookup"><span data-stu-id="dfa36-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-196">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-196">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-197">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-198">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-198">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-199">%LOCALAPPDATA%\Favorites</span><span class="sxs-lookup"><span data-stu-id="dfa36-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-200">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-201">Nenhum, valor introduzido no Windows 10, versão 1709</span><span class="sxs-lookup"><span data-stu-id="dfa36-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-202">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-203">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-204">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-205">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dfa36-206">Esta FOLDERid é usada internamente por aplicativos .NET para habilitar a funcionalidade do aplicativo de plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="dfa36-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="dfa36-207">Ele não se destina a ser usado diretamente de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dfa36-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="dfa36-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-209">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-209">GUID</span></span></td>
<td><span data-ttu-id="dfa36-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span><span class="sxs-lookup"><span data-stu-id="dfa36-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-211">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-211">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-212">AppDataProgramData</span><span class="sxs-lookup"><span data-stu-id="dfa36-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-213">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-213">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-214">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-215">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-215">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-216">%LOCALAPPDATA%\ProgramData</span><span class="sxs-lookup"><span data-stu-id="dfa36-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-217">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-218">Nenhum, valor introduzido no Windows 10, versão 1709</span><span class="sxs-lookup"><span data-stu-id="dfa36-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-219">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-220">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-221">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-222">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="dfa36-223">Esta FOLDERid é usada internamente por aplicativos .NET para habilitar a funcionalidade do aplicativo de plataforma cruzada.</span><span class="sxs-lookup"><span data-stu-id="dfa36-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="dfa36-224">Ele não se destina a ser usado diretamente de um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="dfa36-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="dfa36-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-226">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-226">GUID</span></span></td>
<td><span data-ttu-id="dfa36-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="dfa36-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-228">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-228">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-229">Atalhos de aplicativo</span><span class="sxs-lookup"><span data-stu-id="dfa36-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-230">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-230">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-231">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-232">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-232">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-233">Atalhos do%LOCALAPPDATA%\Microsoft\Windows\Application</span><span class="sxs-lookup"><span data-stu-id="dfa36-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-234">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-235">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-236">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-237">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-238">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-239">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="dfa36-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-241">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-241">GUID</span></span></td>
<td><span data-ttu-id="dfa36-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span><span class="sxs-lookup"><span data-stu-id="dfa36-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-243">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-243">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-244">Aplicativos</span><span class="sxs-lookup"><span data-stu-id="dfa36-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-245">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-245">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-246">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-247">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-247">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-248">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-249">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-250">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-251">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-252">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-253">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-254">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="dfa36-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-256">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-256">GUID</span></span></td>
<td><span data-ttu-id="dfa36-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="dfa36-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-258">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-258">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-259">Atualizações instaladas</span><span class="sxs-lookup"><span data-stu-id="dfa36-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-260">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-260">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-261">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-262">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-262">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-263">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-264">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-265">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-266">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-267">Nenhum, valor introduzido no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfa36-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="dfa36-268">Nas versões anteriores do Windows, as informações nesta página foram incluídas em <strong>Adicionar ou remover programas</strong> se a caixa <strong>Mostrar atualizações</strong> estava marcada.</span><span class="sxs-lookup"><span data-stu-id="dfa36-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-269">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-270">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="dfa36-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-272">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-272">GUID</span></span></td>
<td><span data-ttu-id="dfa36-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="dfa36-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-274">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-274">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-275">Rolo da câmera</span><span class="sxs-lookup"><span data-stu-id="dfa36-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-276">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-276">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-277">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-278">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-278">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-279">%USERPROFILE%\Pictures\Camera</span><span class="sxs-lookup"><span data-stu-id="dfa36-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-280">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-281">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-282">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-283">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-284">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-285">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="dfa36-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-287">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-287">GUID</span></span></td>
<td><span data-ttu-id="dfa36-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span><span class="sxs-lookup"><span data-stu-id="dfa36-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-289">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-289">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-290">Pasta de gravação temporária</span><span class="sxs-lookup"><span data-stu-id="dfa36-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-291">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-291">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-292">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-293">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-293">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span><span class="sxs-lookup"><span data-stu-id="dfa36-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-295">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="dfa36-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-297">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-298">Gravação de CD</span><span class="sxs-lookup"><span data-stu-id="dfa36-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-299">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-300">Gravação de Settings\Application Data\Microsoft\CD de USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="dfa36-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="dfa36-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-302">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-302">GUID</span></span></td>
<td><span data-ttu-id="dfa36-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="dfa36-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-304">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-304">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-305">Programas e Recursos</span><span class="sxs-lookup"><span data-stu-id="dfa36-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-306">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-306">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-307">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-308">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-308">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-309">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-310">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-311">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-312">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-313">Adicionar ou remover programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-314">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-315">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="dfa36-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-317">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-317">GUID</span></span></td>
<td><span data-ttu-id="dfa36-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="dfa36-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-319">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-319">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-320">Ferramentas Administrativas</span><span class="sxs-lookup"><span data-stu-id="dfa36-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-321">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-321">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-322">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-323">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-323">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-324">Ferramentas do%ALLUSERSPROFILE%\Microsoft\Windows\Start Iniciar\programas\ferramentas</span><span class="sxs-lookup"><span data-stu-id="dfa36-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-325">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="dfa36-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-327">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-328">Ferramentas Administrativas</span><span class="sxs-lookup"><span data-stu-id="dfa36-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-329">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-330">Ferramentas do%ALLUSERSPROFILE%\Start Iniciar\programas\ferramentas</span><span class="sxs-lookup"><span data-stu-id="dfa36-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="dfa36-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-332">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-332">GUID</span></span></td>
<td><span data-ttu-id="dfa36-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span><span class="sxs-lookup"><span data-stu-id="dfa36-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-334">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-334">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-335">Links de OEM</span><span class="sxs-lookup"><span data-stu-id="dfa36-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-336">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-336">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-337">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-338">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-338">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-339">Links do%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="dfa36-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-340">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="dfa36-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-342">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-343">Links de OEM</span><span class="sxs-lookup"><span data-stu-id="dfa36-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-344">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-345">Links do%ALLUSERSPROFILE%\OEM</span><span class="sxs-lookup"><span data-stu-id="dfa36-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="dfa36-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-347">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-347">GUID</span></span></td>
<td><span data-ttu-id="dfa36-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span><span class="sxs-lookup"><span data-stu-id="dfa36-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-349">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-349">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-350">Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-351">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-351">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-352">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-353">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-353">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Iniciar\programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-355">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="dfa36-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-357">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-358">Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-359">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-360">%ALLUSERSPROFILE%\Start Iniciar\programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="dfa36-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-362">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-362">GUID</span></span></td>
<td><span data-ttu-id="dfa36-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="dfa36-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-364">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-364">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-365">Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="dfa36-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-366">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-366">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-367">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-368">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-368">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-369">Menu%ALLUSERSPROFILE%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="dfa36-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-370">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="dfa36-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-372">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-373">Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="dfa36-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-374">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-375">Menu%ALLUSERSPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="dfa36-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="dfa36-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-377">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-377">GUID</span></span></td>
<td><span data-ttu-id="dfa36-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span><span class="sxs-lookup"><span data-stu-id="dfa36-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-379">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-379">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-380">Inicialização</span><span class="sxs-lookup"><span data-stu-id="dfa36-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-381">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-381">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-382">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-383">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-383">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="dfa36-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-385">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="dfa36-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-387">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-388">Inicialização</span><span class="sxs-lookup"><span data-stu-id="dfa36-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-389">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="dfa36-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="dfa36-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-392">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-392">GUID</span></span></td>
<td><span data-ttu-id="dfa36-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="dfa36-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-394">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-394">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-395">Modelos</span><span class="sxs-lookup"><span data-stu-id="dfa36-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-396">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-396">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-397">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-398">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-398">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="dfa36-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-400">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="dfa36-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-402">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-403">Modelos</span><span class="sxs-lookup"><span data-stu-id="dfa36-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-404">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-405">%ALLUSERSPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="dfa36-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="dfa36-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-407">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-407">GUID</span></span></td>
<td><span data-ttu-id="dfa36-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span><span class="sxs-lookup"><span data-stu-id="dfa36-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-409">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-409">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-410">Computador</span><span class="sxs-lookup"><span data-stu-id="dfa36-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-411">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-411">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-412">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-413">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-413">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-414">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-415">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="dfa36-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-417">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-418">Meu Computador</span><span class="sxs-lookup"><span data-stu-id="dfa36-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-419">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-420">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="dfa36-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-422">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-422">GUID</span></span></td>
<td><span data-ttu-id="dfa36-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="dfa36-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-424">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-424">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-425">Conflitos</span><span class="sxs-lookup"><span data-stu-id="dfa36-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-426">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-426">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-427">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-428">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-428">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-429">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-430">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-431">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-432">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-433">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="dfa36-433">Not applicable.</span></span> <span data-ttu-id="dfa36-434">Este <strong>KNOWNFOLDERID</strong> refere-se ao Gerenciador de sincronização do Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfa36-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="dfa36-435">Não é a pasta referenciada pelo <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>mais antigo.</span><span class="sxs-lookup"><span data-stu-id="dfa36-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-436">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-437">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="dfa36-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-439">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-439">GUID</span></span></td>
<td><span data-ttu-id="dfa36-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span><span class="sxs-lookup"><span data-stu-id="dfa36-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-441">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-441">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-442">Conexões de Rede</span><span class="sxs-lookup"><span data-stu-id="dfa36-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-443">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-443">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-444">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-445">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-445">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-446">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-447">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="dfa36-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-449">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-450">Conexões de Rede</span><span class="sxs-lookup"><span data-stu-id="dfa36-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-451">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-452">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="dfa36-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-454">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-454">GUID</span></span></td>
<td><span data-ttu-id="dfa36-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="dfa36-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-456">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-456">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-457">Contatos</span><span class="sxs-lookup"><span data-stu-id="dfa36-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-458">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-458">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-459">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-460">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-460">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-461">%USERPROFILE%\Contacts</span><span class="sxs-lookup"><span data-stu-id="dfa36-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-462">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-463">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-464">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-465">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-466">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-467">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="dfa36-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-469">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-469">GUID</span></span></td>
<td><span data-ttu-id="dfa36-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span><span class="sxs-lookup"><span data-stu-id="dfa36-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-471">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-471">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-472">Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="dfa36-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-473">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-473">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-474">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-475">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-475">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-476">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-477">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="dfa36-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-479">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-480">Painel de Controle</span><span class="sxs-lookup"><span data-stu-id="dfa36-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-481">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-482">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="dfa36-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-484">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-484">GUID</span></span></td>
<td><span data-ttu-id="dfa36-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span><span class="sxs-lookup"><span data-stu-id="dfa36-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-486">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-486">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-487">Cookies</span><span class="sxs-lookup"><span data-stu-id="dfa36-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-488">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-488">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-489">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-490">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-490">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-491">%APPDATA%\Microsoft\Windows\Cookies</span><span class="sxs-lookup"><span data-stu-id="dfa36-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-492">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="dfa36-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-494">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-495">Cookies</span><span class="sxs-lookup"><span data-stu-id="dfa36-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-496">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-497">%USERPROFILE%\Cookies</span><span class="sxs-lookup"><span data-stu-id="dfa36-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="dfa36-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-499">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-499">GUID</span></span></td>
<td><span data-ttu-id="dfa36-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="dfa36-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-501">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-501">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-502">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="dfa36-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-503">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-503">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-504">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-505">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-505">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-506">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="dfa36-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-507">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="dfa36-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-509">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-510">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="dfa36-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-511">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-512">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="dfa36-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="dfa36-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-514">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-514">GUID</span></span></td>
<td><span data-ttu-id="dfa36-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span><span class="sxs-lookup"><span data-stu-id="dfa36-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-516">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-516">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-517">DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="dfa36-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-518">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-518">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-519">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-520">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-520">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="dfa36-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-522">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-523">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-524">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-525">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-526">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-527">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="dfa36-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-529">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-529">GUID</span></span></td>
<td><span data-ttu-id="dfa36-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="dfa36-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-531">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-531">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-532">Documentos</span><span class="sxs-lookup"><span data-stu-id="dfa36-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-533">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-533">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-534">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-535">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-535">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-536">%USERPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="dfa36-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-537">Equivalentes a CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="dfa36-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="dfa36-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-539">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-540">Meus Documentos</span><span class="sxs-lookup"><span data-stu-id="dfa36-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-541">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-542">Documentos do%USERPROFILE%\My</span><span class="sxs-lookup"><span data-stu-id="dfa36-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="dfa36-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-544">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-544">GUID</span></span></td>
<td><span data-ttu-id="dfa36-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span><span class="sxs-lookup"><span data-stu-id="dfa36-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-546">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-546">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-547">Documentos</span><span class="sxs-lookup"><span data-stu-id="dfa36-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-548">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-548">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-549">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-550">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-550">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span><span class="sxs-lookup"><span data-stu-id="dfa36-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-552">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-553">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-554">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-555">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-556">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-557">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="dfa36-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-559">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-559">GUID</span></span></td>
<td><span data-ttu-id="dfa36-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="dfa36-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-561">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-561">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-562">Downloads</span><span class="sxs-lookup"><span data-stu-id="dfa36-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-563">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-563">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-564">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-565">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-565">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-566">%USERPROFILE%\Downloads</span><span class="sxs-lookup"><span data-stu-id="dfa36-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-567">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-568">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-569">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-570">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-571">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-572">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="dfa36-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-574">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-574">GUID</span></span></td>
<td><span data-ttu-id="dfa36-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="dfa36-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-576">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-576">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-577">Favoritos</span><span class="sxs-lookup"><span data-stu-id="dfa36-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-578">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-578">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-579">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-580">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-580">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-581">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="dfa36-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-582">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="dfa36-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-584">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-585">Favoritos</span><span class="sxs-lookup"><span data-stu-id="dfa36-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-586">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-587">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="dfa36-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="dfa36-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-589">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-589">GUID</span></span></td>
<td><span data-ttu-id="dfa36-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="dfa36-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-591">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-591">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-592">Fontes</span><span class="sxs-lookup"><span data-stu-id="dfa36-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-593">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-593">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-595">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-595">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-596">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="dfa36-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-597">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="dfa36-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-599">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-600">Fontes</span><span class="sxs-lookup"><span data-stu-id="dfa36-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-601">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-602">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="dfa36-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="dfa36-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="dfa36-604">Esta FOLDERid foi preterida no Windows 10, versão 1803 e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="dfa36-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="dfa36-605">Nessas versões, ele retorna <strong>0x80070057-E_INVALIDARG</strong>
</span><span class="sxs-lookup"><span data-stu-id="dfa36-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-606">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-606">GUID</span></span></td>
<td><span data-ttu-id="dfa36-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="dfa36-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-608">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-608">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-609">Jogos</span><span class="sxs-lookup"><span data-stu-id="dfa36-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-610">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-610">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-611">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-612">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-612">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-613">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-614">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-615">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-616">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-617">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-618">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-619">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="dfa36-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-621">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-621">GUID</span></span></td>
<td><span data-ttu-id="dfa36-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span><span class="sxs-lookup"><span data-stu-id="dfa36-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-623">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-623">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="dfa36-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-625">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-625">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-626">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-627">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-627">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="dfa36-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-629">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-630">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-631">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-632">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-633">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-634">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="dfa36-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-636">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-636">GUID</span></span></td>
<td><span data-ttu-id="dfa36-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="dfa36-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-638">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-638">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-639">Histórico</span><span class="sxs-lookup"><span data-stu-id="dfa36-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-640">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-640">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-641">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-642">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-642">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-643">%LOCALAPPDATA%\Microsoft\Windows\History</span><span class="sxs-lookup"><span data-stu-id="dfa36-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-644">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="dfa36-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-646">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-647">Histórico</span><span class="sxs-lookup"><span data-stu-id="dfa36-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-648">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-649">Settings\History de USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="dfa36-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="dfa36-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-651">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-651">GUID</span></span></td>
<td><span data-ttu-id="dfa36-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span><span class="sxs-lookup"><span data-stu-id="dfa36-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-653">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-653">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-654">Homegroup</span><span class="sxs-lookup"><span data-stu-id="dfa36-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-655">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-655">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-656">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-657">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-657">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-658">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-659">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-660">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-661">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-662">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-663">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-664">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="dfa36-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-666">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-666">GUID</span></span></td>
<td><span data-ttu-id="dfa36-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span><span class="sxs-lookup"><span data-stu-id="dfa36-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-668">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-668">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-669">O nome do usuário (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="dfa36-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-670">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-670">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-671">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-672">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-672">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-673">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-674">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-675">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-676">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-677">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-678">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-679">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="dfa36-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-681">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-681">GUID</span></span></td>
<td><span data-ttu-id="dfa36-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="dfa36-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-683">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-683">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-684">ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="dfa36-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-685">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-685">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-686">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-687">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-687">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="dfa36-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-689">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-690">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-691">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-692">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-693">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-694">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="dfa36-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-696">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-696">GUID</span></span></td>
<td><span data-ttu-id="dfa36-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span><span class="sxs-lookup"><span data-stu-id="dfa36-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-698">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-698">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-699">Arquivos Temporários da Internet</span><span class="sxs-lookup"><span data-stu-id="dfa36-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-700">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-700">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-701">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-702">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-702">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary arquivos da Internet</span><span class="sxs-lookup"><span data-stu-id="dfa36-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-704">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="dfa36-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-706">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-707">Arquivos Temporários da Internet</span><span class="sxs-lookup"><span data-stu-id="dfa36-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-708">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-709">Arquivos da Internet Settings\Temporary de USERPROFILE%</span><span class="sxs-lookup"><span data-stu-id="dfa36-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="dfa36-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-711">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-711">GUID</span></span></td>
<td><span data-ttu-id="dfa36-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span><span class="sxs-lookup"><span data-stu-id="dfa36-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-713">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-713">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-714">A Internet</span><span class="sxs-lookup"><span data-stu-id="dfa36-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-715">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-715">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-716">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-717">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-717">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-718">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-719">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="dfa36-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-721">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="dfa36-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-723">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-724">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="dfa36-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-726">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-726">GUID</span></span></td>
<td><span data-ttu-id="dfa36-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span><span class="sxs-lookup"><span data-stu-id="dfa36-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-728">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-728">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-729">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="dfa36-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-730">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-730">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-731">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-732">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-732">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-733">%APPDATA%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="dfa36-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-734">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-735">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-736">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-737">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-738">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-739">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="dfa36-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-741">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-741">GUID</span></span></td>
<td><span data-ttu-id="dfa36-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="dfa36-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-743">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-743">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-744">Links</span><span class="sxs-lookup"><span data-stu-id="dfa36-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-745">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-745">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-746">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-747">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-747">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-748">%USERPROFILE%\Links</span><span class="sxs-lookup"><span data-stu-id="dfa36-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-749">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-750">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-751">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-752">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-753">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-754">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="dfa36-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-756">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-756">GUID</span></span></td>
<td><span data-ttu-id="dfa36-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span><span class="sxs-lookup"><span data-stu-id="dfa36-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-758">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-758">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-759">Local</span><span class="sxs-lookup"><span data-stu-id="dfa36-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-760">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-760">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-761">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-762">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-762">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-763">% LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span><span class="sxs-lookup"><span data-stu-id="dfa36-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-764">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="dfa36-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-766">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-767">Dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="dfa36-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-768">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-769">Dados Locais\dados de \%</span><span class="sxs-lookup"><span data-stu-id="dfa36-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="dfa36-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-771">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-771">GUID</span></span></td>
<td><span data-ttu-id="dfa36-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="dfa36-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-773">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-773">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-774">LocalLow</span><span class="sxs-lookup"><span data-stu-id="dfa36-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-775">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-775">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-776">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-777">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-777">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-778">%USERPROFILE%\AppData\LocalLow</span><span class="sxs-lookup"><span data-stu-id="dfa36-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-779">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-780">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-781">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-782">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-783">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-784">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="dfa36-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-786">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-786">GUID</span></span></td>
<td><span data-ttu-id="dfa36-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span><span class="sxs-lookup"><span data-stu-id="dfa36-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-788">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-788">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-789">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-790">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-790">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-792">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-792">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-793">%WINDIR%\resources\0409 (página de código)</span><span class="sxs-lookup"><span data-stu-id="dfa36-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-794">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="dfa36-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-796">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-797">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-798">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-799">%WINDIR%\resources\0409 (página de código)</span><span class="sxs-lookup"><span data-stu-id="dfa36-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="dfa36-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-801">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-801">GUID</span></span></td>
<td><span data-ttu-id="dfa36-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="dfa36-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-803">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-803">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-804">Música</span><span class="sxs-lookup"><span data-stu-id="dfa36-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-805">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-805">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-806">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-807">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-807">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-808">%USERPROFILE%\Music</span><span class="sxs-lookup"><span data-stu-id="dfa36-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-809">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="dfa36-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-811">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-812">Minhas músicas</span><span class="sxs-lookup"><span data-stu-id="dfa36-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-813">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-814">%USERPROFILE%\My Documentos\minhas músicas</span><span class="sxs-lookup"><span data-stu-id="dfa36-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="dfa36-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-816">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-816">GUID</span></span></td>
<td><span data-ttu-id="dfa36-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span><span class="sxs-lookup"><span data-stu-id="dfa36-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-818">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-818">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-819">Música</span><span class="sxs-lookup"><span data-stu-id="dfa36-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-820">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-820">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-821">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-822">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-822">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span><span class="sxs-lookup"><span data-stu-id="dfa36-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-824">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-825">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-826">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-827">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-828">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-829">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="dfa36-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-831">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-831">GUID</span></span></td>
<td><span data-ttu-id="dfa36-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="dfa36-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-833">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-833">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-834">Atalhos de rede</span><span class="sxs-lookup"><span data-stu-id="dfa36-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-835">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-835">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-836">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-837">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-837">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-838">Atalhos do%APPDATA%\Microsoft\Windows\Network</span><span class="sxs-lookup"><span data-stu-id="dfa36-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-839">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="dfa36-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-841">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-842">NetHood</span><span class="sxs-lookup"><span data-stu-id="dfa36-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-843">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-844">%USERPROFILE%\NetHood</span><span class="sxs-lookup"><span data-stu-id="dfa36-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="dfa36-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-846">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-846">GUID</span></span></td>
<td><span data-ttu-id="dfa36-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="dfa36-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-848">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-848">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-849">Rede</span><span class="sxs-lookup"><span data-stu-id="dfa36-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-850">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-850">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-851">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-852">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-852">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-853">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-854">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="dfa36-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-856">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-857">Meus locais de rede</span><span class="sxs-lookup"><span data-stu-id="dfa36-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-858">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-859">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="dfa36-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-861">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-861">GUID</span></span></td>
<td><span data-ttu-id="dfa36-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span><span class="sxs-lookup"><span data-stu-id="dfa36-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-863">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-863">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-864">Objetos 3D</span><span class="sxs-lookup"><span data-stu-id="dfa36-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-865">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-865">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-866">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-867">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-867">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-868">Objetos%USERPROFILE%\3D</span><span class="sxs-lookup"><span data-stu-id="dfa36-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-869">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-870">Nenhum, valor introduzido no Windows 10, versão 1703</span><span class="sxs-lookup"><span data-stu-id="dfa36-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-871">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-872">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-873">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-874">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="dfa36-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-876">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-876">GUID</span></span></td>
<td><span data-ttu-id="dfa36-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span><span class="sxs-lookup"><span data-stu-id="dfa36-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-878">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-878">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-879">Imagens originais</span><span class="sxs-lookup"><span data-stu-id="dfa36-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-880">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-880">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-881">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-882">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-882">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-883">Imagens do%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original</span><span class="sxs-lookup"><span data-stu-id="dfa36-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-884">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-885">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-886">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-887">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-888">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-889">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="dfa36-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-891">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-891">GUID</span></span></td>
<td><span data-ttu-id="dfa36-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span><span class="sxs-lookup"><span data-stu-id="dfa36-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-893">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-893">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-894">Apresentações de slides</span><span class="sxs-lookup"><span data-stu-id="dfa36-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-895">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-895">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-896">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-897">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-897">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-898">%USERPROFILE%\Pictures\Slide mostra</span><span class="sxs-lookup"><span data-stu-id="dfa36-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-899">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-900">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-901">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-902">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-903">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-904">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="dfa36-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-906">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-906">GUID</span></span></td>
<td><span data-ttu-id="dfa36-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="dfa36-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-908">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-908">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-909">Imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-910">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-910">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-911">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-912">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-912">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="dfa36-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-914">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-915">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-916">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-917">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-918">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-919">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="dfa36-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-921">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-921">GUID</span></span></td>
<td><span data-ttu-id="dfa36-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="dfa36-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-923">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-923">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-924">Imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-925">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-925">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-926">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-927">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-927">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-928">%USERPROFILE%\Pictures</span><span class="sxs-lookup"><span data-stu-id="dfa36-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-929">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="dfa36-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-931">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-932">Minhas imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-933">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-934">%USERPROFILE%\My Documentos\minhas imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="dfa36-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-936">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-936">GUID</span></span></td>
<td><span data-ttu-id="dfa36-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="dfa36-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-938">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-938">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-939">Playlists</span><span class="sxs-lookup"><span data-stu-id="dfa36-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-940">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-940">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-941">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-942">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-942">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-943">%USERPROFILE%\Music\Playlists</span><span class="sxs-lookup"><span data-stu-id="dfa36-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-944">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-945">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-946">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-947">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-948">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-949">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="dfa36-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-951">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-951">GUID</span></span></td>
<td><span data-ttu-id="dfa36-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span><span class="sxs-lookup"><span data-stu-id="dfa36-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-953">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-953">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-954">Impressoras</span><span class="sxs-lookup"><span data-stu-id="dfa36-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-955">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-955">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-956">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-957">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-957">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-958">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-959">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="dfa36-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-961">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-962">Impressoras e faxes</span><span class="sxs-lookup"><span data-stu-id="dfa36-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-963">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-964">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="dfa36-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-966">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-966">GUID</span></span></td>
<td><span data-ttu-id="dfa36-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span><span class="sxs-lookup"><span data-stu-id="dfa36-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-968">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-968">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-969">Atalhos de impressora</span><span class="sxs-lookup"><span data-stu-id="dfa36-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-970">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-970">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-971">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-972">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-972">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-973">Atalhos do%APPDATA%\Microsoft\Windows\Printer</span><span class="sxs-lookup"><span data-stu-id="dfa36-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-974">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="dfa36-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-976">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-977">PrintHood</span><span class="sxs-lookup"><span data-stu-id="dfa36-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-978">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-979">%USERPROFILE%\PrintHood</span><span class="sxs-lookup"><span data-stu-id="dfa36-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="dfa36-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-981">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-981">GUID</span></span></td>
<td><span data-ttu-id="dfa36-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span><span class="sxs-lookup"><span data-stu-id="dfa36-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-983">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-983">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-984">O nome do usuário (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="dfa36-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-985">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-985">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-987">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-987">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-988">% USERPROFILE% (%SystemDrive%\Users \% username%)</span><span class="sxs-lookup"><span data-stu-id="dfa36-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-989">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="dfa36-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-991">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-992">O nome do usuário (% USERNAME%)</span><span class="sxs-lookup"><span data-stu-id="dfa36-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-993">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-994">% USERPROFILE% (%SystemDrive%\Documents e configurações \% nome de usuário%)</span><span class="sxs-lookup"><span data-stu-id="dfa36-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="dfa36-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-996">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-996">GUID</span></span></td>
<td><span data-ttu-id="dfa36-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span><span class="sxs-lookup"><span data-stu-id="dfa36-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-998">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-998">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="dfa36-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1000">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1000">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1002">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1002">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1003">% ALLUSERSPROFILE% (% ProgramData%,%SystemDrive%\ProgramData)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1004">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="dfa36-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1006">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1007">Dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1008">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1009">Dados do%ALLUSERSPROFILE%\Application</span><span class="sxs-lookup"><span data-stu-id="dfa36-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="dfa36-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1011">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1012">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1012">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1014">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1014">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1015">Arquivos de Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1016">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1016">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1018">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1018">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1019">% ProgramFiles% (arquivos%systemdrive%\Arquivos)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1020">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="dfa36-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1022">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1023">Arquivos de Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1024">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1025">% ProgramFiles% (arquivos%systemdrive%\Arquivos)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="dfa36-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1027">Não há suporte para esse valor em sistemas operacionais de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="dfa36-1028">Também não há suporte para aplicativos de 32 bits em execução em sistemas operacionais de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="dfa36-1029">A tentativa de usar FOLDERID_ProgramFilesX64 em uma das situações resulta em um erro.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="dfa36-1030">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1031">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1031">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1033">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1033">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1034">Arquivos de Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1035">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1035">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1037">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1037">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1038">% ProgramFiles% (arquivos%systemdrive%\Arquivos)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1039">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1040">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1041">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1042">Arquivos de Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1043">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1044">% ProgramFiles% (arquivos%systemdrive%\Arquivos)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="dfa36-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1046">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1047">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1047">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1049">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1049">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1050">Arquivos de Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1051">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1051">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1053">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1053">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1054">% ProgramFiles% (arquivos%systemdrive%\Arquivos)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1055">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1057">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1058">Arquivos de Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1059">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1060">% ProgramFiles% (arquivos%systemdrive%\Arquivos)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="dfa36-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1062">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1063">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1063">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1065">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1065">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1066">Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1067">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1067">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1069">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1069">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1070">Arquivos%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1071">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1073">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1074">Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1075">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1076">Arquivos%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="dfa36-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1078">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1079">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1079">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1081">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1081">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1082">Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1083">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1083">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1085">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1085">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1086">Arquivos%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1087">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1088">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1089">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1090">Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1091">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1092">Arquivos%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="dfa36-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1094">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1095">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1095">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1097">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1097">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1098">Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1099">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1099">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1101">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1101">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1102">Arquivos%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1103">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1105">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1106">Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1107">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1108">Arquivos%ProgramFiles%\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="dfa36-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1110">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1110">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1112">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1112">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1113">Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1114">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1114">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1115">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1116">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1116">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1117">%APPDATA%\Microsoft\Windows\Start Iniciar\programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1118">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1120">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1121">Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1122">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1123">%USERPROFILE%\Start Iniciar\programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="dfa36-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1125">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1125">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1127">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1127">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1128">Público</span><span class="sxs-lookup"><span data-stu-id="dfa36-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1129">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1129">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1131">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1131">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1132">% PUBLIC% (%SystemDrive%\Users\Public)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1133">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1134">Nenhum, novo para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1135">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1136">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1137">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1138">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="dfa36-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1140">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1140">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1142">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1142">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1143">Área de trabalho pública</span><span class="sxs-lookup"><span data-stu-id="dfa36-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1144">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1144">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1145">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1146">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1146">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1147">%PUBLIC%\Desktop</span><span class="sxs-lookup"><span data-stu-id="dfa36-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1148">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="dfa36-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1150">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1151">Área de trabalho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1152">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1153">%ALLUSERSPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="dfa36-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="dfa36-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1155">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1155">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1157">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1157">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1158">Documentos Públicos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1159">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1159">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1160">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1161">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1161">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1162">%PUBLIC%\Documents</span><span class="sxs-lookup"><span data-stu-id="dfa36-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1163">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1165">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1166">Documentos compartilhados</span><span class="sxs-lookup"><span data-stu-id="dfa36-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1167">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1168">%ALLUSERSPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="dfa36-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="dfa36-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1170">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1170">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1172">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1172">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1173">Downloads Públicos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1174">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1174">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1175">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1176">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1176">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1177">%PUBLIC%\Downloads</span><span class="sxs-lookup"><span data-stu-id="dfa36-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1178">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1179">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1180">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1181">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1182">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1183">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="dfa36-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1185">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1185">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1187">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1187">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="dfa36-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1189">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1189">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1190">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1191">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1191">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="dfa36-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1193">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1194">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1195">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1196">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1197">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1198">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="dfa36-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1200">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1200">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1202">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1202">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1203">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1204">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1204">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1205">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1206">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1206">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="dfa36-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1208">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1209">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1210">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1211">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1212">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1213">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="dfa36-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1215">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1215">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1217">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1217">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1218">Músicas Públicas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1219">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1219">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1220">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1221">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1221">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1222">%PUBLIC%\Music</span><span class="sxs-lookup"><span data-stu-id="dfa36-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1223">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="dfa36-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1225">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1226">Música compartilhada</span><span class="sxs-lookup"><span data-stu-id="dfa36-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1227">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1228">Música%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="dfa36-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="dfa36-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1230">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1230">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1232">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1232">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1233">Imagens públicas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1234">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1234">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1235">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1236">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1236">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1237">%PUBLIC%\Pictures</span><span class="sxs-lookup"><span data-stu-id="dfa36-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1238">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="dfa36-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1240">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1241">Imagens compartilhadas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1242">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1243">%ALLUSERSPROFILE%\Documents\My imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="dfa36-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1245">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1245">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1247">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1247">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1248">Toques</span><span class="sxs-lookup"><span data-stu-id="dfa36-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1249">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1249">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1250">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1251">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1251">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="dfa36-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1253">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1254">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1255">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1256">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1257">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1258">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="dfa36-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1260">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1260">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1262">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1262">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1263">Imagens da conta pública</span><span class="sxs-lookup"><span data-stu-id="dfa36-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1264">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1264">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1265">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1266">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1266">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1267">%PUBLIC%\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="dfa36-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1268">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1269">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1270">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1271">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1272">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1273">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="dfa36-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1275">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1275">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1277">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1277">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1278">Vídeos Públicos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1279">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1279">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1280">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1281">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1281">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1282">%PUBLIC%\Videos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1283">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="dfa36-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1285">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1286">Vídeo compartilhado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1287">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1288">Vídeos de%ALLUSERSPROFILE%\Documents\My</span><span class="sxs-lookup"><span data-stu-id="dfa36-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="dfa36-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1290">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1290">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1292">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1292">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1293">Início Rápido</span><span class="sxs-lookup"><span data-stu-id="dfa36-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1294">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1294">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1295">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1296">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1296">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1297">Inicialização do%APPDATA%\Microsoft\Internet Explorer\Quick</span><span class="sxs-lookup"><span data-stu-id="dfa36-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1298">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1299">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1300">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1301">Início Rápido</span><span class="sxs-lookup"><span data-stu-id="dfa36-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1302">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1303">Inicialização do%APPDATA%\Microsoft\Internet Explorer\Quick</span><span class="sxs-lookup"><span data-stu-id="dfa36-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="dfa36-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1305">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1305">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1307">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1307">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1308">Itens recentes</span><span class="sxs-lookup"><span data-stu-id="dfa36-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1309">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1309">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1310">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1311">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1311">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1312">%APPDATA%\Microsoft\Windows\Recent</span><span class="sxs-lookup"><span data-stu-id="dfa36-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1313">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="dfa36-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1315">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1316">Meus documentos recentes</span><span class="sxs-lookup"><span data-stu-id="dfa36-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1317">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1318">%USERPROFILE%\Recent</span><span class="sxs-lookup"><span data-stu-id="dfa36-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="dfa36-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1320">Não usado.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1320">Not used.</span></span> <span data-ttu-id="dfa36-1321">Esse valor é indefinido a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="dfa36-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1323">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1323">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1325">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1325">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1326">TV gravada</span><span class="sxs-lookup"><span data-stu-id="dfa36-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1327">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1327">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1328">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1329">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1329">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1330">%PUBLIC%\RecordedTV.library-ms</span><span class="sxs-lookup"><span data-stu-id="dfa36-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1331">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1332">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1333">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1334">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1335">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1336">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="dfa36-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1338">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1338">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1340">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1340">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1341">Lixeira</span><span class="sxs-lookup"><span data-stu-id="dfa36-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1342">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1342">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1343">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1344">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1344">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1345">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1346">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="dfa36-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1348">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1349">Lixeira</span><span class="sxs-lookup"><span data-stu-id="dfa36-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1350">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1351">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="dfa36-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1353">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1353">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1355">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1355">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1356">Recursos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1357">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1357">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1359">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1359">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1360">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="dfa36-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1361">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="dfa36-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1363">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1364">Recursos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1365">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1366">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="dfa36-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="dfa36-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1368">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1368">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1370">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1370">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1371">Toques</span><span class="sxs-lookup"><span data-stu-id="dfa36-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1372">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1372">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1373">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1374">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1374">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="dfa36-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1376">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1377">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1378">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1379">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1380">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1381">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="dfa36-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1383">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1383">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1385">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1385">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1386">Roaming</span><span class="sxs-lookup"><span data-stu-id="dfa36-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1387">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1387">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1388">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1389">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1389">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1390">% APPDATA% (%USERPROFILE%\AppData\Roaming)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1391">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="dfa36-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1393">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1394">Dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1395">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1396">% APPDATA% (dados de%USERPROFILE%\Application)</span><span class="sxs-lookup"><span data-stu-id="dfa36-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="dfa36-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1398">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1398">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1400">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1400">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1401">RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="dfa36-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1402">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1402">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1403">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1404">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1404">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="dfa36-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1406">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1407">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1408">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1409">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1410">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1411">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="dfa36-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1413">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1413">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1415">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1415">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1416">RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="dfa36-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1417">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1417">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1418">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1419">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1419">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="dfa36-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1421">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1422">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1423">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1424">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1425">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1426">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="dfa36-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1428">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1428">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1430">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1430">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1431">Música de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1432">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1432">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1433">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1434">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1434">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1435">Música%PUBLIC%\Music\Sample</span><span class="sxs-lookup"><span data-stu-id="dfa36-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1436">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1437">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1438">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1439">Música de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1440">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span><span class="sxs-lookup"><span data-stu-id="dfa36-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="dfa36-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1443">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1443">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1445">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1445">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1446">Imagens de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1447">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1447">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1448">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1449">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1449">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1450">%PUBLIC%\Pictures\Sample imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1451">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1452">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1453">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1454">Imagens de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1455">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1456">Imagens do%ALLUSERSPROFILE%\Documents\My Pictures\Sample</span><span class="sxs-lookup"><span data-stu-id="dfa36-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="dfa36-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1458">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1458">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1460">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1460">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1461">Listas de reprodução de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1462">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1462">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1463">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1464">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1464">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1465">Listas de reprodução do%PUBLIC%\Music\Sample</span><span class="sxs-lookup"><span data-stu-id="dfa36-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1466">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1467">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1468">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1469">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1470">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1471">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="dfa36-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1473">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1473">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1475">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1475">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1476">Vídeos de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1477">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1477">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1478">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1479">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1479">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1480">Vídeos de%PUBLIC%\Videos\Sample</span><span class="sxs-lookup"><span data-stu-id="dfa36-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1481">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1482">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1483">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1484">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1485">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1486">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="dfa36-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1488">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1488">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1490">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1490">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1491">Saved Games</span><span class="sxs-lookup"><span data-stu-id="dfa36-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1492">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1492">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1493">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1494">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1494">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1495">Jogos de%USERPROFILE%\Saved</span><span class="sxs-lookup"><span data-stu-id="dfa36-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1496">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1497">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1498">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1499">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1500">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1501">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="dfa36-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1503">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1503">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1505">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1505">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1506">Imagens salvas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1507">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1507">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1508">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1509">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1509">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1510">%USERPROFILE%\Pictures\Saved imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1511">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1512">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1513">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1514">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1515">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1516">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="dfa36-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1518">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1518">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1520">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1520">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1521">Biblioteca de imagens salvas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1522">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1522">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1523">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1524">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1524">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="dfa36-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1526">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1527">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1528">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1529">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1530">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1531">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="dfa36-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1533">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1533">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1535">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1535">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1536">Searches</span><span class="sxs-lookup"><span data-stu-id="dfa36-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1537">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1537">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1538">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1539">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1539">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1540">%USERPROFILE%\Searches</span><span class="sxs-lookup"><span data-stu-id="dfa36-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1541">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1542">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1543">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1544">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1545">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1546">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="dfa36-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1548">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1548">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1550">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1550">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1551">Capturas de tela</span><span class="sxs-lookup"><span data-stu-id="dfa36-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1552">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1552">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1553">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1554">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1554">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1555">%USERPROFILE%\Pictures\Screenshots</span><span class="sxs-lookup"><span data-stu-id="dfa36-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1556">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1557">Nenhum, valor introduzido no Windows 8</span><span class="sxs-lookup"><span data-stu-id="dfa36-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1558">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1559">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1560">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1561">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="dfa36-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1563">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1563">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1565">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1565">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1566">Arquivos Offline</span><span class="sxs-lookup"><span data-stu-id="dfa36-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1567">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1567">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1568">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1569">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1569">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1570">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1571">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1572">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1573">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1574">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1575">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1576">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="dfa36-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1578">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1578">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1580">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1580">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1581">Histórico</span><span class="sxs-lookup"><span data-stu-id="dfa36-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1582">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1582">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1583">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1584">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1584">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span><span class="sxs-lookup"><span data-stu-id="dfa36-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1586">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1587">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1588">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1589">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1590">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1591">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="dfa36-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1593">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1593">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1595">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1595">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1596">Resultados da Pesquisa</span><span class="sxs-lookup"><span data-stu-id="dfa36-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1597">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1597">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1598">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1599">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1599">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1600">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1601">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1602">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1603">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1604">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1605">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1606">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="dfa36-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1608">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1608">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1610">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1610">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="dfa36-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1612">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1612">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1613">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1614">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1614">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1615">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1616">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1617">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1618">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1619">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1620">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1621">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="dfa36-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1623">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1623">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1625">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1625">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1626">Modelos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1627">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1627">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1628">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1629">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1629">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span><span class="sxs-lookup"><span data-stu-id="dfa36-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1631">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1632">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1633">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1634">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1635">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1636">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="dfa36-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1638">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1638">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1640">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1640">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1641">SendTo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1642">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1642">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1643">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1644">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1644">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1645">%APPDATA%\Microsoft\Windows\SendTo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1646">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="dfa36-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1648">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1649">SendTo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1650">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1651">%USERPROFILE%\SendTo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="dfa36-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1653">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1653">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1655">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1655">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1656">Miniaplicativo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1657">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1657">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1658">COMMON</span><span class="sxs-lookup"><span data-stu-id="dfa36-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1659">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1659">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="dfa36-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1661">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1662">Nenhum, novo para o Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1663">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1664">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1665">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1666">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="dfa36-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1668">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1668">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1670">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1670">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1671">Miniaplicativo</span><span class="sxs-lookup"><span data-stu-id="dfa36-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1672">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1672">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1673">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1674">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1674">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="dfa36-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1676">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1677">Nenhum, novo para o Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1678">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1679">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1680">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1681">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="dfa36-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1683">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1683">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1685">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1685">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="dfa36-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1687">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1687">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1688">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1689">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1689">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1690">%USERPROFILE%\OneDrive</span><span class="sxs-lookup"><span data-stu-id="dfa36-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1691">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1692">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1693">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1694">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1695">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1696">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="dfa36-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1698">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1698">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1700">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1700">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1701">Rolo da câmera</span><span class="sxs-lookup"><span data-stu-id="dfa36-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1702">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1702">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1703">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1704">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1704">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1705">%USERPROFILE%\OneDrive\Pictures\Camera</span><span class="sxs-lookup"><span data-stu-id="dfa36-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1706">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1707">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1708">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1709">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1710">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1711">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="dfa36-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1713">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1713">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1715">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1715">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1716">Documentos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1717">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1717">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1718">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1719">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1719">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1720">%USERPROFILE%\OneDrive\Documents</span><span class="sxs-lookup"><span data-stu-id="dfa36-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1721">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1722">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1723">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1724">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1725">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1726">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="dfa36-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1728">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1728">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1730">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1730">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1731">Imagens</span><span class="sxs-lookup"><span data-stu-id="dfa36-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1732">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1732">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1733">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1734">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1734">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1735">%USERPROFILE%\OneDrive\Pictures</span><span class="sxs-lookup"><span data-stu-id="dfa36-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1736">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1737">Nenhum, valor introduzido no Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="dfa36-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1738">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1739">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1740">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1741">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="dfa36-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1743">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1743">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1745">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1745">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1746">Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="dfa36-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1747">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1747">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1748">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1749">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1749">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1750">Menu%APPDATA%\Microsoft\Windows\Start</span><span class="sxs-lookup"><span data-stu-id="dfa36-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1751">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="dfa36-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1753">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1754">Menu Iniciar</span><span class="sxs-lookup"><span data-stu-id="dfa36-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1755">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1756">Menu%USERPROFILE%\Start</span><span class="sxs-lookup"><span data-stu-id="dfa36-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="dfa36-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1758">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1758">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1760">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1760">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1761">Inicialização</span><span class="sxs-lookup"><span data-stu-id="dfa36-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1762">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1762">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1763">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1764">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1764">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="dfa36-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1766">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="dfa36-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1768">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1769">Inicialização</span><span class="sxs-lookup"><span data-stu-id="dfa36-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1770">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="dfa36-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="dfa36-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1773">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1773">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1775">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1775">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1776">Central de Sincronização</span><span class="sxs-lookup"><span data-stu-id="dfa36-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1777">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1777">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1778">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1779">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1779">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1780">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1781">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1782">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1783">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1784">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1785">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1786">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="dfa36-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1788">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1788">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1790">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1790">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1791">Resultados da sincronização</span><span class="sxs-lookup"><span data-stu-id="dfa36-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1792">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1792">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1793">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1794">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1794">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1795">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1796">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1797">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1798">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1799">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1800">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1801">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="dfa36-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1803">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1803">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1805">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1805">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1806">Configurar a sincronização</span><span class="sxs-lookup"><span data-stu-id="dfa36-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1807">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1807">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1808">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1809">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1809">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1810">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1811">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1812">Nenhum, valor introduzido no Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1813">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1814">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1815">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1816">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="dfa36-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1818">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1818">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1820">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1820">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1821">System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1822">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1822">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1824">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1824">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1825">%windir%\System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1826">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="dfa36-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1828">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1829">system32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1830">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1831">%windir%\System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="dfa36-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1833">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1833">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1835">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1835">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1836">System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1837">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1837">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1839">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1839">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1840">%windir%\System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1841">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1843">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1844">system32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1845">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1846">%windir%\System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="dfa36-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1848">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1848">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1850">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1850">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1851">Modelos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1852">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1852">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1853">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1854">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1854">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1855">%APPDATA%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="dfa36-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1856">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="dfa36-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1858">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1859">Modelos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1860">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1861">%USERPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="dfa36-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="dfa36-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="dfa36-1863">Não é usado no Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="dfa36-1864">Sem suporte a partir do Windows 7.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="dfa36-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1866">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1866">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1868">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1868">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1869">Fixado pelo usuário</span><span class="sxs-lookup"><span data-stu-id="dfa36-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1870">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1870">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1871">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1872">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1872">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User fixado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1874">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1875">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1876">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1877">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1878">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1879">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="dfa36-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1881">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1881">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1883">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1883">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1884">Usuários</span><span class="sxs-lookup"><span data-stu-id="dfa36-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1885">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1885">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1887">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1887">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1888">%SystemDrive%\Users</span><span class="sxs-lookup"><span data-stu-id="dfa36-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1889">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1890">Nenhum, novo para o Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dfa36-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1891">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1892">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1893">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1894">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="dfa36-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1896">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1896">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1898">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1898">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1899">Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1900">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1900">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1901">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1902">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1902">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1903">%LOCALAPPDATA%\Programs</span><span class="sxs-lookup"><span data-stu-id="dfa36-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1904">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1905">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1906">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1907">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1908">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1909">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="dfa36-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1911">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1911">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1913">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1913">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1914">Programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1915">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1915">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1916">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1917">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1917">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1918">%LOCALAPPDATA%\Programs\Common</span><span class="sxs-lookup"><span data-stu-id="dfa36-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1919">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1920">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1921">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1922">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1923">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1924">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="dfa36-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1926">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1926">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1928">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1928">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1929">O nome completo do usuário (por exemplo, Jean Philippe rosca) inserido quando a conta de usuário foi criada.</span><span class="sxs-lookup"><span data-stu-id="dfa36-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1930">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1930">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1931">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1932">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1932">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1933">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1934">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1935">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1936">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1937">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1938">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1939">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="dfa36-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1941">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1941">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1943">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1943">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1944">Bibliotecas</span><span class="sxs-lookup"><span data-stu-id="dfa36-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1945">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1945">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1946">VIRTUAISLUNS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1947">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1947">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1948">Não aplicável — pasta virtual</span><span class="sxs-lookup"><span data-stu-id="dfa36-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1949">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1950">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1951">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1952">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1953">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1954">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="dfa36-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1956">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1956">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1958">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1958">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1959">Vídeos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1960">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1960">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1961">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1962">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1962">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1963">%USERPROFILE%\Videos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1964">CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1964">CSIDL</span></span></td>
<td><span data-ttu-id="dfa36-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="dfa36-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1966">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1967">Meus vídeos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1968">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1969">%USERPROFILE%\My Documentos\minhas vídeos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="dfa36-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1971">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1971">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1973">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1973">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1974">Vídeos</span><span class="sxs-lookup"><span data-stu-id="dfa36-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1975">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1975">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1976">Peruser</span><span class="sxs-lookup"><span data-stu-id="dfa36-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1977">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1977">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span><span class="sxs-lookup"><span data-stu-id="dfa36-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1979">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1980">Nenhum, valor introduzido no Windows 7</span><span class="sxs-lookup"><span data-stu-id="dfa36-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1981">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1982">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1983">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1984">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="dfa36-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="dfa36-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dfa36-1986">GUID</span><span class="sxs-lookup"><span data-stu-id="dfa36-1986">GUID</span></span></td>
<td><span data-ttu-id="dfa36-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="dfa36-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1988">Nome de exibição</span><span class="sxs-lookup"><span data-stu-id="dfa36-1988">Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="dfa36-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1990">Tipo de pasta</span><span class="sxs-lookup"><span data-stu-id="dfa36-1990">Folder Type</span></span></td>
<td><span data-ttu-id="dfa36-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="dfa36-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1992">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-1992">Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1993">WINDIR</span><span class="sxs-lookup"><span data-stu-id="dfa36-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1994">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="dfa36-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dfa36-1996">Nome de exibição herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="dfa36-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="dfa36-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dfa36-1998">Caminho padrão herdado</span><span class="sxs-lookup"><span data-stu-id="dfa36-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="dfa36-1999">WINDIR</span><span class="sxs-lookup"><span data-stu-id="dfa36-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="dfa36-2000">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfa36-2000">Remarks</span></span>

<span data-ttu-id="dfa36-2001">A interpretação de determinados valores de **KNOWNFOLDERID** depende se a pasta faz parte de um aplicativo de 32 bits ou 64 bits e se esse aplicativo está sendo executado em um sistema operacional de 32 ou de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="dfa36-2002">Se seu aplicativo precisar distinguir entre, por exemplo, **arquivos de programas** e **arquivos de programas (x86)**, você deverá usar o **KNOWNFOLDERID** correto para a situação.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="dfa36-2003">As tabelas a seguir resumem o uso de **KNOWNFOLDERID** nesses casos.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="dfa36-2004">**PASTAS de os \_ ProgramId**</span><span class="sxs-lookup"><span data-stu-id="dfa36-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="dfa36-2005">Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="dfa36-2005">Operating System</span></span> | <span data-ttu-id="dfa36-2006">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dfa36-2006">Application</span></span> | <span data-ttu-id="dfa36-2007">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="dfa36-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="dfa36-2008">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-2008">Default Path</span></span> | <span data-ttu-id="dfa36-2009">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="dfa36-2010">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2010">32 bit</span></span> | <span data-ttu-id="dfa36-2011">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2011">32 bit</span></span> | <span data-ttu-id="dfa36-2012">PASTAS de os \_ ProgramId</span><span class="sxs-lookup"><span data-stu-id="dfa36-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="dfa36-2013">Arquivos de programas de% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="dfa36-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="dfa36-2014">arquivos de \_ programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="dfa36-2015">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2015">32 bit</span></span> | <span data-ttu-id="dfa36-2016">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2016">32 bit</span></span> | <span data-ttu-id="dfa36-2017">PASTA de \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="dfa36-2018">Arquivos de programas de% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="dfa36-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="dfa36-2019">FILESX86 do \_ programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="dfa36-2020">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2020">32 bit</span></span> | <span data-ttu-id="dfa36-2021">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2021">32 bit</span></span> | <span data-ttu-id="dfa36-2022">FOLDERid \_ ProgramFilesX64 (sem suporte em sistemas operacionais de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="dfa36-2023">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-2023">Not applicable</span></span> | <span data-ttu-id="dfa36-2024">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-2024">Not applicable</span></span> |
| <span data-ttu-id="dfa36-2025">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2025">64 bit</span></span> | <span data-ttu-id="dfa36-2026">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2026">64 bit</span></span> | <span data-ttu-id="dfa36-2027">PASTAS de os \_ ProgramId</span><span class="sxs-lookup"><span data-stu-id="dfa36-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="dfa36-2028">Arquivos de programas de% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="dfa36-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="dfa36-2029">arquivos de \_ programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="dfa36-2030">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2030">64 bit</span></span> | <span data-ttu-id="dfa36-2031">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2031">64 bit</span></span> | <span data-ttu-id="dfa36-2032">PASTA de \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="dfa36-2033">\\Arquivos de programa% systemdrive% (x86)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="dfa36-2034">FILESX86 do \_ programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="dfa36-2035">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2035">64 bit</span></span> | <span data-ttu-id="dfa36-2036">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2036">64 bit</span></span> | <span data-ttu-id="dfa36-2037">PASTA de \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="dfa36-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="dfa36-2038">Arquivos de programas de% SystemDrive% \\</span><span class="sxs-lookup"><span data-stu-id="dfa36-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="dfa36-2039">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-2039">None</span></span> |
| <span data-ttu-id="dfa36-2040">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2040">64 bit</span></span> | <span data-ttu-id="dfa36-2041">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2041">32 bit</span></span> | <span data-ttu-id="dfa36-2042">PASTAS de os \_ ProgramId</span><span class="sxs-lookup"><span data-stu-id="dfa36-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="dfa36-2043">\\Arquivos de programa% systemdrive% (x86)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="dfa36-2044">arquivos de \_ programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="dfa36-2045">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2045">64 bit</span></span> | <span data-ttu-id="dfa36-2046">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2046">32 bit</span></span> | <span data-ttu-id="dfa36-2047">PASTA de \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="dfa36-2048">\\Arquivos de programa% systemdrive% (x86)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="dfa36-2049">FILESX86 do \_ programa CSIDL \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="dfa36-2050">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2050">64 bit</span></span> | <span data-ttu-id="dfa36-2051">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2051">32 bit</span></span> | <span data-ttu-id="dfa36-2052">FOLDERid \_ ProgramFilesX64 (sem suporte para aplicativos de 32 bits)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="dfa36-2053">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-2053">Not applicable</span></span> | <span data-ttu-id="dfa36-2054">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-2054">Not applicable</span></span> |


<span data-ttu-id="dfa36-2055">**PASTA de \_ ProgramFilesCommon**</span><span class="sxs-lookup"><span data-stu-id="dfa36-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="dfa36-2056">Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="dfa36-2056">Operating System</span></span> | <span data-ttu-id="dfa36-2057">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dfa36-2057">Application</span></span> | <span data-ttu-id="dfa36-2058">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="dfa36-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="dfa36-2059">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-2059">Default Path</span></span> | <span data-ttu-id="dfa36-2060">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="dfa36-2061">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2061">32 bit</span></span> | <span data-ttu-id="dfa36-2062">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2062">32 bit</span></span> | <span data-ttu-id="dfa36-2063">PASTA de \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="dfa36-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="dfa36-2064">Arquivos% ProgramFiles% \\ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="dfa36-2065">arquivos de \_ programa CSIDL \_ \_ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="dfa36-2066">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2066">32 bit</span></span> | <span data-ttu-id="dfa36-2067">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2067">32 bit</span></span> | <span data-ttu-id="dfa36-2068">PASTA de \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="dfa36-2069">Arquivos% ProgramFiles% \\ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="dfa36-2070">Arquivos de \_ programas CSIDL \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="dfa36-2071">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2071">32 bit</span></span> | <span data-ttu-id="dfa36-2072">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2072">32 bit</span></span> | <span data-ttu-id="dfa36-2073">FOLDERid \_ ProgramFilesCommonX64 (indefinido)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="dfa36-2074">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-2074">Not applicable</span></span> | <span data-ttu-id="dfa36-2075">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="dfa36-2075">Not applicable</span></span> |
| <span data-ttu-id="dfa36-2076">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2076">64 bit</span></span> | <span data-ttu-id="dfa36-2077">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2077">64 bit</span></span> | <span data-ttu-id="dfa36-2078">PASTA de \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="dfa36-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="dfa36-2079">Arquivos% ProgramFiles% \\ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="dfa36-2080">arquivos de \_ programa CSIDL \_ \_ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="dfa36-2081">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2081">64 bit</span></span> | <span data-ttu-id="dfa36-2082">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2082">64 bit</span></span> | <span data-ttu-id="dfa36-2083">PASTA de \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="dfa36-2084">% ProgramFiles (x86)% \\ Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="dfa36-2085">Arquivos de \_ programas CSIDL \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="dfa36-2086">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2086">64 bit</span></span> | <span data-ttu-id="dfa36-2087">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2087">64 bit</span></span> | <span data-ttu-id="dfa36-2088">PASTA de \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="dfa36-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="dfa36-2089">Arquivos% ProgramFiles% \\ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="dfa36-2090">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-2090">None</span></span> |
| <span data-ttu-id="dfa36-2091">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2091">64 bit</span></span> | <span data-ttu-id="dfa36-2092">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2092">32 bit</span></span> | <span data-ttu-id="dfa36-2093">PASTA de \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="dfa36-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="dfa36-2094">% ProgramFiles (x86)% \\ Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="dfa36-2095">arquivos de \_ programa CSIDL \_ \_ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="dfa36-2096">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2096">64 bit</span></span> | <span data-ttu-id="dfa36-2097">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2097">32 bit</span></span> | <span data-ttu-id="dfa36-2098">PASTA de \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="dfa36-2099">% ProgramFiles (x86)% \\ Arquivos comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="dfa36-2100">Arquivos de \_ programas CSIDL \_ \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="dfa36-2101">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2101">64 bit</span></span> | <span data-ttu-id="dfa36-2102">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2102">32 bit</span></span> | <span data-ttu-id="dfa36-2103">PASTA de \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="dfa36-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="dfa36-2104">Arquivos% ProgramFiles% \\ comuns</span><span class="sxs-lookup"><span data-stu-id="dfa36-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="dfa36-2105">Nenhum</span><span class="sxs-lookup"><span data-stu-id="dfa36-2105">None</span></span> |


<span data-ttu-id="dfa36-2106">**Sistema FOLDERid \_**</span><span class="sxs-lookup"><span data-stu-id="dfa36-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="dfa36-2107">Sistema Operacional</span><span class="sxs-lookup"><span data-stu-id="dfa36-2107">Operating System</span></span> | <span data-ttu-id="dfa36-2108">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="dfa36-2108">Application</span></span> | <span data-ttu-id="dfa36-2109">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="dfa36-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="dfa36-2110">Default Caminho</span><span class="sxs-lookup"><span data-stu-id="dfa36-2110">Default Path</span></span> | <span data-ttu-id="dfa36-2111">Equivalente de CSIDl</span><span class="sxs-lookup"><span data-stu-id="dfa36-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="dfa36-2112">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2112">32 bit</span></span> | <span data-ttu-id="dfa36-2113">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2113">32 bit</span></span> | <span data-ttu-id="dfa36-2114">Sistema FOLDERid \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2114">FOLDERID\_System</span></span> | <span data-ttu-id="dfa36-2115">% WINDIR% \\ System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-2115">%windir%\\system32</span></span> | <span data-ttu-id="dfa36-2116">sistema CSIDl \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="dfa36-2117">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2117">32 bit</span></span> | <span data-ttu-id="dfa36-2118">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2118">32 bit</span></span> | <span data-ttu-id="dfa36-2119">PASTA de \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="dfa36-2120">% WINDIR% \\ System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-2120">%windir%\\system32</span></span> | <span data-ttu-id="dfa36-2121">SYSTEMX86 CSIDl \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="dfa36-2122">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2122">64 bit</span></span> | <span data-ttu-id="dfa36-2123">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2123">64 bit</span></span> | <span data-ttu-id="dfa36-2124">Sistema FOLDERid \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2124">FOLDERID\_System</span></span> | <span data-ttu-id="dfa36-2125">% WINDIR% \\ System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-2125">%windir%\\system32</span></span> | <span data-ttu-id="dfa36-2126">sistema CSIDl \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="dfa36-2127">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2127">64 bit</span></span> | <span data-ttu-id="dfa36-2128">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2128">64 bit</span></span> | <span data-ttu-id="dfa36-2129">PASTA de \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="dfa36-2130">% WINDIR% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="dfa36-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="dfa36-2131">SYSTEMX86 CSIDl \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="dfa36-2132">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2132">64 bit</span></span> | <span data-ttu-id="dfa36-2133">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2133">32 bit</span></span> | <span data-ttu-id="dfa36-2134">Sistema FOLDERid \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2134">FOLDERID\_System</span></span> | <span data-ttu-id="dfa36-2135">% WINDIR% \\ System32</span><span class="sxs-lookup"><span data-stu-id="dfa36-2135">%windir%\\system32</span></span> | <span data-ttu-id="dfa36-2136">sistema CSIDl \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="dfa36-2137">64 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2137">64 bit</span></span> | <span data-ttu-id="dfa36-2138">32 bits</span><span class="sxs-lookup"><span data-stu-id="dfa36-2138">32 bit</span></span> | <span data-ttu-id="dfa36-2139">PASTA de \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="dfa36-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="dfa36-2140">% WINDIR% \\ SysWOW64</span><span class="sxs-lookup"><span data-stu-id="dfa36-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="dfa36-2141">SYSTEMX86 CSIDl \_</span><span class="sxs-lookup"><span data-stu-id="dfa36-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="dfa36-2142">Nós usamos as cadeias de caracteres de ambiente para fornecer caminhos genéricos ao longo deste tópico.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="dfa36-2143">As tabelas a seguir fornecem exemplos dos caminhos que essas cadeias de caracteres de ambiente representam.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="dfa36-2144">Em alguns casos, esses caminhos podem não corresponder àqueles em um computador específico devido às escolhas feitas durante a instalação ou redirecionamento de pasta posterior.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="dfa36-2145">Observe que alguns caminhos foram alterados para o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="dfa36-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="dfa36-2146">**Windows Vista e posterior**</span><span class="sxs-lookup"><span data-stu-id="dfa36-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="dfa36-2147">Cadeia de caracteres do ambiente</span><span class="sxs-lookup"><span data-stu-id="dfa36-2147">Environment String</span></span> | <span data-ttu-id="dfa36-2148">Caminho de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="dfa36-2149">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="dfa36-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="dfa36-2150">C: \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="dfa36-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="dfa36-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2151">%APPDATA%</span></span> | <span data-ttu-id="dfa36-2152">C: \\ Users \\ *nome_do_usuário* \\ AppData \\ roaming</span><span class="sxs-lookup"><span data-stu-id="dfa36-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="dfa36-2153">LocalAppData</span><span class="sxs-lookup"><span data-stu-id="dfa36-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="dfa36-2154">C: \\ Users \\ *nome_do_usuário* \\ AppData \\ local</span><span class="sxs-lookup"><span data-stu-id="dfa36-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="dfa36-2155">%ProgramData%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2155">%ProgramData%</span></span> | <span data-ttu-id="dfa36-2156">C: \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="dfa36-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="dfa36-2157">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2157">%ProgramFiles%</span></span> | <span data-ttu-id="dfa36-2158">C: \\ arquivos de programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="dfa36-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="dfa36-2160">C: \\ arquivos de programas (x86)</span><span class="sxs-lookup"><span data-stu-id="dfa36-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="dfa36-2161">PUBLICADA</span><span class="sxs-lookup"><span data-stu-id="dfa36-2161">%PUBLIC%</span></span> | <span data-ttu-id="dfa36-2162">C: \\ usuários \\ públicos</span><span class="sxs-lookup"><span data-stu-id="dfa36-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="dfa36-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2163">%SystemDrive%</span></span> | <span data-ttu-id="dfa36-2164">C:</span><span class="sxs-lookup"><span data-stu-id="dfa36-2164">C:</span></span> |
| <span data-ttu-id="dfa36-2165">Perfil</span><span class="sxs-lookup"><span data-stu-id="dfa36-2165">%USERPROFILE%</span></span> | <span data-ttu-id="dfa36-2166">C: \\ usuários \\ *nome de usuário*</span><span class="sxs-lookup"><span data-stu-id="dfa36-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="dfa36-2167">WINDIR</span><span class="sxs-lookup"><span data-stu-id="dfa36-2167">%windir%</span></span> | <span data-ttu-id="dfa36-2168">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="dfa36-2168">C:\\Windows</span></span> |


<span data-ttu-id="dfa36-2169">**Windows XP e versões anteriores**</span><span class="sxs-lookup"><span data-stu-id="dfa36-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="dfa36-2170">Cadeia de caracteres do ambiente</span><span class="sxs-lookup"><span data-stu-id="dfa36-2170">Environment String</span></span> | <span data-ttu-id="dfa36-2171">Caminho de exemplo</span><span class="sxs-lookup"><span data-stu-id="dfa36-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="dfa36-2172">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="dfa36-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="dfa36-2173">C: \\ documenta e configurações \\ todos os usuários</span><span class="sxs-lookup"><span data-stu-id="dfa36-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="dfa36-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2174">%APPDATA%</span></span> | <span data-ttu-id="dfa36-2175">C: \\ Documents and Settings \\ *nome de usuário* \\ dados de aplicativos</span><span class="sxs-lookup"><span data-stu-id="dfa36-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="dfa36-2176">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2176">%ProgramFiles%</span></span> | <span data-ttu-id="dfa36-2177">C: \\ arquivos de programas</span><span class="sxs-lookup"><span data-stu-id="dfa36-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="dfa36-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="dfa36-2178">%SystemDrive%</span></span> | <span data-ttu-id="dfa36-2179">C:</span><span class="sxs-lookup"><span data-stu-id="dfa36-2179">C:</span></span> |
| <span data-ttu-id="dfa36-2180">Perfil</span><span class="sxs-lookup"><span data-stu-id="dfa36-2180">%USERPROFILE%</span></span> | <span data-ttu-id="dfa36-2181">C: \\ Documents and Settings \\ *nome de usuário*</span><span class="sxs-lookup"><span data-stu-id="dfa36-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="dfa36-2182">WINDIR</span><span class="sxs-lookup"><span data-stu-id="dfa36-2182">%windir%</span></span> | <span data-ttu-id="dfa36-2183">C: \\ Windows</span><span class="sxs-lookup"><span data-stu-id="dfa36-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="dfa36-2184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfa36-2184">Requirements</span></span>


| <span data-ttu-id="dfa36-2185">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfa36-2185">Requirement</span></span> | <span data-ttu-id="dfa36-2186">Valor</span><span class="sxs-lookup"><span data-stu-id="dfa36-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa36-2187">parâmetro</span><span class="sxs-lookup"><span data-stu-id="dfa36-2187">Header</span></span><br/> | <dl> <span data-ttu-id="dfa36-2188"><dt>KnownFolders. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa36-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa36-2189">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfa36-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa36-2190">**CSIDl**</span><span class="sxs-lookup"><span data-stu-id="dfa36-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="dfa36-2191">Pastas conhecidas</span><span class="sxs-lookup"><span data-stu-id="dfa36-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="dfa36-2192">Trabalhando com pastas conhecidas em aplicativos</span><span class="sxs-lookup"><span data-stu-id="dfa36-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="dfa36-2193">Como estender pastas conhecidas com pastas personalizadas</span><span class="sxs-lookup"><span data-stu-id="dfa36-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="dfa36-2194">[Exemplo de pastas conhecidas](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dfa36-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
