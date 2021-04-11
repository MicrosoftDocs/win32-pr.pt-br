---
title: TfEditCookie (msctf. h)
description: O tipo de dados TfEditCookie identifica uma sessão de edição que tem um bloqueio.
ms.assetid: 1de17286-5d56-4302-a144-5fe6ca7d5557
keywords:
- TfEditCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69281bc38b5df6c22dd5306877aecdb8025af84a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008820"
---
# <a name="tfeditcookie"></a><span data-ttu-id="c7d4b-104">TfEditCookie</span><span class="sxs-lookup"><span data-stu-id="c7d4b-104">TfEditCookie</span></span>

<span data-ttu-id="c7d4b-105">O tipo de dados **TfEditCookie** identifica uma sessão de edição que tem um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c7d4b-105">The **TfEditCookie** data type identifies an edit session that has a lock.</span></span>


```C++
typedef DWORD TfEditCookie;
```



## <a name="remarks"></a><span data-ttu-id="c7d4b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7d4b-106">Remarks</span></span>

<span data-ttu-id="c7d4b-107">O tipo de dados **TfEditCookie** é fornecido pelo Gerenciador do TSF e é usado por um cliente (serviço de aplicativo ou de texto) para identificar uma sessão de edição com um bloqueio somente leitura ou de leitura/gravação em vários métodos.</span><span class="sxs-lookup"><span data-stu-id="c7d4b-107">The **TfEditCookie** data type is supplied by the TSF manager and is used by a client (application or text service) to identify an edit session with a read-only or read/write lock in various methods.</span></span>

<span data-ttu-id="c7d4b-108">Um valor de **TfEditCookie** é obtido de uma das maneiras a seguir.</span><span class="sxs-lookup"><span data-stu-id="c7d4b-108">A **TfEditCookie** value is obtained in one of the following ways.</span></span>

-   <span data-ttu-id="c7d4b-109">O cliente chama [ITfDocumentMgr:: CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span><span class="sxs-lookup"><span data-stu-id="c7d4b-109">The client calls [ITfDocumentMgr::CreateContext](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext).</span></span>
-   <span data-ttu-id="c7d4b-110">O Gerenciador do TSF chama o método ITfEditSession do cliente [::D oeditsession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) .</span><span class="sxs-lookup"><span data-stu-id="c7d4b-110">The TSF manager calls the client [ITfEditSession::DoEditSession](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession) method.</span></span>
-   <span data-ttu-id="c7d4b-111">O Gerenciador do TSF chama o método [ITfCompositionSink:: OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) do cliente.</span><span class="sxs-lookup"><span data-stu-id="c7d4b-111">The TSF manager calls the client [ITfCompositionSink::OnCompositionTerminated](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated) method.</span></span>
-   <span data-ttu-id="c7d4b-112">O Gerenciador do TSF chama o método [ITfCleanupContextSink:: OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) do cliente.</span><span class="sxs-lookup"><span data-stu-id="c7d4b-112">The TSF manager calls the client [ITfCleanupContextSink::OnCleanupContext](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext) method.</span></span>
-   <span data-ttu-id="c7d4b-113">O Gerenciador do TSF chama o método [ITfTextEditSink:: onendedit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) do cliente.</span><span class="sxs-lookup"><span data-stu-id="c7d4b-113">The TSF manager calls the client [ITfTextEditSink::OnEndEdit](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c7d4b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7d4b-114">Requirements</span></span>



| <span data-ttu-id="c7d4b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7d4b-115">Requirement</span></span> | <span data-ttu-id="c7d4b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="c7d4b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c7d4b-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7d4b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c7d4b-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7d4b-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="c7d4b-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c7d4b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c7d4b-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7d4b-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c7d4b-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="c7d4b-121">Redistributable</span></span><br/>          | <span data-ttu-id="c7d4b-122">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="c7d4b-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="c7d4b-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c7d4b-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7d4b-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7d4b-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="c7d4b-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="c7d4b-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c7d4b-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c7d4b-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c7d4b-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7d4b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7d4b-128">**ITfCleanupContextSink::OnCleanupContext**</span><span class="sxs-lookup"><span data-stu-id="c7d4b-128">**ITfCleanupContextSink::OnCleanupContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcleanupcontextsink-oncleanupcontext)
</dt> <dt>

[<span data-ttu-id="c7d4b-129">**ITfCompositionSink::OnCompositionTerminated**</span><span class="sxs-lookup"><span data-stu-id="c7d4b-129">**ITfCompositionSink::OnCompositionTerminated**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcompositionsink-oncompositionterminated)
</dt> <dt>

[<span data-ttu-id="c7d4b-130">**ITfDocumentMgr:: CreateContext**</span><span class="sxs-lookup"><span data-stu-id="c7d4b-130">**ITfDocumentMgr::CreateContext**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfdocumentmgr-createcontext)
</dt> <dt>

[<span data-ttu-id="c7d4b-131">**ITfEditSession::D oEditSession**</span><span class="sxs-lookup"><span data-stu-id="c7d4b-131">**ITfEditSession::DoEditSession**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfeditsession-doeditsession)
</dt> <dt>

[<span data-ttu-id="c7d4b-132">**ITfTextEditSink:: onendedit**</span><span class="sxs-lookup"><span data-stu-id="c7d4b-132">**ITfTextEditSink::OnEndEdit**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftexteditsink-onendedit)
</dt> </dl>

 

 





