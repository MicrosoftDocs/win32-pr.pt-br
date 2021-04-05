---
title: TfClientId (msctf. h)
description: O tipo de dados TfClientId é usado para identificar o cliente.
ms.assetid: 984dc390-6e15-4491-8c06-77c27c5bdd6f
keywords:
- TfClientId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ffba8e1d5ea3c8114d9f567c3829141dd8902dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644493"
---
# <a name="tfclientid"></a><span data-ttu-id="f9e2c-104">TfClientId</span><span class="sxs-lookup"><span data-stu-id="f9e2c-104">TfClientId</span></span>

<span data-ttu-id="f9e2c-105">O tipo de dados **TfClientId** é usado para identificar o cliente.</span><span class="sxs-lookup"><span data-stu-id="f9e2c-105">The **TfClientId** data type is used to identify the client.</span></span>


```C++
typedef DWORD TfClientId;
```



## <a name="remarks"></a><span data-ttu-id="f9e2c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9e2c-106">Remarks</span></span>

<span data-ttu-id="f9e2c-107">No TSF, os aplicativos e serviços de texto são geralmente chamados de clientes.</span><span class="sxs-lookup"><span data-stu-id="f9e2c-107">Within TSF, applications and text services are generally referred to as clients.</span></span> <span data-ttu-id="f9e2c-108">Cada cliente recebe um identificador exclusivo que ele usa para se identificar ao chamar vários métodos do Gerenciador de TSF.</span><span class="sxs-lookup"><span data-stu-id="f9e2c-108">Each client receives a unique identifier that it uses to identify itself when calling various TSF manager methods.</span></span> <span data-ttu-id="f9e2c-109">Esse identificador é do tipo **TfClientId** .</span><span class="sxs-lookup"><span data-stu-id="f9e2c-109">This identifier is of the **TfClientId** type.</span></span>

<span data-ttu-id="f9e2c-110">O tipo de dados **TfClientId** é fornecido pelo Gerenciador de TSF.</span><span class="sxs-lookup"><span data-stu-id="f9e2c-110">The **TfClientId** data type is supplied by the TSF manager.</span></span> <span data-ttu-id="f9e2c-111">Um aplicativo obtém um valor de **TfClientId** quando chama [ITfThreadMgr:: Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span><span class="sxs-lookup"><span data-stu-id="f9e2c-111">An application obtains a **TfClientId** value when it calls [ITfThreadMgr::Activate](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate).</span></span> <span data-ttu-id="f9e2c-112">O valor de TfClientId para um serviço de texto é passado para o método [ITfTextInputProcessor:: Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) .</span><span class="sxs-lookup"><span data-stu-id="f9e2c-112">The TfClientId value for a text service is passed to the [ITfTextInputProcessor::Activate](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate) method.</span></span> <span data-ttu-id="f9e2c-113">Qualquer objeto que não caiba nas categorias acima pode obter um identificador de cliente chamando [ITfClientId:: Getclientid](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span><span class="sxs-lookup"><span data-stu-id="f9e2c-113">Any object that does not fit the above categories can obtain a client identifier by calling [ITfClientId::GetClientId](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9e2c-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9e2c-114">Requirements</span></span>



| <span data-ttu-id="f9e2c-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9e2c-115">Requirement</span></span> | <span data-ttu-id="f9e2c-116">Valor</span><span class="sxs-lookup"><span data-stu-id="f9e2c-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f9e2c-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9e2c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f9e2c-118">Aplicativos do Windows 2000 Professional \[ Desktop aplicativos \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f9e2c-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                    |
| <span data-ttu-id="f9e2c-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f9e2c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f9e2c-120">Aplicativos da área de trabalho do Windows 2000 Server aplicativos \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="f9e2c-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="f9e2c-121">Redistribuível</span><span class="sxs-lookup"><span data-stu-id="f9e2c-121">Redistributable</span></span><br/>          | <span data-ttu-id="f9e2c-122">TSF 1,0 no Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f9e2c-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="f9e2c-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f9e2c-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9e2c-124"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9e2c-124"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="f9e2c-125">INSERI</span><span class="sxs-lookup"><span data-stu-id="f9e2c-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f9e2c-126"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f9e2c-126"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9e2c-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9e2c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9e2c-128">**ITfClientId:: getclientid**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-128">**ITfClientId::GetClientId**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfclientid-getclientid)
</dt> <dt>

[<span data-ttu-id="f9e2c-129">**ITfTextInputProcessor:: ativar**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-129">**ITfTextInputProcessor::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itftextinputprocessor-activate)
</dt> <dt>

[<span data-ttu-id="f9e2c-130">**ITfThreadMgr:: ativar**</span><span class="sxs-lookup"><span data-stu-id="f9e2c-130">**ITfThreadMgr::Activate**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfthreadmgr-activate)
</dt> </dl>

 

 





