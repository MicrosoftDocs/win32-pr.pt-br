---
description: Contém informações sobre a caixa de diálogo exibida pela função CryptUIDlgSelectCertificate.
ms.assetid: 073a67a0-427b-4b81-82a0-1bb0a216a335
title: Estrutura de CRYPTUI_SELECTCERTIFICATE_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_SELECTCERTIFICATE_STRUCT
- CRYPTUI_SELECTCERTIFICATE_STRUCTA
- CRYPTUI_SELECTCERTIFICATE_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3db7e59006e964b7335a4a246fb63d7ca7b80577
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105755952"
---
# <a name="cryptui_selectcertificate_struct-structure"></a><span data-ttu-id="4f1db-103">\_Estrutura de \_ struct CRYPTUI SELECTCERTIFICATE</span><span class="sxs-lookup"><span data-stu-id="4f1db-103">CRYPTUI\_SELECTCERTIFICATE\_STRUCT structure</span></span>

<span data-ttu-id="4f1db-104">A estrutura de **\_ \_ struct CRYPTUI SELECTCERTIFICATE** contém informações sobre a caixa de diálogo exibida pela função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4f1db-104">The **CRYPTUI\_SELECTCERTIFICATE\_STRUCT** structure contains information about the dialog box displayed by the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f1db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f1db-105">Syntax</span></span>


```C++
typedef struct _CRYPTUI_SELECTCERTIFICATE_STRUCT {
  DWORD               dwSize;
  HWND                hwndParent;
  DWORD               dwFlags;
  LPCTSTR             szTitle;
  DWORD               dwDontUseColumn;
  LPCTSTR             szDisplayString;
  PFNCFILTERPROC      pFilterCallback;
  PFNCCERTDISPLAYPROC pDisplayCallback;
  void                *pvCallbackData;
  DWORD               cDisplayStores;
  HCERTSTORE          *rghDisplayStores;
  DWORD               cStores;
  HCERTSTORE          *rghStores;
  DWORD               cPropSheetPages;
  LPCPROPSHEETPAGE    rgPropSheetPages;
  HCERTSTORE          hSelectedCertStore;
} CRYPTUI_SELECTCERTIFICATE_STRUCT, *PCRYPTUI_SELECTCERTIFICATE_STRUCT;
```



