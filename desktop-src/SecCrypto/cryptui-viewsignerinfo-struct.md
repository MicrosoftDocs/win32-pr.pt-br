---
description: Contém informações para a função CryptUIDlgViewSignerInfo.
ms.assetid: 2b76de4f-4b35-477e-a67e-435434e066c6
title: Estrutura de CRYPTUI_VIEWSIGNERINFO_STRUCT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPTUI_VIEWSIGNERINFO_STRUCT
- CRYPTUI_VIEWSIGNERINFO_STRUCTA
- CRYPTUI_VIEWSIGNERINFO_STRUCTW
api_type:
- NA
api_location: ''
ms.openlocfilehash: da150da6b5115e20a78a4edca64a5c9a97f66132
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011012"
---
# <a name="cryptui_viewsignerinfo_struct-structure"></a><span data-ttu-id="6d28d-103">\_Estrutura de \_ struct CRYPTUI VIEWSIGNERINFO</span><span class="sxs-lookup"><span data-stu-id="6d28d-103">CRYPTUI\_VIEWSIGNERINFO\_STRUCT structure</span></span>

<span data-ttu-id="6d28d-104">\[A estrutura de **\_ \_ struct CRYPTUI VIEWSIGNERINFO** está disponível para uso nos sistemas operacionais especificados na seção requisitos.</span><span class="sxs-lookup"><span data-stu-id="6d28d-104">\[The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="6d28d-105">Ele poderá ser alterado ou ficar indisponível em versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="6d28d-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="6d28d-106">A estrutura de **\_ \_ struct CRYPTUI VIEWSIGNERINFO** contém informações para a função [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6d28d-106">The **CRYPTUI\_VIEWSIGNERINFO\_STRUCT** structure contains information for the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="6d28d-107">Essa estrutura não é declarada em um arquivo de cabeçalho publicado.</span><span class="sxs-lookup"><span data-stu-id="6d28d-107">This structure is not declared in a published header file.</span></span> <span data-ttu-id="6d28d-108">Para usar essa estrutura, declare-a no formato exato mostrado.</span><span class="sxs-lookup"><span data-stu-id="6d28d-108">To use this structure, declare it in the exact format shown.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6d28d-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6d28d-109">Syntax</span></span>


```C++
typedef struct tagCRYPTUI_VIEWSIGNERINFO_STRUCT {
  DWORD            dwSize;
  HWND             hwndParent;
  DWORD            dwFlags;
  LPCTSTR          szTitle;
  CMSG_SIGNER_INFO *pSignerInfo;
  HCRYPTMSG        hMsg;
  LPCSTR           pszOID;
  DWORD_PTR        dwReserved;
  DWORD            cStores;
  HCERTSTORE       *rghStores;
  DWORD            cPropSheetPages;
  LPCPROPSHEETPAGE rgPropSheetPages;
} CRYPTUI_VIEWSIGNERINFO_STRUCT, *PCRYPTUI_VIEWSIGNERINFO_STRUCT;
```



## <a name="members"></a><span data-ttu-id="6d28d-110">Membros</span><span class="sxs-lookup"><span data-stu-id="6d28d-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="6d28d-111">**dwSize**</span><span class="sxs-lookup"><span data-stu-id="6d28d-111">**dwSize**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-112">O tamanho, em bytes, dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="6d28d-112">The size, in bytes, of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-113">**hwndParent**</span><span class="sxs-lookup"><span data-stu-id="6d28d-113">**hwndParent**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-114">O identificador da janela para ser o pai da caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d28d-114">The handle of the window to be the parent of the dialog box.</span></span> <span data-ttu-id="6d28d-115">Esse membro pode ser **nulo** se a caixa de diálogo não deve ter nenhum pai.</span><span class="sxs-lookup"><span data-stu-id="6d28d-115">This member can be **NULL** if the dialog box should have no parent.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-116">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="6d28d-116">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-117">Um conjunto de sinalizadores que modifica o comportamento da função [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="6d28d-117">A set of flags that modifies the behavior of the [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md) function.</span></span> <span data-ttu-id="6d28d-118">Não há sinalizadores definidos no momento, portanto, esse membro deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6d28d-118">There are no flags currently defined, so this member must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-119">**szTitle**</span><span class="sxs-lookup"><span data-stu-id="6d28d-119">**szTitle**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-120">Um ponteiro para uma cadeia de caracteres terminada em nulo que contém o título a ser exibido na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="6d28d-120">A pointer to a null-terminated string that contains the title to be displayed in the dialog box.</span></span> <span data-ttu-id="6d28d-121">Se esse membro for **nulo**, será usado um título padrão.</span><span class="sxs-lookup"><span data-stu-id="6d28d-121">If this member is **NULL**, a default title is used.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-122">**pSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="6d28d-122">**pSignerInfo**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-123">Um ponteiro para uma estrutura de [**\_ \_ informações de signatário CMSG**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) que contém as informações de signatário a serem exibidas.</span><span class="sxs-lookup"><span data-stu-id="6d28d-123">A pointer to a [**CMSG\_SIGNER\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cmsg_signer_info) structure that contains the signer information to display.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-124">**hMsg**</span><span class="sxs-lookup"><span data-stu-id="6d28d-124">**hMsg**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-125">O identificador da mensagem da qual as informações de signatário foram extraídas.</span><span class="sxs-lookup"><span data-stu-id="6d28d-125">The handle of the message that the signer information was extracted from.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-126">**pszOID**</span><span class="sxs-lookup"><span data-stu-id="6d28d-126">**pszOID**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-127">Um ponteiro para uma cadeia de caracteres ANSI terminada em nulo que contém a representação de cadeia de caracteres do [*identificador de objeto*](../secgloss/o-gly.md) (OID) que significa para qual o certificado que fez a assinatura deve ser validado.</span><span class="sxs-lookup"><span data-stu-id="6d28d-127">A pointer to a null-terminated ANSI string that contains the string representation of the [*object identifier*](../secgloss/o-gly.md) (OID) that signifies what the certificate that did the signing should be validated for.</span></span> <span data-ttu-id="6d28d-128">Por exemplo, se isso estiver sendo chamado para exibir a assinatura de uma CTL ( [*lista de certificados confiáveis*](../secgloss/c-gly.md) ), a cadeia de caracteres do OID de **assinatura de uso do szOID \_ KP \_ CTL \_ \_** deverá ser passada.</span><span class="sxs-lookup"><span data-stu-id="6d28d-128">For example, if this is being called to view the signature of a [*certificate trust list*](../secgloss/c-gly.md) (CTL), the **szOID\_KP\_CTL\_USAGE\_SIGNING** OID string should be passed in.</span></span> <span data-ttu-id="6d28d-129">Se esse membro for **nulo**, o certificado não será validado para usos.</span><span class="sxs-lookup"><span data-stu-id="6d28d-129">If this member is **NULL**, the certificate is not validated for usages.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-130">**dwReserved**</span><span class="sxs-lookup"><span data-stu-id="6d28d-130">**dwReserved**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-131">Este parâmetro não é usado no momento.</span><span class="sxs-lookup"><span data-stu-id="6d28d-131">This parameter is not currently used.</span></span> <span data-ttu-id="6d28d-132">Este membro deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="6d28d-132">This member must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-133">**cStores**</span><span class="sxs-lookup"><span data-stu-id="6d28d-133">**cStores**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-134">O número de elementos na matriz **rghStores** .</span><span class="sxs-lookup"><span data-stu-id="6d28d-134">The number of elements in the **rghStores** array.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-135">**rghStores**</span><span class="sxs-lookup"><span data-stu-id="6d28d-135">**rghStores**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-136">Uma matriz de valores **HCERTSTORE** que representam os outros repositórios de certificados para pesquisar o certificado que assinou a mensagem.</span><span class="sxs-lookup"><span data-stu-id="6d28d-136">An array of **HCERTSTORE** values that represent the other certificate stores to search for the certificate that signed the message.</span></span> <span data-ttu-id="6d28d-137">Se esse membro for **nulo**, nenhum repositório adicional será pesquisado.</span><span class="sxs-lookup"><span data-stu-id="6d28d-137">If this member is **NULL**, no additional stores are searched.</span></span> <span data-ttu-id="6d28d-138">O membro **cStores** contém o número de elementos nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="6d28d-138">The **cStores** member contains the number of elements in this array.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-139">**cPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="6d28d-139">**cPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-140">O número de elementos na matriz **rgPropSheetPages** .</span><span class="sxs-lookup"><span data-stu-id="6d28d-140">The number of elements in the **rgPropSheetPages** array.</span></span>

</dd> <dt>

<span data-ttu-id="6d28d-141">**rgPropSheetPages**</span><span class="sxs-lookup"><span data-stu-id="6d28d-141">**rgPropSheetPages**</span></span>
</dt> <dd>

<span data-ttu-id="6d28d-142">Uma matriz de ponteiros de estrutura [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) que definem páginas adicionais a serem exibidas na caixa de diálogo padrão.</span><span class="sxs-lookup"><span data-stu-id="6d28d-142">An array of [**PROPSHEETPAGE**](/windows/win32/api/prsht/ns-prsht-propsheetpagea_v2) structure pointers that define any extra pages to display in the standard dialog box.</span></span> <span data-ttu-id="6d28d-143">Se esse membro for **nulo**, nenhuma página adicional será exibida.</span><span class="sxs-lookup"><span data-stu-id="6d28d-143">If this member is **NULL**, no additional pages will be displayed.</span></span> <span data-ttu-id="6d28d-144">O membro **cPropSheetPages** contém o número de elementos nesta matriz.</span><span class="sxs-lookup"><span data-stu-id="6d28d-144">The **cPropSheetPages** member contains the number of elements in this array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d28d-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d28d-145">Requirements</span></span>



| <span data-ttu-id="6d28d-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d28d-146">Requirement</span></span> | <span data-ttu-id="6d28d-147">Valor</span><span class="sxs-lookup"><span data-stu-id="6d28d-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d28d-148">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d28d-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6d28d-149">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="6d28d-149">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="6d28d-150">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6d28d-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6d28d-151">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="6d28d-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6d28d-152">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="6d28d-152">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6d28d-153">**CRYPTUI \_ VIEWSIGNERINFO \_ STRUCTW** (Unicode) e **CRYPTUI \_ VIEWSIGNERINFO \_ structA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6d28d-153">**CRYPTUI\_VIEWSIGNERINFO\_STRUCTW** (Unicode) and **CRYPTUI\_VIEWSIGNERINFO\_STRUCTA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d28d-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="6d28d-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d28d-155">**CryptUIDlgViewSignerInfo**</span><span class="sxs-lookup"><span data-stu-id="6d28d-155">**CryptUIDlgViewSignerInfo**</span></span>](cryptuidlgviewsignerinfo.md)
</dt> </dl>

 

 
