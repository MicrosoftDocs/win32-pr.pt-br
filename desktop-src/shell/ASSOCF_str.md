---
description: Fornece informações para os métodos de interface IQueryAssociations.
ms.assetid: e67d0282-9090-43e6-aedf-bb1fc0443221
title: Enumeração ASSOCF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70ddb0b4fb89925c643eb01c276772b9a7151578
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104172533"
---
# <a name="assocf-enumeration"></a><span data-ttu-id="453bc-103">Enumeração ASSOCF</span><span class="sxs-lookup"><span data-stu-id="453bc-103">ASSOCF enumeration</span></span>

<span data-ttu-id="453bc-104">Fornece informações para os métodos de interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) .</span><span class="sxs-lookup"><span data-stu-id="453bc-104">Provides information to the [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="453bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="453bc-105">Syntax</span></span>

<span codelanguage="ManagedCPlusPlus"></span>

<table><colgroup><col style="width: 100%" /></colgroup><thead><tr class="header"><th><span data-ttu-id="453bc-106">C++</span><span class="sxs-lookup"><span data-stu-id="453bc-106">C++</span></span></th></tr></thead><tbody><tr class="odd"><td><pre><code>typedef enum  { 
  ASSOCF_NONE                  = 0x00000000,
  ASSOCF_INIT_NOREMAPCLSID     = 0x00000001,
  ASSOCF_INIT_BYEXENAME        = 0x00000002,
  ASSOCF_OPEN_BYEXENAME        = 0x00000002,
  ASSOCF_INIT_DEFAULTTOSTAR    = 0x00000004,
  ASSOCF_INIT_DEFAULTTOFOLDER  = 0x00000008,
  ASSOCF_NOUSERSETTINGS        = 0x00000010,
  ASSOCF_NOTRUNCATE            = 0x00000020,
  ASSOCF_VERIFY                = 0x00000040,
  ASSOCF_REMAPRUNDLL           = 0x00000080,
  ASSOCF_NOFIXUPS              = 0x00000100,
  ASSOCF_IGNOREBASECLASS       = 0x00000200,
  ASSOCF_INIT_IGNOREUNKNOWN    = 0x00000400,
  ASSOCF_INIT_FIXED_PROGID     = 0x00000800,
  ASSOCF_IS_PROTOCOL           = 0x00001000,
  ASSOCF_INIT_FOR_FILE         = 0x00002000
} ASSOCF;</code></pre></td></tr></tbody></table>



## <a name="constants"></a><span data-ttu-id="453bc-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="453bc-107">Constants</span></span>

 <span data-ttu-id="453bc-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF \_ nenhum**</span><span class="sxs-lookup"><span data-stu-id="453bc-108"><span id="ASSOCF_NONE"></span><span id="assocf_none"></span>**ASSOCF\_NONE**</span></span> 

<span data-ttu-id="453bc-109">Nenhuma das opções a seguir está definida.</span><span class="sxs-lookup"><span data-stu-id="453bc-109">None of the following options are set.</span></span>

 <span data-ttu-id="453bc-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF \_ init \_ NOREMAPCLSID**</span><span class="sxs-lookup"><span data-stu-id="453bc-110"><span id="ASSOCF_INIT_NOREMAPCLSID"></span><span id="assocf_init_noremapclsid"></span>**ASSOCF\_INIT\_NOREMAPCLSID**</span></span> 

<span data-ttu-id="453bc-111">Instrui os métodos de interface [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) a não mapear valores CLSID para valores de ProgID.</span><span class="sxs-lookup"><span data-stu-id="453bc-111">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) interface methods not to map CLSID values to ProgID values.</span></span>

 <span data-ttu-id="453bc-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF \_ init \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="453bc-112"><span id="ASSOCF_INIT_BYEXENAME"></span><span id="assocf_init_byexename"></span>**ASSOCF\_INIT\_BYEXENAME**</span></span> 