## <a name="members"></a><span data-ttu-id="4f1db-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4f1db-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="4f1db-107">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="4f1db-107">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-108">O tamanho, em bytes, dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="4f1db-108">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-109">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="4f1db-109">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-110">O identificador da janela pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f1db-110">The handle of the parent window of the dialog box.</span></span> <span data-ttu-id="4f1db-111">Se esse valor for **nulo**, a janela pai será a janela da área de trabalho padrão.</span><span class="sxs-lookup"><span data-stu-id="4f1db-111">If this value is **NULL**, the parent window is the default desktop window.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-112">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="4f1db-112">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-113">Especifica opções adicionais para a função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) .</span><span class="sxs-lookup"><span data-stu-id="4f1db-113">Specifies additional options for the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function.</span></span> <span data-ttu-id="4f1db-114">Isso pode ser zero ou um ou um valor nulo **ou** dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="4f1db-114">This can be zero or a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="4f1db-115">Valor</span><span class="sxs-lookup"><span data-stu-id="4f1db-115">Value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="4f1db-116">Significado</span><span class="sxs-lookup"><span data-stu-id="4f1db-116">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPTUI_SELECTCERT_ADDFROMDS"></span><span id="cryptui_selectcert_addfromds"></span><dl> <span data-ttu-id="4f1db-117"><dt>**CRYPTUI \_ SELECTCERT \_ ADDFROMDS**</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-117"><dt>**CRYPTUI\_SELECTCERT\_ADDFROMDS**</dt></span></span> </dl>                              | <span data-ttu-id="4f1db-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="4f1db-118">Reserved.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="CRYPTUI_SELECTCERT_LEGACY"></span><span id="cryptui_selectcert_legacy"></span><dl> <span data-ttu-id="4f1db-119"><dt>**CRYPTUI \_ SELECTCERT \_ Legacy**</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-119"><dt>**CRYPTUI\_SELECTCERT\_LEGACY**</dt></span></span> </dl>                                       | <span data-ttu-id="4f1db-120">Especifica que a caixa de diálogo herdada deve ser exibida.</span><span class="sxs-lookup"><span data-stu-id="4f1db-120">Specifies that the legacy dialog is to be displayed.</span></span><br/>                                                                                                                                                                                                                                                                                                                      |
| <span id="CRYPTUI_SELECTCERT_MULTISELECT"></span><span id="cryptui_selectcert_multiselect"></span><dl> <span data-ttu-id="4f1db-121"><dt>**CRYPTUI \_ SELECTCERT \_ MultiSelect**</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-121"><dt>**CRYPTUI\_SELECTCERT\_MULTISELECT**</dt></span></span> </dl>                        | <span data-ttu-id="4f1db-122">Permite que o usuário selecione mais de um certificado na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f1db-122">Allows the user to select more than one certificate in the dialog box.</span></span> <span data-ttu-id="4f1db-123">Se esse sinalizador for definido, a função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) sempre retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4f1db-123">If this flag is set, the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function always returns **NULL**.</span></span> <span data-ttu-id="4f1db-124">O membro **hSelectedCertStore** dessa estrutura deve conter um identificador para um repositório de certificados.</span><span class="sxs-lookup"><span data-stu-id="4f1db-124">The **hSelectedCertStore** member of this structure must contain a handle to a certificate store.</span></span> <span data-ttu-id="4f1db-125">Os certificados selecionados pelo usuário serão adicionados a esse armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4f1db-125">The certificates selected by the user will be added to this store.</span></span><br/> |
| <span id="CRYPTUI_SELECTCERT_PUT_WINDOW_TOPMOST"></span><span id="cryptui_selectcert_put_window_topmost"></span><dl> <span data-ttu-id="4f1db-126"><dt>**CRYPTUI \_ SELECTCERT \_ colocar a \_ janela na \_ extremidade superior**</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-126"><dt>**CRYPTUI\_SELECTCERT\_PUT\_WINDOW\_TOPMOST**</dt></span></span> </dl> | <span data-ttu-id="4f1db-127">Força a interface do usuário de criptografia a ser a janela superior na tela.</span><span class="sxs-lookup"><span data-stu-id="4f1db-127">Forces the cryptography UI to be the top window on the screen.</span></span><br/>                                                                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="4f1db-128">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="4f1db-128">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-129">O título de exibição da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f1db-129">The display title for the dialog box.</span></span> <span data-ttu-id="4f1db-130">Se o valor desse membro for **nulo**, o título padrão de "Selecionar certificado" será usado.</span><span class="sxs-lookup"><span data-stu-id="4f1db-130">If the value of this member is **NULL**, the default title of "Select Certificate" is used.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-131">**dwDontUseColumn**</span><span class="sxs-lookup"><span data-stu-id="4f1db-131">**dwDontUseColumn**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-132">Sinalizadores que podem ser combinados para excluir colunas da exibição.</span><span class="sxs-lookup"><span data-stu-id="4f1db-132">Flags that can be combined to exclude columns of the display.</span></span>



