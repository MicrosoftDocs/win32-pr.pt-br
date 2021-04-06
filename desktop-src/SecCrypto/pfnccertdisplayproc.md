---
description: Uma função de retorno de chamada definida pelo usuário que permite que o chamador da função CryptUIDlgSelectCertificate manipule a exibição de certificados que o usuário seleciona para exibir.
ms.assetid: fdb9e9e0-02f1-42e0-9a11-204d916a1a88
title: Função de retorno de chamada PFNCCERTDISPLAYPROC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PFNCCERTDISPLAYPROC
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 7371e983b339ff8bfa9edb1b7fb795ab64596a98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011079"
---
# <a name="pfnccertdisplayproc-callback-function"></a><span data-ttu-id="0975c-103">Função de retorno de chamada PFNCCERTDISPLAYPROC</span><span class="sxs-lookup"><span data-stu-id="0975c-103">PFNCCERTDISPLAYPROC callback function</span></span>

<span data-ttu-id="0975c-104">A função **PFNCCERTDISPLAYPROC** é uma função de retorno de chamada definida pelo usuário que permite que o chamador da função [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) manipule a exibição de certificados que o usuário seleciona para exibir.</span><span class="sxs-lookup"><span data-stu-id="0975c-104">The **PFNCCERTDISPLAYPROC** function is a user-defined callback function that allows the caller of the [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) function to handle the display of certificates that the user selects to view.</span></span>

## <a name="syntax"></a><span data-ttu-id="0975c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0975c-105">Syntax</span></span>


```C++
BOOL WINAPI * PFNCCERTDISPLAYPROC(
  _In_ PCCERT_CONTEXT pCertContext,
  _In_ HWND           hWndSelCertDlg,
  _In_ void           *pvCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="0975c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0975c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0975c-107">*pCertContext* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0975c-107">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0975c-108">Um ponteiro para uma estrutura de [**\_ contexto de certificado**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) que representa o certificado a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="0975c-108">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure that represents the certificate to display.</span></span>

</dd> <dt>

<span data-ttu-id="0975c-109">*hWndSelCertDlg* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0975c-109">*hWndSelCertDlg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0975c-110">Um identificador para a caixa de diálogo da qual o certificado foi selecionado para exibição.</span><span class="sxs-lookup"><span data-stu-id="0975c-110">A handle to the dialog box from which the certificate was selected for viewing.</span></span>

</dd> <dt>

<span data-ttu-id="0975c-111">*pvCallbackData* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="0975c-111">*pvCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0975c-112">Dados adicionais usados pela função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0975c-112">Additional data used by the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0975c-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0975c-113">Return value</span></span>

<span data-ttu-id="0975c-114">Essa função retorna **true** para indicar que ele lida com a exibição do certificado e que a caixa de diálogo não deve exibir o certificado.</span><span class="sxs-lookup"><span data-stu-id="0975c-114">This function returns **TRUE** to indicate that it handles display of the certificate and that the dialog box should not display the certificate.</span></span> <span data-ttu-id="0975c-115">Se essa função retornar **false**, a caixa de diálogo exibirá o certificado.</span><span class="sxs-lookup"><span data-stu-id="0975c-115">If this function returns **FALSE**, the dialog box displays the certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="0975c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0975c-116">Requirements</span></span>



| <span data-ttu-id="0975c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="0975c-117">Requirement</span></span> | <span data-ttu-id="0975c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="0975c-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0975c-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0975c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="0975c-120">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0975c-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0975c-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0975c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="0975c-122">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0975c-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 