<span data-ttu-id="453bc-113">Identifica o valor do parâmetro *pwszAssoc* de [**IQueryAssociations:: init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) como um nome de arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="453bc-113">Identifies the value of the *pwszAssoc* parameter of [**IQueryAssociations::Init**](/windows/win32/api/shlwapi/nf-shlwapi-iqueryassociations-init) as an executable file name.</span></span> <span data-ttu-id="453bc-114">Se esse sinalizador não for definido, a chave raiz será definida como o ProgID associado à chave **. exe** em vez do ProgID do arquivo executável.</span><span class="sxs-lookup"><span data-stu-id="453bc-114">If this flag is not set, the root key will be set to the ProgID associated with the **.exe** key instead of the executable file's ProgID.</span></span>

 <span data-ttu-id="453bc-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF \_ abrir \_ BYEXENAME**</span><span class="sxs-lookup"><span data-stu-id="453bc-115"><span id="ASSOCF_OPEN_BYEXENAME"></span><span id="assocf_open_byexename"></span>**ASSOCF\_OPEN\_BYEXENAME**</span></span> 

<span data-ttu-id="453bc-116">Idêntico a **ASSOCF \_ init \_ BYEXENAME**.</span><span class="sxs-lookup"><span data-stu-id="453bc-116">Identical to **ASSOCF\_INIT\_BYEXENAME**.</span></span>

 <span data-ttu-id="453bc-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF \_ init \_ DEFAULTTOSTAR**</span><span class="sxs-lookup"><span data-stu-id="453bc-117"><span id="ASSOCF_INIT_DEFAULTTOSTAR"></span><span id="assocf_init_defaulttostar"></span>**ASSOCF\_INIT\_DEFAULTTOSTAR**</span></span> 