| <span data-ttu-id="4f1db-133">Valor</span><span class="sxs-lookup"><span data-stu-id="4f1db-133">Value</span></span>                                                                                                                                                                                                                                                                                       | <span data-ttu-id="4f1db-134">Significado</span><span class="sxs-lookup"><span data-stu-id="4f1db-134">Meaning</span></span>                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <span id="CRYPTUI_SELECT_ISSUEDTO_COLUMN"></span><span id="cryptui_select_issuedto_column"></span><dl> <span data-ttu-id="4f1db-135"><dt>**CRYPTUI \_ Selecione \_ emitido \_**</dt> para a coluna <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-135"><dt>**CRYPTUI\_SELECT\_ISSUEDTO\_COLUMN**</dt> <dt>1 (0x1)</dt></span></span> </dl>             | <span data-ttu-id="4f1db-136">Não exibir informações **emitidas** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-136">Do not display **ISSUEDTO** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_ISSUEDBY_COLUMN"></span><span id="cryptui_select_issuedby_column"></span><dl> <span data-ttu-id="4f1db-137"><dt>**CRYPTUI \_ Selecione \_ ISSUEDBY \_ coluna**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-137"><dt>**CRYPTUI\_SELECT\_ISSUEDBY\_COLUMN**</dt> <dt>2 (0x2)</dt></span></span> </dl>             | <span data-ttu-id="4f1db-138">Não exibir informações de **ISSUEDBY** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-138">Do not display **ISSUEDBY** information.</span></span><br/>    |
| <span id="CRYPTUI_SELECT_INTENDEDUSE_COLUMN"></span><span id="cryptui_select_intendeduse_column"></span><dl> <span data-ttu-id="4f1db-139"><dt>**CRYPTUI \_ Selecione \_ INTENDEDUSE \_ coluna**</dt> <dt>4 (0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-139"><dt>**CRYPTUI\_SELECT\_INTENDEDUSE\_COLUMN**</dt> <dt>4 (0x4)</dt></span></span> </dl>    | <span data-ttu-id="4f1db-140">Não exibir informações de **IntendedUse** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-140">Do not display **IntendedUse** information.</span></span><br/> |
| <span id="CRYPTUI_SELECT_FRIENDLYNAME_COLUMN"></span><span id="cryptui_select_friendlyname_column"></span><dl> <span data-ttu-id="4f1db-141"><dt>**CRYPTUI \_ Selecione \_ FriendlyName \_ coluna**</dt> <dt>8 (0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-141"><dt>**CRYPTUI\_SELECT\_FRIENDLYNAME\_COLUMN**</dt> <dt>8 (0x8)</dt></span></span> </dl> | <span data-ttu-id="4f1db-142">Não exibir informações de nome.</span><span class="sxs-lookup"><span data-stu-id="4f1db-142">Do not display name information.</span></span><br/>            |
| <span id="CRYPTUI_SELECT_LOCATION_COLUMN"></span><span id="cryptui_select_location_column"></span><dl> <span data-ttu-id="4f1db-143"><dt>**CRYPTUI \_ Selecione \_ a \_ coluna de localização**</dt> <dt>16 (0x10)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-143"><dt>**CRYPTUI\_SELECT\_LOCATION\_COLUMN**</dt> <dt>16 (0x10)</dt></span></span> </dl>           | <span data-ttu-id="4f1db-144">Não exibir informações de localização.</span><span class="sxs-lookup"><span data-stu-id="4f1db-144">Do not display location information.</span></span><br/>        |
| <span id="CRYPTUI_SELECT_EXPIRATION_COLUMN"></span><span id="cryptui_select_expiration_column"></span><dl> <span data-ttu-id="4f1db-145"><dt>**CRYPTUI \_ Selecione \_ a \_ coluna de expiração**</dt> <dt>32 (0x20)</dt></span><span class="sxs-lookup"><span data-stu-id="4f1db-145"><dt>**CRYPTUI\_SELECT\_EXPIRATION\_COLUMN**</dt> <dt>32 (0x20)</dt></span></span> </dl>     | <span data-ttu-id="4f1db-146">Não exibir informações de expiração.</span><span class="sxs-lookup"><span data-stu-id="4f1db-146">Do not display expiration information.</span></span><br/>      |



 

</dd> <dt>

<span data-ttu-id="4f1db-147">**szDisplayString**</span><span class="sxs-lookup"><span data-stu-id="4f1db-147">**szDisplayString**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-148">Texto exibido na caixa de diálogo para instruir o usuário.</span><span class="sxs-lookup"><span data-stu-id="4f1db-148">Text that is displayed in the dialog box to instruct the user.</span></span> <span data-ttu-id="4f1db-149">Se o valor desse membro for **nulo**, a cadeia de caracteres padrão "selecionar um certificado que você deseja usar" será usada.</span><span class="sxs-lookup"><span data-stu-id="4f1db-149">If the value of this member is **NULL**, the default string "Select a certificate you want to use" is used.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-150">**pFilterCallback**</span><span class="sxs-lookup"><span data-stu-id="4f1db-150">**pFilterCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-151">Um ponteiro para uma função de retorno de chamada [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) que filtra os certificados que são exibidos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f1db-151">A pointer to a [**PFNCFILTERPROC**](/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc) callback function that filters the certificates that are displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-152">**pDisplayCallback**</span><span class="sxs-lookup"><span data-stu-id="4f1db-152">**pDisplayCallback**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-153">Um ponteiro para uma função de retorno de chamada [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) que exibe certificados que o usuário seleciona para exibir.</span><span class="sxs-lookup"><span data-stu-id="4f1db-153">A pointer to a [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md) callback function that displays certificates that the user selects to view.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-154">**pvCallbackData**</span><span class="sxs-lookup"><span data-stu-id="4f1db-154">**pvCallbackData**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-155">Dados adicionais que são passados para as funções de retorno de chamada especificadas pelos membros **pFilterCallback** e **pDisplayCallback** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-155">Additional data that is passed to the callback functions specified by the **pFilterCallback** and **pDisplayCallback** members.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-156">**cDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="4f1db-156">**cDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-157">O número de repositórios de certificados na matriz **rghDisplayStores** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-157">The number of certificate stores in the **rghDisplayStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-158">**rghDisplayStores**</span><span class="sxs-lookup"><span data-stu-id="4f1db-158">**rghDisplayStores**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-159">Um ponteiro para uma matriz de armazenamentos que contém certificados disponíveis para seleção na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f1db-159">A pointer to an array of stores that contain certificates available for selection in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-160">**cStores**</span><span class="sxs-lookup"><span data-stu-id="4f1db-160">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-161">O número de repositórios de certificados na matriz **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-161">The number of certificate stores in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-162">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="4f1db-162">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-163">Um ponteiro para uma matriz de repositórios de certificados para pesquisar ao criar uma cadeia de certificados e verificar a relação de confiança dos certificados exibidos na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="4f1db-163">A pointer to an array of certificate stores to search when building a certificate chain and verifying trust for the certificates displayed in the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-164">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="4f1db-164">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-165">O número de páginas de propriedades na matriz **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-165">The number of property pages in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-166">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="4f1db-166">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-167">Um ponteiro para uma matriz de estruturas **PROPSHEETPAGE** que representam páginas de propriedades que são passadas para a caixa de diálogo de exibição de certificado quando um certificado é selecionado para exibição.</span><span class="sxs-lookup"><span data-stu-id="4f1db-167">A pointer to an array of **PROPSHEETPAGE** structures that represent property pages that are passed to the certificate viewing dialog box when a certificate is selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="4f1db-168">**hSelectedCertStore**</span><span class="sxs-lookup"><span data-stu-id="4f1db-168">**hSelectedCertStore**</span></span>
</dt> <dd>

<span data-ttu-id="4f1db-169">Um identificador para um repositório de certificados criado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="4f1db-169">A handle to a certificate store created by the caller.</span></span> <span data-ttu-id="4f1db-170">Os certificados selecionados pelo usuário são adicionados a esse armazenamento.</span><span class="sxs-lookup"><span data-stu-id="4f1db-170">The certificates selected by the user are added to this store.</span></span> <span data-ttu-id="4f1db-171">Se o número de certificados nesse repositório for o mesmo antes e depois de chamar [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), o usuário fechou a caixa de diálogo sem selecionar nenhum certificado.</span><span class="sxs-lookup"><span data-stu-id="4f1db-171">If the number of certificates in this store is the same before and after calling [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md), the user closed the dialog box without selecting any certificates.</span></span>

<span data-ttu-id="4f1db-172">Esse membro não será usado se o membro **dwFlags** dessa estrutura não contiver o sinalizador **CRYPTUI \_ SELECTCERT \_ MultiSelect** .</span><span class="sxs-lookup"><span data-stu-id="4f1db-172">This member is not used if the **dwFlags** member of this structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f1db-173">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f1db-173">Requirements</span></span>



| <span data-ttu-id="4f1db-174">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f1db-174">Requirement</span></span> | <span data-ttu-id="4f1db-175">Valor</span><span class="sxs-lookup"><span data-stu-id="4f1db-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f1db-176">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f1db-176">Minimum supported client</span></span><br/> | <span data-ttu-id="4f1db-177">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="4f1db-177">Windows XP \[desktop apps only\]</span></span><br/>                                                                     |
| <span data-ttu-id="4f1db-178">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="4f1db-178">Minimum supported server</span></span><br/> | <span data-ttu-id="4f1db-179">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="4f1db-179">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4f1db-180">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="4f1db-180">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4f1db-181">**CRYPTUI \_ SELECTCERTIFICATE \_ STRUCTW** (Unicode) e **CRYPTUI \_ SELECTCERTIFICATE \_ structA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4f1db-181">**CRYPTUI\_SELECTCERTIFICATE\_STRUCTW** (Unicode) and **CRYPTUI\_SELECTCERTIFICATE\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4f1db-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="4f1db-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f1db-183">**CryptUIDlgSelectCertificate**</span><span class="sxs-lookup"><span data-stu-id="4f1db-183">**CryptUIDlgSelectCertificate**</span></span>](cryptuidlgselectcertificate.md)
</dt> </dl>

 

 




