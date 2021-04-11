---
description: Exibe uma caixa de diálogo que permite que um usuário selecione um certificado.
ms.assetid: 242c19a7-179b-4fc0-a050-a1b598566a6b
title: Função CryptUIDlgSelectCertificate
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 65d9993cd1e035473e731056d33b7a391ef47b5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171675"
---
# <a name="cryptuidlgselectcertificate-function"></a><span data-ttu-id="3355e-103">Função CryptUIDlgSelectCertificate</span><span class="sxs-lookup"><span data-stu-id="3355e-103">CryptUIDlgSelectCertificate function</span></span>

<span data-ttu-id="3355e-104">A função **CryptUIDlgSelectCertificate** exibe uma caixa de diálogo que permite que um usuário selecione um certificado.</span><span class="sxs-lookup"><span data-stu-id="3355e-104">The **CryptUIDlgSelectCertificate** function displays a dialog box that allows a user to select a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="3355e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3355e-105">Syntax</span></span>


```C++
);
```



## <a name="parameters"></a><span data-ttu-id="3355e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3355e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3355e-107">*PCSC* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3355e-107">*pcsc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3355e-108">Um ponteiro para uma estrutura de [**\_ \_ struct CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) que contém informações sobre a caixa de diálogo a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="3355e-108">A pointer to a [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure that contains information about the dialog box to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3355e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3355e-109">Return value</span></span>

<span data-ttu-id="3355e-110">Um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) que representa o certificado selecionado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="3355e-110">A pointer to a [**CERT\_CONTEXT**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate selected by the user.</span></span> <span data-ttu-id="3355e-111">Quando você terminar de usar esse certificado, deverá passar esse ponteiro para a função [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) para diminuir a contagem de referência do contexto do certificado.</span><span class="sxs-lookup"><span data-stu-id="3355e-111">When you have finished using this certificate, you must pass this pointer to the [**CertFreeCertificateContext**](/windows/win32/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function to decrement the reference count of the certificate context.</span></span>

<span data-ttu-id="3355e-112">Se o membro **dwFlags** da estrutura *PCSC* não contiver o sinalizador **CRYPTUI \_ SELECTCERT \_ MultiSelect** , um valor de retorno de **NULL** significa que o usuário fechou a caixa de diálogo sem selecionar um certificado.</span><span class="sxs-lookup"><span data-stu-id="3355e-112">If the **dwFlags** member of the *pcsc* structure does not contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, a return value of **NULL** means that the user closed the dialog box without selecting a certificate.</span></span>

<span data-ttu-id="3355e-113">Se o membro **dwFlags** da estrutura *PCSC* contiver o sinalizador **CRYPTUI \_ SELECTCERT \_ MultiSelect** , essa função sempre retornará **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3355e-113">If the **dwFlags** member of the *pcsc* structure does contain the **CRYPTUI\_SELECTCERT\_MULTISELECT** flag, this function always returns **NULL**.</span></span> <span data-ttu-id="3355e-114">Os certificados selecionados estarão contidos no repositório de certificados que é representado pelo membro **hSelectedCertStore** de *PCSC*.</span><span class="sxs-lookup"><span data-stu-id="3355e-114">The selected certificates will be contained in the certificate store that is represented by the **hSelectedCertStore** member of *pcsc*.</span></span> <span data-ttu-id="3355e-115">Se o número de certificados no repositório for o mesmo antes e depois de chamar **CryptUIDlgSelectCertificate**, o usuário fechou a caixa de diálogo sem selecionar nenhum certificado.</span><span class="sxs-lookup"><span data-stu-id="3355e-115">If the number of certificates in the store is the same before and after calling **CryptUIDlgSelectCertificate**, the user closed the dialog box without selecting any certificates.</span></span>

## <a name="remarks"></a><span data-ttu-id="3355e-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3355e-116">Remarks</span></span>

<span data-ttu-id="3355e-117">Se o membro **dwFlags** da estrutura [**de \_ \_ struct CRYPTUI SELECTCERTIFICATE**](cryptui-selectcertificate-struct.md) for definido como **CRYPTUI \_ SELECTCERT \_ Legacy**, a caixa de diálogo herdada será exibida.</span><span class="sxs-lookup"><span data-stu-id="3355e-117">If the **dwFlags** member of the [**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**](cryptui-selectcertificate-struct.md) structure is set to **CRYPTUI\_SELECTCERT\_LEGACY**, the legacy dialog is displayed.</span></span> <span data-ttu-id="3355e-118">Caso contrário, a caixa de diálogo de seleção de certificado atual será exibida.</span><span class="sxs-lookup"><span data-stu-id="3355e-118">Otherwise, the current certificate selection dialog is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="3355e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3355e-119">Requirements</span></span>



| <span data-ttu-id="3355e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3355e-120">Requirement</span></span> | <span data-ttu-id="3355e-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3355e-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3355e-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3355e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3355e-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3355e-123">Windows�XP \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3355e-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3355e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3355e-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3355e-125">Windows Server�2003 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3355e-126">Fim do suporte</span><span class="sxs-lookup"><span data-stu-id="3355e-126">End of support</span></span><br/> | <span data-ttu-id="3355e-127">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="3355e-127">Windows�7 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3355e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3355e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="3355e-129"><dt>Cryptui. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3355e-129"><dt>Cryptui.lib</dt></span></span> </dl>            |
| <span data-ttu-id="3355e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="3355e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3355e-131"><dt>Cryptui.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3355e-131"><dt>Cryptui.dll</dt></span></span> </dl>            |
| <span data-ttu-id="3355e-132">Nomes Unicode e ANSI</span><span class="sxs-lookup"><span data-stu-id="3355e-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="3355e-133">**CryptUIDlgSelectCertificateW** (Unicode) e **CryptUIDlgSelectCertificateA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="3355e-133">**CryptUIDlgSelectCertificateW** (Unicode) and **CryptUIDlgSelectCertificateA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3355e-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="3355e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3355e-135">**CRYPTUI \_ SELECTCERTIFICATE \_ struct**</span><span class="sxs-lookup"><span data-stu-id="3355e-135">**CRYPTUI\_SELECTCERTIFICATE\_STRUCT**</span></span>](cryptui-selectcertificate-struct.md)
</dt> </dl>

<span data-ttu-id="3355e-136">�</span><span class="sxs-lookup"><span data-stu-id="3355e-136">�</span></span>

<span data-ttu-id="3355e-137">�</span><span class="sxs-lookup"><span data-stu-id="3355e-137">�</span></span>