<span data-ttu-id="453bc-118">Especifica que quando um método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) não encontra o valor solicitado sob a chave raiz, ele deve tentar recuperar o valor comparável da **\*** subchave.</span><span class="sxs-lookup"><span data-stu-id="453bc-118">Specifies that when an [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **\*** subkey.</span></span>

 <span data-ttu-id="453bc-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF \_ init \_ DEFAULTTOFOLDER**</span><span class="sxs-lookup"><span data-stu-id="453bc-119"><span id="ASSOCF_INIT_DEFAULTTOFOLDER"></span><span id="assocf_init_defaulttofolder"></span>**ASSOCF\_INIT\_DEFAULTTOFOLDER**</span></span> 

<span data-ttu-id="453bc-120">Especifica que quando um método [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) não encontra o valor solicitado sob a chave raiz, ele deve tentar recuperar o valor comparável da subchave **Folder** .</span><span class="sxs-lookup"><span data-stu-id="453bc-120">Specifies that when a [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) method does not find the requested value under the root key, it should attempt to retrieve the comparable value from the **Folder** subkey.</span></span>

 <span data-ttu-id="453bc-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF \_ NOUSERSETTINGS**</span><span class="sxs-lookup"><span data-stu-id="453bc-121"><span id="ASSOCF_NOUSERSETTINGS"></span><span id="assocf_nousersettings"></span>**ASSOCF\_NOUSERSETTINGS**</span></span> 

<span data-ttu-id="453bc-122">Especifica que somente **a \_ \_ raiz de classes hKey** deve ser pesquisada e que o **HKEY \_ Current \_ User** deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="453bc-122">Specifies that only **HKEY\_CLASSES\_ROOT** should be searched, and that **HKEY\_CURRENT\_USER** should be ignored.</span></span>

 <span data-ttu-id="453bc-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF \_ NOtruncate**</span><span class="sxs-lookup"><span data-stu-id="453bc-123"><span id="ASSOCF_NOTRUNCATE"></span><span id="assocf_notruncate"></span>**ASSOCF\_NOTRUNCATE**</span></span> 

<span data-ttu-id="453bc-124">Especifica que a cadeia de caracteres de retorno não deve ser truncada.</span><span class="sxs-lookup"><span data-stu-id="453bc-124">Specifies that the return string should not be truncated.</span></span> <span data-ttu-id="453bc-125">Em vez disso, retorne um valor de erro e o tamanho necessário para a cadeia de caracteres completa.</span><span class="sxs-lookup"><span data-stu-id="453bc-125">Instead, return an error value and the required size for the complete string.</span></span>

 <span data-ttu-id="453bc-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF \_ verificar**</span><span class="sxs-lookup"><span data-stu-id="453bc-126"><span id="ASSOCF_VERIFY"></span><span id="assocf_verify"></span>**ASSOCF\_VERIFY**</span></span> 

<span data-ttu-id="453bc-127">Instrui os métodos [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) para verificar se os dados são precisos.</span><span class="sxs-lookup"><span data-stu-id="453bc-127">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to verify that data is accurate.</span></span> <span data-ttu-id="453bc-128">Essa configuração permite que os métodos **IQueryAssociations** leiam dados do disco rígido do usuário para verificação.</span><span class="sxs-lookup"><span data-stu-id="453bc-128">This setting allows **IQueryAssociations** methods to read data from the user's hard disk for verification.</span></span> <span data-ttu-id="453bc-129">Por exemplo, eles podem verificar o nome amigável no registro em relação a um armazenado no arquivo. exe.</span><span class="sxs-lookup"><span data-stu-id="453bc-129">For example, they can check the friendly name in the registry against the one stored in the .exe file.</span></span> <span data-ttu-id="453bc-130">Definir esse sinalizador normalmente reduz a eficiência do método.</span><span class="sxs-lookup"><span data-stu-id="453bc-130">Setting this flag typically reduces the efficiency of the method.</span></span>

 <span data-ttu-id="453bc-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF \_ REMAPRUNDLL**</span><span class="sxs-lookup"><span data-stu-id="453bc-131"><span id="ASSOCF_REMAPRUNDLL"></span><span id="assocf_remaprundll"></span>**ASSOCF\_REMAPRUNDLL**</span></span> 

<span data-ttu-id="453bc-132">Instrui os métodos [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) a ignorar Rundll.exe e retornar informações sobre seu destino.</span><span class="sxs-lookup"><span data-stu-id="453bc-132">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods to ignore Rundll.exe and return information about its target.</span></span> <span data-ttu-id="453bc-133">Normalmente, os métodos **IQueryAssociations** retornam informações sobre o primeiro. exe ou. dll em uma cadeia de caracteres de comando.</span><span class="sxs-lookup"><span data-stu-id="453bc-133">Typically **IQueryAssociations** methods return information about the first .exe or .dll in a command string.</span></span> <span data-ttu-id="453bc-134">Se um comando usa Rundll.exe, a definição desse sinalizador informa o método para ignorar Rundll.exe e retornar informações sobre seu destino.</span><span class="sxs-lookup"><span data-stu-id="453bc-134">If a command uses Rundll.exe, setting this flag tells the method to ignore Rundll.exe and return information about its target.</span></span>

 <span data-ttu-id="453bc-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF \_ NOcorreções**</span><span class="sxs-lookup"><span data-stu-id="453bc-135"><span id="ASSOCF_NOFIXUPS"></span><span id="assocf_nofixups"></span>**ASSOCF\_NOFIXUPS**</span></span> 

<span data-ttu-id="453bc-136">Instrui os métodos [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) a não corrigir erros no registro, como o nome amigável de uma função que não corresponde a um encontrado no arquivo. exe.</span><span class="sxs-lookup"><span data-stu-id="453bc-136">Instructs [**IQueryAssociations**](/windows/win32/api/shlwapi/nn-shlwapi-iqueryassociations) methods not to fix errors in the registry, such as the friendly name of a function not matching the one found in the .exe file.</span></span>

 <span data-ttu-id="453bc-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF \_ IGNOREBASECLASS**</span><span class="sxs-lookup"><span data-stu-id="453bc-137"><span id="ASSOCF_IGNOREBASECLASS"></span><span id="assocf_ignorebaseclass"></span>**ASSOCF\_IGNOREBASECLASS**</span></span> 

<span data-ttu-id="453bc-138">Especifica que o valor de BaseClass deve ser ignorado.</span><span class="sxs-lookup"><span data-stu-id="453bc-138">Specifies that the BaseClass value should be ignored.</span></span>

 <span data-ttu-id="453bc-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF \_ init \_ IGNOREUNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="453bc-139"><span id="ASSOCF_INIT_IGNOREUNKNOWN"></span><span id="assocf_init_ignoreunknown"></span>**ASSOCF\_INIT\_IGNOREUNKNOWN**</span></span> 

<span data-ttu-id="453bc-140">**Introduzido no Windows 7**.</span><span class="sxs-lookup"><span data-stu-id="453bc-140">**Introduced in Windows 7**.</span></span> <span data-ttu-id="453bc-141">Especifica que o ProgID "desconhecido" deve ser ignorado; em vez disso, falha.</span><span class="sxs-lookup"><span data-stu-id="453bc-141">Specifies that the "Unknown" ProgID should be ignored; instead, fail.</span></span>

 <span data-ttu-id="453bc-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**\_ \_ ProgID fixo ASSOCF \_ init**</span><span class="sxs-lookup"><span data-stu-id="453bc-142"><span id="ASSOCF_INIT_FIXED_PROGID"></span><span id="assocf_init_fixed_progid"></span>**ASSOCF\_INIT\_FIXED\_PROGID**</span></span> 

<span data-ttu-id="453bc-143">**Introduzido no Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="453bc-143">**Introduced in Windows 8**.</span></span> <span data-ttu-id="453bc-144">Especifica que o ProgID fornecido deve ser mapeado usando os padrões do sistema, em vez dos padrões do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="453bc-144">Specifies that the supplied ProgID should be mapped using the system defaults, rather than the current user defaults.</span></span>

 <span data-ttu-id="453bc-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF \_ é \_ protocolo**</span><span class="sxs-lookup"><span data-stu-id="453bc-145"><span id="ASSOCF_IS_PROTOCOL"></span><span id="assocf_is_protocol"></span>**ASSOCF\_IS\_PROTOCOL**</span></span> 

<span data-ttu-id="453bc-146">**Introduzido no Windows 8**.</span><span class="sxs-lookup"><span data-stu-id="453bc-146">**Introduced in Windows 8**.</span></span> <span data-ttu-id="453bc-147">Especifica que o valor é um protocolo e deve ser mapeado usando os padrões do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="453bc-147">Specifies that the value is a protocol, and should be mapped using the current user defaults.</span></span>

 <span data-ttu-id="453bc-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF \_ init \_ para \_ arquivo**</span><span class="sxs-lookup"><span data-stu-id="453bc-148"><span id="ASSOCF_INIT_FOR_FILE"></span><span id="assocf_init_for_file"></span>**ASSOCF\_INIT\_FOR\_FILE**</span></span> 

<span data-ttu-id="453bc-149">**Introduzido em Windows 8.1**.</span><span class="sxs-lookup"><span data-stu-id="453bc-149">**Introduced in Windows 8.1**.</span></span> <span data-ttu-id="453bc-150">Especifica que o ProgID corresponde a uma associação baseada em extensão de arquivo.</span><span class="sxs-lookup"><span data-stu-id="453bc-150">Specifies that the ProgID corresponds with a file extension based association.</span></span> <span data-ttu-id="453bc-151">Use junto com o **ASSOCF \_ init \_ Fixed \_ ProgID**.</span><span class="sxs-lookup"><span data-stu-id="453bc-151">Use together with **ASSOCF\_INIT\_FIXED\_PROGID**.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="453bc-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="453bc-152">Requirements</span></span>



| <span data-ttu-id="453bc-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="453bc-153">Requirement</span></span> | <span data-ttu-id="453bc-154">Valor</span><span class="sxs-lookup"><span data-stu-id="453bc-154">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="453bc-155">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="453bc-155">Minimum supported client</span></span> | <span data-ttu-id="453bc-156">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="453bc-156">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span>               |
| <span data-ttu-id="453bc-157">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="453bc-157">Minimum supported server</span></span> | <span data-ttu-id="453bc-158">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="453bc-158">Windows 2000 Server \[desktop apps only\]</span></span>                                 |
| <span data-ttu-id="453bc-159">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="453bc-159">Header</span></span>                   |  <span data-ttu-id="453bc-160">Shlwapi. h</span><span class="sxs-lookup"><span data-stu-id="453bc-160">Shlwapi.h</span></span>  |



## <a name="see-also"></a><span data-ttu-id="453bc-161">Confira também</span><span class="sxs-lookup"><span data-stu-id="453bc-161">See also</span></span>

 <span data-ttu-id="453bc-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span><span class="sxs-lookup"><span data-stu-id="453bc-162">[**AssocQueryKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerykeya) [**AssocQueryString**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa) [**AssocQueryStringByKey**](/windows/win32/api/shlwapi/nf-shlwapi-assocquerystringa)</span></span> 

 

 

<span data-ttu-id="453bc-163">© 2017 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="453bc-163">© 2017 Microsoft.</span></span> <span data-ttu-id="453bc-164">Todos os direitos reservados.</span><span class="sxs-lookup"><span data-stu-id="453bc-164">All rights reserved.</span></span>
