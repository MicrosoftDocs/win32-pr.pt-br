---
title: Método WSMan. GetErrorMessage (WSManDisp. h)
description: Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro.
ms.assetid: 5f0a5259-8356-4406-8612-34f4921184f0
ms.tgt_platform: multiple
keywords:
- Gerenciamento Remoto do Windows do método GetErrorMessage
- Método GetErrorMessage Gerenciamento Remoto do Windows, objeto WSMan
- Gerenciamento Remoto do Windows de objeto WSMan, Método GetErrorMessage
topic_type:
- apiref
api_name:
- WSMan.GetErrorMessage
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d085e6f19c64f609fe1389a2822df1594ee69bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104295787"
---
# <a name="wsmangeterrormessage-method"></a><span data-ttu-id="6460e-106">Método WSMan. GetErrorMessage</span><span class="sxs-lookup"><span data-stu-id="6460e-106">WSMan.GetErrorMessage method</span></span>

<span data-ttu-id="6460e-107">Retorna uma cadeia de caracteres formatada que contém o texto de um número de erro.</span><span class="sxs-lookup"><span data-stu-id="6460e-107">Returns a formatted string that contains the text of an error number.</span></span> <span data-ttu-id="6460e-108">Esse método executa a mesma operação que o WinRM da linha de comando **WinRM** **helpmsg** *decimal ou o número de erro hexadecimal*.</span><span class="sxs-lookup"><span data-stu-id="6460e-108">This method performs the same operation as the **Winrm** command-line **winrm helpmsg** *decimal or hexadecimal error number*.</span></span>

## <a name="syntax"></a><span data-ttu-id="6460e-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6460e-109">Syntax</span></span>


```VB
WSMan.GetErrorMessage( _
  ByVal errorNumber, _
  ByRef errorMessage _
)
```



## <a name="parameters"></a><span data-ttu-id="6460e-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6460e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6460e-111">*errorNumber* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="6460e-111">*errorNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6460e-112">Um número de mensagem de erro em decimal ou hexadecimal do WinRM, do WinHTTP ou de outros componentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="6460e-112">An error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.</span></span>

</dd> <dt>

<span data-ttu-id="6460e-113">*ErrorMessage* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="6460e-113">*errorMessage* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6460e-114">Uma cadeia de caracteres de mensagem de erro formatada como mensagens retornadas do comando **WinRM** .</span><span class="sxs-lookup"><span data-stu-id="6460e-114">An error message string formatted like messages returned from the **Winrm** command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6460e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="6460e-115">Remarks</span></span>

<span data-ttu-id="6460e-116">O método C++ correspondente é [**IWSManEx:: GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span><span class="sxs-lookup"><span data-stu-id="6460e-116">The corresponding C++ method is [**IWSManEx::GetErrorMessage**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-geterrormessage).</span></span>

## <a name="requirements"></a><span data-ttu-id="6460e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6460e-117">Requirements</span></span>



| <span data-ttu-id="6460e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6460e-118">Requirement</span></span> | <span data-ttu-id="6460e-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6460e-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6460e-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6460e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6460e-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6460e-121">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="6460e-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6460e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6460e-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6460e-123">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="6460e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6460e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6460e-125"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6460e-125"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6460e-126">INSERI</span><span class="sxs-lookup"><span data-stu-id="6460e-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6460e-127"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6460e-127"><dt>WSManDisp.idl</dt></span></span> </dl> |
| <span data-ttu-id="6460e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6460e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="6460e-129"><dt>WSManDisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6460e-129"><dt>WSManDisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6460e-130">DLL</span><span class="sxs-lookup"><span data-stu-id="6460e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6460e-131"><dt>WSMAuto.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6460e-131"><dt>WSMAuto.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6460e-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="6460e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6460e-133">**WSMan**</span><span class="sxs-lookup"><span data-stu-id="6460e-133">**WSMan**</span></span>](wsman.md)
</dt> </dl>

 

 





